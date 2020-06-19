[title]: # (Constraints)
[tags]: # (constraints)
[priority]: # (4)
# Known Constraints and Limitations

## Special Considerations

If the SCIM endpoints do not make changes to secrets, users, groups or group membership, consider using these permissions:

   * Administer Reports
   * View Folders
   * View Groups
   * View Reports
   * View Secret
   * View Users

Once the role has been created, you can assign the application account to the newly created role.

## SailPoint Integration Concepts and Limitations

This section reviews any SailPoint-specific limitations.

   * In SailPoint IdentityIQ, there are “containers” and “privileged data.” The containers map to SS folders, and privileged data maps to secrets.
   * SailPoint allows adding permissions to containers, but they cannot be directly added to privileged data. That is, they cannot be added directly to a SS secret. So when a user gets access to a container, the user is really getting access to a SS folder.
   * While there is no direct way to give users access to a specific secret, they can still be given access indirectly by adding a user into a group that already has access to both the folder/container and the secret/privileged data.
   * When a users are given access to a container/folder, either with direct access or by adding them to a group, they only have "view” access to the container. More granular assignment of permission levels can only be defined in SS.
   * If the “view” permission setting seen in the Configuring a “SailPoint IdentityIQ Endpoint” section is not configured correctly, an incorrectly formatted POST call to the SCIM Connector application will result, which returns a HTTP 400 error message.
   * Any sensitive information that is associated with a secret/privileged data, such as a password, is not shared over the SCIM Connector and must be viewed in SS.
   * Personal folders in SS can be viewed in SailPoint, but users cannot be given direct access to the folders. However, users can be given access by adding them to an existing group. The owner of the personal folder cannot have their access removed from the folder.
   * Using custom attributes or extensions with SailPoint IdentityIQ and the SCIM Connector is not currently supported.
