[title]: # (Tenable)
[tags]: # (introduction)
[priority]: # (1)
# Tenable Integration with Secret Server

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
