[title]: # (Package the App)
[tags]: # (introduction)
[priority]: # (106)
# Package the App

Packaging is the final step before uploading your app to Splunkbase. For this,
you take your App directory and compress it into a single file that can be
uploaded to Splunkbase.

Splunkbase uploads are required to have the .spl file extension. For
example: myapp.spl. SPL format is identical
to [.tar.gz](http://en.wikipedia.org/wiki/Tar_(file_format)) format. The only
difference is the file extension.

Make sure you have placed all the app components in the correct location, have
moved all customizations from `\\local to \\default`, and have tested your app
before you package it.

## Additional Information for Splunk App and Secret Server

### Packaging your app for Splunkbase

The final step before uploading your app to Splunkbase is packaging. This means taking your app's directory and turning it into a single compressed file which can be uploaded to Splunkbase. Splunkbase uploads are required to have the .spl file extension, e.g. myapp.spl. SPL format is identical to .tar.gz format. The only difference is the file extension. Make sure you have placed all the app components in the correct location, have moved all customizations from /local to /default, and have tested your app before you package it.

## To move all customizations from \\local” to “\\default

1. Go to `C:\\Program Files\\Splunk\\etc\\apps\\splunkapp\\local`.

   ![Local](images/40d1519cb20cac12e92798b70fbc3e15.png)

1. Copy the data folder.

1. Go to C:\\Program Files\\Splunk\\etc\\apps\\splunkapp\\default.

   ![Default](images/dfdf75700d0718996784e4e121025fa7.png)

1. Paste the data folder. The __Replace or Skip Files__ dialog box appears.

   ![Replace or Skip Files](images/24292c28d5599450bbdfaff7eb156565.png)

1. Click __Replace the file in the destination__.

## To package the app to TAR using 7-Zip

1. Install __7-Zip__ from <http://www.7-zip.org/>.

1. Open __7-Zip__.

   ![7-Zip](images/b85643da5fe5cd5b3ffa929594938f36.png)
1. On 7-Zip file explorer, navigate to the parent directory of your app (for
    example: `c:\\Program Files\\Splunk\\etc\\apps`.

   ![Apps](images/9fa1f828135e633adf72e4e09d3c2069.png)
1. Click the __Add__ icon. The __Add to Archive__ dialog box appears.

   ![Add to Archive](images/c176582e7ff0feffa0118260869ea698.png)

   ![Add to Archive](images/6b10c27e593fd055a5d1af71bb7a9aa8.png)
1. Select the __Archive format__ as tar.

1. Click the ellipsis icon to choose the location where you want to save the TAR file.

   ![Archive format](images/1849d85d1a0c5f7c3c80401f6a5b4a87.png)

   ![Archive format](images/5a80a57633bd98ec4074b49e9940a8aa.png)
1. Click __Open__.

   ![Open](images/688ec4dfbe66b1cbe306f0f59df7fa53.png)
1. Click __OK__.

## To package the app to GZIP using 7-Zip

1. Open __7-Zip__.

1. On 7-Zip file explorer, navigate to the location where you have saved the
    TAR file.

   ![TAR file](images/fd79962c7d575564b2473fb4c007e2f2.png)
1. Select the file.

1. Select the __Archive format__ as gzip.
   ![Archive format](images/95e292850d8306e4a75e69aac133471d.png)

1. Click __OK__.

The App is packaged, and you can upload the App to your Splunkbase.
