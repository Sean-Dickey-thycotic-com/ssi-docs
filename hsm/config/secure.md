[title]: # (Securing HSM Integration)
[tags]: # (secure)
[priority]: # (12)
# Securing HSM Integration

The wizard to enable and disable HSM integration is protected by the “Administer HSM” role permissions
in Secret Server. These permissions should be carefully assigned – if at all. Additionally, an Event
Subscription can be created that sends alerts when this role permission is assigned or unassigned from
a role.

Configuring the HSM also has its own Event Subscriptions for when the HSM integration is enabled or
disabled.

Additionally, an application setting can be added to Secret Server to prevent changes to HSM
configuration. Disabling and enabling this requires direct access to the file system where Secret Server
is installed.

To enable this, edit the `web-appSettings.config` file within Secret Server to contain a key called
__LockHsmConfiguration__ with a value of True as follows:

``` 

<?xml version="1.0" encoding="utf-8" ?>
<appSettings>
 <add key="LockHsmConfiguration" value="True" />
</appSettings>

```

This will prevent access to the HSM configuration pages regardless of role permissions. The only way to
gain access is to remove this setting, thus proving you at least have access to the server where Secret
Server is installed.
