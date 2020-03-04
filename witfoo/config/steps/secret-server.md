[title]: # (Configure Secret Server)
[tags]: # (witfoo,secret server)
[priority]: # (2)
[display]: # (all)
# Configure Secret Server for WitFoo

You must configure settings in Thycotic Secret Server for WitFoo to fetch syslogs.

To configure Secret Server settings:

1. Sign into __Secret Server__.

  ![secret-server-1](images/secret-server-1.png)

  The __All Secrets__ page appears.

  ![secret-server-2](images/secret-server-2.png)
1. Click __Admin__ | __Configuration__.

   ![secret-server-3](images/secret-server-3.png)

   The __Configuration__ page appears.

   ![secret-server-4](images/secret-server-4.png)
1. At the bottom of the page, click __Edit__.

   ![secret-server-5](images/secret-server-5.png)

   The __Edit Configuration__ page appears.

   ![secret-server-6](images/secret-server-6.png)
1. Under __Syslog/CEF Logging Advanced Settings Information__ area, select __Enable Syslog/CEF Logging__ check box.

   ![secret-server-7](images/secret-server-7.png)
1. Configure the following settings:

    ![secret-server-8](images/secret-server-8.png)
    * In the __Syslog/CEF Server__ box__,__ type the __IP address__ of the WitFoo virtual appliance.
    * In the __Syslog/CEF Port__ box, type the __port number__ of the WitFoo virtual appliance.
    * In the __Syslog/CEF Protocol__ list, select the __protocol__.
1. Click __Save__.

   You will start receiving event logs. For example, in Secret Server, if you have created a user and assigned a role to the user, those logs are populated in the WitFoo virtual appliance.
1. Log in to the WitFoo Precinct virtual appliance with the registered credentials.
1. In the search bar enter the **IP address** of Secret Server.
