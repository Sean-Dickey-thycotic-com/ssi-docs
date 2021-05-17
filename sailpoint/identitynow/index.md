[title]: # (SailPoint IdentityNow)
[tags]: # (introduction)
[priority]: # (2)
# SailPoint IdentityNow

## What is IdentityNow?

IdentityNow by Sailpoint is a cloud based Identity and Access Management tool designed to simplify access changes during HR events such as onboarding, job function changes, and offboarding.  IdentityNow centralizes access management decisions for business systems into a single console with unified workflows. Thycotic Secret Server is one of the tools for which IdentityNow can manage access granting roles to users based on their position inside the business which can come with access to specific privileged secrets.  When a user transitions business roles the secrets to which they will have access can also be modified without further effort on the part of the administrator.  In addition if an employee or contractor leaves the organization their access to secrets can be removed ensuring that critical business assets remain protected.

## Why Use Secret Server with IdentityNow?

IdentityNow customers still require Thycotic’s Secret Server for privileged account management because although IdentityNow excels at managing individual user access to systems you would not want to use it to manage shared resources such as service accounts.  Additionally Secret Server offers more fully featured tools specific to privileged account management with audit, password rotation, dependency management, and others.  By using both products in combination clients can achieve the automation benefits for provisioning and managing user accounts and access through IdentityNow along with the security advantages of Privileged Access Management through Secret Server.

## How do Secret Server and IdentityNow communicate?

IdentityNow and Secret Server are both capable of using the System for Cross-domain Identity Management (SCIM) to send messages about triggering events.  SCIM is a standard data exchange format used in managing identity between cloud enabled systems.  Thycotic provides a SCIM connector which can be installed on any server in the client’s environment and will ingest messages from IdentityNow or other SCIM supporting IDAM systems and convert them into REST calls to the Secret Server API.  When a user is provisioned or modified inside of IdentityNow it will trigger a message to the Thycotic SCIM connector, the connector will parse the message and then make the appropriate changes inside of Secret Server
