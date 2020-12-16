[title]: # (Verifying Integration)
[tags]: # (introduction)
[priority]: # (5)

# Verifying Integration / Troubleshooting

## Validation Process

You can validate the integration is working two ways.

1. Test Credential

    Run a **Test Credential** action directly on the Credential you have added.

    ![test credential prompt](images\b7bb42f223bf596db6e793fc02aeda36.png)

    ![test credential validation successful prompt](images\48a534ec67de1cecf454c2589a8d5ea3.png)

2. Configure a **Discovery Schedule** and run it against a destination system in which you know the credentials will work for an authenticated scan. Below is an example of the configuration against a singular
system

    ![discovery schedule form view](images\2785aee68e6110ccfa77a27207ad018a.png)

    Another screenshot is provided below for the results:

    ![discovery status form view](images\dce997113cfd1e2f6091ec0791cfd40a.png)

    Below is the individual asset results:

    ![individual asset results view 1](images\9ac0044fd5d7de8191b5084262411ea0.png)

    ![individual asset results view 2](images\68cbb8ea204582e4aa4d405c74f4725b.png)

## Certificate Errors

If you observe failures in validating credentials, review the MID Server's agent log. If you find errors referring to `PKIX path` failures, the SSL certificate for Secret Server needs to be imported into the Java Keystore for the MID Server agent. See the [configuration section for more details](../getting-started/install)

An example log of the PKIX errors:

![PKIX certificate errors](images\4e9aca6c55d96794b8829ab44e64a63a.png)
