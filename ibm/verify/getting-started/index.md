[title]: # (Prerequisites)
[tags]: # (prerequisites)
[priority]: # (500)
# Prerequisites

## Operating System Requirements

* Windows Server 2012 through Windows Server 2016, 64-bit.

## System Requirements

* Minimum Windows Server OS requirements specific to the actual OS version.

## Network Requirements

* v Port 443 open to the IBM Security Verify tenant address – TLS.

* v Port 1812 inbound from RADIUS Client server's UDP. Communication over UDP between the IBM Verify Gateway for RADIUS and the RADIUS client must be through the configured RADIUS server port. The default RADIUS server port is 1812.

## VC_redist.x64.exe

* Microsoft Visual C++ 2017 Redistributable (x64) version 14.14.26429.

* This file can be obtained directly from the [MSDN web site](https://go.microsoft.com/fwlink/?LinkId=746572).

## Microsoft .NET Framework 4.6.1

* If not installed, the IBM Verify Gateway for RADIUS installer (setup.exe) automatically initiates the download of the Microsoft .NET Framework from the Microsoft website.
