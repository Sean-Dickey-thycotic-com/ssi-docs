[title]: # (Configuration)
[tags]: # (introduction)
[priority]: # (100)
# Configuration

## Integrating Splunk Cloud with Secret Server

The following are the overall steps to integrate Splunk Cloud with Secret Server.

>**Note:** Both TCP and UDP Protocols are available to use when integrating Secret Server with Splunk Cloud. TCP is noted as the preferable way to collect the syslogs due to more accurate packet captures for Secret Server events.

* [Registering with Splunk](registering-Splunk.md)
* [Installing and configuring Universal Forwarder](install-config-universal.md)
* [Configuration using TCP](steps/tcp.md)
* [Configuration using UDP](steps/udp.md)

>**Note:** Please be aware that the last steps are only for users that are interested in publishing the Splunk App. These steps are not required for configuring Splunk Cloud with Secret Server.

## Publishing and Packaging Splunk App

The Splunk app is a quick way to get analysis, reports, health checks, and
usage of your on-premises Secret Server instance. The App is created on the enterprise edition of Splunk so that it can be
packaged and published on the Splunkbase.

## Publishing and Packaging Splunk App to Splunkbase

To create a Splunk App, ensure that the prerequisites are met. This section
provides the steps to create an app, dashboard, and package the app.

The following are the steps to be performed:

* [Create an App](create-an-app.md)
* [Create Dashboard](create-dashboard.md)
* [Package the App](package-the-app.md)
