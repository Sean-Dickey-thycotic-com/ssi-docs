[title]: # (Configuring Secret Server for UiPath)
[tags]: # (uipath)
[priority]: # (204)
#  How to Configure Secret Server for UiPath

## In Secret Server:

1. Create a new Application Account under __Admin | Users__.

1. Setup a new onboarding rule in the SDK Client Management under __Admin | See All | Tools and Integrations__. 

   >**Note:** Keep track of the onboarding rule name and key In Orchestrator.

1. Add a new Credential Store under the Credential Stores menu under your profile.

   * __Secret Server URL__: The URL of your secret server instance.

   * __Rule Name__: The client onboarding rule name.

   * __Rule Key__: The optional key from the onboarding rule.

   * __Reset Key__: Random text used to revoke the Secret Server SDK and reinitalize it.

   * __Username Field Slug__: The slug name of the Secret Template field that Orchestrator will pull the username from when retrieving an Asset from Secret Server.

   * __Password Field Slug__: The slug name of the Secret Tempalte field that Orchestrator will pull the password from when retrieving an Asset from Secret Server.

   * __SDK Config Storage Path__: When initialized, the Secret Server SDK creates encrypted storage files. These by default are stored in the user's profile directory. If the orchestrator IIS App Pool is not set to Load User Profile, then that path is the Windows temp directory. If the IIS App Pool is set to Load User Profile, you can change this to the app pool identity's profile path. Or you create a custom path and grant permissions to the app pool identity.

1. Create an asset of type Credential and select the Secret Server Credential Store. For the External Name enter the Secret Id of an existing Secret you want to pull the username / password from.
   * When the asset is used in a robot process, it will pull the username and password from the Secret.

1. Create a robot and select the Secret Server Credential Store. Enter the username and use the Secret Id as the External Name.
   * Now when the robot logs in it will pull the password from the field on the corresponding Secret.

   >**Note:** The Application User linked to the client SDK rule must have permissions to the Secrets accessed by UI Path. You can assign it to a group and grant that group access to the required folders, or grant it explicit access to the Secrets.

   >**Note**: Ensure that the orchestrator machine trusts the TLS certificate used by Secret Server.