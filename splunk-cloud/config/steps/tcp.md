[title]: # (Configuration for TCP)
[tags]: # (tcp)
[priority]: # (1)
# Configuration for TCP

>**Note:** Using TCP over the UDP Protocol is preferable when attempting to capture events from Secret Server.

After configuring the Universal Forwarder, please follow the steps below to enable the TCP protocol to collect the syslog for the desired Secret Server instance(s).

1. Navigate to __Secret Server__.
1. Go to __Admin | Configuration__.
1. Click on __Syslog/CEF logging Advanced Settings Information__.
1. Edit the following settings:
   __Enable Syslog/CEF Logging__: Yes
   __Syslog/CEF Server__: IP address for the server
   __Syslog/CEF Port__: Port number
   __Syslog/CEF Protocol__: TCP
1. Click __Save__.
1. Navigate back to __Splunk Cloud__.
1. Click on __Settings__.
1. Click on __Add Data__.
1. Click on __Forward__.
1. You can create a __New Server Class__ or select a previously created on.
1. Click on the option for __TCP/UDP__.
1. Click on __TCP__.
1. Enter the __port number__ for the server.
1. Click __Next__.
1. Click on __Source Type__.
1. Enter __`syslog`__.
1. Click on __Review__.
1. Review your settings and click __Submit__.
1. You can then click Start searching after the connection was successfully created.
