[title]: # (OpenShift)
[tags]: # (Openshift, Kubernetes, K8S, OKD)
[priority]: # (1)

# OpenShift Deployment

The integration provided by Thycotic for managing OpenShift Secrets is a Mutating Admissions Webhook. The webhook functions by intercepting Kubernetes Secrets calls that feature the webhook's annotation and translating these in to requests for Secrets from Thycotic Secret Server.

This guide is designed to walk you through how the integration fits together with all its constituent parts, and gives some example templates (in OpenShift YAML), designed to get you up and running with the integration quickly and effectively.

As a reference, the integration itself is available open source from here, hence you're able to modify it to suit the specific needs of your organization:

https://github.com/thycotic/tss-k8s

https://github.com/thycotic/dsv-k8s

The integration also backs off to the Thycotic golang integration components, which are also available open source:

https://github.com/thycotic/tss-sdk-go

https://github.com/thycotic/dsv-sdk-go

>**Note**: This guide is tailored towards OpenShift deployment, however the method is also generally supported and cross-compatible on Kubernetes. 
