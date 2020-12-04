[title]: # (Configuration)
[tags]: # (introduction)
[priority]: # (100)

# Configuring MID Server Agent

## Create MID Server JAR File

1. Access your ServiceNow portal
1. Navigate to **MID Server | JAR Files**
1. Click the **New** button
1. Click the **paperclip** on the top right
1. Click **Choose file** in the **Attachments** prompt
1. Locate the JAR file you downloaded from [Thycotic/service-now-credential-resolver](https://github.com/thycotic/service-now-credential-resolver)
1. Click **Open** to upload the file
1. Click the **X** to close the **Attachments** prompt
1. Enter the below details:
   * Name: **Thycotic Credential Resolver**
   * Source: **https://github.com/thycotic/service-now-credential-resolver**
1. Click **Submit** (or **Update**)

### Verify Agent download

Once you have submitted the JAR file through ServiceNow, your MID Servers will pull the file. You can verify the file has been downloaded by checking the `extlib` directory within your agent's root path.

> **Note**: If updating the file, verify the modified date changes to the current day's timestamp.

# Edit Agent Config

The `config.xml` file will be modified to add additional elements for the credential resolver's parameters. These are added at the end of the file just before the closing tag `</parameters>`. Follow the steps below for updating the config file:

1. Edit the `config.xml` configuration file for your MID Server
1. Copy and paste the associated contents (_based on the mode chosen_) just before the `</parameter>` tag at the end of the file
1. Adjust the values accordingly
1. Save the config.xml and close your editor
1. Navigate to **MID Server | Servers** in the ServiceNow portal
1. **Restart** the MID Server that was just updated

## Just-In-Time Mode

| Attribute | Value Description |
| --------- | ----------------- |
| `ext.tss.url` | URL for your Secret Server |
| `ext.tss.oauth2.username` | Secret Server User Account for API access |
| `ext.tss.oauth2.password` | Secret Server User Account password |
| `ext.tss.allow.self_signed_certificate` | Set to `true` if you are using a self-signed cert for Secret Server instance |

Content to copy/paste into the `config.xml` file:

```xml
   <parameter name="ext.tss.url" value="<replace>" />
   <parameter name="ext.tss.oauth2.username" value="<replace>" />
   <parameter name="ext.tss.oauth2.password" value="<replace>" />
   <parameter name="ext.tss.allow.self_signed_certificates" value="false" />
```

## Grant File Mode

| Attribute | Value Description |
| --------- | ----------------- |
| `ext.tss.url` | URL for your Secret Server |
| `ext.tss.oauth2.grant_file` | Path to the file, recommended to write this file to the agent directory |
| `ext.tss.allow.self_signed_certificate` | Set to `true` if you are using a self-signed cert for Secret Server instance |

Content to copy/paste into the `config.xml` file:

```xml
   <parameter name="ext.tss.url" value="<replace>" />
   <parameter name="ext.tss.oauth2.grant_file" value="oauth2_grant.json" />
   <parameter name="ext.tss.allow.self_signed_certificates" value="false" />
```

### Scheduled Task

The recommended method for generating the grant file is utilizing a Scheduled Task. A task can be used to run a PowerShell script that requests a token using the `oauth2/token` endpoint or using the `tss` utility with the [Secret Server Client SDK](<!-- Need short URL for SDK page -->).

Save one of the scripts below to a desired location on the agent server, and then configure a task to call each one. The frequency that each one will be triggered should be based on the **Webservices session timeout** value for Secret Server (e.g., set to 20 minutes, would recommend triggering the task every 19 minutes ).

#### refresh-oauth2.ps1

> **Note:** To provide a more secure method for the username/password required for the OAuth2 endpoint, a password file is utilized where the value is encrypted. Note that this process is unique to a MID Server. It must be created individually on each MID Server.

Issue this command to create the password file:

```PowerShell
 'replace with the password' | ConvertTo-SecureString -AsPlainText -Force | Export-Clixml -Path c:\Thycotic\passfile.XML
 ```

```powershell
param(
    [string]$SecretServerUrl,
    [string]$User,
    [string]$PasswordFile,
    [string]$Path
)
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12

$password = Import-Clixml -Path $PasswordFile
$plainTextPwd = [Runtime.InteropServices.Marshal]::PtrToStringAuto([Runtime.InteropServices.Marshal]::SecureStringToBSTR($password))

$body = @{
    "grant_type" = "password"
    "username" = $User
    "password" = $plainTextPwd
}

$value = Invoke-RestMethod -Method POST -Uri "$SecretServerUrl/oauth2/token" -Body $body | Select-Object -Expandproperty access_token
Set-Content -Path $Path -Encoding Ascii -Force -Value $value -NoNewline
```

Example argument for task:

```powershell
-NoProfile -ExecutionPolicy Bypass -Command "C:\Thycotic\refresh-oauth2.ps1 -SecretServerUrl 'https://enterprisevault.com/SecretServer' -User midapp -PasswordFile 'C:\Thycotic\passfile.xml'"
```

#### refresh-oauth2_useSDK.ps1

```powershell
[cmdletbinding()]
param(
    [string]$Path,
    [string]$SdkPath
)
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12

if (Test-Path $SdkPath) {
    Set-Location $SdkPath
} else {
    throw "Unable to find SDK Path: $SdkPath"
}

if (Test-Path '.\tss.exe') {
    try {
        $value = .\tss.exe token
    } catch {
        throw "Unable to obtain token: $($_.Exception.Message)"
    }
}

Set-Content -Path $Path -Encoding Ascii -Force -Value $value -NoNewline
```

Example argument for task:

```powershell
-NoProfile -ExecutionPolicy Bypass -Command "C:\Thycotic\refresh-oauth2_useSDK.ps1 -Path C:\ServiceNow\prod\agent\oauth2_grant.json -SdkPath C:\Thycotic\secretserver-sdk-1.4.1-win-x64"
```

## Secret Server SSL

> **Note:** The following applies to on-premises installations of Secret Server

Suppose your certificate for the Secret Server site is published from an internal Active Directory Certificate Authority (CA). In that case, that certificate needs to be added to the MID Server Agent's local Keystore for Java.

ServiceNow has documented the method for adding the certificate and can be found [here](https://docs.servicenow.com/search?q=Add+SSL+certificates+for+the+MID+Server&facetreset=yes). The following provides a few details that are not included by ServiceNow.

1. Download your SSL certificate for Secret Server to the MID Server.
1. Open a PowerShell prompt and set the location to the Java bin directory: `<fullAgentPath>\jre\bin`
1. Run the following command, replacing with your environment specifics:

```powershell
.\keytool.exe -import -alias <cert alias> -file <full path to *.cer file> -keystore '<fullAgentPath>\jre\bin\security\cacerts'
```

> **Note:** You will be prompted to provide the password for the Keystore. If this has not been altered previously, it will be `changeit`.

> **Note:** The second prompt will be if you trust the certificate being imported.
