[title]: # (Integrate Secret Server with IBM IGI Admin Console)
[tags]: # (introduction)
[priority]: # (102)
# Integrate Secret Server with IBM IGI Admin Console

The integration of Secret Server is done with IBM IGI Admin Console to fetch Secret Server data into IBM IGI Admin Console.

Following are the steps: 

* [Import attribute mapping file](#Import-attribute-mapping-file)
* [Configure the connector](#Configure-theconnector)
* [Update user details in Secret Server through IBM IGI](#Update-user-details-in-Secret-Server-through-IBM-IGI)
     * [Add user](#Add-user)
     * [Configure account](#Configure-account)
     * [Check user details and change password](#Check-user-details-and-change-password)

The detailed procedure for each step  is explained below.

## Import attribute mapping file

You can import the attribute mapping files using the IBM IGI Administration Console.

**To import the attribute mapping file:**
1.	Sign into **Secret Server**. 

     ![secretserverlogin](images/secretserverlogin.png)

     The **All Secrets** page appears.

     ![allsecretspage](images/allsecretspage.png)

2.	Click **Admin** > **Folders**. 

    ![admindfoldersmenu](images/admindfoldersmenu.png)

     The **Folders** page appears.

     ![folderspage](images/folderspage.png)

3.	Double-click **Personal Folders**. Verify the presence of **admin** folder.

4.	Click **Admin** > **Groups**. The **Groups** tab appears. Verify the presence of **Everyone** group.

    ![admingroups](images/admingroups.png)

5.	Go to **IBM Security Identity Governance and Intelligence** administrative UI.

    ![ibmigiloginpage](images/ibmigiloginpage.png)

6.	Fill in the required information, such as user name, password, and click **Login**. The **IBM IGI Administration Console** dashboard appears.

    ![ibmigidashboard](images/ibmigidashboard.png)

7.	In the **Quick Links** section, click **IBM Security Identity Governance and Intelligence Administration Console**.

     > **Note:** If you have a self-signed certificate, you may get a 'site can't be reached' message in that case you need to use the IP Address instead of domain name.

      The **IBM IGI Administration Console** login page appears.

    ![ibmigiadminconsole](images/ibmigiadminconsole.png)

8.	Fill in the required information, such as user ID, password, and click **Login**. The **IBM IGI Administration Console** UI appears.

     ![enterpriseconnectors](images/enterpriseconnectors.png)

9.	Click **Enterprise Connectors**. The **Enterprise Connectors** page with the **Monitor** tab selected appears.

    ![enterpriseconnectormonitortab](images/enterpriseconnectormonitortab.png)

10.	Click **Manage** > **Profiles**.

     ![managetabprofile](images/managetabprofile.png)

11.	In the **Actions** list, click **Import**. 

     ![importmanageprofiles](images/importmanageprofiles.png) 

     The **Import** dialog box appears.

     ![importdialogbox](images/importdialogbox.png)

12.	Click **Choose File**. The **Open** dialog box appears. 

    ![opendialogboxone](images/opendialogboxone.png)

13.	Navigate to the `ThycoticAdapterProfile` file and click **Open**.

     ![importthycoticadapterprofile](images/importthycoticadapterprofile.png)

14.	Click **Upload file**. A message, '**Profile imported successfully. Close this window to proceed.**' appears. Click **Close**.

    ![importdialogboxwithmessageone](images/importdialogboxwithmessageone.png)

15. In the **Enterprise Connectors** page, Click **Manage** > **Profiles**.

     ![managetabprofiletwo](images/managetabprofiletwo.png)

16. In the **Actions** list, click **Import**. The **Import** dialog box appears.

    ![importdialogboxtwo](images/importdialogboxtwo.png)

17. Select **Attribute Mapping** option and click **Choose File**. The **Open** dialog box appears. 

    ![opendialogboxtwo](images/opendialogboxtwo.png)

18. Navigate to the `ThycoticAdapterProfileMapping.def` file, and click **Open**.

     ![importthycoticadapterprofilemapping](images/importthycoticadapterprofilemapping.png)

19. Click **Upload file**. A message, '**Attribute Mapping defining imported successfully. Close this window to proceed.**' appears.

     ![importdialogboxwithmessagethree](images/importdialogboxwithmessagethree.png)

20. Click **Close**.

The attribute mapping definition is imported successfully.

## Configure the connector

The next step is to configure the connector.

**To configure the Connector:**
1.	Click **Manage** > **Connectors**.

    ![managetabconnectors](images/managetabconnectors.png)

2.	In the **Actions** list, click **Add**. 

    ![addmanagerconnectors](images/addmanagerconnectors.png)

3.	In the **Connector Details** section, fill in the required information.

     ![connectordetails](images/connectordetails.png)

       a.	**Name** - Type the name of the connector.
  
       b.	**Profile Type** - Select `Identity Brokerage`.
  
       c.	**Profile** - Select `Thycotic Profile`.
  
       d.	**Entity** - Select `Account`.
  
       e.	**Trace ON** - Select the check box.
  
      f.	**Trace Level** - Select `INFO`.
  
      g.	**History ON** - Select the check box

4.	Click **Save**. More options are available for selection.

     ![additionalconnectordetails](images/additionalconnectordetails.png)

5.	Select the check boxes: **Enabled**, **Enable write-to channel**, and **Enable read-from channel**, and then	click **Save**.
6.	Click **Driver Configuration** tab and fill in the required details.

    ![driverconfigurationdetails](images/driverconfigurationdetails.png)

     a.	**Tivoli Directory Integration location** - Type the IP Address of the Dispatcher where the Dispatcher is installed.
  
     b.	**Secret Server URL** - Type the secret server URL
  
     c.	**Secret Server User ID** - Type the secret server user ID.
  
     d.	**Secret Server Password** - Type the password.

7.	Click **Save**.

    ![driverconfigurationdetailstwo](images/driverconfigurationdetailstwo.png)

8. In the **Driver** section, on the upper-right click **Save**.
9.	Click **Test Connection**. If the connection is successful, a message, '**The connection is successful.**' appears. Click **Ok**.

    ![informationdialogbox](images/informationdialogbox.png)

10. Click **Channel-Write To** tab > **Mapping**.

     ![channelwriteto](images/channelwriteto.png)

11.	Verify the presence of the mapping files.

     ![channelwritetomappedfiles](images/channelwritetomappedfiles.png)

12.	Click **Channel-Read From** tab > **Mapping**.

    ![channelreadfrom](images/channelreadfrom.png)

13.	Verify the presence of the mapping files.

    ![channelreadfrommappedfiles](images/channelreadfrommappedfiles.png)

14. Click   **Monitor** > **Connector Status**.

    ![monitorconnectorstatus](images/monitorconnectorstatus.png)

15.	Select the connector.

    ![selectfrequency](images/selectconnector.png)

16. In the **Schedule Details** >  **Frequency** list, select the value as `20 seconds` and then select **Effective Immedialtely**.

    ![selectfrequency](images/selectfrequency.png)

17.	In the **Actions** list, click Start. 

    ![startconnector](images/startconnector.png)

    The **Information** dialog box appears. Click **Ok**.

     ![connectorinformationdialogbox](images/connectorinformationdialogbox.png)

18.	Click **Monitor** > **Change Log Sync Status**.

     ![monitorchangelogsyncstatus](images/monitorchangelogsyncstatus.png)

19.	Select the connector.

20.	In the **Actions list**, click **Sync Now**. 

     ![syncnowmonitortab](images/syncnowmonitortab.png)

21.	To verify the synch, on the right-hand side click **Sync History**. The sync must be completed.

     ![synchisytorymonitortab](images/synchisytorymonitortab.png)

22.	In the menu on the left-hand side, click **Access Governance Core**. 

    ![accessgovernancecoremenu](images/accessgovernancecoremenu.png)

    The **Access Governance Core** UI appears.

     ![accessgovernancecoreui](images/accessgovernancecoreui.png)

23.  Click **Manage** > **Applications**.

     ![accessgovernancemanageapplications](images/accessgovernancemanageapplications.png)

24.	Select the account.

    ![manageapplicationsselectaccount](images/manageapplicationsselectaccount.png)

25.	On the right-hand side, click **Application Access**. All the information from Secret Server appears.

     ![manageapplicationaccess](images/manageapplicationaccess.png)

26.	Click **Manage** > **Account Configurations**.

     ![manageaccountconfigurations](images/manageaccountconfigurations.png)

27.	Select the account.

     ![manageaccountconfigurationsselectaccount](images/manageaccountconfigurationsselectaccount.png)

28.	On the right-hand side, click **Accounts**. All the users of secret server appear.
 
      ![manageaccountconfigurationaccounts](images/manageaccountconfigurationaccounts.png)

Now, the connector is configured successfully and data from Secret Server is synchronized. 

## Update user details in Secret Server through IBM IGI

The connector is configured, now you need to update the user details of Secret Server through IBM IGI. You need to:
* [Add user](#Add-user)
* [Configure accounts](#Configure-accounts)
* [Check user details and change password](#Check-user-details-and-change-password)


### Add user
In this step you need to add user.

**To add user detials in Secret Server through IBM IGI:**

1.	Go to **IBM IGI Administrator Console**.
2.	In the menu click **Access Governance Core**.

     ![accessgovernancemenutwo](images/accessgovernancemenutwo.png)

3.	Click **Manage** > **Users**.

    ![agcmanageusers](images/agcmanageusers.png)

4.	In the **Actions** list, click **Add**.

    ![agcmanageusersadd](images/agcmanageusersadd.png)

5.	In the **Details** section, fill in the required information.

    ![agcmanageusersdetails](images/agcmanageusersdetails.png)

       a.	In the **User Type** list, select `Employee`.
  
       b.	Select **OU Master**. In the **User Transfer** dialog box, select `ACME Corp`  and click **OK**.
  
       c.	In the **Master UID** text box, type the master user ID.

6.	Click **Save**. The **Password** dialog box appears.

     ![passworddialogbox](images/passworddialogbox.png)

7.	Fill in the required infomation, such as new password, confirm password, and then click **OK**.
     
    **Note**: The **Password Requirements** appear on the right-hand side.

    A message,‘**Operation successfully completed.**’appears. Click **Ok**. 

    ![informationdialogboxtwo](images/informationdialogboxtwo.png)

   The **User** is created in the **Users** section.
     ![agcmanageuserscreated](images/agcmanageuserscreated.png)

The next step is to configure account.

### Configure account

In this step, you need to configure account.

**To configure account:**
1.	Click **Account Configurations**.

     ![agcmanageaccountconfigurations](images/agcmanageaccountconfigurations.png)

2.	Select the account.
3.	On the right-hand side, click **Attribute-to-Permission Mapping**.

     ![agcattributetopermissionmappings](images/agcattributetopermissionmapping.png)

4.	In the **Actions** list, click **Discover Account attributes from Target**. 

     ![agcattributetopermissionmappingactionslist](images/agcattributetopermissionmappingactionslist.png)

     The **Discover Attributes from Target** dialog box appears.

     ![discoverattributesfromtarget](images/discoverattributesfromtarget.png)

5.	Select the **Attribute Name** check box in the header.

     ![discoverattributesfromtargetheader](images/discoverattributesfromtargetheader.png)

6.	Click **Import**. A message, ‘**Operation successfully completed.**’ appears. Click **Ok**.The files are imported.

     ![informationdialogboxtwo](images/informationdialogboxtwo.png)

7.	On the right-hand side, click **Target Attributes**.

     ![targetattributes](images/targetattributes.png)

8.	In the **Actions** list, click **Discover Account attributes from Target**. 

     ![discoveraccountattributesfromtargets](images/discoveraccountattributesfromtargets.png)

     The **Discover Attributes from Target** dialog box appears.

     ![discoverattributesfromtargettwo](images/discoverattributesfromtargettwo.png)

9.	Select the **Attribute Name** check box in the header.

     ![discoverattributesfromtargetheadertwo](images/discoverattributesfromtargetheadertwo.png)

10.	Click **Import**. A message, ‘**Operation successfully completed.**’ appears. Click **Ok**. The files are imported.

     ![informationdialogboxtwo](images/informationdialogboxtwo.png)

11.	On the left-hand side, select the **Users** tab.

     ![manageusersaccountselected](images/manageusersaccountselected.png)

12.	Select the user.
13.	On the right-hand side, click **Accounts**. The master account is listed.

     ![manageuseraccounts](images/manageuseraccounts.png)

14.	In the **Actions** list, click **Add**. 

     ![manageusersaccountactionslist](images/manageusersaccountactionslist.png)

     The **New Account** dialog box appears.

     ![newaccount](images/newaccount.png)

15. In the **Account Configuration** list, select the Secret Server account. The **Account Creation** tab is selected.

     ![newaccountexpanded](images/newaccountexpanded.png)

16.	Go to  **Account Creation** tab> **Details** section > **Account ID**.

17. In the **Account ID**  text box, type the account ID and click **Next**. The **Password** tab is selected.

     ![newaccountpassword](images/newaccountpassword.png)

     Fill in the required information, such as new password, confirm password, and then click **Next**. The **Target Attributes** tab is selcted.

     ![newaccounttargetattributes](images/newaccounttargetattributes.png)

18.	In the **User’s Display Name** text box, type the display name for the user.
19.	Click **Save**. The user is listed in the **Accounts** tab.

     ![userlistedinaccountid](images/userlistedinaccountid.png)

20.	Click the **Events** tab. 

     ![manageuserseventstab](images/manageuserseventstab.png)

21.	At the bottom of the **Events** tab, click on **OUT Events**. The event is listed. Wait till the **Status** and the **ERC Status** is displayed as **Success**.
22.	Go to **Secret Server** > **Admin** > **Users**. 

     ![secretserveradminuser](images/secretserveradminuser.png)

     The user is created in Secret Server. The user name and the display name for the user is displayed.
 
23.	Go to **IBM IGI Administrator console** and in the menu click **Access Governance Core**.
24.	Click **Manage** tab > **Users** > **Accounts**. 

     ![manageusersaccountstwo](images/manageusersaccountstwo.png)

25.	Select the account.
26.	In the **Action** list, click **Edit**. 

     ![manageusersaccountedit](images/manageusersaccountedit.png)

     The **Edit Account** dialog box appears.

     ![editaccount](images/editaccount.png)

     Fill in the required information, such as first name, last name, email, display name, and then click **Next**. The **Target Attributes** tab appears.
 
      ![editaccounttargetattributes](images/editaccounttargetattributes.png)

27.	In the **User’s Display Name** text box, change the display name for the user. Click **Save**.
28.	Click the **Events** tab. At the bottom of the **Events** section, click **OUT Event**. 

     ![manageuserseventstabtwo](images/manageuserseventstabtwo.png)

     The event is listed. Wait till the **Status** and the **ERC Status** is displayed as **Success**.

     ![manageuserseventstabthree](images/manageuserseventstabthree.png)

The next step is to check user details and change password.

### Check user details and change password

The last step is to check user details and change passsword.
**To verify the details and change the passowrd:**

1.	Go to the **Secret Server** > **Admin** > **Users**. 

2. Click the user that is added. The details of the user is updated.

     ![viewuser](images/viewuser.png)

3.	Go to **IBM IGI Administrator Console**.
4.	In the menu, click **Access Governance Core**.
5.	Click **Manage** tab > **Users** > **Accounts** tab. Select the account.
6.	In the Actions list, click **Change Pwd**. 

     ![manageusersacountchangepassword](images/manageusersacountchangepassword.png)

     The **Change Password** dialog box appears.

     ![changepassword](images/changepassword.png)

7. Fill in the required information, such as new password, confirm password, and then Click **OK**. A message, ‘**Operation successfully completed.**’ appears. Click **Ok**.

     ![informationdialogboxtwo](images/informationdialogboxtwo.png)

8.	Click the **Events** tab. 

9.	At the bottom of the **Events** tab, click on **OUT Event**. The event is listed. Wait till the Status and the **ERC Status** is displayed as **Success**.

The Secret Server is sucessfully integrated with IBM IGI Admin Console.