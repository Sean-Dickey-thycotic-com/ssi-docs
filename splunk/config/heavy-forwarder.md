[title]: # (Setting up the Windows heavy forwarder)
[tags]: # (heavy forwarder)
[priority]: # (103)
# Setting up the Windows heavy forwarder to forward data to the splunk cloud

Setting up a [heavy](https://docs.splunk.com/Splexicon:Heavyforwarder) forwarder is a two-step process:

## Install a full Splunk Enterprise instance

1. After completing the installation, log in to your Splunk as an admin on the instance that will be forwarding data.

1. Click __Settings__ | __Forwarding and receiving__.  

   ![Forwarding and receiving](images/0bf37bc88a3eded542f6d9d44debe8d9.png)
1. Select __Forwarding defaults__.  

   ![Forwarding defaults](images/2cedded6901a2663eb96cee040687f6b.png)
1. Select __yes__ to store and maintain a local copy of the indexed data on the forwarder.  

   ![forwarder](images/c52420ad8c5e8c0277ea68521edfd8bb.png)
1. At Configure forwarding, click __Add new__.  

   ![Add new](images/75efb64b461002a60cb5af8ae7538826.png)
1. Enter the hostname or IP address for the receiving Splunk instance(s), along with the __receiving port__ specified when the receiver was configured. For example, you might enter __receivingserver.com:9997__.

   ![receiving port](images/b3191d4f006d1a939df96df11662f808.png)
1. Click __Save__.
1. Navigate to __Server Control__ by clicking on __Setting__ | __Server Control__.

   ![Server Control](images/597fe5cf0589f315f512ad413cdd243c.png)
1. Click on __Restart Splunk__.

   ![Restart Splunk](images/2450155435e0e226193360d147bf9295.png)
1. Download the SPL package from your splunk cloud.

   >**Note:** It is not the regular universal forwarder exe you get from splunk (no need to install the separate universal forwarder software).<https://yourcloudname.splunkcloud.com/en-US/app/splunkclouduf/setupuf>

1. On the Splunk Cloud Home page, click __Download Universal Forwarder Credentials__ to download the splunkclouduf.spl file.

   ![Download Universal Forwarder Credentials](images/dcb781352a296f07430055d41dfefc5b.png)
1. When prompted, click __Save File__ and click __OK__. By default,
the splunkclouduf.spl file downloads to the Downloads directory. If you download to a different location, make note of that location.

1. Move the splunkclouduf.spl file to the `C:\\ProgramFiles\\Splunk\\etc\\apps directory of your enterprise.`
1. Open a command prompt window and run the following command:
`tar xvf splunkclouduf.spl`.

1. Navigate to the `/bin subdirectory` of your deployment server.

1. In the command prompt window, Run the following command on your Splunk Heavy Forwarder (or whatever path you install splunk too) :

   ```
    __splunk install app \<full path to splunkclouduf.spl| -auth
    \<username|:\<password|__ where \<full path to splunkclouduf.spl| is the path to the directory where the splunkclouduf.spl file is located and \<username|:\<password| are the username and password of splunk enterprise.

   ```

1. Restart your forwarder: `/splunk restart`.
1. Once splunk is restarted you'll need to check the correct __output.conf__ is installed.
1. Make sure that `C:\\ProgramFiles\\Splunk\\etc\\apps\\yourcloudnamesplunkcloud\\default\\outsputs.conf`is the same as `C:\\Program Files\\Splunk\\etc\\system\\local\\outputs.conf`.

1. __If__ the files above aren't the same copy `C:\\ProgramFiles\\Splunk\\etc\\apps\\yourcloudnamesplunkcloud\\default\\outsputs.conf to C:\\Program Files\\Splunk\\etc\\system\\local\\outputs.conf and restart splunk.`

## Configuring Secret Server settings

__To configure Secret Server settings:__

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

## Configuration in Splunk enterprise

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

## Accessing Secret Server Events in the SplunkCloud

Login to splunk cloud and click on __search and Reporting and__ enter the query: `source=”syslog”` and click __Search icon__.

   ![](images/3ee96cc9ae6ebcbb6855393408a73342.png)
