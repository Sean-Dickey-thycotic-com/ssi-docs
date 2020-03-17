[title]: # (Configure the OpenID Connect Provider)
[tags]: # (introduction)
[priority]: # (104)
# Configure the OpenID Connect Provider

## Configure OpenID Connect Provider
The next step is to configure the OpenID Connect Provider. 

__To configure OpenID Connect Provider:__

1. Type the `IP address` along with the port number (For example: 10.60.25.21:9443) in the browser and press __Enter__.

   >**Note:** The default port number is 9443.

   ![accessibmigione](images/accessibmigione.png)

1. Click __Advanced__ and click __Proceed to `IP Address` (unsafe)__.

   ![accessibmigitwo](images/accessibmigitwo.png)

1. The __IBM IGI Login__ page appears.

      ![ibmlogintwo](images/ibmlogintwo.png)
1. Fill in the required information, such as the user name, password, and click __Log In__. The IBM IGI user interface appears.
     >**Note:** The default value for user name and password is `admin`.

1. Click __Configure__ > __Manage Server Setting__ > __OpenID Connect Provider Configuration__. The __Connect Provider Configuration__ page appears.

   ![openidconnectprovider](images/openidconnectprovider.png)
1. Click __Disable__.

   ![openidconnectproviderstatus](images/openidconnectproviderstatus.png)
1. A message, '__Are you sure you want to disable OpenID Connect Authentication configuration?__' appears.

   ![openidconnectprovidermessage](images/openidconnectprovidermessage.png)
1. Click __Yes__. The status of the configuration appears.

   ![openidconnectprovidersystemnotification](images/openidconnectprovidersystemnotification.png)

   >**Note:** In the IBM IGI UI, the notifications are listed in the __Notifications__ section.

   ![restartibmigiserver](images/restartibmigiserver.png)
1. In the __Server Control__ section, select the server and click __Restart__.

   ![restartibmigilocalmgmtinterface](images/restartibmigilocalmgmtinterface.png)
1. Go to the __IBM IGI Virtual Appliance__.

   ![Virtualappliancereboot](images/Virtualappliancereboot.png)
1. In the Virtual Appliance, type `reboot` and press __Enter__.
1. To confirm, type `YES` and press __Enter__. The __IBM IGI login__ dialog box appears.

   ![ibmigilogin](images/ibmigilogin.png)
1. Fill in the required information, such as the user name, password, and click __Log In__. The IBM IGI user interface appears.

   ![ibmigiuserinterface](images/ibmigiuserinterface.png)

The Virtual Appliance for IBM IGI is configured and setup. Now, the next step is to install [Security Directory Integrator 7.2](installing-security-directory-integrator-2.md).
