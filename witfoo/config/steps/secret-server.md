[title]: # (Secret Server)
[tags]: # (witfoo,secret server)
[priority]: # (2)
[display]: # (all)

# What to do in Secret Server

You must configure settings in Thycotic Secret Server for WitFoo to fetch
syslogs.

To configure Secret Server settings:

1.  Sign into **Secret Server**.

![secret-server-1](images/secret-server-1.png)

The **All Secrets** page appears.

![secret-server-2](images/secret-server-2.png)

1.  Click **Admin** \> **Configuration**.

    ![secret-server-3](images/secret-server-3.png)

    The **Configuration** page appears.

    ![secret-server-4](images/secret-server-4.png)

1.  At the bottom of the page, click **Edit**.

    ![secret-server-5](images/secret-server-5.png)

    The **Edit Configuration** page appears.

    ![secret-server-6](images/secret-server-6.png)

1.  Under **Syslog/CEF Logging Advanced Settings Information** area, select
    **Enable Syslog/CEF Logging** check box.

    ![secret-server-7](images/secret-server-7.png)

1.  Configure the following settings:

    ![secret-server-8](images/secret-server-8.png)

-   In the **Syslog/CEF Server** box**,** type the **IP address** of the WitFoo
    virtual appliance.

-   In the **Syslog/CEF Port** box, type the **port number** of the WitFoo
    virtual appliance.

-   In the **Syslog/CEF Protocol** list, select the **protocol**.

1.  Click **Save**.

    You will start receiving event logs. For example, in Secret Server, if you
    have created a user and assigned a role to the user, those logs are
    populated in the WitFoo virtual appliance.
