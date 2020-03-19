[title]: # (Check and extend the validity of the certificate)
[tags]: # (introduction)
[priority]: # (102)
# Check and extend the validity of the certificate

Make sure that your certificate is valid. If the validity expires, you need to extend the validity.

__To check and extend validity of the certificate:__

1. Go to `C:\Program Files\IBM\TDI\V7.2\jvm\jre\bin`.

   ![ikeymanfile](images/ikeymanfile.png)
1. Select `ikeyman` file, right-click the file and click __Run as administrator__.
1. In the User __Account Control__ dialog box, click __Yes__. The __IBM Key Management__ dialog box appears.
1. Click __Open__ ![openicon](images/openicon.png) icon. The __Open__ dialog box appears.

   ![opendialogboxtimsol](images/opendialogboxtimsol.png)
1. Click __Browse__ and navigate to the `timsol` folder which is located at `C:\Program Files\IBM\TDI\V7.2\timsol`.
1. In the `timsol` folder, select the `testserver.jks` and click __OK__. The __Password Prompt__ dialog box appears.

   ![passwordprompttestserverjks](images/passwordprompttestserverjks.png)
1. In the __Password__ text box, type the password, and click __OK__.

    >**Note:: The default password of testserver.jks is `server`.
1. On the right-hand side, click __View/Edit__. A Warning ‘__The selected certificate has expired!__’ might appear.

   ![certificateexpiredtestserver](images/certificateexpiredtestserver.png)
1. Click __OK__. The certificate details appear.
1. Click __Open__ ![openicon](images/openicon.png) icon. The __Open__ dialog box appears.
1. Navigate to the `serverapi` folder which is located at `C:\Program Files\IBM\TDI\V7.2\timsol\serverapi`.

   ![opendialogboxserverapi](images/opendialogboxserverapi.png)
1. Select `testadmin.jks` and click __Open__.
1. In the __Open dialog__ box, click __OK__. The __Password Prompt__ dialog box appears.

   ![passwordprompttestadmin](images/passwordprompttestadmin.png)
1. In the __Password__ text box, type the password, and click __OK__.

   > __Note__: The default password of testserver.jks is `administrator`.
1. On the right-hand side, click __View/Edit__. A Warning ‘__The selected certificate has expired!__’ might appear.

   ![certificateexpiredtestadmin](images/certificateexpiredtestadmin.png)
1. Click __OK__. The certificate details appear.
1. In __Windows Search__, type `cmd` and press __Enter__. The results are auto-populated.
1. Right-click `Command Prompt` and click __Run as Administrator__. 
1. In the __User Account Control__ dialog box, click __Yes__. The __Administrator: Command Prompt__ appears.
1. To move to the `timsol` folder, type `C:\Program Files\IBM\TDI\V7.2\timsol and press Enter`.
1. Run the following eight commands:

    a. `"c:\Program Files\IBM\TDI\V7.2\jvm\jre\bin\keytool" -selfcert -v -alias server -validity 730 -keystore testserver.jks -storepass server`

     ![commandone](images/commandone.png)

    b. `"c:\Program Files\IBM\TDI\V7.2\jvm\jre\bin\keytool" -selfcert -v -alias admin -validity 730 -keystore serverapi\testadmin.jks -storepass administrator`

     ![commandtwo](images/commandtwo.png)

    c. `"c:\Program Files\IBM\TDI\V7.2\jvm\jre\bin\keytool" -export -alias server -keystore testserver.jks -storepass server  -file myserver.crt`

     ![commandthree](images/commandthree.png) 

     d. `"c:\Program Files\IBM\TDI\V7.2\jvm\jre\bin\keytool" -export -alias admin -keystore serverapi\testadmin.jks -storepass administrator  -file myadmin.crt`

     ![commandfour](images/commandfour.png)

    e. `"c:\Program Files\IBM\TDI\V7.2\jvm\jre\bin\keytool" -delete -alias admin -keystore testserver.jks -storepass server`

     ![commandfive](images/commandfive.png)

    f. `"c:\Program Files\IBM\TDI\V7.2\jvm\jre\bin\keytool" -import -alias admin -keystore testserver.jks -storepass server -file myadmin.crt`

     ![commandsix](images/commandsix.png)
  
     >**Note:** To trust this certificate, type yes.

     ![trustcertificateone](images/trustcertificateone.png)

     g. `"c:\Program Files\IBM\TDI\V7.2\jvm\jre\bin\keytool" -delete -alias server -keystore serverapi\testadmin.jks -storepass administrator`

     ![commandseven](images/commandseven.png)

    h. `"c:\Program Files\IBM\TDI\V7.2\jvm\jre\bin\keytool" -import -alias server -keystore serverapi\testadmin.jks -storepass administrator -file myserver.crt`

     ![commandeight](images/commandeight.png)

     >**Note__:** To trust this certificate, type yes.

      ![trustcertificatetwo](images/trustcertificatetwo.png)

     >**Note:** Go to `C:\Program Files\IBM\TDI\V7.2\timsol` and verify that certificates `myadmin` and `myserver` are added to the `timsol` folder.

1. Go to `C:\Program Files\IBM\TDI\V7.2\timsol` and copy the `testserver.jks` file.
1. Go to `C:\Program Files\IBM\TDI\V7.2` and paste the `testserver.jks` file.
1. Go to `C:\Program Files\IBM\TDI\V7.2\timsol\serverapi` and copy `testadmin.jks` file.
1. Go to `C:\Program Files\IBM\TDI\V7.2\serverapi` and paste `testadmin.jks` file.

The validity of the certificate is verififed and now you need to import the Thycotic certificate.
