[title]: # (SAP Hana)
[tags]: # (introduction)
[priority]: # (1)
# SAP Hana – Database Password Changing (ODBC) 

This document is a guide to performing privileged password rotation for __SAP’s HANA__ database type. The password changing mechanism leverages the in-built ODBC connector for Thycotic Secret Server and can also be easily adapted to other database types that make use of ODBC drivers for password changing. This document assumes an intermediate level knowledge of Secret Server function and makes some
assumptions about the availability of components – for example, the installation of the SAP HANA ODBC driver itself is not covered and is assumed available.