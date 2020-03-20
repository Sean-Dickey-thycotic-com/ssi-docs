[title]: # (Okta for SAML)
[tags]: # (introduction)
[priority]: # (1)
# Okta for SAML Integration

The integration between Thycotic Secret Server and Okta is created and maintained by Okta. This document provides guidance and best practice for implementing the integration. It is based on the following publicly available documentation from the vendor and testing performed by Thycotic. Integrations are supported to the extent of the third-party product procedures documented for this integration. Please contact the third-party for any customized setup of the integrated product.

This document is to serve as the configuration document for integrating Okta for SAML and Secret Server.

Secret Server acts as a SAML Service Provider that can communicate with Okta for authentication. This allows Secret Server the use of SAML Identity Provider (IdP) authentication instead of the normal authentication process for single sign-on (SSO). To do this, Secret Server acts as a SAML Service Provider (SP) that can communicate with any configured SAML IdP, including Okta.
