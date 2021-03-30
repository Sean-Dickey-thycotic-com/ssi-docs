[title]: # (How to Export Event Mappings)
[tags]: # (introduction)
[priority]: # (105)
# How to export the event mappings along with the Custom DSM

**After Creating your QIDmap entries, you can map them to your events using the
DSM editor and export them via the export option.**

1. Navigate and login to __Qradar__.
1. Click on __Admin__.  

    ![](images/712c5b9b62bc2dcf480f7bfa7ffcb75d.png)
1. Click on the __DSM editor__ option.
1. Select the created log source, search for __"Thy"__.

    ![](images/updatedimage.png)
1. Click on __Select__.

1. Click on __Export.__  

    ![](images/2352e52b47becaa503a7bcb700593c36.png)
1. Enter in the required details.
1. Click on __Export__.

    ![](images/caae05fd9b51484ae9f17b40f00a23aa.png)
1. The zip will be downloaded.

    ![](images/2335cf3deff6f17c3c77db18efe104e3.png)

## To search for your DSM using the ContentManagement Tool

__Enter in the following command:__

   `[root\@qradar \~]\# /opt/qradar/bin/contentManagement.pl --action
search --content-type 24 --id all --regex "\\w" \|grep Secret`

   ![](images/a301e9fb778a475bc449e3d9b4e66254.png)

## To export the custom mappings

__Enter in the following command:__

   `[root\@qradar \~]\# /opt/qradar/bin/contentManagement.pl -a export -c all`

   `/opt/qradar/bin/contentManagement.pl -a export -c sensordevicetype -i 4001`

## Result

   ![tag](images/c4cdc4f2d5e27d2805bdc294d1c86b02.png)
   ![tag](images/72ee84c17eac16402705341cb1ad374a.png)

1. Rename the zip file to `MyExport.zip`.

1. On the new Qradar install, copy the .zip file and reimport it.

   __Enter in the following command:__

   `[root\@qradar \~]\# /opt/qradar/bin/contentManagement.pl --action import --file MyExport.zip`
