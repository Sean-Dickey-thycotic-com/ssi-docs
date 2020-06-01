[title]: # (Verifying Integration)
[tags]: # (introduction)
[priority]: # (5)
## Verifying Integration / Troubleshooting

### Validation Process

You can validate the integration is working two different ways. First, you can
run a **Test Credential** action directly on the Credential you have added

![](images\b7bb42f223bf596db6e793fc02aeda36.png)

![](images\48a534ec67de1cecf454c2589a8d5ea3.png)

The second way to verify is to configure a **Discovery Schedule** and run it
against a destination system in which you know the credentials will work for an
authenticated scan. Below is an example of the configuration against a singular
system

![](images\2785aee68e6110ccfa77a27207ad018a.png)

Another screenshot is provided below for the results:

![](images\dce997113cfd1e2f6091ec0791cfd40a.png)

Below is the individual asset results:

![](images\9ac0044fd5d7de8191b5084262411ea0.png)

![](images\68cbb8ea204582e4aa4d405c74f4725b.png)

### Certificate Errors in Agent log files

Another area that might require troubleshooting is if you observe this in your
mid server agent log files:

![](images\4e9aca6c55d96794b8829ab44e64a63a.png)

If you are using this default parameter in the config.xml file, but have not
imported your Secret Server certificate into the Java keystore, its possible
that this error will prevent integration. You can alternatively set this flag to
“true”.

**\<parameter name="ext.tss.allow.self_signed_certificates" value="false" /\>**

Please note that if your Secret Server environment is using a certificate
(HTTPS), which is likely, you will want to import your public key web server
certificate into the Java keystore. Below is a screenshot of the command line
option for this. This command needs ran from the jre/jdk bin directory:

Keytool -import -alias desiredaliasname -file “path\\to\\public.cer” -keystore
“java\\path\\to\\cacerts”

![](images\3c108790a72d8207126f8b38f4bbfa47.png)

The default password to the Java keystore is: **changeit**

It will prompt you to import the certificate. Type in “Yes” and hit enter.

Verification of import of certificate via KeyStore Explorer

![](images\57029fd84282dabf93b159a55d2745c9.png)

In our testing it was only required for us to import the Web Server certificate
itself and not our root certificate. Your results may vary.

The Mid-Server integration also has its own Java keystore that is located at:

\\Service
Now\\mid.newyork-06-26-2019__patch2-09-18-2019_09-24-2019_1701.windows.x86-64\\agent\\keystore

We’ve observed that importing your public Secret Server certificate into this
keystore corrupts the Mid-Server keystore. It should only be necessary to import
the certificate into the main Java keystore. We observed that If you do
accidentally import this into the agent specific keystore, you can fix that
keystore by simply “rekeying” the Mid-Server.

![](images\a6c3e1465a0d54d5e7c068600bd789cb.png)

### Discovery Producing Access_Denied Messages for Hosts

If you observe an Access Denied issue when using an Active Directory template
and running a Discovery Schedule, this can be resolved two different ways:

1.  Adjust the Secret in Secret Server to append the domain to the username
    field:

![](images\22b6700629cca2d8475dbb78756650d5.png)

ServiceNow does not have a field mapping for the Domain field. This means that
if a domain must be supplied to authenticate to a destination system for the
integration, this must be provided in the Username field in Secret Server. For
Active Directory templates, this will result in what is pictured above. For
Windows templates, it may be necessary to specify “.\\” before the machine name.
For more details on acceptable Windows credential type fields, please check this
link:

<https://docs.servicenow.com/bundle/london-servicenow-platform/page/product/credentials/reference/r_WindowsCredentialsForm.html#d816677e164>
