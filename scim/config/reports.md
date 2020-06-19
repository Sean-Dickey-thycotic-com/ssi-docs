[title]: # (Reports)
[tags]: # (reports)
[priority]: # (109)
# Reports Generated for Secret Server

After the Thycotic SCIM Connector has been installed and configured, two custom reports are generated in SS. These reports are used for bulk transactions and filtering.

>**Note:** To reduce the access privileges for the SCIM server, you can create the reports manually in SS and remove the “Administer Reports” rights from the application role that was created in SS.

To manually generate the reports in Secret Server, use the following information:

__Report 1:__

   * __Report Name:__ SCIM All Users

   * __Report Description:__ Report to bulk retrieve user information for the Thycotic SCIM Server

   * __Report Category:__ User

   * __Chart Type:__ None

   * __Page Size:__ All

   * __Report SQL:__

   ``` 
   SELECT [UserId] ,[UserName] ,[DisplayName] ,[LastLogin] ,[Created]  ,[EmailAddress] ,[PasswordLastChanged] ,[Enabled]

   FROM [dbo].[tbUser] WITH (NOLOCK)

   WHERE [Enabled]=1

   AND [IsLockedOut]='False' AND [IsApplicationAccount] = 'False' AND    isnull([EmailAddress],'')!=''
   ``` 

When previewed, the report header must be as shown below:

   ![tag]()

__Report 2:__

   * __Report Name:__ SCIM All User Groups

   * __Report Description:__ Report to bulk retrieve group membership information for the Thycotic SCIM Server

   * __Report Category:__ Groups

   * __Chart Type:__ None

   * __Page Size:__ All

   * __Report SQL:__

   ``` 
   SELECT U.UserId, G.GroupName, G.GroupID, U.UserName

   FROM [dbo].[tbUser] U WITH (NOLOCK)

   Inner join tbUserGroup UG WITH (NOLOCK)

   ON

   U.UserId= UG.UserID AND U.[Enabled]=1 AND U.[IsLockedOut]='False' AND
   U.[IsApplicationAccount] = 'False’ AND isnull([EmailAddress],'')!=''

   Inner Join

   tbGroup G

   ON

   G.GroupID=UG.GroupID AND G.Active=1
   ```
When previewed, the report header must be as shown below:

   ![tag]()
