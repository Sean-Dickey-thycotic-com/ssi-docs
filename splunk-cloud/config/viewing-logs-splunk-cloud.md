[title]: # (Viewing logs in Splunk Cloud)
[tags]: # (introduction)
[priority]: # (105)
# Viewing logs in Splunk Cloud

To view logs in the Splunk cloud, you must first clear the Secret Server
Application Pool and then add data. After adding data, you must search for the
logs using a query.

**To clear and add data:**

1.  Type IIS in the **Search** box. The **Internet Information Services (IIS)
    Manager app** is populated.

    ![](media/d6e83bea620e0eeda623e49f4a9cb570.png)

2.  Click the **Internet Information Services (IIS) Manager** app. The
    **Internet Information Services (IIS) Manager** dialog box appears.

3.  Go to **Connections** \> **Application Pools** \> **SecretServer**.

    ![](media/c783635423dfd1fa2d406900ddafdd9a.png)

4.  Right-click **SecretServer** and click **Recycle**.

5.  Go to **Splunk Cloud Instance** \> **Settings** \> **Add Data** \>
    **Forward**. The **Select Forwarders** page appears.

    ![](media/055ff81572522f34b6c990784d7e250c.png)

    In the **Available host(s)** text box, the computer on which the Universal
    Forwarder instance is installed is displayed.

6.  Click **Existing** \> **Select** \> Select the name of the Server Class.

    ![](media/55baf8e76744d83bcb7765bb2e166d84.png)

**Note:** To select a new server class, click **New** and add a new **Server
Class**.

The Universal Forwarder is selected. This Universal Forwarder sends data to the
Splunk platform.

![](media/498d2d65b08202cda8ff8167480b17ed.png)

1.  Click **Next**. The **Select Source** page appears.

    ![](media/ff3d0797955376af5f4d913ca1e6a8c0.png)

2.  On the left-hand side, click **Files & Directories**.

    ![](media/78cdef85e7708c5637cd615f0e0102d9.png)

3.  In the **File or Directory** text box, type the path of the syslog file that
    is created in [Step 1](#Adding_Keys_Step_01).

4.  Click **Next**. The **Input Settings** page appears.

    ![](media/9dbb756481acd86fb1552df93a6563fb.png)

5.  Click **Source type** as **Automatic**

6.  In the **Index** list, select **Default**.

7.  Click **Review**. The **Review** page appears.

    ![](media/08bcb075a354334bcc4636e6fb8947c4.png)

8.  In the **Review** page, review the information.

9.  Click **Submit**. The message “**File input has been created
    successfully.**” appears.

    ![](media/d897c291e77fccd6624a5b8bf539273e.png)

10. Click **Start Searching**. The **New Search** page appears.

    ![](media/a7c27070481fc09f6584e7ac269bb9cb.png)

11. In the **New Search** text box, type the query and click Search

    ![](media/cf99b0eb8675e6b3ea7360d29a29c5b7.png)

    icon.

>   *Note: For more information on search, see the following link:*
>   <https://docs.splunk.com/Documentation/Splunk/latest/SearchReference/Search>

![](media/2b70387416120596cf60c831e23cf322.png)

The Syslogs from the secret server appears along with the details.

![](media/3bc5bdad55fb411b56ece9b03ad0ff1a.png)

The logs can be successfully viewed in the Splunk Cloud.