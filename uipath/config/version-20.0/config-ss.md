[title]: # (Configuration Steps for Secret Server)
[tags]: # (secret server)
[priority]: # (202)
# Configuration Steps for Secret Server

### Create an Application Account

1. Navigate to Secret Server and login.

   ![login](images/354a1c82b52524c49fdf564a5ec74745.png)

1. Click Log in

1. Click __Admin | Users__.

   ![Users](images/93ad973164dcc2904d28f61b121a8bb0.png)
1. Click the __Create New__ button at the bottom of the screen.

   ![Create New](images/febaeb602d40499f7c05064447cbe599.png)
1. Enter in a __User Name, Email Address and Password__.

   ![Enter](images/cca22bc2dc0fc8af8472765eab5ef0e1.png)
1. Click the __Advanced__ option.
1. Check the box for __Application Account__.
1. Click __Save__.

   >**Note:** Generally when the UIPath Application Account is a domain account, the AppPool should have "Load User Profile" set to true.

   ![Save](images/c8ce4a55dbbfd9588a1b2d1fc1618e5d.png)
1. Click __Ok__ on the next screen to convert the user to an Application Account.

   ![Ok](images/b9f583010415752a0b8495e8dc69be5d.png)
1. Click on __Assign Roles__.

   ![Assign Roles](images/cd81d8912e5d41d31dc450f49902bbb1.png)
1. Assign the __User__ role. (Please See our Best Practices Section if you would like to do Least Privilege)

1. Click __Save Changes__.

### Create a Secret for the UiPath Integration

1. Navigate back to __Home__ in Secret Server.

   ![Home](images/8ed0dfec27e37896c018c7fa3a96b15c.png)

1. Click on __(+)__ icon next to __Secrets__.

   ![Secrets](images/0034517c3c01ab565bd678a08e1f7f64.png)
1. Search for the __Windows Account__ template. Please be mindful that this is an example template we are using for these instructions. Any template may be used as long as a username and password is being referenced.

1. Click on __Windows Account__.

   ![Windows Account](images/92307bba399904054480d40510803b96.png)
1. For the New Windows Account template, you will need to complete the following fields:

   * __Name__: Name of the Secret

   * __Machine__: This can be anything in theory as the integration does not
        match based on the Secret Machine value and reads from the password
        field based on the SecretID. If you are using the Secret for
        RPC/Heartbeat, etc, then have this match a valid machine name FQDN

   * __Username and Password__: The account username and password that you
        intend to integrate with a UiPath asset.

1. Click __Create Secret__.

   ![Create Secret](images/bf712177c8764d8c47b54e8dcfa3deda.png)
1. Click on the __Sharing__ Tab, then __Edit.__

1. Under the Search area for __Add Groups/Users__, enter in your __UiPath application account__. The API account only requires “View” access to Secrets you intend to integrate with

1. Click __Save__.

   ![Save](images/9f60c898074ac90bafcc0bdeffee537b.png)