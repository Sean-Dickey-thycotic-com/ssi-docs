[title]: # (Manual Installation)
[tags]: # (manual, installation)
[priority]: # (5)
# Manual Installation

To manually install the SCIM Connector:

1. Download the Installer ZIP file for the SCIM Connector application.
1. Using Administrator credentials, unzip the contents of the ZIP file into the IIS directory. For example, unzip the contents to `C:\inetpub\wwwroot\SCIMConnector`.
1. Navigate to the web.config file, located in the application root directory, and modify the following properties:
   ```
   <add key="CERT_NAME" value="CN={Your Certificate Name}" />
   <add key="LOG_PATH" value=" {Application Root File Path} \Log" />
   ```
1. The certificate that is used in this step is for encryption or decryption with the Configuration.enc file. For this certificate to be valid it must meet the following criteria:

   * It should be added to the machines personal certificate store so all uses on the machine have access. This is not the user’s personal store. After adding it, you should be able to see it in the “Manage Computer Certificates” dialog under __Personal | Certificates__.
   * It should be set for encryption/decryption (which can usually be specified when adding it to the certificate store).
   * __IIS_USRS__ must have read permissions to the certificate. This is usually set for certificates by default.
1. If you don’t want to manually create a certificate, or use an existing one, you can use the following PowerShell command to generate one. This is the same certificate that is generated with the default installer:
   ```
   New-SelfSignedCertificate -Type DocumentEncryptionCert -Subject "CN=SSScim" -Provider "Microsoft Enhanced Cryptographic Provider v1.0" -KeyUsage KeyEncipherment, DigitalSignature -KeyAlgorithm RSA -KeyLength 4096 -CertStoreLocation "Cert:\LocalMachine\My" -NotAfter (Get-Date).AddMonths(36)
   ```
1. Open IIS Manager.
1. Create a new application pool.
1. Right click on the folder under __Default Web Site__ that contains the SCIM Connector files (usually the __SCIMConnector__ folder) and select __Convert to Application__. The Add Application dialog box appears:
1. Click the __Select__ button to choose the application pool that you created.
1. Click to select the __Test Settings__ option to ensure IIS returns “The application pool identity is valid.”
1. Right-click the newly created application (SCIMConnector) and select __Manage Application | Browse__.

>**Note:** The first user to register is automatically approved to access the Thycotic SCIM Connector. Additional users can be registered to access the SCIM Connector later, but these other accounts require approval (from within the SCIM Connector application itself) before access is granted.

1. Open one of the approved browsers and navigate to localhost/SCIMConnector/. A Sign in page appears:
1. Complete the sign in information you entered earlier.
1. Click the __Sign In__ button. The SCIM Connector interface appears:
1. Click the Settings menu item on the left. The Settings tab appears: