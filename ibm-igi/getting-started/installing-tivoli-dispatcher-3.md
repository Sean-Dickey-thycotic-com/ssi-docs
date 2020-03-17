[title]: # (Installing Tivoli Dispatcher)
[tags]: # (introduction)
[priority]: # (106)
# Step Three: Installing Tivoli Dispatcher

You must install the Tivoli Dispatcher using the __IBM Security Identity Adapter__   wizard. The Tivoli Dispatcher is a Security Directory Integrator component that enables the IGI to communicate with IBM Security Directory Integrator.

__To install Tivoli Dispatcher:__

1. Go to the __Thycotic Shared Folder__ > __IGI__ > __Thycotic Adapter__ > __SIA_RMI_7139_SDI_7X_ML__.
1. In the __Widnows Search__ box type `cmd`. The results are auto-populated. Right-click __Command Prompt__ and click __Run as administrator__.
1. In the __User Account Control__ dialog box, click __Yes__.

   ![administratorcommandprompt](images/administratorcommandprompt.png)
1. In the __Command Prompt__ type the following:
`cd <path where the DispatcherInstall is located>`
and press __Enter__.
1. In the __Command Prompt__ then type the following:
`Java -jar DispatcherInstall.jar`  
and press __Enter__. The __IBM Security Identity Adapter__ wizard appears.

   ![ibmsecurityidentityadapter](images/ibmsecurityidentityadapter.png)
1. Click __OK__. The __ITDI Based Dispatcher__ panel appears.

   ![itdibaseddispathcher](images/itdibaseddispathcher.png)
1. Click __Next__. The __Choose ITDI Home Directory__ panel appears.

   ![chooseitdihomedirectory](images/chooseitdihomedirectory.png)
1. Click __Choose__ to select Security Directory Integrator path and click __Next__. The __Choose a Solution Directory__ panel appears.

   ![chooseasolutiondirectory](images/chooseasolutiondirectory.png)
1. Add `\timsol` to the `ITDI Home Directory` and click __Next__. The __Dispatcher Instance Name__ panel appears.

   >**Note:** Timsol is the folder where all the Tivoli directory integrator based dispatcher file is placed.

   ![dispatcherinstancename](images/dispatcherinstancename.png)
1. Click __Next__. The __Port Number__ panel appears.

   ![portnumber](images/portnumber.png)
1. Click __Next__. The __Enable JVM Security__ panel appears.

   ![enablejvmsecurity](images/enablejvmsecurity.png)
1. Type username, password, re-type  password and click __Next__. The __Enable SSL__ panel appears.

   ![enablessl](images/enablessl.png)
1. Click __Next__. The __Installing Dispatcher__ panel appears.

   ![installingdispatcher](images/installingdispatcher.png)
1. Click __Next__. The __Pre-Installation Summary__ panel appears.

   ![preinstallationsummary](images/preinstallationsummary.png)
1. Click __Install__.

     ![installcomplete](images/installcomplete.png)
1. In the __Install Complete__ panel, click __Done__. The Security Directory Integrator is installed.
1. To verify the installation, go to `C:\Program Files\IBM\TDI\V7.2` and verify if the `timsol` folder is created.
1. In the __Search__ box type `services`. The results are auto-populated.
1. Click `Services`. Verify if the __IBM Security Directory Integrator (ISIM Adapters)__ service is running.
1. The Tivoli Dispatcher is successfully installed.

The next step is to [configure IBM IGI and Dispatcher to access the Admin Console](../config/integrate-ss-ibm-igi-admin-console-5.md) 