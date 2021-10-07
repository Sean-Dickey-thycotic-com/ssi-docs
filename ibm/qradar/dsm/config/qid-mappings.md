[title]: # (QID Mappings)
[tags]: # (introduction)
[priority]: # (104)
# QID Mappings

The QID or QRadar Identifier is what QRadar uses to give events their name, high-level category and lowlevel category.

1. We now need to create custom QIDs. Do this by SSH-ing into the QRadar console, changing the directory to __/opt/QRadar/bin__ and running the following command:

   `./qidmap_cli.sh -c --qname <name> --qdescription <description> --severity <severity> --lowlevelcategoryid <ID>`

   For Example:

   `./qidmap_cli.sh -c --qname “USER – LOGIN” --qdescription “A user as logged in.” --severity 1 --lowlevelcategoryid 19001`

   ![tag](images/config5.png)
1. Alternatively you could use a csv list as demonstrated in the in the __Import List__ section and use it with the following command to import several QIDs at once:

   `/opt/QRadar/bin/qidmap_cli.sh -i -f <filename.txt>`

   19001 is used for most of the low-level category IDs as an example.

1. Using the program __sendnow__, send the list of all events to your QRadar box in the .txt file you named (example: __tss events all.txt__) to generate every possible event. The events can be found in the Event List section below.

## Event List

