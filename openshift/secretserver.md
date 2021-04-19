[title]: # (OpenShift)
[tags]: # (Openshift, Kubernetes, K8S, OKD)
[priority]: # (1)

# Architecture

![](https://github.com/tcarolanthycotic/openshift/blob/main/Documentation/images/tssopenshift.png)

The diagram above represents the visual version of the architecture and its components.

# General Description

The integration is a [Mutating Admissions Webhook](https://kubernetes.io/docs/reference/access-authn-authz/extensible-admission-controllers/#admission-webhooks) that intercepts requests for OpenShift Secrets using a specialized annotation. The request is then updated with data from Secret Server and passed in to the OpenShift Secrets vault. This ensures that credentials in the OpenShift Secrets Vault are aligned with the values as managed by Secret Server, hence password changes can occur on the Secret Server side and be able to be reflected in the OpenShift Secrets Vault.

The deployment is designed to be easily integratable in to existing deployment environments, as Secret requests only need to have the various [Annotations](#Annotations) added to them in order for the Secret Server based workflow to be enacted.

>**Note**: There are numerous different ways of configuring OpenShift for different operating environments. Hence this guide, although intending to give a solid baseline idea for deployment of the integration, will not be the sole, authoritative way in which the integration can function or be deployed. All examples below use the `default` namespace which, alongside some other components, will likely need to be modified to ensure suitability with your organization's OpenShift environment.

## The Webhook 

The webhook is at the front end of the integration and intercepts the requests for Secrets that are inbound to the OpenShift Secrets store, when the requests are given the appropriate annotation. Below is a basic configuration YAML for deploying the webhook in your OpenShift instance.

### Example Webhook YAML
```yaml
---
apiVersion: admissionregistration.k8s.io/v1
kind: MutatingWebhookConfiguration
metadata:
  name: tss-injector
  labels:
    app: tss
webhooks:
  - name: tss.thycotic.com
    rules:
      - apiGroups: ["*"]
        apiVersions: ["*"]
        operations: ["CREATE", "UPDATE"]
        resources: ["secrets"]
    clientConfig:
      service:
        namespace: default
        name: tss-injector
        path: "/inject"
        port: 8543
      caBundle: ""
    admissionReviewVersions: ["v1"]
    sideEffects: None
    timeoutSeconds: 5
```
### The Webhook Certificate

Each of the pods in the deployment are in posesssion (via [ConfigMaps](#Certificate)) of a certificate that they present in order to identify themselves to the OpenShift instance. The `caBundle` value in the webhook must be the base64 encoded version of the public certificate (crt) that the pods are presenting.

## The Service

As per standard OpenShift configuration, a loadbalanced service allows orchestrated applications to be handled effectively from an internal OpenShift networking standpoint. Hence, we want this service to direct all requests to the appropriate deployment/pods when an annotated Secret request comes in. 

Below is an example of the service and how it could look against the `default` namespace:

### Example Service YAML
``` yaml
---
apiVersion: v1
kind: Service
metadata:
  name: tss-injector
  namespace: default
  labels:
    app: tss-injector
spec:
  ports:
    - port: 8543
      targetPort: 18543
  selector:
    app: tss-injector
  type: LoadBalancer
```



## ConfigMaps

### Roles Configuration
The `roles.json` file is accessed by the pods in the deployment through a ConfigMap. The file gives the pods information about where Secret Server is located, and how they should authenticate with it (via a set of credentials).

__Secret Server Cloud Example__
```json
{
    "default": {
        "credentials": {
            "username": "username",
            "password": "password"
        },
        "serverURL": "https://mytenant.secretsvaultcloud.com"
    }
}
```

Multiple roles and vaults can also be used. 

>**Note**: In the absence of a role being explicitly specified, the `default` role will be used.

__Multiple Vaults Example__
```json
{
    "alternaterole": {
        "credentials": {
            "username": "username",
            "password": "password"
        },
        "serverURL": "https://myfirsttenant.secretsvaultcloud.com"
    },
    "default": {
        "credentials": {
            "username": "username",
            "password": "password"
        },
       "serverURL": "https://mysecondtenant.secretsvaultcloud.com"
    }
}
```

### Certificate

Two ConfigMaps are required for the certificate. One to hold the public certificate (.crt), and one for the private key associated therewith (.key).

__*IMPORTANT*__ The public certificate must have a CN (Command Name) of `deploymentname.namespace.svc`. To fit directly in to the examples given here, a CN of `tss-injector.default.svc` must be present on the certificate.

Examples of these config maps (`tss-crt` and `tss-key`) are in the [Sample Deployment YAML](#example-deployment-yaml) under `volumes`.

__Container Mapping:__
These items are mapped in to the injector container through the `ENTRYPOINT` in the Dockerfile, which is, in its most basic form:

```
FROM tss-injector:latest
ARG cert_file
ARG key_file
ARG roles_file
COPY ${cert_file} ./tss.pem
COPY --chown=tss ${key_file} ./tss.key
COPY ${roles_file} ./roles.json
ENTRYPOINT ["tss-injector-svc", "-cert", "tss.pem", "-key", "tss.key", "-roles", "roles.json" ]
```

>**Note**: The `tss-injector` image on Docker Hub does not include these references, however the Docker Hub image reference (`thycotictc/openshift:latest`) in the Deployment below already includes the above configuration.


## The Deployment

The final component of the integration is the deployment and the pods associated with it. Each pod includes a single running container that is the injector application, which is designed to go out to the target vaulting platform and retrieve the intended Secret values.

Note that the deployment example below includes all of the configuration input as detailed in the sections above.

### Example Deployment YAML
``` yaml
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: tss-injector
  namespace: default
  labels:
    app: tss-injector
spec:
  replicas: 5
  selector:
    matchLabels:
      app: tss-injector
  template:
    metadata:
      labels:
        app: tss-injector
      namespace: default
    spec:
      containers:
        - image: thycotictc/openshift:latest
          name: tss-injector
          command: ["tss-injector-svc", "-cert", "tss.crt", "-key", "tss.key", "-roles", "roles.json" ]
          workingDir: "/config"
          resources:
            requests:
              memory: "512Mi"
              cpu: "250m"
            limits:
              memory: "2048Mi"
              cpu: "1000m"
          ports:
            - containerPort: 18543
              name: tss
          volumeMounts:
          - name: config-volume
            mountPath: /config
      volumes:
        - name: config-volume
          projected:
            sources:
              - configMap:
                  name: tss-config
                  items:
                  - key: roles.json
                    path: roles.json
              - configMap:
                  name: tss-key
                  items:
                  - key: tss.key
                    path: tss.key
              - configMap:
                  name: tss-cert
                  items:
                  - key: tss.crt
                    path: tss.crt 
```

## The Requests

### Annotations

The four annotations that affect the behavior of the webhook are:

```golang
const(
    roleAnnotation   = "tss.thycotic.com/role"
    setAnnotation    = "tss.thycotic.com/set-secret"
    addNotation      = "tss.thycotic.com/add-to-secret"
    updateAnnotation = "tss.thycotic.com/update-secret"
)
```
* `roleAnnotation` identifies the role that should be used, as per the [roles.json](#roles-configuration) entry
* `addAnnotation` adds missing fields without overwriting or removing existing fields.
* `updateAnnotation` adds and overwrites existing fields but does not remove fields.
* `setAnnotation` overwrites fields and removes fields that do not exist in the TSS Secret.

>**Note**: Only one of these should be specified on any given k8s Secret, however, if more
than one are defined then the order of precedence is `setAnnotation` then
`addAnnotation` then `updateAnnotation`.

### Secret Examples

In addition to the annotation, the `secretID` value will also need to be provided. This corresponds to the value of the target Secret within Secret Server from which data needs to be retrieved.

>**Note**: The data fields on the request itself are generally ignored, depending on the annotation used.

#### SET
``` yaml
---
apiVersion: v1
kind: Secret
metadata:
  name: my-secret-name
  annotations:
    tss.thycotic.com/set-secret: "10"
type: Opaque
data:
  data: dW5tb2RpZmllZC11c2VybmFtZQ==
```

#### ADD
``` yaml
---
apiVersion: v1
kind: Secret
metadata:
  name: user-domain
  annotations:
    tss.thycotic.com/add-to-secret: "10"
type: Opaque
data:
  data: dW5tb2RpZm
```