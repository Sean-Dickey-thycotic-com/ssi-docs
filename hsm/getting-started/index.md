[title]: # (Requirements)
[tags]: # (requirements)
[priority]: # (2)
# HSM Requirements

Each HSM must provide support for certain algorithms through CNG.

* __RSA__ 4096 – support for RSA with 4096-bit keys is required. The HSM must also support RSA for
encryption and decryption, in addition to signing.
* __PKCS#1 v1.5 Padding__ – The HSM must support PKCS#1 v1.5 padding for RSA encryption.

Additionally, closely follow the requirements and recommendations of the HSM vendor for things such
as minimum latency, redundancy, and operating environment.

Due to limitations of the account, the NETWORK SERVICE account is not supported as an account for the
IIS Application Pool. It is recommended to configure Secret Server’s Application Pool as a service account.

In the advanced settings for the application pool, set "Load User Profile" to true.

>**Note:** Some HSM CNG providers interfere with each other. It is recommended that no more than one
HSM CNG provider is configured on a Windows installation at a time.

## Further Considerations

* If your HSM properly supports CNG and supports the right algorithms
* Each HSM must provide support for certain algorithms through CNG

* Since Secret Server is using Microsoft’s CNG API to communicate with HSMs the following two references should be included:

   * The NCRYPT_IMPL_TYPE_PROPERTY (L"Impl Type") value must be NCRYPT_IMPL_HARDWARE_FLAG (0x00000001, The provider is hardware based).

   https://docs.microsoft.com/en-us/windows/win32/seccng/key-storage-property-identifiers

   * The CNG Algorithm Identifiers must support BCRYPT_RSA_ALGORITHM ("RSA") - The RSA public key algorithm. Standard: PKCS #1 v1.5 and v2.0.

   https://docs.microsoft.com/en-us/windows/win32/seccng/cng-algorithm-identifiers
