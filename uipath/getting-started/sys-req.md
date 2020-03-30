[title]: # (Requirements)
[tags]: # (requirements)
[priority]: # (101)
# Integration Requirements

## Pre-requisites

* Thycotic Secret Server version 8.9 or later.

* UiPath Version 19.10 or later.

* Active Uipath account.

* Orchestrator-CredentialStorePlugins:

   * Visual Studio with .NET Framework 4.7.2

* Windows Server 2008 R2 SP1 or later.

* SQL Server 2008 R2 Standard or Enterprise Edition or later.

* For further information about system requirements for UiPath orchestrator please visit https://docs.uipath.com/orchestrator/docs/hardware-requirements-orchestrator.

* The integration uses the Secret Server SDK, which is documented in more detail here: https://github.com/thycotic/sdk-documentation.

* Ensure that the orchestrator machine trusts the TLS certificate used by Secret Server.

>**Note:** To use these credential store plugins for UI Path orchestrator, drop the corresponding dll into the plugins directory in the UI Path Orchestrator install directory and modify the web.config as specified here: https://github.com/UiPath/Orchestrator-CredentialStorePlugins.
