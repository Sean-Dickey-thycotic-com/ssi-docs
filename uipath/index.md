[title]: # (UiPath)
[tags]: # (introduction)
[priority]: # (1)
# UiPath Integration with Secret Server

The integration between Thycotic Secret Server and UiPath is created and maintained by UiPath. This document provides guidance and best practice for implementing the integration. It is based on the following publicly available documentation from the vendor and testing performed by Thycotic.

UiPath Orchestrator is a web application that enables you to deploy, schedule, monitor and manage Robots and processes through  centralized work queues. Please visit UiPath's website for [further information](https://www.uipath.com/developers/video-tutorials/introduction-to-uipath).

The Secret Server integration is read only. When an asset or robot is created in UI Path Orchestrator it is linked to a pre-existing secret using the Secret Id.

The integration uses the Secret Server SDK, which is documented in more detail here: https://github.com/thycotic/sdk-documentation.
