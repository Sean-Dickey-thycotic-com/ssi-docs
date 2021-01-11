[title]: # (Constraints)
[tags]: # (introduction)
[priority]: # (2)

# Known Constraints and Limitations

* There is no Domain field mapping on the ServiceNow side, therefore the Active Directory secret requires the username field to be formatted as `user@domain` or `domain\user`.

* If Secret Server is utilizing an SSL certificate issued from an Active Directory Certificate Authority (internal CA) the SSL for the site has to be imported into the keystore for the MID Server agent. Documented by ServiceNow [here](https://docs.servicenow.com/search?q=Add+SSL+certificates+for+the+MID+Server&facetreset=yes). (_See configuration guide for more details._)
