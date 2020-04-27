[title]: # (Requirements)
[tags]: # (requirements)
[priority]: # (101)
# Integration Requirements

## System Requirements

| Product  |   |  Details |
| ----- | ----- | ----- |
| __UiPath__|  |  |
|  | Version | UiPath Version 19.10 or later. |
| | Software | Orchestrator-CredentialStorePlugins: Visual Studio with .NET Framework 4.7.2|
|  | Hardware | For further information about system requirements for UiPath orchestrator please visit: https://docs.uipath.com/orchestrator/docs/hardware-requirements-orchestrator.|
| __Secret Server__ |  |  |
| | Version | Thycotic Secret Server version 10.4 or later. |
|  | Hardware | For further information about system requirements for Secret Server please visit: https://docs.thycotic.com/ss/10.8.0/secret-server-setup/system-requirements/index.md. |
| | | |

>**Note:** The following steps listed for the integration between Secret Server and UiPath are only applicable to UiPath Orchestrator On-Premise.

* The integration uses the Secret Server SDK, which is documented in more detail here: https://github.com/thycotic/sdk-documentation.

* Ensure that the orchestrator machine trusts the TLS certificate used by Secret Server and can reach the server that Secret Server is installed on to.

>**Note:** To use these credential store plugins for UI Path orchestrator, drop the corresponding dll in github into the plugins directory in the UI Path Orchestrator install directory and modify the web.config as specified here: https://github.com/UiPath/Orchestrator-CredentialStorePlugins.
