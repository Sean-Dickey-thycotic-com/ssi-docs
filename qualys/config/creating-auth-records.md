[title]: # (Creating Authentication Records)
[tags]: # (authentication)
[priority]: # (102)
# Creating Authentication Records

Once the authentication vault has been configured, individual authentication credentials can be configured to retrieve their passwords from Secret Server.

1. __Authentication | New | record type__.

   Authentication vault configuration requires three additional details to retrieve the password:

   * __Vault Type__: Set to Thycotic Secret Server.
   * __Vault Title__: The previously created Authentication Vault record in Qualys.
   * __Secret Name__: The Secret record in Secret Server containing the accounts password. In this case, the Secret name for the Windows account is Qualystest.

   ![record type](images/4b02782601a1f983f28f95fff25d5b9b.png)
1. Navigate to __Scan__ \> __Authentication__.

1. Click on __New__ dropdown and select __Windows Record__.

   ![Windows Record](images/62fa5c45468de445ae51c064542ee7cf.png)

   >**Note:** The Secret name must match the corresponding Secret name in Secret Server.

   ![Windows Authentication](images/d593ed0bee4d546c2960a59c4a274275.png)

   >**Note:** The __UserName__ in the above screenshot should be the same as the Secret's username. In addition to creating a Secret with the correct password for the credentials used for authenticated scanning, the Application account (set in the previous steps for Configuring the Vault, under step 4) must have at least a View access to the Secret.

1. Click __Share__ to view the permissions on the Secret.

   ![Share](images/4b02782601a1f983f28f95fff25d5b9b.png)

A Secret inherits permissions from the folder settings. View the folder level permissions by editing the folder in which the Secret is stored.

Once the Secret is configured with the proper permission, Qualys can use it in scans. Run a scan that uses that authentication record to verify that everything is working end-to-end.