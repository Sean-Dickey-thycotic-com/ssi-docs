[title]: # (Constraints)
[tags]: # (introduction)
[priority]: # (2)

# Known Constraints and Limitations

* The current implementation requests a token immediately prior to requesting the secret, when operating in just-in-time mode.  One-time token authentication with expiration-timer based renewal, will be offered in the next iteration of the integration

* When using token-in-file mode, there is not currently a way to trigger the powershell script to run based only on the event of Discovery being triggered (manually or scheduled)

* There is no Domain field mapping on the ServiceNow side, this requires that the domain field must be combined with the username field within a Secret Server Secret. Please see the troubleshooting section for more details