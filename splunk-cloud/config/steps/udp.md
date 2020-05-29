[title]: # (Configuration for UDP)
[tags]: # (udp)
[priority]: # (2)
# Configuration for UDP

1. Navigate to __Splunk Cloud__.
1. Click on __Download Universal Forwarder__.
1. Go to __downloads__ on the machine.
1. Right-click and copy the __`splunkclouduf.spl`__ file.
1. Navigate to the following file path: `c:\program files\SplunkUniversalforwarder\ect\apps`.
1. Riight click and paste the __`splunkclouduf.spl`__ file in the apps folder.
1. Open __Command Prompt__ as Admin.
1. In Command Prompt go to the following location: `c:\program files\SplunkUniversalforwarder\ect\apps`.
1. Run the following command: `tar xvf splunkclouduf.spl`
1. After the command completes successfully, go to the following file path: `cd c:\program files\SplunkUniversalforwarder\bin`.
1. Run the following command: `splunk install app c:\programfiles\SplunkUniversalforwarder\ect\apps\splunkclouduf.spl -auth <username:password>`
1. If the command was successful you should review the following message:
`App c:\program files\SplunkUniversalforwarder\ect\apps\splunkclouduf.spl installed`.
1. Navigate to __Secret Server__.
1. Go to __Admin | Configuration__.
1. Click on __Syslog/CEF logging Advanced Settings Information__.
1. Edit the following settings:
   __Enable Syslog/CEF Logging__: Yes
   __Syslog/CEF Server__: IP address for the server
   __Syslog/CEF Port__: Port number
   __Syslog/CEF Protocol__: UDP
1. Click __Save__.
1. Navigate back to __Splunk Cloud__.
1. Click on __Settings__.
1. Click on __Add Data__.
1. Click on __Forward__.
1. You can create a __New Server Class__ or select a previously created on.
1. Click on the option for __TCP/UDP__.
1. Click on __UDP__.
1. Enter the __port number__ for the server.
1. Click __Next__.
1. Click on __Source Type__.
1. Enter __`syslog`__.
1. Click on __Review__.
1. Review your settings and click __Submit__.
1. You can then click Start searching after the connection was successfully created.
