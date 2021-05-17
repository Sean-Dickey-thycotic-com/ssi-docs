[title]: # (Silent HSM Operation)
[tags]: # (operation)
[priority]: # (10)
# Silent HSM Operation

Because Secret Server is a web application with no one physically present at the server at most times,
Secret Server interacts with the HSM in “silent” mode. This will prevent the HSM from attempting to
interact with any users logged onto the server.

Some HSM features require interaction. If the HSM is configured in such a way that requires interaction,
Secret Server will be unable to communicate with the HSM and fail during the configuration steps.
An example of such a configuration is Operator Card Sets in Thales network HSMs. If the Thales CNG
provider is configured to use an Operator Card Set, or OCS, for key protection instead of Module
protection, someone must be physically present at the HSM and the Server to insert their operator card
when the key is needed. If the OCS quorum is more than a single card, Secret Server cannot interact with
the HSM because it requires inserting and removing the OCS cards.

It is recommended that Thales’ CNG provider is configured to use Module protection instead of an OCS.
It is possible to use an OCS with Secret Server if the quorum is exactly one card and the card is left in the
HSM at all times.

It is recommended to consult your HSM vendor and their documentation to ensure that the HSM and
their CNG provider are able to operate in silent mode and are configured to do so.
