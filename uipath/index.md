[title]: # (UiPath)
[tags]: # (introduction)
[priority]: # (1)
# UiPath Integration with Secret Server

UiPath Orchestrator is a web application that enables you to deploy, schedule, monitor and manage Robots and processes through  centralized work queues. Please visit UiPath's website for [further information](https://www.uipath.com/developers/video-tutorials/introduction-to-uipath).

Robotic Process Automation software uses "robot" agents on Windows endpoints to follow scripted actions and solve problems the way a person would - by looking at the screen, reading pages, and copying text into fields.  These robots need credentials to run, and in the course of their duties may also need to use passwords for other systems.  The integration between Secret Server and UiPath ensures that:

* Passwords are securely vaulted in Secret Server
* UiPath bots can request passwords whenever they are needed
* Role-based access controls limit which passwords each bot can use
* All access by bots is captured in the Secret Server Audit Trail
