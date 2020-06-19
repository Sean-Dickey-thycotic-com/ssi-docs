[title]: # (SCIM Connector Settings)
[tags]: # (scim,connector)
[priority]: # (106)
# SCIM Connector Settings

## Settings Page

This page reviews the existing options that are under the __Settings__ option in the menu.

To access the below sections, go to the navigation menu on the left-hand of the SCIM Connector application and select Settings. On the Settings page there are tabs at the top that can be used to view the different option sections.

## Account Tab

This section lists the details of the currently logged-in account. You can modify the existing information in each text box by selecting the __Edit__ link to the right.

   ![tag]()

Complete the text boxes as follows:

   * __First name:__ The first name of the account.
   * __Last name:__ The last name for the account.
   * __Username:__ The user name that will be used to log in to the SCIM Connector application.
   * __Password:__ The password for the account that will be used to log in to the SCIM Connector application.

## Users Tab

This tab lists all the registered user accounts that have access to the SCIM Connector application, as well as listing the user accounts that can be approved or rejected for access. The __Users__ tab has two sections.

   ![tag]()

   * __Users Who Need Approval:__ Includes a list of users that have requested access (which have registered for the SCIM Connector). Access requests can be __Approved__ or __Rejected__. On approval, the user is added to the list of approved users and they can log in.

   * __Approved Users for SCIM:__ Allows for the deletion of an application user or allows another application user to modify the values for another user’s settings. The available text boxes for editing are:

      * __First name:__ The first name of the account.
      * __Last name:__ The last name for the account.
      * __Username:__ The user name that will be used to log in to the SCIM Connector application.
      * __Password:__ The password for the account that will be used to log in to the SCIM Connector application.

## Secret Server Tab

This tab is used to connect to your instance of SS.

To communicate with SS, the SCIM Connector application requires the connection information to your SS. The base URL should point to the location where SS is available by HTTPS, for instance `https://<ip
address>/SecretServer/`.

The Account Name is the name of the application account that was created in SS. The password is the password associated with the SS application account.

For details on configuring this section please see the [Making a Secret Server Connection](making-ss-conect.md) section.

## SCIM Endpoints Tab

This tab is used for connecting to your SCIM-integrated endpoints. For an endpoint to communicate with the SCIM Connector application, a valid endpoint must be configured.

For details on configuring this section please see the [Making a SCIM Endpoint Connection](making-scim-endpoint.md) section.
