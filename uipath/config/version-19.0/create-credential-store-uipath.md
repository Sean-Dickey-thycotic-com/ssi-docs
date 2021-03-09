[title]: # (Create a Credential Store in UiPath Orchestrator)
[tags]: # (credential store)
[priority]: # (302)
# Create a Credential Store in UiPath Orchestrator

1. Copy the SecretServer.SecureStore.dll file into the following directory: 

   `C:/program files(x86)/UiPath/Orchestrator/plugins`

   ![Copy](images/config1.png)

1. Open the web.config file by right-clicking the file and selecting __run as administrator__ under the following path:

   `C:/programfiles(x86)/UiPath/Orchestrator`

1. Modify the web.config file to reflect the Secret Server dll value:

   __`<add Key="Plugins.SecureStores" value=SecretServer.SecureStore.dll" />`__

   ![Web.config](images/config3.png)

   ![Web.config](images/config2.png)
1. Log in to your UiPath Orchestrator account.

   ![Log in](images/config4.png)
1. In the right-hand corner of the screen, click on your account icon
1. Click __Credential Stores__.

   ![Credential Stores](images/config5.png)
1. Click the __Add__ icon.

   ![Add](images/config6.png)
1. Select the __SecretServer__ option under the Type dropdown selection.
1. Click __Create__.

   ![Create](images/config7.png)

   >**Note:** You will need to re-visit the credential store steps, after setting up an onboarding rule in SKD Management and creating an onboarding key in Secret Server. [Setup a New Onboarding Rule in SDK Management](setup-onboarding-rule-sdk.md)