[title]: # (Rotating the BluePrism API Account)
[tags]: # (api aaccount)
[priority]: # (300)
# Rotating the BluePrism API Account

This document is designed to provide a guide for rotating the password to the privileged account (Secret) that is used by BluePrism to access privileged accounts (Secrets) stored in Thycotic Secret Server on behalf of Digital Workers in the BluePrism platform.

The credential that is stored by BluePrism contains three “credential properties” which store the relevant information required for getting access to Secret Server. The properties are “manage_username”,”manage_password” and “server_url”. These details contain the username and password for an “application API” account that the integration uses to get access to Secret Server.

In order to rotate this credential, first Secret Server needs to rotate the password for the local API account that’s being used. Next, it then reaches out to BluePrism to modify the “manage_password” credential property stored against this credential utilizing the AutomateC application provide by BluePrism. This operation is performed remotely on the BluePrism server through the use of Powershell.
This guide assumes that the BluePrism integration is already set up and enabled against Secret Server. If documentation around this process is required, an alternative document should be sought.
