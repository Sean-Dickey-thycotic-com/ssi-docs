[title]: # (Configure and run the Script)
[tags]: # (introduction)
[priority]: # (103)
# Configure and Run the Script

Once all dependencies have been installed, configure the script:

1.  Open the nexpose\\_thycotic.config file located in the Ruby installation
    folder. For example:
    C:\\Ruby25-x64\\lib\\ruby\\gems\\2.5.0\\gems\\nexpose\\_thycotic-02.0\\lib\\nexpose\\_thycotic\\config

2.  Configure Secret Server. Set up the following options for the user who is
    running the Gem:

-   thycotic\\_url: The IP address for the Secret Server instance with WSDL. For
    example: https://127.0.0.1/SecretServer/webservices/sswebservice.asmx?wsdl.

-   thycotic\\_username: The username configured in SS.

-   thycotic\\_passsword: The password for that SS user.

-   comment: The comment used when retrieving each password.

1.  Configure Nexpose by setting the following options:

-   nexpose\\_url: The URL/IP For the Nexpose instance. For example:
    https://192.168.0.1/ .

-   nexpose\\_username: The username in Nexpose.

-   nexpose\\_password: The password for the user in Nexpose.

-   nexpose\\_port: Set if Nexpose was installed with a different port than the
    default 3780.

1.  Configure additional settings:

-   sites: Sites to manage. There can be more than one site.

-   clear\\_creds: Set to True to delete all pre-existing credentials when
    importing from SS.

-   logging\\_enabled: Enables logging to the log directory.

-   log\\_level: Default is info but can be set to debug, warn, or error.

-   log\\_console: Determines if log messages are output to the console.

Step Four: Run the Script
-------------------------

1.  Run the script from the command line: ruby nexpose\\_thycotic. The script
    runs and performs the queries. On windows systems, you can also run the
    nexpose_tycotic command from the C:\\Ruby25-x64\\bin directory.

The credentials will then be available for each asset in your newly existing
site(s). This can be verified by the following lines in the script output and in
the Authentication Tab of the site for each asset.

![](images/ac49409a8714b702dde65b1f54d7247c.png)

![](images/9e047243a5ec07a4925f24dd8b60d47c.png)