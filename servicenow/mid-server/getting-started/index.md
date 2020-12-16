[title]: # (Getting Started)
[tags]: # (Requirements)
[priority]: # (1)

# Getting Started with ServiceNow MID Integration

## Pre-requisites

### System Requirements

#### Thycotic Secret Server

* Version 10.7.00059 or later
* Web Services enabled
* Secret Server User Account (Application Account) with minimum `VIEW` access to the secret(s) configured as Credentials

#### ServiceNow

* MID Server in an `Up` state
* MID Server validated
* MID Server has HTTP or HTTPS access to Secret Server

## ServiceNow Plugin

The ServiceNow **External Credential Store** plugin must be activated for your ServiceNow release. The process for this may vary based on each release of ServiceNow. Search their documentation [here](https://docs.servicenow.com/search?q=External+credential+storage&facetreset=yes) and filter based on the release you have in production.

## Credential Resolver JAR file

Thycotic has open-sourced the credential resolver Java code that can be found on GitHub, [Thycotic/service-now-credential-resolver](https://github.com/thycotic/service-now-credential-resolver). This can be compiled to obtain the JAR file for this integration.

A compiled jar file can be downloaded via the archive file here: [tss-credential-resolver-1.0.zip](https://updates.thycotic.com/secretserver/servicenow/tss-credential-resolver-1.0.zip).
