[title]: # (Install IBM Verify Gateway for RADIUS Server)
[tags]: # (install)
[priority]: # (600)
[display]: # (none)
# Install IBM Verify Gateway for RADIUS Server

## Before You Begin

The IbmRadiusInstaller.msi provided with the IBM Verify Gateway for RADIUS is required.

1. Copy the following two files onto the Windows server disk:

   * Setup.exe

   * IbmRadiusInstaller.msi

1. Download and run **VC_redist.x64.exe** from the link in [Prerequisites](#ibm-verify-gateway-for-radius) if not already installed on the system.

1. Run **Setup.exe**.

1. Accept the defaults and complete the Verify Gateway for RADIUS installation. The Windows Server file system contains the following files in the `C:\Program Files\ibm\IbmRadius directory`:

   * cacert.pem

   * cacert.pem.sample cJSON.dll IbmAuthApi.dll IbmRadius.exe IbmRadiusConfig.json

   * IbmRadiusConfig.json.sample IbmRadiusMsg.dll libcurl.dll

   * LIBEAY32.dll SSLEAY32.dll

   * zlib1.dll

A Windows service is set up for IbmRadius.exe titled IBM RADIUS Service. It's not running, and the startup type is set to Manual.

   >**Note:** A license folder is included under the main installation directory. It includes the associated licenses and notices in the supported languages.
