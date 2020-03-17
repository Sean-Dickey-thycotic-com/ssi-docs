[title]: # (Configuring and Setting Up Virtual Appliance)
[tags]: # (introduction)
[priority]: # (101)
# Step One: Configuring and Setting Up Virtual Appliance for IBM IGI

To integrate IBM IGI with Secret Server, IBM IGI must be installed and configured using a Virtual Appliance. 

Following are the steps:
* Create a Virtual Machine (VM). A VM can be created using tools like VMWare or Hyper-V. For more information, see https://www.ibm.com/support/knowledgecenter/en/SSGHJR_5.2.3/com.ibm.igi.doc/installing/tsk/t_settingup_the_VM.html
*	Set up the Virtual Appliance. The following are the steps to set up a Virtual Appliance:
      * [Install firmware](#Install-firmware)
      * [Set up properties for VM](#Setup-properties-for-VM)
  * [Install IBM IGI](#Install-IBM-IGI)
  
  * [Set up IBM IGI](#Setup-IBM-IGI)
  
  * [Configure OpenID Connect Provider](#Configure-OpenID-Connect-Provider)
 
The detailed procedure for each step is explained below.

## Set up the Virtual Appliance. 

The following are the steps to set up a Virtual Appliance:

 * [Install firmware](#Install-firmware)
 * [Set up properties for VM](#Setup-properties-for-VM)

### Install firmware
After creating a VM, the firmware must be installed.

**To install the firmware on the VM:**
1. On the VM window, right-click the name of the Virtual Machine created and click **Power On**.

     ![vmpoweron](images/vmpoweron.png)

2. Right-click the name of the VM and click **Connect or View** > **Connect via Console**. 

     ![vmconnectviaconsole](images/vmconnectviaconsole.png)

    The **Windows Security** dialog box appears.

    ![vmwindowssecurity](images/vmwindowssecurity.png)

3. Type a password and click **OK**. The Console view appears.

     ![selectlanguage](images/selectlanguage.png)

4. Select the language to be used during the installation as `English` and press **Enter**.

     ![toproceed](images/toproceed.png)

5. To proceed, type `yes` and press **Enter**.

     ![reboottheappliance](images/reboottheappliance.png)

The firmware is successfully installed. After installation is completed, the process prompts to reboot the appliance. Before rebooting the appliance, some properties are to be set.

### Set up properties for VM
You need to set up the properties for hardware configuration.

**To set up properties for VM:**
1. On the VM window, right-click the name of the VM created and click **Properties**.

     ![vmproperties](images/vmproperties.png)

2. Click **Hardware Configuration** > **Virtual DVD drive**.

     ![hwconfiguration](images/hwconfiguration.png)

3.	In the **Media** area, select **No media** and click **OK**. The VM gets updated.
4.	Go to Virtual Appliance and press **Enter** to reboot.

     ![appliancelogin](images/appliancelogin.png)

The VM properties are set successfully. Now, IBM IGI is to be installed.

## Install IBM IGI
This section provides the steps to install IBM IGI.

**To install IBM IGI:**
1.	Type the login credentials. The **IBM Security Identity Governance and Intelligence setup wizard** appears.
     >**Note:** The default value for login and password is `admin`.

     ![ibmigisetupwizardone](images/ibmigisetupwizardone.png)

2.	Press **Enter** to continue. The **Software License Agreement** appears.

     ![softwarelicenceagreement](images/softwarelicenceagreement.png)

3.	In the **Software License Agreement**, select the option **Proceed to acceptance**.

     ![agreeterms](images/agreeterms.png)

4.	Select the option **I agree** to suggest that you agree that you have had the opportunity to review the terms of both the IBM and non-IBM licenses presented and such terms govern this transaction.

     ![fipsmodeconfiguration](images/fipsmodeconfiguration.png)

5.	Under **FIPS 140-2 Mode Configuration**, select the option **Next screen** . 

     ![appliancepassword](images/appliancepassword.png)

6.	Under **Appliance Password**, select the option **Change password** .

     ![changeappliancepassword.](images/changeappliancepassword..png)

7. Under **Change Password**, fill in the required information, such as old password, new password, and confirm new password. The ‘**Password successfully changed.**’ message appears.

     ![appliancepasswordchangeconfirmation](images/appliancepasswordchangeconfirmation.png)

8.	Under **Appliance Password**, select the option **Next screen**.

     ![hostconfiguration](images/hostconfiguration.png)

9.	Under **Host Name Configuration**, select the option **Change the host name**.

     ![changehostname](images/changehostname.png)

10.	Under **Change the Host Name**, enter the FQDN host name. (For example: igi.thycotic.ibm.com )

     ![hostconfiguartionupdated](images/hostconfiguartionupdated.png)

11.	Under **Host Name Configuration**, select the option **Next screen**.

     ![managementinterfaceSettingone](images/managementinterfaceSettingone.png)

12.	Under **Management Interface Settings**, select the option **Configure M.1**.

     ![selectipv4configmode](images/selectipv4configmode.png)

13.	Under **Configure M.1**, select the option **Manual**.

     ![enteripv4values](images/enteripv4values.png)

14.	Fill in the required information, such as type the IPV4 address, IPV4 subnet mask, IPV4 gateway, and then select **IPV6 configuration mode** as **Automatic**.
 
      ![managementinterfacesettingstwo](images/managementinterfacesettingstwo.png)

15. In the **Management Interface Settings**, select the option as **Next screen**.

      ![dnsconfigurationone](images/dnsconfigurationone.png)

16. In **DNS Configuration**, select the option **Set DNS server 1**.

      ![setdnsserverone](images/setdnsserverone.png)

17. In **Set DNS server 1**, type the DNS server IP address. 

     ![dnsconfigurationtwo](images/dnsconfigurationtwo.png)

18. In **DNS Configuration**, select the option **Next screen**.

     ![timeconfiguration](images/timeconfiguration.png)

19. In **Time Configuration**, select the option **Next screen**.

     ![summary](images/summary.png)

20. In **Summary**, select the option **Accept the configuration**. After applying the policy changes, a message, ‘**Policy changes were successfully applied. Local Management Interface has been restarted.**’ appears. 

     ![applyingpolicychanges](images/applyingpolicychanges.png)
 
      The **IBM IGI** appliance login page appears.

     ![ibmigiappliancelogin](images/ibmigiappliancelogin.png)

IBM IGI is successfully installed. Now, let us set up  IBM IGI.

## Set up IBM IGI
This section provides the steps to set up IBM IGI.

**To set up IBM IGI:**

1. In the **igi.thycotic.ibm.com** domain name, enter login and password details. 

2. Type the `IP address` along with the port number (For example: 10.60.25.21:9443) in the browser and press **Enter**.

     >**Note**: The default port number is 9443.

     ![accessibmigione](images/accessibmigione.png)

3.	Click **Advanced** and click **Proceed to `IP Address` (unsafe)**.

     ![accessibmigitwo](images/accessibmigitwo.png)

      The IBM IGI Login page appears.
 
      ![ibmigilogin](images/ibmigilogin.png)

4.	Fill in the required information, such as the user name, password, and click **Login**. The **IBM Security Identity Governance and Intelligence** page appears.
     >**Note:** The default value for user name is `admin`. The value of the password is what you have changed in the Console window.

     ![ibmigifirstpage](images/ibmigifirstpage.png)

5. Click **Setup** for setting up a primary node for the IBM Security Identity Governance and Intelligence cluster. The **IBM IGI setup wizard** appears.

     ![ibmigisetupwizard](images/ibmigisetupwizard.png)

6.	In the **Mode Selection** page, click **Next page**. The **Application Interfaces** page appears.

     ![ibmigisetupwizardapplicationinterface](images/ibmigisetupwizardapplicationinterface.png)

7.	In the **Application Interfaces** page, click the **New** ![newicon](images/newicon.png) icon. The **Add Address** dialog box appears.

8.	In the **Add Address** dialog box, fill in the required information.

    ![addaddress](images/addaddress.png)

    * **IPv4** - Select the required option.
    
    * **Interface FQDN** - Type the fully qualified domain name.
    
    * **Interface Gateway** - Type the interface gateway details.

    * **IPv4 Settings - Address** - Type the IP Address.
    
       >**Note**: Ensure the IP Address is not assigned to any other computer.
    
    * **IPv4 Settings - NetMask** - Type the netmask details.
9.	Click **Save**. A message “**The new application address is added successfully.**” appears and the IP Address is listed.

     ![applicationinterfaces](images/applicationinterfaces.png)

10.	Click **Next page**. The **Mail Server Configuration** page appears.

     ![mailserverconfiguration](images/mailserverconfiguration.png)

11.	Click the **Configure** ![configureicon](images/configureicon.png) icon. The **Mail Server Configuration Details** dialog box appears.

12.	In the **Mail Server Configuration Details** dialog box, fill in all the information.

     ![mailserverconfigurationdetails](images/mailserverconfigurationdetails.png)


13.	Click **Save Configuration**. A message, ‘**Mail server configuration added.**’ appears and the email configuration is listed. 

     ![mailserverconfigurationadded](images/mailserverconfigurationadded.png)

14.	Click **Next page**. The **Database Server Configuration** page appears.

      ![databaseserverqconfiguration](images/databaseserverqconfiguration.png)

15.	Click the **Configure** ![configureicon](images/configureicon.png) icon. The **Identity data store** details dialog box appears.
16.	In the **Connection** tab, fill in all the information.
    
     ![connectiontab](images/connectiontab.png)

 17.	Click **Save Configuration**. A message,'**Identity data store configuration created.** 'appears and the database configurations are displayed.   
  ![databaseserverconfigured](images/dbserverconfigured.png)
     

18.	Click **Next page**.
 
      ![completesetup](images/completesetup.png)

19. In the **Complete Setup** page, click **Complete Setup**. The progress bar of the setup appears.

     ![setupwizardprogressbar](images/setupwizardprogressbar.png)

     The **Complete Setup** page appears.

     ![lastpagecompletesetup](images/lastpagecompletesetup.png)

20. After the completion of the setup, click `here` in the sentence `Click here to go to the dashboard`. The **Session Ended** dialog box appears.

      ![sessionended](images/sessionended.png)
21. In the **Session Ended** dialog box, click the sentence `Click here to return to the local management interface`. The IBM IGI dashboard appears.

    >**Note**: If the IBM IGI dashboard does not appear, type the IP address along with the port number (For example: 10.60.25.21:9443) in the browser and press Enter. If required, replace the domain name with the IP Address. 

     ![ibmigidashboard](images/ibmigidashboard.png)

22. Close the session.


The IBM IGI setup is completed successfully. Now, the OpenID Connect Provider is to be configured.

## Configure OpenID Connect Provider
The next step is to configure the OpenID Connect Provider. 

**To configure OpenID Connect Provider:**

1. Type the `IP address` along with the port number (For example: 10.60.25.21:9443) in the browser and press **Enter**.

    >**Note**: The default port number is 9443.

     ![accessibmigione](images/accessibmigione.png)

2.  Click **Advanced** and click **Proceed to `IP Address` (unsafe)**.

     ![accessibmigitwo](images/accessibmigitwo.png)

     The **IBM IGI Login** page appears.
      ![ibmlogintwo](images/ibmlogintwo.png)
 
3.	Fill in the required information, such as the user name, password, and click **Log In**. The IBM IGI user interface appears. 
     >**Note:** The default value for user name and password is `admin`.

4.	Click **Configure** > **Manage Server Setting** > **OpenID Connect Provider Configuration**. The **Connect Provider Configuration** page appears.

     ![openidconnectprovider](images/openidconnectprovider.png)

5.	Click **Disable**. 

     ![openidconnectproviderstatus](images/openidconnectproviderstatus.png)

     A message, '**Are you sure you want to disable OpenID Connect Authentication configuration?**' appears.

     ![openidconnectprovidermessage](images/openidconnectprovidermessage.png)

6.	Click **Yes**. The status of the configuration appears.

     ![openidconnectprovidersystemnotification](images/openidconnectprovidersystemnotification.png)

    > **Note**: In the IBM IGI UI, the notifications are listed in the **Notifications** section.

     ![restartibmigiserver](images/restartibmigiserver.png)

7. In the **Server Control** section, select the server and click **Restart**.

     ![restartibmigilocalmgmtinterface](images/restartibmigilocalmgmtinterface.png)

8. Go to the **IBM IGI Virtual Appliance**.

     ![Virtualappliancereboot](images/Virtualappliancereboot.png)
9. In the Virtual Appliance, type `reboot` and press **Enter**.

10.	To confirm, type `YES` and press **Enter**. The **IBM IGI login** dialog box appears.

     ![ibmigilogin](images/ibmigilogin.png)    

11. Fill in the required information, such as the user name, password, and click **Log In**. The IBM IGI user interface appears. 

     ![ibmigiuserinterface](images/ibmigiuserinterface.png)



The Virtual Appliance for IBM IGI is configured and setup. Now, the next step is to install [Security Directory Integrator 7.2](\steps\steptwoinstallingsdi7.2.md).
