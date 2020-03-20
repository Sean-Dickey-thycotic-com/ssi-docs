[title]: # (Qualys)
[tags]: # (introduction)
[priority]: # (1)
# Introduction

The integration between Thycotic Secret Server and Qualys is created and maintained by Qualys. This document provides guidance and best practice for implementing the integration. It is based on the following publicly available documentation from the vendor and testing performed by Thycotic. Integrations are supported to the extent of the third-party product procedures documented for this integration. Please contact the third-party for any customized setup of the integrated product.

## Using Secret Server as a Credential Vault for Authenticated Scans

Secret Server is an on-premise, web-based password vault used to help organizations properly manage privileged account
passwords. Secret Server allows users to control access and automate password changes for a variety of enterprise
resources. Organizations can easily deploy Secret Server to be more secure, reduce labor costs, adopt password best practices, and satisfy audit requirements.

QualysGuard can use the Secret Server as a Credential Vault for the accounts used for authenticated scanning. Instead of
adding individual credentials for trusted scans, the Administrator can use named records stored in Secret Server. There are several benefits to this approach:

   * Using Secret Server means that all the credentials used for authenticated scans will be stored securely on-premise and
will not leave the network.

   * Password rotation can happen frequently and automatically as Secret Server performs the password changes and
QualysGuard retrieves the passwords as needed during scans.

   * Credentials can still be securely controlled in Secret Server with full auditing over their usage.
