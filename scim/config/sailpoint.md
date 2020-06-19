[title]: # (Configuring a SailPoint IdentityIQ Endpoint)
[tags]: # (sailpoint)
[priority]: # (104)
# Configuring a SailPoint IdentityIQ Endpoint

## SailPoint IdentityIQ

This section reviews the SailPoint IdentityIQ pre-configuration for use with the SCIM Connector, as well as an use examples and known usability issues.

## Configuring a SailPoint IdentityIQ Endpoint 

The steps in this section are required to configure SailPoint’s IdentityIQ platform for use as a SCIM Endpoint for the Thycotic SCIM Connector application. These steps are taken within SailPoint IdentityIQ, in addition to the steps from the “Making a SCIM Endpoint” section.

1. Navigate to SailPoint IdentityIQ.

   ![tag](images/)
1. Click the Settings menu item and select the Plugins option:

   ![tag](images/)
1. Add the following plugins:

   * __Identity+ Verification__
   * __SCIM PAM Bridge__

1. Select the Application in the top menu and select Application
Definition:

   ![tag](images/)
1. Click the __Add New Application__ button.

   ![tag](images/)
1. Enter the following information:

   * __Name:__ Enter the name for the application.
   
   * __Owner:__ Enter the user account used to connect to the SCIM Connector
application.

   * __Application Type:__ Select __Privileged Account Management__ from the
drop-down menu.

   * Check the box for the Authoritative application option
1. Click __Save__ the settings. This takes you back to the __Application
Definitions__ page.

1. Select the __Configuration__ tab:

   ![tag](images/)
1. Type the following information:
   * __Base URL:__ This should be the URL for the installed SCIM Connector application with “/v2” appended to the end of the URL.
   * __Authentication Type:__ Select the __API Token__ option.
   * __API Token:__ Copy and paste the API token that was generated in the SCIM Connector application when creating the SCIM endpoint (using the Non-expiring token option).
   * __Permissions:__ Click the __(+)__ button to the right and add View
permissions.

   >**Note:** We recommend you remember these values because you will need them again in a later step.

1. Once the above settings are set, click the __Test Connection__ button to see if the configuration works.

1. Click the __Schema__ sub-tab:

   ![tag](images/)
1. Click the __Object Type: account__ drop-down section.

   ![tag](images/)
1. Make sure the Identity Attribute is set to id.

   ![tag](images/)

1. n the __Attributes__ section of the page, click the __Add New Schema Attribute__ button. A new attribute row appears.

1. Add the following attribute row entries:

   ![tag](images/)

1. Go the __Object Type: container__ section and add the following four
attribute row entries:

   ![tag](images/)

1. Using the same method, go to the __Object Type: group__ section and add the following attribute rows:

    ![tag](images/)

1. Click the __Save__ button at the bottom of the page.
1. Return to the __Application Definition__ page.
1. Click the __Unstructured Targets__ tab:

   ![tag](images/)

1. Click the __Add New Unstructured Data Source__ button. The Unstructured Target Configuration page appears:

   ![tag](images/)

1. In the Unstructured Target Configuration dialog that opens, use the
following settings:

   __Name:__ Enter the name of the application that was used earlier.
   __Description:__ Enter a short description.
   __Correlation Rule:__ Select the __PAM Access Mapping Correlation Rule__ value.
   __Target Source Types:__ Select the __Privileged Account Management Collector__ value.
   __Base URL:__ Enter the same __Base URL__ value used earlier.
   __Authentication Type:__ Select the __API Token__ value.
   __API Token:__ Enter the same token that was used earlier.

1. Then click the __Save__ button.
1. Click on the Correlation tab.

   ![tag](images/)

1. Add a new correlation and follow the wizard dialog that pops-up. Ensure the `“email.work.primary.value”` is correlated to the “email” value.

   >**Note:** This correlation value must be set for the integration to correctly match user values.

1. Navigate to the __Identity IQ Configuration__ dialog (under the Global Settings).
1. Select the __Privileged Account Management__ tab.

   ![tag](images/)

1. Set the following options:
   * __The Application used for Privileged Account Management:__ Set the
application that was created earlier.
   * __Enable Privileged Account Management provisioning:__ Enable the check box.
   * __The workflow used to provision identities:__ PAM Identity Provisioning.
1. Click __Save__.
1. In the global navigation at the top of the page, select __Setup | Tasks__.
1. Add the following tasks:

   * __Account Group Aggregation:__ Select the application that was created
earlier.
   * __Account Aggregation:__ Select the application that was created
earlier.
   * __Target Aggregation:__ Select the Target source that was created.

1. After the tasks are added, right click each task and select __Run in Background__ to execute them in the background. The basic configuration is now complete.

## SailPoint Documentation

   * [General SailPoint IdentityIQ Documentation](https://community.sailpoint.com/community/identityiq/product-downloads)
   * [SailPoint SCIM Verification Plugin User Guide](https://community.sailpoint.com/docs/DOC-10479)
   * [Privileged Account Management Deployment Guide](https://community.sailpoint.com/docs/DOC-12926)
   * [Privileged Account Management in IdentityIQ](https://community.sailpoint.com/docs/DOC-9014)
