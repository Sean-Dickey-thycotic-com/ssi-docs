[title]: # (HSM Redundancy)
[tags]: # (redundancy)
[priority]: # (13)
# HSM Redundancy

This varies from HSM to HSM, and the vendor’s documentation on how to back up the HSM should be
referenced. Backups are typically either made to common file location, or another HSM, or onto a smart card
with the HSM’s built-in smart card reader.

As long as the CNG provider is installed on the server and a key exists on the HSM with the same
identifier, Secret Server will attempt to use that key.
