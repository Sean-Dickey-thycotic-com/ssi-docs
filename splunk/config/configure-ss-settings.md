[title]: # (Configuring Secret Server settings)
[tags]: # (universal forwarder )
[priority]: # (105)
# Configuring Secret Server settings

## To configure Secret Server Settings:

1. Sign into __Secret Server__.

   ![](images/0eedc8bb0eff1f03bd0f20061a4c30ec.png)
1. The __Home__ page appears.

   ![](images/1e65851bcd136b7f9a108bdb1fca34f6.png)
1. Click __Admin__ | __Configuration__. The __Configuration__ page appears.

   ![](images/a58bbf3275604a165dac6b461f482a37.png)
1. At the bottom of the page, click __Edit__.  

   ![](images/25e5d8a7bf3355c0bc3c7da4fcaa2b9e.png)
1. The __Edit Configuration__ page appears.  

   ![](images/722f099281644345c3c702cde67f1ac9.png)
1. Select the __Enable Webservices__ settings check box.

1. Under the __Syslog/CEF Logging Advanced Settings Information__ area, select the __Enable Syslog/CEF Logging__ check box and enter the __syslog server__

   >**Note:** This should be the ip of machine/server where splunk enterprise is configured).

   ![](images/38804bb218865a5da3554f51dbd04a8d.png)

1. At the end of the page, click __Save__.  

   ![](images/7b6fdf795f3df95b9e51184f323d434e.png)

## Configuration in Splunk Enterprise

1. Go to __Splunk enterprise__ | __Settings__ | __Add Data__ | Click on __Monitor__.

1. The __Select Source__ page appears. On the left-hand side, click __TCP/UDP.__

1. On right hand side, select UDP/TCP and enter the port which we have configured in Secret Server, Example: __TCP 6514__.  

   ![](images/b2eab78e51ab0e190419b1c2fb09c312.png)
1. Click __Next__. On __Input Settings__ page select source type as syslog.  

   ![](images/63a580a1a1e4f814bf028afa609d4800.png)
1. In the __Index__ list, select __Default__.
1. Click __Review__. The __Review__ page appears, review the information.
1. Click __Submit__. The message “__File input has been created successfully.__” Appears

   ![](images/24747bbe7a251b8fc5f723cdf6ceac91.png)
1. Click __Start Searching__. The __New Search__ page appears.
1. In the __New Search__ text box, type the query and click __Search icon__.

   ![](images/faac80ef3661a00079211b75ff7cc1bf.png)
