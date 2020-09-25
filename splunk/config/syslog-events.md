[title]: # (syslog Events)
[tags]: # (syslog)
[priority]: # (108)
# Syslog Events

| **Type**                       | **TypeId** | **Action**                           | **ActionId** | **Description**                                                        |
|--------------------------------|------------|--------------------------------------|--------------|------------------------------------------------------------------------|
| FOLDER                         | 2          | CREATE                               | 7            | A folder has been created                                              |
| FOLDER                         | 2          | DELETE                               | 8            | A folder has been deleted                                              |
| FOLDER                         | 2          | EDITPERMISSIONS                      | 14           | A folder's permissions have been changed                               |
| FOLDER                         | 2          | SECRETPOLICYCHANGE                   | 10053        | A folder's secret policy was changed                                   |
| SECRET                         | 10001      | CREATE                               | 10001        | A secret has been created                                              |
| SECRET                         | 10001      | DELETE                               | 10002        | A secret has been deleted                                              |
| SECRET                         | 10001      | UNDELETE                             | 10003        | A secret has been undeleted                                            |
| SECRET                         | 10001      | VIEW                                 | 10004        | A secret has been viewed                                               |
| SECRET                         | 10001      | CACHEVIEW                            | 10103        | A secret has been viewed, but cached data was presented                |
| SECRET                         | 10001      | FILESAVE                             | 10102        | A file was saved to a secret                                           |
| SECRET                         | 10001      | EDIT                                 | 10005        | A secret was edited                                                    |
| SECRET                         | 10001      | LAUNCH                               | 10006        | A secret was launched                                                  |
| SECRET                         | 10001      | WEBPASSWORDFILL                      | 10099        | A secret was used to fill a web form                                   |
| SECRET                         | 10001      | HEARTBEATFAILURE                     | 10007        | A secret's heartbeat failed                                            |
| SECRET                         | 10001      | HEARTBEATSUCCESS                     | 10032        | A secret's heartbeat succeeded                                         |
| SECRET                         | 10001      | DEPENDENCYFAILURE                    | 10008        | A secret's dependency failed                                           |
| SECRET                         | 10001      | EXPIREDTODAY                         | 10009        | A secret is expiring today                                             |
| SECRET                         | 10001      | EXPIRES01DAY                         | 10010        | A secret is expiring in one day                                        |
| SECRET                         | 10001      | EXPIRES03DAYS                        | 10013        | A secret is expiring in three days                                     |
| SECRET                         | 10001      | EXPIRES07DAYS                        | 10011        | A secret is expiring in seven days                                     |
| SECRET                         | 10001      | EXPIRES15DAYS                        | 10012        | A secret is expiring in fifteen days                                   |
| SECRET                         | 10001      | EXPIRES30DAYS                        | 10094        | A secret is expiring in thirty days                                    |
| SECRET                         | 10001      | EXPIRES45DAYS                        | 10095        | A secret is expiring in forty-five days                                |
| SECRET                         | 10001      | EXPIRES60DAYS                        | 10096        | A secret is expiring in sixty days                                     |
| SECRET                         | 10001      | SECRETPOLICYCHANGE                   | 10054        | A secret's policy was changed                                          |
| SECRET                         | 10001      | SECRETPASSWORDCHANGE                 | 10055        | A secret's password was changed                                        |
| SECRET                         | 10001      | PASSWORD CHANGE MAX ATTEMPTS REACHED | 10068        | A secret has reached the max amount of attempts to change its password |
| SECRET                         | 10001      | EXPORTSECRET                         | 10093        | A secret was exported                                                  |
| SECRET                         | 10001      | SESSION RECORDING VIEW               | 10019        | A session recording of a launched secret was viewed                    |
| SECRET                         | 10001      | COPY                                 | 10020        | A secret was copied                                                    |
| SECRET                         | 10001      | CHECKIN                              | 10025        | A secret was checked in                                                |
| SECRET                         | 10001      | CHECKOUT                             | 10026        | A secret was checked out                                               |
| SECRET                         | 10001      | HOOKFAILURE                          | 10033        | A hook has failed to initialise a PowerShell script                    |
| SECRET                         | 10001      | HOOKSUCCESS                          | 10034        | A hook has successfully initialised a PowerShell script                |
| SECRET                         | 10001      | HOOKCREATE                           | 10035        | A hook has been created                                                |
| SECRET                         | 10001      | HOOKEDIT                             | 10036        | A hook has been edited                                                 |
| SECRET                         | 10001      | HOOKDELETE                           | 10037        | A hook has been deleted                                                |
| SECRET                         | 10001      | CUSTOM_AUDIT                         | 10038        | A custom audit has been created                                        |
| SECRET                         | 10001      | PASSWORD_DISPLAYED                   | 10039        | A secret's password was displayed                                      |
| SECRET                         | 10001      | PASSWORD_COPIED_TO_CLIPBOARD         | 10040        | A secret's password was copied to the clipboard                        |
| SECRET                         | 10001      | VIEWED_EDIT                          | 10041        | The secret's view option was edited                                    |
| SECRET                         | 10001      | ACCESS_APPROVED                      | 10044        | A secret's access request was approved                                 |
| SECRET                         | 10001      | ACCESS_DENIED                        | 10045        | A secret's access request was denied                                   |
| SECRET                         | 10001      | CUSTOM_PASSWORD_REQUIREMENT_ADDED    | 10046        | A custom password requirement was added to a secret                    |
| SECRET                         | 10001      | CUSTOM_PASSWORD_REQUIREMENT_REMOVED  | 10047        | A custom password requirement was removed from a secret                |
| SECRET                         | 10001      | DEPENDENCY_DELETED                   | 10048        | A dependency was removed from a secret                                 |
| SECRET                         | 10001      | DEPENDENCY_ADDED                     | 10049        | A dependency was added to a secret                                     |
| UNLIMITEDADMIN                 | 10002      | ENABLE                               | 10014        | Unlimited admin mode was enabled                                       |
| UNLIMITEDADMIN                 | 10002      | DISABLE                              | 10015        | Unlimited admin mode was disabled                                      |
| EXPORTSECRETS                  | 10003      | EXPORTED                             | 10016        | Secrets have been exported from Secret Server                          |
| IMPORTSECRETS                  | 10004      | IMPORTED                             | 10017        | Secrets have been imported to Secret Server                            |
| USERAUDIT                      | 10005      | EXPIRENOW                            | 10018        | Secrets have been manually expired                                     |
| SECRETTEMPLATE                 | 10006      | CREATE                               | 10021        | A secret template was created                                          |
| SECRETTEMPLATE                 | 10006      | EDIT                                 | 10022        | A secret template was edited                                           |
| SECRETTEMPLATE                 | 10006      | TEMPLATE COPIED FROM                 | 10023        | A secret template was copied                                           |
| SECRETTEMPLATE                 | 10006      | FIELD ENCRYPTED                      | 10042        | A field in a secret template was marked to be encrypted                |
| SECRETTEMPLATE                 | 10006      | FIELD EXPOSED                        | 10043        | A field in a secret template was marked to be exposed                  |
| SECRETTEMPLATE                 | 10006      | OWNERS_MODIFIED                      | 10107        | The owners of a secret template were changed                           |
| SECRETTEMPLATE                 | 10006      | CREATE SECRET ACCESS CHANGED         | 10108        | Users that have access to create a secret of a template were changed   |
| SCRIPTPOWERSHELL               | 10008      | CREATE                               | 10027        | A powershell script was created                                        |
| SCRIPTPOWERSHELL               | 10008      | DEACTIVATE                           | 10028        | A powershell script was deactivated                                    |
| SCRIPTPOWERSHELL               | 10008      | EDIT                                 | 10029        | A powershell script was edited                                         |
| SCRIPTPOWERSHELL               | 10008      | REACTIVATE                           | 10030        | A powershell script was reactivated                                    |
| SCRIPTPOWERSHELL               | 10008      | VIEW                                 | 10031        | A powershell script was viewed                                         |
| SECRETPOLICY                   | 10009      | CREATE                               | 10051        | A secret policy was created                                            |
| SECRETPOLICY                   | 10009      | EDIT                                 | 10052        | A secret policy was edited                                             |
| SCRIPTSSH                      | 10010      | CREATE                               | 10056        | An ssh script was created                                              |
| SCRIPTSSH                      | 10010      | DEACTIVATE                           | 10057        | An ssh script was deactivated                                          |
| SCRIPTSSH                      | 10010      | EDIT                                 | 10058        | An ssh script was edited                                               |
| SCRIPTSSH                      | 10010      | REACTIVATE                           | 10059        | An ssh script was reactivated                                          |
| SCRIPTSSH                      | 10010      | VIEW                                 | 10060        | An ssh script was viewed                                               |
| SCRIPTSQL                      | 10011      | CREATE                               | 10061        | A SQL script was created                                               |
| SCRIPTSQL                      | 10011      | DEACTIVATE                           | 10062        | A SQL script was deactivated                                           |
| SCRIPTSQL                      | 10011      | EDIT                                 | 10063        | A SQL script was edited                                                |
| SCRIPTSQL                      | 10011      | REACTIVATE                           | 10064        | A SQL script was reactivated                                           |
| SCRIPTSQL                      | 10011      | VIEW                                 | 10065        | A SQL script was viewed                                                |
| ENCRYPTION                     | 10012      | HSM ENABLE                           | 10066        | HSM was enabled                                                        |
| ENCRYPTION                     | 10012      | HSM DISABLE                          | 10067        | HSM was disabled                                                       |
| ENCRYPTION                     | 10012      | KEY MANAGEMENT ENABLE                | 10146        | Key management was enabled                                             |
| ENCRYPTION                     | 10012      | KEY MANAGEMENT EDIT                  | 10147        | Key management was edited                                              |
| ENCRYPTION                     | 10012      | KEY MANAGEMENT DISABLE               | 10148        | Key management was disabled                                            |
| ENCRYPTION                     | 10012      | ROTATE SECRET KEYS                   | 10069        | Rotate secret keys was requested                                       |
| ENCRYPTION                     | 10012      | ROTATE SECRET KEYS CANCEL REQUESTED  | 10070        | Rotate secret keys was canceled                                        |
| ENCRYPTION                     | 10012      | ROTATE SECRET KEYS SUCCESS           | 10071        | Roatate secret keys succeeded                                          |
| ENCRYPTION                     | 10012      | ROTATE SECRET KEYS FAILURE           | 10072        | Roatate secret keys failed                                             |
| SITE                           | 10013      | CREATE                               | 10073        | A site was created                                                     |
| SITE                           | 10013      | EDIT                                 | 10074        | A site was edited                                                      |
| SITE                           | 10013      | ENABLE                               | 10075        | A site was enabled                                                     |
| SITE                           | 10013      | DISABLE                              | 10076        | A site was disabled                                                    |
| SITE                           | 10013      | ADDENGINE                            | 10077        | An engine was added to a site                                          |
| SITE                           | 10013      | REMOVEENGINE                         | 10078        | An engine was removed from a site                                      |
| SITE                           | 10013      | ENGINEONLINE                         | 10079        | An engine was brought online                                           |
| SITE                           | 10013      | ENGINEOFFLINE                        | 10080        | An engine was taken offline                                            |
| SITE                           | 10013      | ENGINEDOWNLOAD                       | 10081        | An engine was downloaded for a site                                    |
| SITE                           | 10013      | ASSIGNEDOMAIN                        | 10091        | A site was assigned to a domain                                        |
| SITE                           | 10013      | REMOVEDOMAIN                         | 10092        | A site was removed from a domain                                       |
| ENGINE                         | 10014      | CREATE                               | 10082        | An engine was created                                                  |
| ENGINE                         | 10014      | ACTIVATE                             | 10083        | An engine was activated                                                |
| ENGINE                         | 10014      | DEACTIVATE                           | 10084        | An engine was deactived                                                |
| ENGINE                         | 10014      | DELETE                               | 10085        | An engine was deleted                                                  |
| ENGINE                         | 10014      | OFFLINE                              | 10151        | An engine was taken offline                                            |
| ENGINE                         | 10014      | ONLINE                               | 10152        | An engine was brought online                                           |
| SITECONNECTOR                  | 10015      | CREATE                               | 10086        | A site connector was created                                           |
| SITECONNECTOR                  | 10015      | EDIT                                 | 10087        | A site connector was edited                                            |
| SITECONNECTOR                  | 10015      | ENABLE                               | 10088        | A site connector was enabled                                           |
| SITECONNECTOR                  | 10015      | DISABLE                              | 10089        | A site connector was disabled                                          |
| SITECONNECTOR                  | 10015      | CREDENTIALVIEW                       | 10090        | A site connector's credentials were viewed                             |
| SECURITYANALYTICSCONFIGURATION | 10016      | EDIT                                 | 10098        | Privileged Behavior Analytic settings were edited                      |
| DUALCONTROL                    | 10017      | CREATE                               | 10104        | A dual control was created                                             |
| DUALCONTROL                    | 10017      | UPDATE                               | 10105        | A dual control was updated                                             |
| DUALCONTROL                    | 10017      | DELETE                               | 10106        | A dual control was deleted                                             |
| USER                           | 1          | CREATE                               | 1            | A user was created                                                     |
| USER                           | 1          | DISABLE                              | 2            | A user was disabled                                                    |
| USER                           | 1          | ENABLE                               | 3            | A user was enabled                                                     |
| USER                           | 1          | LOCKOUT                              | 4            | A user was locked out                                                  |
| USER                           | 1          | ADDEDTOGROUP                         | 5            | A user was added to a group                                            |
| USER                           | 1          | REMOVEDFROMGROUP                     | 6            | A user was removed from a group                                        |
| USER                           | 1          | LOGIN                                | 16           | A user logged in                                                       |
| USER                           | 1          | LOGOUT                               | 17           | A user logged out                                                      |
| USER                           | 1          | LOGINFAILURE                         | 18           | A user failed to log in                                                |
| USER                           | 1          | PASSWORDCHANGE                       | 19           | A user's password was changed                                          |
| USER                           | 1          | OWNERS_MODIFIED                      | 10097        | A user's owner was modified                                            |
| USER                           | 1          | EDIT                                 | 10100        | A user was edited                                                      |
| USER                           | 1          | TWO FACTOR UPDATED                   | 10101        | A user's two factor settings were updated                              |
| USER                           | 1          | TWOFACTORRESET                       | 10149        | A user's two factor was reset                                          |
| USER                           | 1          | TWOFACTORRESETFAILED                 | 10150        | A user's two factor authentication failed                              |
| USER                           | 1          | CHALLENGE_APPLIED                    | 10116        | A PBA challenge was applied to a user                                  |
| USER                           | 1          | CHALLENGE_CLEARED                    | 10117        | A PBA challenge was cleared from a user                                |
| ROLE                           | 3          | CREATE                               | 9            | A role was created                                                     |
| ROLE                           | 3          | ASSIGNUSERORGROUP                    | 10           | A user or group was assigned to a role                                 |
| ROLE                           | 3          | UNASSIGNUSERORGROUP                  | 11           | A user or group was unassigned from a role                             |
| ROLE                           | 3          | ENABLEROLE                           | 20           | A role was enabled                                                     |
| ROLE                           | 3          | DISABLEROLE                          | 21           | A role was disabled                                                    |
| ROLE                           | 3          | EDIT                                 | 10142        | A role was edited                                                      |
| ROLEPERMISSION                 | 4          | ADDEDTOROLE                          | 12           | A permission was added to a role                                       |
| ROLEPERMISSION                 | 4          | REMOVEDFROMROLE                      | 13           | A permission was removed from a role                                   |
| CONFIGURATION                  | 5          | EDIT                                 | 15           | Configuration was edited                                               |
| CONFIGURATION                  | 5          | UPGRADE                              | 10121        | An updated was started or completed                                    |
| CONFIGURATION                  | 5          | DATABASE EDIT                        | 10122        | Database configuration was edited                                      |
| CONFIGURATION                  | 5          | BACKUP                               | 10144        | Database was backed up                                                 |
| GROUP                          | 6          | CREATE                               | 10140        | A group was created                                                    |
| GROUP                          | 6          | EDIT                                 | 10141        | A group was edited                                                     |
| IPADDRESSRANGE                 | 7          | CREATE                               | 10109        | An ip range was created                                                |
| IPADDRESSRANGE                 | 7          | UPDATE                               | 10110        | An ip range was updated                                                |
| IPADDRESSRANGE                 | 7          | DELETE                               | 10111        | An ip range was deleted                                                |
| IPADDRESSRANGE                 | 7          | USER ASSIGN                          | 10112        | A user was assigned to an ip range                                     |
| IPADDRESSRANGE                 | 7          | USER UNASSIGN                        | 10113        | A user was removed from an ip range                                    |
| IPADDRESSRANGE                 | 7          | GROUP ASSIGN                         | 10114        | A group was assigned to an ip range                                    |
| IPADDRESSRANGE                 | 7          | GROUP UNASSIGN                       | 10115        | A group was removed from an ip range                                   |
| TLS                            | 10018      | FAIL                                 | 10118        | A TLS error occurred while connecting to a remote server               |
| LICENSES                       | 10007      | ADD                                  | 10119        | A license was added                                                    |
| LICENSES                       | 10007      | DELETE                               | 10120        | A license was removed                                                  |
| PASSWORDCHANGER                | 10019      | CREATE                               | 10123        | A password changer was created                                         |
| PASSWORDCHANGER                | 10019      | EDIT                                 | 10124        | A password changer was edited                                          |
| PASSWORDCHANGER                | 10019      | ENABLE                               | 10125        | A password changer was enabled                                         |
| PASSWORDCHANGER                | 10019      | DISABLE                              | 10126        | A password changer was diasbled                                        |
| PASSWORDCHANGER                | 10019      | COMMANDEDIT                          | 10127        | A command in a password changer was edited                             |
| PASSWORDCHANGER                | 10019      | COMMANDCREATE                        | 10128        | A command in a password changer was created                            |
| PASSWORDCHANGER                | 10019      | COMMANDDELETE                        | 10129        | A command in a password changer was deleted                            |
| PASSWORDCHANGER                | 10019      | AUTHEDIT                             | 10130        | The password changer's authentication method was edited                |
| PASSWORDCHANGER                | 10019      | SCANFIELDEDIT                        | 10131        | The fields the password changer uses from the secret was edited        |
| CHARACTERSET                   | 10020      | CREATE                               | 10132        | A character set was created                                            |
| CHARACTERSET                   | 10020      | EDIT                                 | 10133        | A character set was edited                                             |
| CHARACTERSET                   | 10020      | ENABLE                               | 10134        | A character set was enabled                                            |
| CHARACTERSET                   | 10020      | DISABLE                              | 10135        | A character set was disabled                                           |
| PASSWORDREQUIREMENT            | 10021      | CREATE                               | 10136        | A password requirement was created                                     |
| PASSWORDREQUIREMENT            | 10021      | EDIT                                 | 10137        | A password requirement was edited                                      |
| DOMAIN                         | 10022      | CREATE                               | 10138        | A domain was created                                                   |
| DOMAIN                         | 10022      | EDIT                                 | 10139        | A domain was edited                                                    |
| DOMAIN                         | 10022      | SYNCHRONIZE                          | 10145        | A domain's users were synchronized                                     |
| BACKUPCONFIGURATION            | 10023      | EDIT                                 | 10143        | The back configuration was edited                                      |
