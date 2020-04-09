[title]: # (Installing Qradar after the RHEL installation)
[tags]: # (introduction)
[priority]: # (4)
# Installing Qradar after the RHEL installation

1. Copy the QRadar ISO to the device.  

   ![tag](images/58c37797b34b2a8ce9041042c652b07e.png)

1. Create the /images/cdrom directory by typing the following command:  

   `mkdir /images/cdrom`

1. Mount the QRadar ISO by using the following command:

   `mount -o loop \<nameofiso.iso\> /images/cdrom`

1. Run the QRadar setup by using the following command:  

   `/images/cdrom/setup`
­­
   ![](images/e7737744ce7e10839f00f7d0202e4a0c.png)

   ![](images/7e49cb10798a7bbc3045072b15b283d3.png)

   >**Note:** A new kernel may be installed as part of the installation, which requires a system restart.  

   ![](images/817a8f526ce449de1e71c52b12a7c3fd.png)

   __Repeat the commands in steps 3 and 4 after the system restart to continue the installation__.

1. Select the appliance type:

   * Software Install
   * High Availability Appliance

1. Select the appliance assignment, and then select next.  

   ![](images/581ea59e9dd0aba716b5a303b67407b6.png)

1. If you selected an appliance for high-availability (HA), select whether the appliance is a console.

1. For the type of setup, select Normal Setup (default) or HA Recovery Setup, and set up the time.  

   ![](images/cc55fd88a9416773ed87ac9e2f4cefa9.png)

1. If you selected HA Recovery Setup, enter the cluster virtual IP address.
1. Select the Internet Protocol version: • Select ipv4 or ipv6.  

   ![](images/88f0bf30e2a044c484dda2818f00f874.png)

   ![](images/c2f0b7832992ea668d8bb99725de7402.png)

1. If you selected ipv6, select manual or auto for the Configuration type.

1. Select the bonded interface setup, if required.

1. Select the management interface.

1. In the wizard, enter a fully qualified domain name in the Hostname field.

1. In the IP address field, enter a static IP address, or use the assigned IP
address.

1. If you do not have an email server, enter localhost in the Email server name
field.

1. Leave the root password as it is.

1. If you are installing a Console, enter an admin password:  

   ![](images/f5ba9d7be9df32f137a3a9ac6bc6084f.png)

1. Click Finish.  
1. Follow the instructions in the installation wizard to complete the installation. The installation process might take several minutes.  

   ![](images/a1e4d04a697f023d7255b1516e0e4fdf.png)

   ![](images/6f5bf8583cb272e2763f0294a70c2152.png)

1. If you are installing a Console, apply your license key.

   a) Log in to QRadar as the admin user,
   https://\<IP_Address_Qradar\>  

   ![](images/9b573a9b7cc81bdecfde775b50f1441a.png)

   b) Click **Login**.

   c) On the navigation menu ( ), click **Admin**.

   d) In the navigation pane, click **System Configuration.**

   e) Click the **System and License Management** icon.  

   ![](images/338e75f912a7f14ca0b69254a2c2657a.png)

   f) From the **Display** list box, select **Licenses**, and upload your license key.  

   ![](images/4f3cebab49a374984c0958bfa1aecdcc.png)

   g) Select the unallocated license and click **Allocate System to License**.

   h) From the list of systems, select a system, and **click Allocate System to License**.  

   ![](images/04ccb477541b07bb30c28dd9d6cbf746.png)