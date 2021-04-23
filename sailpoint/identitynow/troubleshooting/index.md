[title]: # (Troubleshooting)
[tags]: # (troubleshooting)
[priority]: # (500)
# Troubleshooting

It is possible that after following the above steps you may continue to see issues.  These issues will generally fall into one of three categories.  Either connection issues, credential issues, or issues in configuration.

## Connection Issues

The connection between Secret Server and IdentityNow is mediated through the SCIM connector application.  For load purposes, we recommend that the SCIM connector not be installed on the same machine as Secret Server and so this can create connectivity issues based on firewall rules.  The machine on which the SCIM connector is installed will require access to the public internet (IdentityNow is a cloud service) and also will need to be able to communicate to the Secret Server installation.  This should be confirmed during the configuration of the secret server endpoint in the SCIM connector but if that step fails or if connections that were previously working stop the most likely cause is a break in that communication stream.
To test these issues log onto the machine where the SCIM connector is installed and open a browser window.

First, load up your IdentityNow instance and confirm that you can log in.  If this works then load your Secret Server instance and perform the same test.

If either of these pages fails to load then there is a communication error and you will need to work with your network team to restore access it is also possible that the consoles of both applications (Secret Server and IdentityNow) will load but that message flow will still be broken.  In that case please log into your Secret Server instance and confirm that Webservices are enabled.  You can find instructions for doing so here : https://docs.thycotic.com/ss/10.8.0/webservices/enabling-webservices , SCIM relies on the Secret Server webservices to communicate and so cannot work without them enabled.

## Credential Issues

If the connection issue troubleshooting steps do not help then the next issue to investigate would be that the credentials used to access either Secret Server or IdentityNow are correct and have not changed.  

In your Secret Server instance please confirm that the user you created is active and assigned to roles that have permissions to create folders, create and edit secrets in folders, and view the secrets.

Although the individual users might not have access to all folders the credential being used by the SCIM account will need those permissions.  If you are uncertain about the specific permissions you wish to grant it might be a reasonable step to add the user to the “Admin” role temporarily as a test.  If that resolves your issues then it seems likely that invalid permissions in SS were at the root and you can slowly add permissions to the user until everything is working as needed.  Similarly, in IdentityNow make sure that the user whom you are using for that side of the connection has full control over all of the containers being synced between the two systems.

## Configuration Issues

If you have confirmed both the connectivity between all the systems, the user credentials, and permissions but still do not see changes in IdentityNow being reflected in Secret Server.  Please review the configuration under the Sailpoint endpoint you have created in the SCIM connector and make sure that there is a mapping for the type of data you are attempting to have flow.  Because the SCIM connector supports multiple products the name of the permission in the mapping is a free text field so please ensure that it matches correctly to the name of the role in IdentityNow.  Also please make sure that you have configured mappings both for ContainerPermissions and PiviledgedData permissions.

If none of the above steps resolve your issues please review the known issues list at https://docs.thycotic.com/scim/2.5.0/config/known-issues.md or contact Thycotic Support for additional assistance 
