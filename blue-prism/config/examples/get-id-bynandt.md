[title]: # (GetIdByNameAndTemplate)
[tags]: # (getidbynameandtemplate)
[priority]: # (203)
# GetIdByNameAndTemplate

This method searches for a Secret ID using the Secret Name and Template ID.

*REST API
URL* /api/v1/secrets?filter.searchField=name&filter.secretTemplateId=\<templateID\>&filter.searchText=\<search
name\>

Please see the settings below for the input parameters:

`<secret name>` search value, secret name string

`<TemplateID>` restricted template for search, number TemplateID

   * __CredentialName__: Credential name where the store accesses the parameters.

   * __Property username__: Accesses parameters store in the credential vault for Blue Prism

   * __Property password__: Accesses parameters store in the credential vault for Blue Prism

   * __Property server_url__: Accesses parameters store in the credential vault for Blue Prism

Please see the settings below for the output parameters:

Please see the settings below for the output parameters:

   * __Collection Secret Model__: Where key collection ID secret.

__Scheme__

   ![GetUsernameById](../images/8.png)