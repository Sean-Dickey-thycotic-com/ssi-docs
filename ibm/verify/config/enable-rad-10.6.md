[title]: # (Enable RADIUS Two-Factor Authentication for 10.6)
[tags]: # (enable)
[priority]: # (706)
[display]: # (none)
# Enable RADIUS Two-Factor Authentication in Thycotic Verify Privilege Vault 10.6 version

Verify Privilege Vault allows the use of RADIUS two-factor authentication on top of the normal authentication process for additional security needs.

## Configure RADIUS for the Verify Privilege Vault Instance

1. Sign into an account with Administer Configuration and Administer RADIUS permissions.

1. Navigate to __Administration menu__ | __Configuration__ | __Login__.

1. Enable Verify Privilege Vault with your RADIUS server information by going into edit mode.

   * RADIUS Server IP (IP address to your RADIUS Server)

   * RADIUS Client Port (default 1812)

   >**Note:** If your RADIUS server runs on the same machine as your Verify Privilege Vault, client and server ports must be different.

   * RADIUS Server Port (Default 1812 for RSA and 1812 for AuthAnvil.)

   * RADIUS Shared Secret must match chosen RADIUS shared secret on your RADIUS Server. (Shared Secret is a RADIUS term and not related to any Verify Privilege Vault secret.)

   * RADIUS Login explanation (custom message or instruction) Defaults to Please enter your RADIUS passcode.

1. Click __Save__ after entries are confirmed.
