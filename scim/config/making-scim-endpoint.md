[title]: # (Making a SCIM Endpoint Connection)
[tags]: # (scim,endpoint)
[priority]: # (102)
# Making a SCIM Endpoint Connection

## SCIM Endpoints

__Overview__

The SCIM Connector application can connect to multiple SCIM endpoints at a time. Each SCIM endpoint has a defined set of required fields within the SCIM Connector but may also require additional steps from the third-party vendor endpoint.

Below are the basic steps for entering the values for the SCIM endpoint, as well as steps for specific third-party vendors:

1. n the SCIM Connector application, click the __(+)__ button in the top right of the page and select __Add Integration__.
1. Alternatively, users can select the __Settings__ menu on the left, and navigate to the __SCIM Endpoint__ tab at the top of the page.
1. Type in these fields:

   * __Name text box:__ The friendly name you want to give to the endpoint connection.
   * __Username text box:__ The user account that should be used to connect to the endpoint.
   * __Password text box:__ The password for the user account that is used to connect.
   * __Base URL text box:__ The URL for where the calling application resides, so a connection can be established.
   * __Authentication list box:__ There are two authentication methods that are currently supported by the Thycotic SCIM Connector. They are:
   * __Non-expiring token:__ This enables the Token field below, allowing e-token generation and storing the SCIM Connector applications. If the non-expiring token is regenerated or deleted from the SCIM Connector, subsequent calls using the non-expiring token will fail, resulting in an unauthorized request response.
   * __OAuth2:__ This option disables the Token field below and only allows for the OAuth2 standard to be used for authentication calls with the SCIM Connector application.
   * __Token view box:__ This option is enabled when the “Non-expiring token” is the authentication type. Clicking the first button to the immediate right generates the token and fills its value in the Token field. Clicking the second button to the right copies that token to the clipboard.
1. After all the fields have been entered, click __Save__ to validate and save the connection.

   >**Note:** In addition to making a connection to the SCIM Endpoint through the SCIM Connector application, users may need to make configuration adjustments within the target endpoint system.
