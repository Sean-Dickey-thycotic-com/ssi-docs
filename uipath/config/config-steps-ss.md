[title]: # (Configuration Steps for Secret Server)
[tags]: # (configuration, uipath)
[priority]: # (203)
# Configuration Steps for Secret Server

## Create an Application Account

1. Navigate to Secret Server and login.

   ![Log in](images/config8.png)
1. Click __Admin | Users__.

   ![Log in](images/config9.png)
1. Click the __Create New__ button at the bottom of the screen.

   ![Log in](images/config10.png)
1. Enter in a __User Name, Email Address and Password__.

   ![Log in](images/config11.png)
1. Click the __Advanced__ option.
1. Check the box for __Application Account__.
1. Click __Save__.

   ![Log in](images/config12.png)
1. Click __Ok__ on the next screen to convert the user to an Application Account.

   ![Log in](images/config13.png)
1. Click on __Assign Roles__.

   ![Log in](images/config14.png)
1. Assign the __User__ role.
1. Click __Save Changes__.

## Create a Secret for the UiPath

1. Navigate back to __Home__ in Secret Server.

   ![Log in](images/config16.png)
1. Click on __(+)__ icon next to __Secrets__.

   ![Log in](images/config17.png)
1. Search for the __Windows Account__ template.
1. Click on __Windows Account__.

   ![Log in](images/config18.png)
1. For the New Windows Account template, you will need to complete the following fields:
   * __Name__: Name of the Secret
   * __Machine__: The server that UiPath is installed onto
   * __Username and Password__: The account that has access to the UiPath Server
1. Click __Create Secret__.

     ![Log in](images/config19.png)
1. Click on the __Sharing__ Tab.

     ![Log in](images/config20.png)
1. Click on __Edit__.

     ![Log in](images/config21.png)
1. Under the Search area for __Add Groups/Users__, enter in your __UiPath application account__.
1. Click __Save__.

     ![Log in](images/config22.png)
