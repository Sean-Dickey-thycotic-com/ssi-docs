[title]: # (Import Thycotic certificate)
[tags]: # (introduction)
[priority]: # (103)
# Import Thycotic certificate

For secure connection between Thycotic Secret Server and IBM IGI, you will need to import Thycotic certificate.

__To import Thycotic certificate:__

1. Click __Not secure__ part of the Thycotic Server URL . __Your connection to this site is not secure__ dialog box appears.

   ![yourconnection](images/yourconnection.png)
1. Click __Certificate (Invalid)__. The __Certificate__ dialog box appears.

   ![certificatedialogbox](images/certificatedialogbox.png)
1. Click __Details | Copy to File__. The __Welcome to the Certificate Export Wizard__
 appears.

   ![welcometothecertificateexportwizard](images/welcometothecertificateexportwizard.png)
1. Click __Next__. The __Export File Format__ panel appears.

   ![exportfileformatpanel](images/exportfileformatpanel.png)
1. Click __Next__. The __File to Export__ panel appears.

   ![filetoexportpanel](images/filetoexportpanel.png)
1. In the __File name__ text box, type the name for the certificate to be exported.
1. Click __Browse__ and select the location where you want to export the certificate.
1. Click __Next__. The __Completing the Certificate Export Wizard__ appears.

   ![completingthecertificateexportwizard](images/completingthecertificateexportwizard.png)
1. Click __Finish__. The message, ‘__The export was successful.__’ appears. The certificate is exported to the location selected.

   ![exportsuccessfulmessage](images/exportsuccessfulmessage.png)
1. Right-click the certificate where you have exported and click __Install Certificate__.

   ![installcertificate](images/installcertificate.png)
1. The __Welcome to the Certificate Import Wizard__ appears.

   ![welcometocertificateimportwizard](images/welcometocertificateimportwizard.png)
1. In the __Store Location__ area, select __Current User__ and then click __Next__. The __Certificate Store__ panel  appears.

   ![certificatestorepanel](images/certificatestorepanel.png)
1. Select __Place all certificates in the following store__ and then click __Browse__.
1. Select __Personal__ folder and then click __Next__. The __Completing the Certificate Import Wizard__ panel appears.

   ![completingthecertificateimportwizard](images/completingthecertificateimportwizard.png)
1. Click __Finish__. The message ‘__The import was successful.__’ appears.

   ![importsuccessfulmessage](images/importsuccessfulmessage.png)
1. Right-click the certificate where you have exported and click __Install Certificate__.

   ![installcertificatetwo](images/installcertificatetwo.png)
1. The __Welcome to the Certificate Import Wizard__ appears.

   ![welcometocertificateimportwizardtwo](images/welcometocertificateimportwizardtwo.png)
1. In the __Store Location__ area, select __Current User__ and then click __Next__. The __Certificate Store__ panel  appears.

   ![certificatestorepaneltwo](images/certificatestorepaneltwo.png)
1. Select __Place all certificates in the following store__ and then click __Browse__.
1. Select __Trusted Root Certification Authorities__ folder and then click __Next__. The __Completing the Certificate Import Wizard__ panel appears.

   ![completingthecertificateimportwizardtwo](images/completingthecertificateimportwizardtwo.png)
1. Click __Finish__. The message ‘__The import was successful.__’ appears.

   ![importsuccessfultwo](images/importsuccessfultwo.png)

The Thycotic certficate is imported successfully. Now you need to add the certificate.
