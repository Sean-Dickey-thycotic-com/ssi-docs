[title]: # (Troubleshooting)
[tags]: # (introduction)
[priority]: # (500)
# Troubleshooting

The most common script errors are configuration based, such as users without
permission to update sites or query credentials from SS. To troubleshoot:

-   Ensure secrets have the same name in Nexpose and in SS. (IP address or short
    name hostname only for secret name and machine name.)

-   Ensure the cited Nexpose user can save sites and start scans.

-   If issues still exist, email <support@rapid7.com>.

![A screenshot of a cell phone Description automatically generated](images/9aa6773456754928fc942092f6ef5edb.png)

-   The encryption.config file mentioned at the bottom of the configuration file
    does not reference Thycotic’s encryption.config file, nor does it need
    copied to the location specified for this integration to work.

-   Ensure the nexpose_url reflects the actual IP address assigned to the
    network adapter attached to the system running the script and not a
    localhost value.

-   If issues still exist, email support\@rapid7.com.