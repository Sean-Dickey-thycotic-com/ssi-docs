[title]: # (Tenable)
[tags]: # (introduction)
[priority]: # (1)
# Tenable Integration with Secret Server

The integration between Thycotic Secret Server and tenable.sc or tenable.io is created and maintained by Tenable. This document provides guidance and best practice for implementing the integration. It is based on the following publicly available documentation from Tenable and testing performed by Thycotic. This document applies to the integration Tenable.sc. The integration with Tenable’s cloud solution, Tenable.io is not supported. Integrations are supported to the extent of the third-party product procedures documented for this integration. Please contact the third-party for any customized setup of the integrated product.

Other content provided in this document is to assist customers with further understanding the technical requirements needed to configure the integration and address scalability and performance concerns that may be encountered when utilizing the integration.

## Tenable
With Tenable.sc (formerly SecurityCenter) you get a real-time, continuous assessment of your security posture so you can find and fix vulnerabilities faster. Built on Nessus technology, Tenable.sc discovers unknown assets and vulnerabilities, and monitors unexpected network changes before they turn into breaches.

## Tenable and Secret Server

The combined Tenable-Thycotic solution works when a Tenable.sc scan policy is configured to query a
Thycotic Secret Server for privileged credentials. At the time of the scan, Tenable.sc requests the privileged account credentials from Thycotic. Thycotic sends the privileged account credentials to Tenable.sc and the provided credentials are then used to log in to the target system to identify vulnerabilities and misconfigurations.

By integrating Tenable.sc with Thycotic Secret Server, you can:

* Store credentials in Thycotic Secret Server instead of managing and updating the credentials directly within a Tenable solution.

* Reduce the time and effort needed to document credential storage within the organizational
environment.

* Automatically enforce security policies within specific departments or for specific business unit
requirements, simplifying your compliance process.

* Reduce the risk of unsecured privileged accounts and credentials across the enterprise.

Tenable uses Secret Server's APIs to connect to Secret Server. If you would like further information on Tenable and their products, please visit https://docs.tenable.com/.