|                                       |                                                                |    |       |
|---------------------------------------|----------------------------------------------------------------|----|-------|
| CONFIGURATION - EDIT                  | The main Thycotic Secret Server configuration has been edited  | 10 | 19001 |
| FOLDER - CREATE                       | A Folder has been created                                      | 2  | 19001 |
| FOLDER - DELETE                       | A Folder has been deleted                                      | 5  | 19001 |
| FOLDER - EDIT PERMISSIONS             | The configuration has been edited                              | 10 | 19001 |
| FOLDER - SECRET POLICY CHANGE         | The policy assigned to a folder has been changed               | 6  | 19001 |
| FOLDER - SECRET POLICY CHANGE         | The Secret policy assigned to a folder has been changed        | 8  | 19001 |
| GROUP - OWNERS MODIFIED               | The owners of a group have been modified                       | 5  | 19001 |
| LICENSE - EXPIRES 30 DAYS             | Secret servers license will expire in 30 days                  | 1  | 19001 |
| POWERSHELL SCRIPT - CREATE            | A PowerShell script has been created                           | 5  | 19001 |
| POWERSHELL SCRIPT - DEACTIVATE        | A PowerShell script has been deactivated                       | 5  | 19001 |
| POWERSHELL SCRIPT - EDIT              | A PowerShell script has been edited                            | 8  | 19001 |
| POWERSHELL SCRIPT - REACTIVATE        | A PowerShell script has been reactivated                       | 6  | 19001 |
| POWERSHELL SCRIPT - VIEW              | A PowerShell script has been viewed                            | 5  | 19001 |
| ROLE - ASSIGN USER OR GROUP           | A role has been assigned to a user or group                    | 5  | 19001 |
| ROLE - CREATE                         | A role has been created                                        | 5  | 19001 |
| ROLE - UNASSIGN USER OR GROUP         | A role has been unassigned to a user or group                  | 5  | 19001 |
| ROLE PERMISSION - ADDED TO ROLE       | A permission has been added to a role                          | 5  | 19001 |
| ROLE PERMISSION - REMOVED FROM ROLE   | A permission has been removed from a role                      | 5  | 19001 |
| SECRET - ACCESS APPROVED              | Access to a Secret has been approved                           | 2  | 19001 |
| SECRET - ACCESS DENIED                | Access to a Secret has been denied                             | 6  | 19001 |
| SECRET - CHECKIN                      | A Secret has been checked in                                   | 1  | 19001 |
| SECRET - CHECKOUT                     | A Secret has been checked out                                  | 5  | 19001 |
| SECRET - COPY                         | A Secret has been copied                                       | 1  | 19001 |
| SECRET - CREATE                       | A Secret has been created                                      | 1  | 19001 |
| SECRET - CUSTOM AUDIT                 | A custom audit has been created                                | 1  | 19001 |
| SECRET - CUSTOM REQUIREMENT ADDED     | A custom password requirement has been added to a Secret       | 2  | 19001 |
| SECRET - CUSTOM REQUIREMENT REMOVED   | A custom password requirement has been removed from a Secret   | 6  | 19001 |
| SECRET - DELETE                       | A Secret has been deleted                                      | 5  | 19001 |
| SECRET - DEPENDENCY ADDED             | A dependency has been added                                    | 8  | 19001 |
| SECRET - DEPENDENCY FAILURE           | A dependency is missing                                        | 5  | 19001 |
| SECRET - DEPENDENCY REMOVED           | A dependency has been removed                                  | 8  | 19001 |
| SECRET - EDIT                         | A Secret has been edited                                       | 5  | 19001 |
| SECRET - EDIT VIEW                    | A Secrets view option has been edited                          | 8  | 19001 |
| SECRET - EXPIRES 1 DAY                | A Secret expires in 1 day                                      | 5  | 19001 |
| SECRET - EXPIRES 15 DAYS              | A Secret expires in 15 days                                    | 1  | 19001 |
| SECRET - EXPIRES 3 DAYS               | A Secret expires in 3 days                                     | 1  | 19001 |
| SECRET - EXPIRES 7 DAYS               | A Secret expires in 7 days                                     | 1  | 19001 |
| SECRET - EXPIRES TODAY                | A Secret expires today                                         | 1  | 19001 |
| SECRET - HEARTBEAT FAILURE            | Heartbeat has not been detected for over 10 seconds            | 5  | 19001 |
| SECRET - HEARTBEATSUCCESS             | Heartbeat has been detected                                    | 1  | 19001 |
| SECRET - HOOK CREATE                  | A hook has been created                                        | 3  | 19001 |
| SECRET - HOOK DELETE                  | A hook has been deleted                                        | 8  | 19001 |
| SECRET - HOOK EDIT                    | A hook has been edited                                         | 6  | 19001 |
| SECRET - HOOKFAILURE                  | A hook has failed to initialise a PowerShell script            | 8  | 19001 |
| SECRET - HOOKSUCCESS                  | A hook has successfully initialised a PowerShell script        | 1  | 19001 |
| SECRET - LAUNCH                       | A Secret has been launched                                     | 1  | 19001 |
| SECRET - PASSWORD COPIED TO CLIPBOARD | A password has been copied to the clipboard                    | 5  | 19001 |
| SECRET - PASSWORD_DISPLAYED           | A Secret password has been displayed                           | 5  | 19001 |
| SECRET - SECRET POLICY CHANGE         | The Secret policy assigned to a Secret has been changed        | 8  | 19001 |
| SECRET - SESSION RECORDING VIEW       | A Secret recording is being viewed                             | 5  | 19001 |
| SECRET - UNDELETE                     | A Secret has been restored                                     | 1  | 19001 |
| SECRET - VIEW                         | A Secret has been viewed                                       | 1  | 19001 |
| SECRET POLICY - CREATE                | A Secret policy has been created                               | 1  | 19001 |
| SECRET POLICY - EDIT                  | A Secret policy has been edited                                | 6  | 19001 |
| SECRET TEMPLATE - COPY                | A Secret template has been copied                              | 1  | 19001 |
| SECRET TEMPLATE - CREATE              | A Secret template has been created                             | 1  | 19001 |
| SECRET TEMPLATE - EDIT                | A Secret template has been edited                              | 1  | 19001 |
| SECRET TEMPLATE - FIELD ENCRYPTED     | A field in a template has been encrypted                       | 1  | 19001 |
| SECRET TEMPLATE - FIELD EXPOSED       | A field in a template has been exposed                         | 6  | 19001 |
| SECRETS EXPORTD                       | Secrets have been exported                                     | 10 | 19001 |
| SECRETS IMPORTED                      | Secrets have been imported                                     | 1  | 19001 |
| SYSTEM LOG                            | Thycotic Secret server system logs                             | 1  | 19001 |
| UNLIMITED ADMIN - DISABLED            | Unlimited admin has been disabled                              | 10 | 19001 |
| UNLIMITED ADMIN - ENABLED             | Unlimited admin has been enabled                               | 10 | 19001 |
| USER - ADDED TO GROUP                 | A user account has been added to a group                       | 8  | 19001 |
| USER - CREATE                         | A user account has been created                                | 5  | 19001 |
| USER - DISABLE                        | A user account has been disabled                               | 5  | 19001 |
| USER - ENABLE                         | A user account has been enabled                                | 5  | 19001 |
| USER - LOCKOUT                        | A user account has been locked out see payload for information | 10 | 19001 |
| USER - LOGIN                          | A user has logged on                                           | 1  | 19001 |
| USER - LOGIN FAILURE                  | A user has entered an incorrect password                       | 8  | 19001 |
| USER - LOGOUT                         | A user has logged out                                          | 1  | 19001 |
| USER - PASSWORD CHANGE                | A users password has been changed                              | 8  | 19001 |
| USER - REMOVED FROM GROUP             | A user account has been removed from a group                   | 5  | 19001 |
| USERAUDIT - EXPIRENOW                 | All Secrets a user has accessed have expired                   | 5  | 19001 |