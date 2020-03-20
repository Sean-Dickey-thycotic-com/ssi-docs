[title]: # (Configuration)
[tags]: # (introduction)
[priority]: # (100)
# Configuration

## Please review the following steps to setup and configure Royal TS for Secret Server:

   * [Prerequisites for Integration](prerequisites-integration.md).
   * [Configure RTS for Integration](configure-rts-integration.md).
   * [Configure Secret Server for Integration](configure-ss-integration.md).
   * [Create an RDP Credential in Secret Server](Create-rdp-ss.md).

## Royal TS Dynamic Folders

A RTS dynamic folder allows you to import data from external sources. All imported objects are read-only, but you can assign credential objects to other objects outside of dynamic folders.

Dynamic folders have several properties:

- Display Name: Required. A human-readable display name for an object.
- Color. Click the color picker button in the Display Name text box to select a color. In the [User Interface](https://content.royalapplications.com/Help/RoyalTS/V5/reference_options_userinterface.htm) settings you can configure RTS to show the color in the navigation tree, the connection tab, or as a connection border.
- Icon: Click the icon picker button next in the Display Name text box to select and assign a custom icon to the object.
- Description: An optional description for the object.

## RoyalJSON and Dynamic Folders

RoyalJSON (rJSON) is a unidirectional, human-friendly data format for importing data from external sources into RTS/X. It provides users an easy, yet powerful, way to access data stored outside of RTS/X into the application.

You can get dynamic folder samples, as well as documentation, for creating RoyalJson at our [Dynamic Folder Toolbox repository](https://github.com/royalapplications/toolbox/tree/master/Dynamic%20Folder) on GitHub.