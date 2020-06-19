[title]: # (Default Installation)
[tags]: # (default, installation)
[priority]: # (3)
# Default Installation

1. Download the installer file at https://downloads.ss.thycotic.com/integrations/SCIMSetup.exe.
1. Using Local Administrator credentials, run the installation file.
1. Select (the … button) or type the installation folder.
1. Click the Licenses terms and conditions link to review the license terms.
1. Click to select the I agree to the License terms and conditions check box. The Install button becomes enabled.
1. Click the Install button. The installation begins, and the following actions occur:
   * The Install files are installed on the system.
   * The application pool is configured.
   * The IIS web application is configured.
   * A self-signed certificate is added to the certificate store (for encryption purposes).
   * IIS is restarted.
1. The first user to register is automatically approved to access the Thycotic SCIM Connector. Additional users can be registered to access the SCIM Connector later, but these other accounts require approval (from within the SCIM Connector application itself) before access is granted.

   >**Note:** The URL for the Sign in page is to localhost/SCIMConnector/.

1. Click the Sign In button. The SCIM Connector interface appears:
1. Click the Settings menu item on the left. The Settings tab appears:
