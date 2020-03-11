[title]: # (Package the App)
[tags]: # (introduction)
[priority]: # (108)
# Package the App

Step Three: Packaging the App
-----------------------------

Packaging is the final step before uploading your app to Splunkbase. For this,
you take your App directory and compress it into a single file that can be
uploaded to Splunkbase.

Splunkbase uploads are required to have the .spl file extension. For
example: myapp.spl. SPL format is identical
to [.tar.gz](http://en.wikipedia.org/wiki/Tar_(file_format)) format. The only
difference is the file extension.

Make sure you have placed all the app components in the correct location, have
moved all customizations from \\local to \\default, and have tested your app
before you package it.

**To move all customizations from “\\local” to “\\default”:**

1.  Go to C:\\Program Files\\Splunk\\etc\\apps\\splunkapp\\local.

    ![](images/40d1519cb20cac12e92798b70fbc3e15.png)

2.  Copy the data folder.

3.  Go to C:\\Program Files\\Splunk\\etc\\apps\\splunkapp\\default.

    ![](images/dfdf75700d0718996784e4e121025fa7.png)

4.  Paste the data folder. The **Replace or Skip Files** dialog box appears.

    ![](images/24292c28d5599450bbdfaff7eb156565.png)

5.  Click **Replace the file in the destination**.

    **To package the app to TAR using 7-Zip:**

6.  Install **7-Zip** from <http://www.7-zip.org/>.

7.  Open **7-Zip**.

    ![](images/b85643da5fe5cd5b3ffa929594938f36.png)

8.  On 7-Zip file explorer, navigate to the parent directory of your app (for
    example: c:\\Program Files\\Splunk\\etc\\apps).

    ![](images/9fa1f828135e633adf72e4e09d3c2069.png)

9.  Click the **Add**

    ![](images/c176582e7ff0feffa0118260869ea698.png)

    icon. The **Add to Archive** dialog box appears.

    ![](images/6b10c27e593fd055a5d1af71bb7a9aa8.png)

10. Select the **Archive format** as tar.

11. Click the ellipsis

    ![](images/1849d85d1a0c5f7c3c80401f6a5b4a87.png)

    icon to choose the location where you want to save the TAR file.

    ![](images/5a80a57633bd98ec4074b49e9940a8aa.png)

12. Click **Open**.

    ![](images/688ec4dfbe66b1cbe306f0f59df7fa53.png)

13. Click **OK**.

    **To package the app to GZIP using 7-Zip:**

14. Open **7-Zip**.

15. On 7-Zip file explorer, navigate to the location where you have saved the
    TAR file.

    ![](images/fd79962c7d575564b2473fb4c007e2f2.png)

16. Select the file.

17. Select the **Archive format** as gzip.

    ![](images/95e292850d8306e4a75e69aac133471d.png)

18. Click **OK**.

    The App is packaged, and you can upload the App to your Splunkbase.