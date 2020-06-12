[title]: # (Requirements)
[tags]: # (Requirements)
[priority]: # (1)
# Pre-requisites

## System Requirements

|  Product |   |  Details |
|---|---|---|
|   ServiceNow |   |   |
|   | Version |  glide-newyork-06-26-2019__patch4-hotfix1-12-16-2019_12-17-2019_0856.zip or later |
|   |  Hardware |  https://docs.servicenow.com/bundle/orlando-servicenow-platform/page/product/mid-server/reference/r_MIDServerSystemRequirements.html |
|   | Additional Information  |   |
|   |   | To Discover Windows-based servers, the MID Server must be installed on Windows Server 2008-2019  |
|   |   | The Mid-Server Installer package is bundled with OpenJDK. It is still recommended that you install the latest JRE. The minimum JRE version supported is 1.8.0_161. It is noted that ServiceNow will discontinue support of 32-bit MID Servers in a future release.  |
|   |   | Requires a minimum of PowerShell version 3.0 and supports versions up to PowerShell 5.1  |
|   |   | The Mid-Server requires communication outbound to your ServiceNow instance over TCP 443. It is recommended to also allow ICMP echo requests.  |
|   |   | A ServiceNow User account that is designated for MID Server use and has the mid_server role - https://docs.servicenow.com/bundle/orlando-servicenow-platform/page/product/mid-server/task/t_SetupMIDServerRole.html  |
|   |   | Activate the External Credential Storage for Discovery and Orchestration - https://docs.servicenow.com/bundle/helsinki-it-operations-management/page/product/discovery/task/t_ActivateExtrnlCredStoragePlugIn.html  |
| Secret Server   |   |   |
|   | Version  | Thycotic Secret Server version 10.7.00059 or later.  |
|   | Hardware  | For further information about system requirements for Secret Server please visit: https://docs.thycotic.com/ss/10.8.0/secret-server-setup/system-requirements/index.md.  |
|   | Permissions  | A Secret Server Application Account that has “View” access to any credentials that are intended to be integrated for purposes of Mid-Server Discovery  |
|   |   |   |
