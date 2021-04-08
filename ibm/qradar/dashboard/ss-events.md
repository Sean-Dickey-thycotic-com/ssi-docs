[title]: # (Accessing Secret Server Events)
[tags]: # (events)
[priority]: # (302)
# Accessing Secret Server Events in the Secret Server Application within QRadar

1. Login to QRadar as the admin user: `https://<ipaddress>`

   ![](images/8a69f0826c6758514ab82ae604b22048.png)
1. Download __Thycotic Secret Server Dashboard__ extension from <https://exchange.xforce.ibmcloud.com/>.  

   ![](images/2fff8a56cfaa7225e43503a245ea51dc.png)
1. Login to QRadar with Admin role and navigate to the __Extension management__ by clicking on __Admin | Extension Management__.  

    ![](images/184569bdd96bbade61459fefe306855b.png)
1. __Extension Management__ will be displayed and click on __Add__.

   ![](images/4caffd178325c072d557e13c1c952acf.png)
1. Browse to __Thycotic Secret Server Dashboard__ extension downloaded from IBM Exchange, click on the __Add button__.

   ![](images/276f39c44add10626d9287a400a91dd8.png)
1. Download Pulse App from <https://exchange.xforce.ibmcloud.com/> and install the Pulse extension by navigating to extension Management.

   ![](images/2fff8a56cfaa7225e43503a245ea51dc.png)

## Create log source

1. Click __on Admin | Log source__.

   ![](images/07cf3a6e0a06e6c52dd562302b247ab5.png)
1. Click on the __Add__ button.
1. Add log source popup will be displayed.

    1.  Enter the Name down the Log Source Name which will be required in Step 9 in Pulse Dashboard Setup.

    1.  Description.

    1.  Select the log source type created in above steps.

    1.  Enter the __Log source Identifier__ as Host Name of machine where Secret Server is installed.

    1.  Click __Save__.

   ![](images/54f2261433114e0f3fabd1420e089ba0.png)

# Deploy Log Source

1. On the __Admin Page of QRadar__, click on __deploy changes__ button.

   ![](images/48c6869e6d9f8a58aacabfaa0e936afb.png)