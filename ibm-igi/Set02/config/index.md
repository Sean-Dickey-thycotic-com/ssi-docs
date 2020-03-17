[title]: # (Index)
[tags]: # (introduction)
[priority]: # (100)
[display]: # (none)

# Secret Server: IBM IGI Integration Guide

This guide provides the steps to integrate Thycotic Secret Server (SS) with the IBM Security Identity Governance and Intelligence (IGI) tool.

## About IBM IGI 

IBM IGI allows organizations to provision, audit, and report on user access and activity through lifecycle, compliance, and analytics capabilities.

For more information, see https://www.ibm.com/in-en/marketplace/identity-governance-and-intelligence

## Why should IBM IGI be integrated with Thycotic Secret Server?

The  integration manages user accounts and supports data, such as groups, folders, and secrets on Secret Server solution. The integration adapter communicates with the remote server through REST APIs.

The Secret Server adapter supports the following features:
* Adding user accounts
* Changing user account passwords
* Modifying user account attribute
* Assigning and deleting users to or from groups, folders, and secrets
* Suspending and restoring user accounts
* Reconciling user accounts
* Reconciling support data such as groups, folders, and secrets

## Secret Server adapter limitations

* The user account delete operation is not supported by Secret Server and therefore this integration does not support user account deletion.
* The adapter does not support modify, suspend, restore, and password change for application accounts.

## Integrating IBM IGI with Secret Server
Secret Server is a web-based password vault used throughout the world to help organizations manage privileged accounts. This guide explains detailed steps to integrate IBM IGI with Secret Server. 

### Prerequisites
The following are the prerequisites for integrating IBM IGI with Secret Server:
* Ensure Secret Server version is v10.5 or above
* Ensure you have IGI administrator authority to perform the operations
* Ensure the hardware and software requirements mentioned in the following link are met:
https://www.ibm.com/support/knowledgecenter/en/SSGHJR_5.2.0/com.ibm.igi.doc/installing/cpt/c_hardware_reqs.html

> **Note**: For the purpose of this guide, the IBM IGI internal database was used. To use a different data and directory server, refer to the configuration documentation of IBM.


The following are the overall steps to integrate IBM IGI with Secret Server:
* [Step One: Configuring and setting up virtual appliance for IBM IGI](steps\steponeconfiguringva.md) 
* [Step Two: Installing security directory integrator 7.2](steps\steptwoinstallingsdi7.2.md) 
* [Step Three: Installing Tivoli dispatcher](steps\stepthreeinstalllingtivolidispatcher.md) 
* [Step Four: Configuring IBM IGI GUI and dispatcher folder to access admin console](steps\stepfouraccessadminconsole.md) 
* [Step Five: Integrating Secret Server with IBM IGI admin console](steps\stepfiveintegratingsecretserver.md) 



