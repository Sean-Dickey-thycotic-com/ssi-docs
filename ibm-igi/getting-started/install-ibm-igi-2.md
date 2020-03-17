[title]: # (Configuring and Setting Up Virtual Appliance)
[tags]: # (introduction)
[priority]: # (101)
# Install IBM IGI

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