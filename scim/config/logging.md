[title]: # (Logging)
[tags]: # (logging)
[priority]: # (107)
# Logging

There are two places where users can access any logging or messaging within the SCIM Connector application:

## Messaging

In the SCIM Connector application, navigate to the menu on the left and click the __Messages__ menu item. This takes users to a list of any recent messages or logging that has been sent to the SCIM Connector application. The Messaging logs are archived daily on the system, but older logs can be viewed and downloaded from the audit logs (see below).

   ![tag]()

   >**Note:** Once these logs are deleted from the system they cannot be recovered.

Each entry on the Messages list has these parameters:
   * __Timestamp:__ The time that the action call came into the SCIM Connector application.
   * __User Action:__ What type of action was made, such as Post, PATCH,  Get, or Delete.
   * __Request URL:__ The URL path to the application that was making the request.
   * __Response Status:__ The response code, which is the resulting status for the call that was made, such as Bad Request.

## Audit Logs

The Audit logs are the same as the messaging logs; however, they are viewed in a different format. Since the messaging logs are archived each day (by default), once they are archived, they are not directly available inside the SCIM Connector application, but they are still logged and are accessible on the machine that the application is installed on.

Once they are archived, the logs are stored in JSON format. The values listed in the JSON file are the same as the ones listed in the above section.

The audit Logs can typically be accessed from the following location on the machine:

`<Drive>:\inetpub\wwwroot\SCIMConnector\Log`

```
Example Log:

[

{

"RequestURI": "http://localhost:54523/SSEndpoint"",

"Action": "Get",

"User": "Sailpoint_Admin",

"DateTime": "2019-03-09T04:41:26.2138238-05:00",

"ResponseStatus": 200

},
{

"RequestURI": "http://10.0.0.226:80/SSI/appuser"",

"Action": "Get",

"User": " Sailpoint_Admin ",

"DateTime": "2019-03-09T04:52:10.4888392-05:00",

"ResponseStatus": 200

},

{

"RequestURI": "http://10.0.0.226:80/SSI/Users"",

"Action": "Get",

"User": " Sailpoint_Admin ",

"DateTime": "2019-03-09T04:52:10.8459354-05:00",

"ResponseStatus": 200

},

]

```
## SCIM Connector System Files

This section will cover any other topics that might be relevant.

__Log files__ 

   * Default log location is `<application root directory>/Log directory`
   * Default naming convention for log files is `<YEAR><MONTH><DAY><HOUR>`. For example:
`2019030904.log`.

__Encrypted Configuration File__ 

   * File Name: `Configurations.enc`
   * Default location: Application root directory

__Web.config file__ 

The web.config file contains information regarding endpoints and application configuration options:

``` 
<appSettings>
    <add key="CONFIG_FILE_PATH" value="" />
    <add key="CONFIG_FILE_NAME" value="Configurations.enc" />
    <add key="CERT_NAME" value="CN=<Machine Name>" />
    <add key="LOG_PATH" value=" <Application Root File Path> \\Log" />
    <add key="NOTIFICATION_PATH" value="" />
    <add key="SCIM_BASE_URL" value="http:// <SCIM Server domain name or IP address>/SSI" />
    <add key="SS_BASE_URL" value="https:// <Secret Server domain name or IP address>/SecretServer" />
    <add key="SS_TOKEN_ENDPOINT" value="/oauth2/token" />
    <add key="SS_Domain" value="local" />
    <add key="SS_GrantType" value="password" />
    <add key="SS_UsersFilterUrl" value="/api/v1/users?skip=0\&amp;take=999999999" />
    <add key="SS_UsersByIDUrl" value="/api/v1/users/" \>
    <add key="SS_UsersByIDGroupsUrl" value="/api/v1/users/{0}/groups?skip=0\&amp;take=999999999" />
    <add key="SS_GroupsFilterUrl" value="/api/v1/groups?skip=0\&amp;take=999999999"/>
    <add key="SS_GroupsByIDUrl" value="/api/v1/groups/" />
    <add key="SS_GroupsByIDUsersUrl" value="/api/v1/groups/{0}/users?skip=0\&amp;take=999999999" />
    <add key="SS_CreateUpdateUsersUrl" value="/api/v1/Users/" />
    <add key="SS_CreateUpdateGroupsUrl" value="/api/v1/Groups/" />
    <add key="SS_CreateUserInGroupsUrl" value="/api/v1/Groups/{0}/users/" />
    <add key="SS_DeleteUserFromGroupUrl" value="/api/v1/Groups/{0}/users/{1}" />
    <add key="SS_ReportUserAcivityUrl" value="/api/v1/reports/execute" />
    <add key="SS_FoldersFilterUrl" value="/api/v1/folders?skip=0\&amp;take=999999999" />
    <add key="SS_FolderPermissionsByIDUrl" value="/api/v1/folder-permissions?filter.folderid=" />
    <add key="SS_FolderSecretsByIDUrl" value="/api/v1/Secrets?filter.folderId={0}"/>
    <add key="SS_SecretsFilterUrl" value="/api/v1/secrets?skip=0\&amp;take=999999999" />
    <add key="SS_SecretPermissionsByIDUrl" value="/api/v1/secret-permissions?filter.secretId=" />
</appSettings>
```
