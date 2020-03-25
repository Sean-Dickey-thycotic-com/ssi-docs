[title]: # (Manage Host file)
[tags]: # (introduction)
[priority]: # (105)
# Manage Host file

You need to add the details of host file for communication between Secret Server and Dispatcher.

__To manage host file:__

1. Go to __IBM Security Identity Governance and Intelligence__ user interface.
1. Click __Manage System Settings | Network Settings | Hosts File__. The __Manage Hosts File__ page appears.

   ![managehostfile](images/managehostfile.png)
1. Click __New__ ![newicon](images/newicon.png) icon. The __Create Host Record__ dialog box appears.

   ![createhostrecord](images/createhostrecord.png)

   >**Note:** Fields marked with asterisk (*) are mandatory.

1. __Address:__ Type the IP address where the Dispatcher is installed.
1. __Host Name:__ Type the host name.
1. Click __Save__. The record is listed under __Hosts Records__ in the __Manage Host File__ page.
1. Click __New__ ![newicon](images/newicon.png) icon. The __Create Host Record__ dialog box appears.

   ![createhostrecordtwo](images/createhostrecordtwo.png)

   >**Note:** Fields marked with asterisk (*) are mandatory.

1. __Address:__ Type the IP address where the Secret Server is installed.
1. __Host Name:__ Type the host name.
1. Click __Save__.
1. The host record is listed under __Hosts Records__.

   ![managehostfiletwo](images/managehostfiletwo.png)
1. Go to __Windows Services__ and click __IBM Security Directory Integrator__ service.

   ![services](images/services.png)
1. Click __Restart__.
1. Go to the __Windows Firewall__.
1. Add port __1099__ to the Inbound Rule and Outbound Rule.

   >**Note:** This step is mandatory for successful connection of Secret Server and IBM IGI.
