[title]: # (Password Changer Creation)
[tags]: # (password)
[priority]: # (102)
# Password Changer Creation

Now we will head to Thycotic Secret Server and create the password changer within the solution that we will leverage to make password changes on SAP HANA databases.

1. Open Secret Server with sufficient administrative privileges. Head to __Admin | Remote Password Changing__.
1. Click __Configure Password Changers__. Scroll to the bottom of the page and click __New__.
1. We want to Select the Generic ODBC (Datasource) as the base password changer. Give the password changer a name (like SAP HANA Password Changer) and then click __Save__.

   ![tag](images/3.png)
1. Press on the __Edit__ button and you will need to enter the Connection String as follows:

   `DRIVER={HDBODBC};UID=$USERNAME;PWD=$PASSWORD;SERVERNODE=$SERVER`

   ![tag](images/4.png)

   Or (depending on requirements for optional specifying of the database):
   `DRIVER={HDBODBC};UID=$USERNAME;PWD=$PASSWORD;SERVERNODE=$SERVER;DATABASENAME=$DATABASE`

   >**Note:** It is also possible to create a separate password changer that uses the database context as well, if required. These must be separate password changers and cannot be “optionally” used together.

1. Return to the password changer main screen and click __Edit Commands__.
1. Set the Verify Password Changed Commands as a command that the user will have privilege to run,
should they be successfully logged on to the database instance.

   ![tag](images/5.png)

The example given here is:

   `SELECT * FROM SYS.M_DATABASES`

This command can, however, be modified depending on the permissions that the user will (or will not) have on the database instance itself. This can also be left blank, if native connector verification is to be
used and a command not tried on the database itself (not as recommended as a verification method).

The password change commands are:

   `ALTER USER $USERNAME PASSWORD "$NEWPASSWORD"`
