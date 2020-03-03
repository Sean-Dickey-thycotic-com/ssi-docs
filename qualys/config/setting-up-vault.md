[title]: # (Setting up the Vault)
[tags]: # (vault)
[priority]: # (101)
# Setting up the Vault

To use Secret Server, an administrator must configure it as a Vault within Qualys by specifying a URL and credentials to access the on-premises Secret Server instance. Instead of adding username/password credentials for use in trusted scans, the administrator can point to named records that are stored in
Secret Server. Qualys will retrieve the credentials from Secret Server at scan time for trusted scans.

1. Add a new Authentication Vault in Qualys. Navigate to the __Authentication__ tab.
1. Click __Authentication Vaults__ from the __New__ menu section.

   ![Figure 1](images/ab1ba9c25f855f8c2748c4f81835f9a8.png)

   ![Figure 2](images/f0dc00bda3bf6d0deb0b61b7eab2f02d.png)

1. Select __Thycotic Secret Server__ from the list of vaults. Enter the following access information for your Secret Server site:

1. __URL This__ is the URL for Secret Server web services. Ensure that web services are enabled in your Secret Server instance by clicking __Configuration__ from the __Administration__ menu and enabling web services.

1. Add __/sswebservices/sswebservice.asmx__ to your Secret Server URL to obtain the URL for the web services:

   * Example: https://yoursecretserver/sswebservices/sswebservice.asmx

   ![URL](images/6c9057902c0471c3824d54bc15046bd4.png)

   >**Note:** If you do not have SSL enabled, web services can be accessed on http, but that is not advisable for production systems. The vault is accessed from the scan agent, so the Secret Server website must be reachable from the Qualys scanner appliance, not the Qualys cloud instance.

1. __User Name:__ The user account for accessing Secret Server. This can either be local Secret Server account, or an Active Directory account. User accounts can be created in Secret Server from the __Users__ section of the __Administration__ menu. This user account should be application account. Click on __Advance Option__.
1. Click the checkbox of Application Account and __Save__.

   ![Save](images/2f0ffbf92b0b743ddd8950402749163b.png)
