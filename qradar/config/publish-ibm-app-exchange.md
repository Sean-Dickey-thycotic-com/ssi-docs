[title]: # (How to Publish to IBM App Exchange)
[tags]: # (introduction)
[priority]: # (106)
# How to Publish to IBM App Exchange

There are four key steps to get your zip ready for submission using the App Submission portal. All extensions published to the IBM Security App Exchange must include a manifest.txt and must be signed by your IBM issued certificate.

Your extension will not pass validation unless these have been included.  

## Requirements

1. Export your content from your QRadar system
1. Add a customized manifest.txt to the extension
1. Generate and submit a Certificate Signing Request (CSR)
1. Sign your extension
1. Subsequent extension submissions and updated versions

## Step 1: Exporting your extension or content from Qradar

1. To search for your DSM using the ContentManagement Tool

   Enter in the following command:

   `[root\@qradar \~]\# /opt/qradar/bin/contentManagement.pl --action search --content-type 24 --id all --regex "\\w" \|grep Secret`

   ![](images/a301e9fb778a475bc449e3d9b4e66254.png)

1. To export everything and the custom mappings related

   Enter in the following command:

   `[root\@qradar \~]\# /opt/qradar/bin/contentManagement.pl -a export -c all`

   `/opt/qradar/bin/contentManagement.pl -a export -c sensordevicetype -i 4001`

## Results

   ![](images/c4cdc4f2d5e27d2805bdc294d1c86b02.png)

## Adding a manifest to an extension

   Login to App exchange and Click the “Submission Portal” link in the left menu bar, and follow the submission process. (refer below image)

   ![](images/996167c914ec78ce964b3d098e2b2f2d.png)

## Steps for Submission

1. Click on Add new app.

   ![](images/de8a565e42b9e6c5487042a03091cd3a.png)

1. Enter the details to Add Your New Extension:

   ![](images/558368801bd63a011a2b6396f78e0af1.png)

1. Press Submit.
1. Complete the Extension Details Screen.
 
   ![](images/d311f9b0930228eab9ca192381d3191e.png)

   ![](images/ca870322efdd4f22e033021b93794487.png)

1. Provide Your Graphic Assets (Screen shots, Company Logo, Video).

   ![](images/6fecdd12f4169ec5295f7254431e73f7.png)

1. Supply Testing Information for our Validation Engineers.

   ![](images/e58551d5a9113e8fd850432c847e3937.png)

1. Provide Contact Information.

   ![](images/a724e0187076f159f9dbe93d7c0e1e61.png)

   Preview Your Submission Make sure all information is provided. Submit Your Solution for Validation.

   ![](images/22ad911b88c3c0e2980bfb2b185e957a.png)
