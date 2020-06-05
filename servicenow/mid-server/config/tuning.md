[title]: # (Tuning)
[tags]: # (introduction)
[priority]: # (3)
# Tuning Configurable Options

It may be required for you to adjust the field mappings file to fit your
individual needs. If you open tss-credential-resolver-1.0.jar with winzip/winrar
you will notice the following folder structure:

![](images\cc7618007aaef06512869476029b86bb.png)

You can edit the tss-credential-resolver-field-mappings.json file. This is as
simple as ensuring once the pattern mapping file is modified, you re-zip the
files/folders, then rename the new zip file to .jar. You can then upload the
modified .jar file to ServiceNow.

![](images\690fddc76da3e877672c537dcf95cd07.png)

The top-level items are ServiceNow templates, not Secret Server templates. Each
ServiceNow template is matched against the mappings for it, so a ServiceNow
“snmpv3” secret for example can be mapped to any secret in Secret Server that
contains the five items (fields) underneath of it. The sub-fields for each
top-level item will need to match the Secret Server field to the ServiceNow
template field. If you’re using a template in Secret Server that is customized
or based initially from one of these templates, you need to ensure your custom
field values map to the ServiceNow field values. If you are using custom fields,
ensure that these fields map to the appropriate SerivceNow fields. Example:

“windows”: {

[SecretServerField] “machine” : [ServiceNowField] “domain”

If you attempt to use a ServiceNow template that isn’t explicitly mentioned in
the mappings, then the \* mapping will take over and tries to map the fields
“username” and “password” on the Secret Server side to the “User” and “pswd”
field on the ServiceNow side
