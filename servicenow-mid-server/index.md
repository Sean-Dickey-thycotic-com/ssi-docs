[title]: # (ServiceNow Mid-Server)
[tags]: # (introduction)
[priority]: # (1)
# ServiceNow Mid-Server

The integration between Thycotic Secret Server and ServiceNow is created and maintained by ServiceNow. This document provides guidance and best practice for implementing the integration. It is based on the following publicly available documentation from the vendor and testing performed by Thycotic. Integrations are supported to the extent of the third-party product procedures documented for this integration. Please contact the third-party for any customized setup of the integrated product.

This integration contains an implementation of com.snc.discovery.CredentialResolver that enables ServiceNow to use Thycotic Secret Server secrets as Discovery Credentials. The CredentialResolver uses the Secret Server REST API to request secrets, and field-mappings to map the Secret Server secret fields to ServiceNow Discovery Credential-type fields.

The CredentialResolver has two modes of operation with respect to the OAuth2 access_token:

   * Using ext.tss.oauth2.grant file to load an access_token from an OAuth2 Access Grant stored in a file.
  
   * Using ext.tss.oauth2.username and ext.tss.oauth2.password to submit an OAuth2 Access Grant Request using the OAuth2 “password” grant_type just-in-time.


This document was created with versions:

   * Secret Server Version: 10.7.00059

   * ServiceNow Version: glide-newyork-06-26-2019__patch4-hotfix1-12-16-2019_12-17-2019_0856.zip

   * Java 8 Update 231