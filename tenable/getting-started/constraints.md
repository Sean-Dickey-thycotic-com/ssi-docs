[title]: # (Constraints)
[tags]: # (introduction)
[priority]: # (2)
# Known Constraints and Limitations

* This integration performs credentialed scans of Windows and Linux (SSH) hosts with passwords or private keys retrieved directly from Secret Server. Current matching of credentials occurs only based on the Secret Name field.

* The integration currently utilizes only SOAP API calls.

* The integration will not work with Thycotic Secret Server Cloud due to rate limit issues observed which can potentially affect the performance of multiple tenants.
