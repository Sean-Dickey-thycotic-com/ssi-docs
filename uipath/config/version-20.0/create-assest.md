[title]: # (Create An Asset)
[tags]: # (asset)
[priority]: # (205)
# Create An Asset

Creating an asset is what unique ties a component of Orchestrator to a Secret within Secret Server. The asset name will later be referenced in Studio/your Robot and the External Name configured in the asset will match the SecretID you created in the previous steps.

1. Create a new Folder. You can do this by clicking the __Tenant__ button then clicking on __Folders__.

   ![Folders](images/5205e8ef4bee978a171621a82e45dfe7.png)
1. Click the __+__ button in the __Manage Folders__ submenu. You can name the folder appropriately and click __Create__.

   ![Create](images/b08aa3911a796c2c2e8d7296eb5d0c3a.png)
1. Create an Asset within the folder. Click on the new folder you created which is now displayed on the left side menu then click __Assets__.

   ![Assets](images/2d24ea79941a641ca94fa36edc2a18d3.png)

1. Click the __+__ button and create a new asset:

    * For the __Asset Name__ – this can be anything. We recommend calling it
        something that either matches your secret name value or can be
        recognized as being associated with that Secret.

    * For __Type__ – choose “Credential”

    * For __Credential Store –__ choose your Secret Server Credential Store

    * Checkmark the __Global Value__ flag and enter in the SecretID that is associated with the Secret you created earlier. The SecretID can be retrieved in the URL

   ![Global Value](images/be7e6f90e33047e0aa601132d1be23e3.png)
1. Once all information is filled out, click __Create__ at the bottom.

   ![Create](images/84573094a6f9101fab9ee7ca1db8b1de.png)

   ![Create](images/a15c58b99b69e1d2ebfc4a9d8719e8a3.png)