[title]: # (Configuring Secret Server settings)
[tags]: # (configuration)
[priority]: # (301)
# Configuring Secret Server settings

1. Sign into __Secret Server__.

   ![](images/0eedc8bb0eff1f03bd0f20061a4c30ec.png)
1. The __Home__ page appears.

   ![](images/1e65851bcd136b7f9a108bdb1fca34f6.png)
1. Click __Admin__ | __Configuration__.

   ![](images/a58bbf3275604a165dac6b461f482a37.png)
1. At the bottom of the page, click __Edit__.  

   ![](images/25e5d8a7bf3355c0bc3c7da4fcaa2b9e.png)
1. The __Edit Configuration__ page appears.  

   ![](images/722f099281644345c3c702cde67f1ac9.png)
1. Select the __Enable Webservices__ settings check box.

1. Under the __Syslog/CEF Logging Advanced Settings Information__ area, select the __Enable Syslog/CEF Logging__ check box and enter the __syslog server__.

   >**Note:** The syslog server should be the ip of machine/server where universal forwarder is configured), UDP port etc.

   ![](images/be23b83cbbcb90c924421f7d8a3b73eb.png)
1. At the end of the page, click __Save__.  

    ![](images/7b6fdf795f3df95b9e51184f323d434e.png)

*At this point all required configuration to get SysLog information from Secret Server into QRadar is complete.*