[title]: # (ConnectWise)
[tags]: # (introduction)
[priority]: # (1)
# ConnectWise Integration

The integration between Thycotic Secret Server and ConnectWise is created and maintained by ConnectWise. This document provides guidance and best practice for implementing the integration. It is based on the following publicly available documentation from the vendor and testing performed by Thycotic.

## Managing Customer Privileged Accounts

Integrating the Secret Server folder structure with ConnectWise company
information allows companies to quickly organize their privileged accounts based
on the customers they are managing in ConnectWise. This integration helps
eliminate the need to manually update the same data in two different systems.

## THE SECRET SERVER APPROACH TO PRIVILEGED ACCOUNT MANAGEMENT

Many environments with strict Information Security policies require methods to
control and monitor access to privileged accounts. Companies often apply
security policies such as physical access restrictions to hardware, network
firewalls, appropriate-use guidelines, and user account restrictions. In the
case of privileged accounts, access is more difficult to track and verify.
Implementing Secret Server enables organizations to strictly control and track
access to both customer and internal privileged accounts.

## SECRET SERVER CONNECTWISE INTEGRATION EXPLAINED

Secret Server has the ability to read the list of companies via the ConnectWise
API and populate Folders based on Companies and Status.

<!-- 
The int-template folder contains the template structure and template files for integration documents.

1. Make a copy of the template folder at the root of the integration repo.
1. Rename the folder to reflect the actual integration product name, e.g. okta-for-saml.md. Use lowercase and hyphens for the names.
1. Each folder requires an index.md file.
1. The metadata tag `` needs to be removed or changed to `[display]: # (all)` once real contents is created and ready for publication.
1. Each contents section needs an images folder if screen captures are part of the markdown files. Refer to the Okta for SAML folder to see an example on where/when the images folder is required. We cannot stage a template structure with images folders in place, empty folders cannot be committed into a repo.
1. This index file becomes the introduction/overview page for the integration.
1. Some topics are optional at this point and should only be filled in if information is readily available:

  * consider-architecture.md
  * consider-implementation.md
  * troubleshooting.md

1. The priority metadata tag determines the order of the TOC outline. For the files in the template that order is established. If a new file is added, adjust priority numbers accordingly to have the new .md file at the correct place in the TOC. 
-->
