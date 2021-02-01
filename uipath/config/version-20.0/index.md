[title]: # (Version 20.0)
[tags]: # (introduction)
[priority]: # (1)
# UiPath Orchestrator Configuration (Version 20.0)

* [Prepare Orchestrator For Integration](prep-orch.md)
* [Configuration Steps for Secret Server](config-ss.md)
* [Setup a New Onboarding Rule in SDK Management](setup-onboarding.md)
* [Create An Credential Store in UiPath Orchestrator](cred-store.md)
* [Create An Asset](create-assest.md)
* [Create a Robot in UiPath Orchestrator](create-robot.md)
* [Create a Process and Verifying Integration](create-process.md)
* [Best Practices](best-prac.md)

This document is intended to provide instructions for configuring the integration between Secret Server and UiPath orchestrator for secure credential retrieval.

## Configuration

Before configuring UiPath Orchestrator to integrate with Secret Server you will need to make sure you have met all the system requirements found below

>**Note**: The following steps incorporate the use of a credential store and only apply to UiPath Orchestrator On-Premise.

## System Requirements

| Product  |   |  Details |
| ----- | ----- | ----- |
| __UiPath__|  |  |
|  | Version | UiPath Version 20.10 or later. |
| | Software | UiPath Orchestrator, Studio, and Robot. We recommend reviewing Prerequisites required for Orchestrator installation here. We suggest leveraging UiPath’s PowerShell script for installing many of the IIS pre-requisites. |
|  | Hardware | For further information about system requirements for UiPath Orchestrator please visit - https://docs.uipath.com/installation-and-upgrade/docs/orchestrator-hardware-requirements.|
| __Secret Server__ |  |  |
| | Version | Thycotic Secret Server version 10.4 or later. |
|  | Hardware | For further information about system requirements for Secret Server please visit: https://docs.thycotic.com/ss/10.9.0/secret-server-setup/system-requirements/index.md. |
| | | |
