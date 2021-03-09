[title]: # (IBM WebSphere)
[tags]: # (introduction)
[priority]: # (500)
# IBM WebSphere

>**Note**: Integration details coming soon.

IBM WebSphere Integration with Secret Server
WebSphere is a set of Java-based tools (middleware and application server) from IBM that allows customers to create and manage sophisticated business Web sites. The central WebSphere tool is the WebSphere Application Server (WAS), an application server that a customer can use to connect Web site users with Java applications or servlets.

The integration between Secret Server and WebSphere ensures that:

* Passwords are securely vaulted in Secret Server
* Users can enable Secret Server Credential Provider (SSCP) to fetch credentials from the Secret Server for JDBC data sources
* Users can configure credentials retrieval on a global level, data source level and a combination of enterprise application and data source level
* Users can configure local credentials cache so credentials fetched from the Secret Server are cached in-memory

In combination, these tools allow developers and organizations that are leveraging Websphere to move away from statically assigned passwords to a centralized, audited and dynamic password and credential schema. Credentials are retrieved "on demand" and can be regularly rotated, without interfering with the underlying running of the Websphere platform, or the applications that depend upon it.


