[title]: # (Configuring HSM Integration)
[tags]: # (configuration)
[priority]: # (11)
# Configuring HSM Integration

To configure the HSM integration, go to the __ADMIN__ menu and click __Configuration__, then select the __HSM__
tab. This will start the HSM wizard, which will guide the process of selecting the HSM’s CNG provider.

The list of available CNG Providers is done by querying for the list of registered CNG providers. Each
provider must correctly report that it is a “Hardware” provider, and that it is not a Smart Card reader. If
an error occurs while querying the CNG provider for its properties, it will not appear in the list, however
the error is reported to Secret Server’s system log. If the desired CNG provider does not appear in the
list of CNG providers, ensure that the CNG provider is correctly registered and that IIS has been restarted
after the CNG provider is registered. Also check that an error is not occurring while querying the HSM by
examining the system log.

Once the CNG providers are selected, Secret Server will simulate encryption and decryption operations
and verify the results to check that it is functioning properly. The final step will be to verify the selected
providers, and then enable HSM integration. Detailed steps are provided throughout the HSM
configuration wizard.
