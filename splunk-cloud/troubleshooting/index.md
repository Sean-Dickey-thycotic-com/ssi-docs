[title]: # (Additional Information)
[tags]: # (introduction)
[priority]: # (500)
# Additional Information for Splunk App and Secret Server

## Packaging your app for Splunkbase

The final step before uploading your app to Splunkbase is packaging. This means taking your app's directory and turning it into a single compressed file which can be uploaded to Splunkbase. Splunkbase uploads are required to have the .spl file extension, e.g. myapp.spl. SPL format is identical to .tar.gz format. The only difference is the file extension. Make sure you have placed all the app components in the correct location, have moved all customizations from /local to /default, and have tested your app before you package it.

## Using 7-Zip

To package the Splunk App using 7-Zip, follow these steps:
1. Install 7-Zip from http://www.7-zip.org/.
1. Open 7-Zip.
1. Navigate 7-Zip's file explorer to the parent directory of your app (for example c:\Program Files\Splunk\etc\apps).
1. Select your app's folder in the left pane of 7-Zip.
1. Click "Add" (the green plus sign) on 7-Zip's toolbar.
1. An "Add to Archive" dialog box will come up.
1. Choose "tar" from the "Archive Format" dropdown box. The filename shown in the "Archive" textbox should change to have a ".tar" file extension.
1. Click the "..." button in the upper-right-corner to choose a location for your temporary tar file outside the Splunk Enterprise Program Files folders, because you won't want these files cluttering up your actual Splunk Enterprise install.
1. Click OK to create the .tar file
1. Now it's time to zip up the .tar file into a .tar.gz. Back in 7-Zip's main UI, select the .tar file you created in the previous step
1. Click the "Add" button in the toolbar
