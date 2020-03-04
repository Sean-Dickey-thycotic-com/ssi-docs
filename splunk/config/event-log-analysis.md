[title]: # (Configuration and Event Log Analysis)
[tags]: # (configuration)
[priority]: # (101)
# Initial Configuration and Event Log Analysis

Use the steps below to quickly configure SS and Splunk. To setup your external
audit server to gather events that you can export from SS:

1. Navigate to **Admin \> Configuration.**

   ![](images/1.png)
1. Click the **Edit** button at the bottom of the page.

1. If necessary, click the **General** tab.

   ![general](images/2.jpg)
1. Scroll down to the **Syslog/CEF Logging…** section:

1. Click to enable the **Syslog/CEF Logging** check box. The Syslog/CEF
    Logging… section appears:

   ![](images/3.png)
1. Type the Splunk server's IP address in the **Syslog/CEF Server** text box.

1. Type the Splunk server's port in the **Syslog/CEF Port** text box.

1. Click to select the **Syslog/CEF Protocol** dropdown list and select
    **TCP**.

1. Click to select the **Syslog/CEF Site** dropdown list and select **Local**.

1. Click the **Save** button at the bottom of the page.