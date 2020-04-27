[title]: # (Royal TS)
[tags]: # (introduction)
[priority]: # (1)
# Introduction

The integration between Thycotic Secret Server and Royal TS is created and maintained by Royal TS. This document provides guidance and best practice for implementing the integration. It is based on the following publicly available documentation from the vendor and testing performed by Thycotic. Integrations are supported to the extent of the third-party product procedures documented for this integration. Please contact the third-party for any customized setup of the integrated product.

### Thycotic 

Thycotic IT security and password management solutions empower companies to remove the complexities of proper access control and management of privileged accounts. An Inc. 5000 company, Thycotic is trusted by more than 3,000 organizations worldwide—including Fortune 500 members, enterprises, government agencies, technology firms, universities, non-profits and managed service providers. To learn more, please visit [thycotic.com](http://www.thycotic.com/).

### Secret Server

Thycotic Secret Server (SS) is an on-premises Web-based password vault used throughout the world to help organizations properly manage privileged account passwords. SS allows users to control access and automate password changes for a variety of enterprise resources, such as servers, databases, network devices, and applications. SS features auditing throughout the application and role-based access control (RBAC) on all of its information and features. Organizations can easily deploy SS to ensure security, reduce labor costs, adopt password best practices, and satisfy audit requirements.

### Royal TS

Royal TS (Terminal Services), called RTS in this document, provides powerful, easy and secure access to remote systems for server admins, system engineers, developers and others who need to access remote systems using different protocols. RTS supports RDP, VNC, SSH, HTTP/S, and more. It is available for Windows, OS X, iOS and Android, and RTS documents open on all those platforms. See [http://www.royalts.com](http://www.royalts.com/) or more information.

### Royal TS and Secret Server Integration

SS randomizes and stores passwords for accounts on target systems on a regular recurring basis. Because these passwords are stored and managed in a vault, they can be retrieved via a SOAP or REST Web service. RTS integrates with SS via a PowerShell script, provided by RTS. Specifically, SS integrates with the RTS dynamic folder feature.

### Connection Management

With RTS, you can organize and manage all your connections to your remote systems. The following connection types are currently available and supported:

- External Application
- File Transfer
- Hyper-V Management
- Performance View
- PowerShell Connection
- Remote Desktop
- TeamViewer
- Terminal
- Terminal Services Management
- VMware
- VNC
- Web Page
- Windows Events View
- Windows Processes
- Windows Services

With RTS, you can check your event logs, restart services, or manage Hyper-V and VMware virtual machines right from your mobile device without connecting to remote desktops.
