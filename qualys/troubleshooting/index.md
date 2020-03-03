[title]: # (Troubleshooting)
[tags]: # (introduction)
[priority]: # (500)
# Troubleshooting

If the authenticated scan is failing, or isn’t finding the Secret there are a
few settings to check to make sure the integration is configured correctly:

__Are web services enabled?__

Web services in Secret Server must be enabled for this integration to function. Check the web services status from the __Configuration__ section of the __Administration__ menu.

__Is Secret Server accessible?__

The URL defined when setting up the authentication vault must be accessible by the Qualys appliance. Ensure proper DNS settings and firewall rules are in place to allow access from the appliance to Secret Server web services.

__Are permissions and security settings configured correctly?__

The Qualys user needs at least read access to the Secret.

   >**Note:** If certain security settings are in place, such as Approval for Access, and Hide Launcher Password the user will need elevated access. Other settings such as DoubleLock will prevent the Qualys account from accessing the Secret. If a Secret is configured for Check Out, Secret Server will automatically check out the Secret to the Qualys user.

__Check audit trails__

To help determine whether the Qualys account is correctly accessing Secret Server and the stored credential, check the audit on the Qualys user to see if it is logging in successfully from the appliance and view the audit on the Secret to see if there are view records which will show that the Secret was
actually accessed.

__BEST PRACTICES__

__Folders__

Permissions in Secret Server are similar to NTFS, and are assigned at the Secret or folder level. To make maintenance simple going forward, a standard model is to place all the credentials needed for scanning in a separate folder that the
security team can manage. Give the Qualys Secret Server account read-only access to the folder and it will automatically gain access to new credentials added to the folder for scanning. In the example screenshots in this guide, the scanadmin
Secret is placed in the Scan Credentials folder, which an admin and the Qualys user account have access to.

__Groups__

If there are multiple authentication vaults set up in Qualys with separate user accounts for accessing Secret Server, it is recommended to assign all of them to a local Secret Server group to simplify permission management moving forward.

__SSL__

Ensure that Secret Server is configured to force connections over HTTPS. This can be verified by clicking the __Security Hardening__ tab from the __Reports__ section of Secret Server.

__IP Address Restrictions__

Secret Server allows whitelisting of IP address ranges to restrict where accounts can log in from. For the Qualys Secret Server account, it is recommended to only allow it access from the Qualys agent appliance to help prevent misuse of the account.

__Event Subscriptions / SIEM__

Configure email or SIEM alerts to get notified if the Qualys account gets locked out of fails to login to the vault. This can indicate the password was updated in Active Directory or Secret Server without updating the Qualys Authentication Vault record. For more information on alerts refer to the user guide and the
syslog integration guide.
