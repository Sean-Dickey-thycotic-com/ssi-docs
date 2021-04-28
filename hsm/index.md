[title]: # (HSM)
[tags]: # (introduction)
[priority]: # (1)
# HSM

Secret Server integrates with hardware security modules, or HSMs, to provide additional security of
Secret Server’s encryption key. When Secret Server is configured to use an HSM, the encryption key is
protected by the HSM. HSMs offer several security features that traditional servers cannot. Depending
on the model and design of the HSM, most HSMs are designed to be physically tamper-proof. HSMs may
also be independent hardware that are on a network, which allows physically placing the HSM is a more
secure location that might otherwise be too inconvenient for a server.
To provide broad support for HSMs, Secret Server supports any HSM that can be configured with
Microsoft’s Cryptography Next Generation provider, or CNG. CNG is a layer provided by Windows Server
2008 and later that HSM manufacturers can interface with. If your HSM properly supports CNG and
supports the right algorithms, Secret Server will be able to utilize your HSM.
CNG provider installation and configuration varies from HSM to HSM, however, documentation is
available from each HSM vendor on how to correctly install CNG providers.