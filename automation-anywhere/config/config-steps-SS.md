[title]: # (Configuration Steps for Secret Server)
[tags]: # (configuration)
[priority]: # (101)
# Configuration Steps for Secret Server

## Create an Application Account

1. Navigate to Secret Server and login.

   ![Secret Server](images/config8.png)
1. Click __Admin | Users__.

   ![Users](images/config9.png)
1. Click the __Create New__ button at the bottom of the screen.

   ![Create New](images/config10.png)
1. Enter in a __User Name, Email Address and Password__.
1. Click the __Advanced__ option.
1. Check the box for __Application Account__.
1. Click __Save__.
1. Click __Ok__ on the next screen to convert the user to an Application Account.

   ![Application Account](images/config13.png)
1. Click on __Assign Roles__.

   ![Assign Roles](images/config14.png)
1. Assign the __User__ role.
1. Click __Save Changes__.

## Create a Secret for Automation Anywhere

1. Navigate back to __Home__ in Secret Server.
1. Click on __(+)__ icon next to __Secrets__.

   ![Secrets](images/config17.png)
1. Search for the __Windows Account__ template.
1. Click on __Windows Account__.

   ![Windows Account](images/config18.png)
1. For the New Windows Account template, you will need to complete the following fields:
   * __Name__: Name of the Secret
   * __Machine__: The server that Automation Anywhere is installed onto
   * __Username and Password__: The account that has access to the Automation Anywhere Server
1. Click __Create Secret__.
1. Click on the __Sharing__ Tab.
1. Click on __Edit__.
1. Under the Search area for __Add Groups/Users__, enter in your __Automation Anywhere application account__.
1. Click __Save__.
