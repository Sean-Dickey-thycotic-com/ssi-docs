[title]: # (Implementation Considerations)
[tags]: # (introduction)
[priority]: # (103)
# Implementation Considerations

Blue Prism Visual Business Object Studio allows you to call Thycotic Secret Server REST APIs. You can find additional information regarding the available APIs [here](https://updates.thycotic.net/secretserver/restapiguide/TokenAuth).

Information about the BluePrism Login Agent can be found here
[here](https://usermanual.wiki/Pdf/Blue20Prism20User20Guide2020Login20Agent.779174028/html).

There are two primary use-cases for using BluePrism and Secret Server.

   1. Requesting credentials for the purpose of logging into a machine with a BluePrism robot.

   1. Requesting credentials as part of a workflow that requires an additional password.

For both cases, you will need the following:

   * A Secret Server access token for use with API requests

   * A SecretID to query the correct Secret in Secret Server

   * The username associated with the Secret

   * The password associated with the Secret

The __SecretID__ of a Secret can be found by navigating to that Secret in the Secret Server UI, and looking at the URL. The Secret Server API also offers the ability to look up a SecretID by the Secret’s name, or by the Secret Name and Secret Template.

An optional Secret Server feature called Checkout enables users to reserve exclusive access to a given Secret for a period of time, or until it is checked back in. API methods for checking Secrets out and in can be used in this situation.
