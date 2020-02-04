[title]: # (Template Root File)
[tags]: # (introduction)
[priority]: # (1)
[display]: # (none)
# Template Root File

<!-- 
The int-template folder contains the template structure and template files for integration documents.

1. Make a copy of the template folder at the root of the integration repo.
1. Rename the folder to reflect the actual integration product name, e.g. okta-for-saml.md. Use lowercase and hyphens for the names.
1. Each folder requires an index.md file.
1. The metadata tag `[display]: # (none)` needs to be removed or changed to `[display]: # (all)` once real contents is created and ready for publication.
1. Each contents section needs an images folder if screen captures are part of the markdown files. Refer to the Okta for SAML folder to see an example on where/when the images folder is required. We cannot stage a template structure with images folders in place, empty folders cannot be committed into a repo.
1. This index file becomes the introduction/overview page for the integration.
1. Some topics are optional at this point and should only be filled in if information is readily available:

  * consider-architecture.md
  * consider-implementation.md
  * troubleshooting.md

1. The priority metadata tag determines the order of the TOC outline. For the files in the template that order is established. If a new file is added, adjust priority numbers accordingly to have the new .md file at the correct place in the TOC. 
-->