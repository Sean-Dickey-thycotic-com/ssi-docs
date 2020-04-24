[title]: # (Requirements)
[tags]: # (requirements)
[priority]: # (101)
# Integration Requirements

## System Requirements

|   |   |   |
| ----- | ----- | ----- |
| __UiPath__|  |  |
|  Version |  | UiPath Version 19.10 or later. |
| Software |  | Orchestrator-CredentialStorePlugins: Visual Studio with .NET Framework 4.7.2|
| System requirements | | For further information about system requirements for UiPath orchestrator please visit: https://docs.uipath.com/orchestrator/docs/hardware-requirements-orchestrator.|
| __Secret Server__ |  |  |
| System requirements |  | For further information about system requirements for Secret Server please visit: https://thycotic.force.com/support/s/article/System-Requirements-for-Secret-Server. |
| | | |

* The integration uses the Secret Server SDK, which is documented in more detail here: https://github.com/thycotic/sdk-documentation.

* Ensure that the orchestrator machine trusts the TLS certificate used by Secret Server and can reach the server that Secret Server is installed on to.

>**Note:** To use these credential store plugins for UI Path orchestrator, drop the corresponding dll in github into the plugins directory in the UI Path Orchestrator install directory and modify the web.config as specified here: https://github.com/UiPath/Orchestrator-CredentialStorePlugins.
