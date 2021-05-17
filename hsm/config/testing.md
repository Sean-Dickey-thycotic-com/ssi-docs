[title]: # (Testing HSM CNG Configuration)
[tags]: # (testing)
[priority]: # (14)
# Testing HSM CNG Configuration

Secret Server does its own testing and verification of the HSM and its CNG provider before the HSM
integration can be enabled. To further diagnose any issues with the HSM, the __certutil__ command line
utility that is part of Windows can test the HSM with the __–csptest__ option specified. An example output
may contain something like this:

* __Provider Name:__ SafeNet Key Storage Provider
* __Name:__ SafeNet Key Storage Provider

```
Asymmetric Encryption Algorithms:
 RSA
 BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE -- 3
 NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION -- 4
 NCRYPT_SIGNATURE_OPERATION -- 10 (16)
 NCryptCreatePersistedKey(SafeNet Key Storage Provider, RSA)
 Name: cngtest-6166f8fe-8caf-4e30-8e5c-a-24575

```

__Pass__ 

Examine the output of the test by looking for your CNG Provider Name for your HSM and verifying the
result. It is recommended that this test be run using the same account as the Application Pool Secret
Server is using. If the testing tool reports errors, consult your HSM’s vendor or documentation for
resolution.
