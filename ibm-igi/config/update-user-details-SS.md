[title]: # (Update user details in Secret Server through IBM IGI)
[tags]: # (introduction)
[priority]: # (108)
# Update user details in Secret Server through IBM IGI

The connector is configured, now you need to update the user details of Secret Server through IBM IGI. You need to:

* __Add user__
* __Configure accounts__

## Add user

__To add user detials in Secret Server through IBM IGI:__

1. Go to __IBM IGI Administrator Console__.
1. In the menu click __Access Governance Core__.

   ![accessgovernancemenutwo](images/accessgovernancemenutwo.png)
1. Click __Manage | Users__.

   ![agcmanageusers](images/agcmanageusers.png)
1. In the __Actions__ list, click __Add__.

   ![agcmanageusersadd](images/agcmanageusersadd.png)
1. In the __Details__ section, fill in the required information.

   ![agcmanageusersdetails](images/agcmanageusersdetails.png)

       a.	In the __User Type__ list, select `Employee`.
  
       b.	Select __OU Master__. In the __User Transfer__ dialog box, select `ACME Corp`  and click __OK__.
  
       c.	In the __Master UID__ text box, type the master user ID.
1. Click __Save__. The __Password__ dialog box appears.

   ![passworddialogbox](images/passworddialogbox.png)
1. Fill in the required infomation, such as new password, confirm password, and then click __OK__.

   >**Note:** The __Password Requirements__ appear on the right-hand side.

1. A message,‘__Operation successfully completed.__’appears.
1. Click __Ok__.

   ![informationdialogboxtwo](images/informationdialogboxtwo.png)
1. The __User__ is created in the __Users__ section.

   ![agcmanageuserscreated](images/agcmanageuserscreated.png)

The next step is to configure account.

## Configure account

__To configure account:__

1. Click __Account Configurations__.

   ![agcmanageaccountconfigurations](images/agcmanageaccountconfigurations.png)
1. Select the account.
1. On the right-hand side, click __Attribute-to-Permission Mapping__.

   ![agcattributetopermissionmappings](images/agcattributetopermissionmapping.png)
1. In the __Actions__ list, click __Discover Account attributes from Target__.

   ![agcattributetopermissionmappingactionslist](images/agcattributetopermissionmappingactionslist.png)
1. The __Discover Attributes from Target__ dialog box appears.

   ![discoverattributesfromtarget](images/discoverattributesfromtarget.png)
1. Select the __Attribute Name__ check box in the header.

   ![discoverattributesfromtargetheader](images/discoverattributesfromtargetheader.png)
1. Click __Import__. A message, ‘__Operation successfully completed.__’ appears. Click __Ok__.The files are imported.

   ![informationdialogboxtwo](images/informationdialogboxtwo.png)
1. On the right-hand side, click __Target Attributes__.

   ![targetattributes](images/targetattributes.png)
1. In the __Actions__ list, click __Discover Account attributes from Target__.

   ![discoveraccountattributesfromtargets](images/discoveraccountattributesfromtargets.png)
1. The __Discover Attributes from Target__ dialog box appears.

   ![discoverattributesfromtargettwo](images/discoverattributesfromtargettwo.png)
1. Select the __Attribute Name__ check box in the header.

   ![discoverattributesfromtargetheadertwo](images/discoverattributesfromtargetheadertwo.png)
1. Click __Import__. A message, ‘__Operation successfully completed.__’ appears. Click __Ok__. The files are imported.

   ![informationdialogboxtwo](images/informationdialogboxtwo.png)
1. On the left-hand side, select the __Users__ tab.

   ![manageusersaccountselected](images/manageusersaccountselected.png)
1. Select the user.
1. On the right-hand side, click __Accounts__. The master account is listed.

   ![manageuseraccounts](images/manageuseraccounts.png)
1. In the __Actions__ list, click __Add__.

   ![manageusersaccountactionslist](images/manageusersaccountactionslist.png)
1. The __New Account__ dialog box appears.

   ![newaccount](images/newaccount.png)
1. In the __Account Configuration__ list, select the Secret Server account. The __Account Creation__ tab is selected.

   ![newaccountexpanded](images/newaccountexpanded.png)
1. Go to  __Account Creation__ tab> __Details__ section > __Account ID__.
1. In the __Account ID__  text box, type the account ID and click __Next__. The __Password__ tab is selected.

   ![newaccountpassword](images/newaccountpassword.png)
1. Fill in the required information, such as new password, confirm password, and then click __Next__. The __Target Attributes__ tab is selcted.

   ![newaccounttargetattributes](images/newaccounttargetattributes.png)
1. In the __User’s Display Name__ text box, type the display name for the user.
1. Click __Save__. The user is listed in the __Accounts__ tab.

   ![userlistedinaccountid](images/userlistedinaccountid.png)
1. Click the __Events__ tab.

   ![manageuserseventstab](images/manageuserseventstab.png)
1. At the bottom of the __Events__ tab, click on __OUT Events__. The event is listed. Wait till the __Status__ and the __ERC Status__ is displayed as __Success__.
1. Go to __Secret Server | Admin | Users__.

   ![secretserveradminuser](images/secretserveradminuser.png)
1. The user is created in Secret Server. The user name and the display name for the user is displayed.
1. Go to __IBM IGI Administrator console__ and in the menu click __Access Governance Core__.
1. Click __Manage__ tab __Users | Accounts__.

   ![manageusersaccountstwo](images/manageusersaccountstwo.png)
1. Select the account.
1. In the __Action__ list, click __Edit__.

   ![manageusersaccountedit](images/manageusersaccountedit.png)
1. The __Edit Account__ dialog box appears.

   ![editaccount](images/editaccount.png)
1. Fill in the required information, such as first name, last name, email, display name, and then click __Next__. The __Target Attributes__ tab appears.

   ![editaccounttargetattributes](images/editaccounttargetattributes.png)
1. In the __User’s Display Name__ text box, change the display name for the user.
1. Click __Save__.
1. Click the __Events__ tab.
1. At the bottom of the __Events__ section, click __OUT Event__.

   ![manageuserseventstabtwo](images/manageuserseventstabtwo.png)

1. The event is listed. Wait till the __Status__ and the __ERC Status__ is displayed as __Success__.

   ![manageuserseventstabthree](images/manageuserseventstabthree.png)
