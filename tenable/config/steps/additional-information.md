[title]: # (Additional information)
[tags]: # (tuning)
[priority]: # (4)
# Additional information

![Additional Information](images/ref1.png)

__maxConcurrentRequestsPerCPU__

The property is defined in

`C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Aspnet.config
<system.web>
  <applicationPool maxConcurrentRequestsPerCPU="5000"
</system.web>"`

![Additional Information](images/ref3.png)

__requestQueueLimit__

The property is defined in  

`C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config\machine.config
<system.web>
  <processModel requestQueueLimit="5000" />
</system.web>`

![Additional Information](images/ref6.png)