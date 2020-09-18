[title]: # (Setting up the Windows Heavy Forwarder)
[tags]: # (heavy forwarder)
[priority]: # (103)
# Setting up the Windows Heavy Forwarder to forward data to the splunk cloud

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
