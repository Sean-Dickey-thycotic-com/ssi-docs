[title]: # (Constraints)
[tags]: # (introduction)
[priority]: # (2)

# Known Constraints and Limitations

* There is no Domain field mapping on the ServiceNow side, this requires that an Active Directory account must have the username in format of `user@domain`.

* If Secret Server is utilizing an SSL certificate issued from an Active Directory Certificate Authority (internal CA) then the SSL for the site has to be imported into the keystore for the MID Server agent. Documented by ServiceNow [here](https://docs.servicenow.com/search?q=Add+SSL+certificates+for+the+MID+Server&facetreset=yes). (See configuration guide for more details.)
