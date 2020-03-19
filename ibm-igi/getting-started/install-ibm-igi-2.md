[title]: # (Install IBM IGI)
[tags]: # (introduction)
[priority]: # (101)
# Install IBM IGI

This section provides the steps to install IBM IGI.

__To install IBM IGI:__

1. Type the login credentials. The __IBM Security Identity Governance and Intelligence setup wizard__ appears.
     >**Note:** The default value for login and password is `admin`.

     ![ibmigisetupwizardone](images/ibmigisetupwizardone.png)

1. Press __Enter__ to continue. The __Software License Agreement__ appears.

     ![softwarelicenceagreement](images/softwarelicenceagreement.png)
1. In the __Software License Agreement__, select the option __Proceed to acceptance__.

     ![agreeterms](images/agreeterms.png)
1. Select the option __I agree__ to suggest that you agree that you have had the opportunity to review the terms of both the IBM and non-IBM licenses presented and such terms govern this transaction.

     ![fipsmodeconfiguration](images/fipsmodeconfiguration.png)
1. Under __FIPS 140-2 Mode Configuration__, select the option __Next screen__.

     ![appliancepassword](images/appliancepassword.png)
1. Under __Appliance Password__, select the option __Change password__ .

     ![changeappliancepassword.](images/changeappliancepassword..png)
1. Under __Change Password__, fill in the required information, such as old password, new password, and confirm new password. The ‘__Password successfully changed.__’ message appears.

     ![appliancepasswordchangeconfirmation](images/appliancepasswordchangeconfirmation.png)

1. Under __Appliance Password__, select the option __Next screen__.

     ![hostconfiguration](images/hostconfiguration.png)
1. Under __Host Name Configuration__, select the option __Change the host name__.

     ![changehostname](images/changehostname.png)
1. Under __Change the Host Name__, enter the FQDN host name. (For example: igi.thycotic.ibm.com )

     ![hostconfiguartionupdated](images/hostconfiguartionupdated.png)
1. Under __Host Name Configuration__, select the option __Next screen__.

     ![managementinterfaceSettingone](images/managementinterfaceSettingone.png)
1. Under __Management Interface Settings__, select the option __Configure M.1__.

     ![selectipv4configmode](images/selectipv4configmode.png)
1. Under __Configure M.1__, select the option __Manual__.

     ![enteripv4values](images/enteripv4values.png)
1. Fill in the required information, such as type the IPV4 address, IPV4 subnet mask, IPV4 gateway, and then select __IPV6 configuration mode__ as __Automatic__.

      ![managementinterfacesettingstwo](images/managementinterfacesettingstwo.png)
1. In the __Management Interface Settings__, select the option as __Next screen__.

      ![dnsconfigurationone](images/dnsconfigurationone.png)
1. In __DNS Configuration__, select the option __Set DNS server 1__.

      ![setdnsserverone](images/setdnsserverone.png)
1. In __Set DNS server 1__, type the DNS server IP address. 

     ![dnsconfigurationtwo](images/dnsconfigurationtwo.png)
1. In __DNS Configuration__, select the option __Next screen__.

     ![timeconfiguration](images/timeconfiguration.png)
1. In __Time Configuration__, select the option __Next screen__.

     ![summary](images/summary.png)
1. In the __Summary__, select the option __Accept the configuration__.
1. After applying the policy changes, a message, ‘__Policy changes were successfully applied. Local Management Interface has been restarted.__’ appears.

     ![applyingpolicychanges](images/applyingpolicychanges.png)
1. The __IBM IGI__ appliance login page appears.

     ![ibmigiappliancelogin](images/ibmigiappliancelogin.png)

1. IBM IGI is successfully installed.
