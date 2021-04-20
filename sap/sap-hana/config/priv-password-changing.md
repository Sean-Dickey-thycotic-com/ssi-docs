[title]: # (Privileged Password Changing)
[tags]: # (password)
[priority]: # (104)
# Privileged Password Changing

If the account whose password we need to change does not have the ability to change its own password, this function will need to be performed another “associated” account that does have the ability to change the password on the users behalf. We will need an additional password changer for this.

1. Head to __Admin | Remote Password Changing_ and create a new password changer called “SAP HANA Privileged Password Changer” and use the password changer created in the previous section as the base password changer.
1. Edit the password changer (Click Edit) and update the connection string to as follows:

   `DRIVER={HDBODBC};UID=$[1]$USERNAME;PWD=$[1]$PASSWORD;SERVERNODE=$SERVER`

   >**Note:**  the `$[1]` that precedes the username and password now. This denotes an “associated” Secret, and must be an account that has privileges that allow it to change passwords on other users’ behalf.

   ![tag](images/10.png)
1. Edit the __Verify Password Changed Commands__ to as follows:

   `VALIDATE USER $USERNAME PASSWORD "$PASSWORD"`

   The Password Change commands can stay as they were previously.

   ![tag](images/11.png)

1. Create a Secret Template that utilises the password changer “SAP HANA Privileged Password Changer” (see the previous section for details, instead of the standard SAP HANA Password Changer,
ensuring that the password requirements are still set to “SAP”.

1. Create a Secret with the new Secret Template and head to the __RPC__ tab. Add an associated Secret that has privileges to change the password on behalf of the user that is listed in the Secret that you are
manipulating. Note that the associated Secret order number must match the integer in the connection string as noted in __Step 2__ (ie `$[1]`).

   ![tag](images/12.png)
1. Perform a privileged password change.
