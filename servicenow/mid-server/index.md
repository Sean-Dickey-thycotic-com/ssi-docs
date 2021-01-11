[title]: # (MID Server)
[tags]: # (introduction)
[priority]: # (300)

# ServiceNow MID Server

The integration between Thycotic Secret Server and a ServiceNow MID Server is maintained by Thycotic. This document is provided as a guide and best practice for implementing the Thycotic Credential Resolver with ServiceNow MID servers in your environment.

This integration contains an implementation of the `com.snc.discovery.CredentialResolver` that enables ServiceNow to use Secret Server secrets as Discovery Credentials with the MID Server(s). The Credential Resolver uses the Secret Server REST API to request secrets, and field-mappings to map the secret fields to ServiceNow Discovery Credential fields.

## Implementation Modes

The REST API for Secret Server utilizes an OAuth2 token for authentication. The Java class in use by our Credential Resolver was written to handle two modes for this authentication:

### Just-In-Time Mode

In this mode the MID Server agent configuration file is modified to include the Secret Server API accounts username and password. In this mode the MID Server agent will handle authenticating to the REST API and requesting the needed OAuth2 token to retrieve secrets.

> **Note**: It does require providing the username and password in plain text within the configuration file. If this method is utilized ensure access to the MID Server and the agent folder are restricted.

### Grant File Mode

In this mode the MID Server agent configuration file is modified to include the path to a `oauth2_grant.json` file. This file will contain the access token the agent will use for authenticating the API calls. It requires an external source to write the OAuth2 token to the file.

The external source will require execution on a regular schedule based on the Web Services configuration of your Secret Server instance. The recommended mechanism documented is Windows Task Scheduler.
