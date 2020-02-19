[title]: # (Constraints)
[tags]: # (introduction)
[priority]: # (2)
# Known Constraints and Limitations

* This integration performs credentialed scans of Windows and Linux (SSH) hosts with passwords or private keys retrieved directly from Secret Server. Current matching of credentials occurs only based on the Secret Name field

* The integration currently utilizes only SOAP API calls

* The integration will not work with our Secret Server Cloud offering due to rate limit issues observed which can potentially affect the performance of multiple tenants

* Updated tenable.io instructions have been provided, but we have not observed that the integration itself works against Secret Server On-Premise publicly available Web Server installations. We observe that Tenable.io “Views” the credential but it is never used in the credentialed scan. A ticket has been submitted (1/20/2020) to Tenable to further investigate this and debug logs have been provided to Tenable.
