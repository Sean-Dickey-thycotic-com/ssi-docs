[title]: # (Requirements)
[tags]: # (requirements)
[priority]: # (1)
# Integration Requirements

## System Requirements

* Thycotic Secret Server version 8.9 or later.

* Tenable.sc 5.3.2 or later.

* A tenable.sc environment with a Nessus (scanner) installation or a tenable.io subscription with a Nessus (scanner).

* A Secret Server API account with minimum permission “View” access to any secrets that are intended to be integrated.

* This integration only matches credentials based on the Secret Name field within a Secret from Secret Server and the “Thycotic Secret
Name” field within a Thycotic Secret Server credential in Tenable.

* If utilizing tenable.sc, a user account with the “Security Manager” role must be created in order to configure an Active Scan. Your administrator account will be used to create associated policies.

* If utilizing tenable.sc, this document assumes you have already created an organization, repository, a scan zone, and have installed and configured the Nessus scanner.
