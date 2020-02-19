[title]: # (Secret Server Tuning)
[tags]: # (tuning)
[priority]: # (4)
# Secret Server Tuning

Consider not allowing duplicative Secret Names within your Secret Server environment to mitigate issues with the integration. If you are allowing duplicative Secret Names, we recommend making sure that there are no duplicative secrets for the specific secrets you intend to integrate. The integration will not be able to determine which Secret to use since the integration is based entirely on the Secret name field.

## Scalability

Tenable’s integration is using SOAP API calls and will make three API calls per scanner. These calls are Authenticate, SearchSecretsByExposedValues, and GetSecret. Tenable has a 5 second timeout when making these API calls. Out of box IIS can only process ~5,000 simultaneous inbound requests. These API responses are slow and are measured in seconds. A large inbound volume of these calls can overwhelm Secret Server.

If you intend to integrate many Secrets with Tenable, there are several main areas that should be considered

* Adjust Secret Server’s IIS to handle a larger volume of API requests
* Decrease the number of concurrent systems in the Active Scan
* Decrease the values for Scan specific settings
* Consider creating dedicated Secret Server web servers that are utilized just for API use cases like Tenable

## Adjust Secret Server’s IIS to handle a larger volume of API requests

IIS is very configurable, but the out of the box settings will only allow a maximum of 5,000 simultaneous connections to Secret Server.  

__Configuration Settings__ 

|  Property |   | File  |
|---|---|---|
|  appConcurrentRequestLimit |   | C:\Windows\System32\inetsrv\config\applicationHost.config  |
| maxConcurrentRequestsPerCPU  |   | C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Aspnet.config  |
|  RequestQueueLimit |   | C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config\machine.config  |
|   |   |   |

>**Note:** The .NET Framework version on your system might be different than v4.0.30319.

__Configuration Values__

| Property  |   | Default  | New  |
|---|---|---|---|
|  appConcurrentRequestLimit |   | 5,000  | 100,000  |
|  maxConcurrentRequestsPerCPU |   |  5,000 |  100,000 |
| requestQueueLimit  |   |  5,000 | 100,000  |
|   |   |   |   |

__appConcurrentRequestLimit__ 

The property is defined in  
`C:\Windows\System32\inetsrv\config\applicationHost.config
<system.webServer>
  <serverRuntime appConcurrentRequestLimit="5000" />
</system.webServer>`

