[title]: # (Secret Server Dashboard)
[tags]: # (dashboard)
[priority]: # (304)
# Extension Configuration

1. In the System Configuration section, click __Extensions Management__.

   ![](images/a510e1ad9b64a255489da0e1232a3ddc.png)

## In the Extensions Management window

1. Click __Add__.
1. Select the app archive downloaded from IBM App Exchange.
1. Select the __Install immediately__ check box.

   ![](images/a40de416471e321fe7f65ebd5b5892f5.png)

   >**Note:** When the installation is complete, refresh the browser window before you use the extension

## Create Authentication Token

Before you can use the extension, you must create an __authentication token__. IBM QRadar requires that you use an authentication token to authenticate the QRadar API calls that the extension leverages. You use the __Manage Authorized Services__ window on the __Admin__ tab to create authentication token.

1. On the __Admin__ tab, go to the __User Management__ section.
1. Click __Authorized Services__.
   
   ![](images/6654a12d5702590207a1b75eef1e275e.png)

## Create token

1. In the Manage Authorized Services window, click __Add Authorized Service__.

   ![](images/30e9a2fcdf41a91dd92b25df9b0048a5.png)

## Add the following information to the Add Authorized Service fields

* In the __Service Name__ field, type a name for this authorized service

* From the __User Role__ list, select __Admin__ the user role

* From the __Security Profile__ list, select the security profile that you want to assign to this authorized service

* In the __Expiry Date__ list, type or select a date that you want this service to expire. If an expiry date is not necessary, select __No Expiry__

* Click __Create Service__

   ![](images/a71c298a2adb448e63a98fdbc4fb93e2.png)

## Copy Token

1. Click the row that contains the created service.

1. Copy the token string from the __Selected Token__ field in the “*menu bar”*.

1. Close the Manage Authorized Services window.

   ![](images/684956e23515d8ddb4cc9e163dd15a5a.png)

## Add token to enable extension

1. Navigate to __admin__ | __Secret Server Dashboard__ under App section

   ![](images/d79658914539bb3e5ac6a9dd74d6e998.png)
1. The Configuration page will be displayed.
1. Enter the __Log source identifier__ previously configured.
1. Paste the token string into the __SEC Token__ field.

   ![](images/f59cdbb93fe6b2fdb00de10ae386f4c4.png)

   >**Note:** This SEC token will be used in the Secret Server app to display dashboard, reports etc.

1. Click __Save__.

## Viewing the extension

1. Click the *“Secret Server dashboard”*

   ![](images/cf2968cf40288703e2a41539a7fa32aa.png)

   ![](images/2f215b37ab997b1f23b34c4b4899219a.png)
