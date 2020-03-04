[title]: # (Constraints)
[tags]: # (introduction)
[priority]: # (3)
# Known Constraints and Limitations

1.  The integration only works with IP address matching and short name (NetBIOS)
    hostnames. You cannot currently supply FQDN values with the integration,
    which implies the scanner nodes are required to resolve short names
    appropriately.

2.  The integration cannot handle specifying CIDR ranges in the site
    configuration within Nexpose/Insight VM. You must have 1:1 mapping.

3.  If a Secret is checked out, an error message appears while running the
    script stating it is unable to access that particular Secret/asset for
    integration. You will receive an indication of which user currently has the
    Secret checked out. This asset will not be added within the authentication
    section of the site configuration in Rapid7.

4.  If utilizing Ruby on Windows, the highest version known to be working with
    integration is 2.5.7-1 with both hostnames and IP addresses. The latest
    version of Ruby for Windows works with IP address matching only.
