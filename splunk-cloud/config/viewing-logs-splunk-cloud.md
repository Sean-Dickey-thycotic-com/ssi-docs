[title]: # (Viewing logs in Splunk Cloud)
[tags]: # (introduction)
[priority]: # (105)
# Viewing logs in Splunk Cloud

To view logs in the Splunk cloud, you must first clear the Secret Server
Application Pool and then add data. After adding data, you must search for the
logs using a query.

## To clear and add data

1. Type IIS in the __Search__ box. The __Internet Information Services (IIS)
    Manager app__ is populated.

    ![Search](images/d6e83bea620e0eeda623e49f4a9cb570.png)
1. Click the __Internet Information Services (IIS) Manager__ app. The
    __Internet Information Services (IIS) Manager__ dialog box appears.

1. Go to __Connections | Application Pools | Secret Server__.

   ![Secret Server](images/c783635423dfd1fa2d406900ddafdd9a.png)
1. Right-click __SecretServer__ and click __Recycle__.

1. .  Go to __Splunk Cloud Instance | Settings | Add Data__ |
    __Forward__. The __Select Forwarders__ page appears.

   ![Select Forwarders](images/055ff81572522f34b6c990784d7e250c.png)
1. In the __Available host(s)__ text box, the computer on which the Universal
    Forwarder instance is installed is displayed.

1. Click __Existing | Select | Select the name of the Server Class__.

   ![Select the name of the Server Class](images/55baf8e76744d83bcb7765bb2e166d84.png)

   >**Note:** To select a new server class, click __New__ and add a new __Server Class__.

The Universal Forwarder is selected. This Universal Forwarder sends data to the
Splunk platform.

   ![Server Clas](images/498d2d65b08202cda8ff8167480b17ed.png)

1. Click __Next__. The __Select Source__ page appears.

   ![Select Source](images/ff3d0797955376af5f4d913ca1e6a8c0.png)
1. On the left-hand side, click __Files & Directories__.

   ![Files & Directories](images/78cdef85e7708c5637cd615f0e0102d9.png)
1. In the __File or Directory__ text box, type the path of the syslog file that
    is created in [Step 1](#Adding_Keys_Step_01).
1. Click __Next__. The __Input Settings__ page appears.

    ![Input Settings](images/9dbb756481acd86fb1552df93a6563fb.png)
1. Click __Source type__ as __Automatic__

1. In the __Index__ list, select __Default__.

1. Click __Review__. The __Review__ page appears.

    ![Review](images/08bcb075a354334bcc4636e6fb8947c4.png)
1. In the __Review__ page, review the information.
1. Click __Submit__. The message “__File input has been created successfully.__” appears.

    ![Submit](images/d897c291e77fccd6624a5b8bf539273e.png)
1. Click __Start Searching__. The __New Search__ page appears.

    ![New Search](images/a7c27070481fc09f6584e7ac269bb9cb.png)
1. In the __New Search__ text box, type the query and click Search icon.

    ![New Search](images/cf99b0eb8675e6b3ea7360d29a29c5b7.png)

   >**Note:** For more information on search, see the following link: <https://docs.splunk.com/Documentation/Splunk/latest/SearchReference/Search>

   ![More information](images/2b70387416120596cf60c831e23cf322.png)

   The Syslogs from the secret server appears along with the details.

   ![Syslogs](images/3bc5bdad55fb411b56ece9b03ad0ff1a.png)

   The logs can be successfully viewed in the Splunk Cloud.
