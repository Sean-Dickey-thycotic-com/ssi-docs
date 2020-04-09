[title]: # (How to Export Event Mappings)
[tags]: # (introduction)
[priority]: # (105)
# How to export the event mappings along with the Custom DSM

**After Creating your QIDmap entries, you can map them to your events using the
DSM editor and export them via the export option.**

1. Navigate Login to Qradar and click on Admin  

    ![](images/712c5b9b62bc2dcf480f7bfa7ffcb75d.png)
1. Click on DSM editor option and select created log source i.e SecretServer in our case**  

    ![](images/29061db7ce75bdd0d249fff45f92f6b6.png)
1. Click on Select.

1. Then click on Export option**  

    ![](images/2352e52b47becaa503a7bcb700593c36.png)
1. Enter the details and click on Export button.

    ![](images/caae05fd9b51484ae9f17b40f00a23aa.png)
1. Zip will be downloaded.

    ![](images/2335cf3deff6f17c3c77db18efe104e3.png)

   __You create a custom DSM, and map new events to it using the DSM Editor, lets call it "SecretServer"__.

## To search for your DSM using the ContentManagement Tool

Enter in the following command:

   `[root\@qradar \~]\# /opt/qradar/bin/contentManagement.pl --action
search --content-type 24 --id all --regex "\\w" \|grep Secret`   

   ![](images/a301e9fb778a475bc449e3d9b4e66254.png)

## To export everything and the custom mappings related

Enter in the following command:

   `[root\@qradar \~]\# /opt/qradar/bin/contentManagement.pl -a export -c all`

   `/opt/qradar/bin/contentManagement.pl -a export -c sensordevicetype -i 4001`

## Result

   ![](images/c4cdc4f2d5e27d2805bdc294d1c86b02.png)

   ![](images/72ee84c17eac16402705341cb1ad374a.png)

1. Rename your zip file MyExport.zip

1. On the new Qradar fresh install, just copy the .zip file and reimport it

Enter in the following command:

   `[root\@qradar \~]\# /opt/qradar/bin/contentManagement.pl --action import --file MyExport.zip`