[title]: # (Scan for Vulnerabilities)
[tags]: # (scan, vulnerabilities)
[priority]: # (103)
# SCAN FOR VULNERABILITIES

Scan your systems for known vulnerabilities and understand your security risk.
By automating your scans you'll get up to date security intelligence in real
time.

**Let’s launch a vulnerability scan**

Go to Scans \> Scans \> New \> Scan (or Schedule Scan).

Following window will get open. Check for Scanner appliance, if showing Scanner
appliance not available then need to setup Scanner appliance first.

![](images/07a1524e85a73bcf217c278a3f1372d0.png)

**Setting up Scanner appliance**

Qualys Scanner Appliance, an option with the Qualys Cloud Platform from Qualys,
Inc. With the Qualys Scanner Appliance, you can assess internal network devices,
systems and web applications. The Scanner Appliance is a robust, scalable
solution for scanning networks of all sizes including large distributed
networks.

**Use Scanner Appliances**

You could configure physical scanner appliance, virtual scanner appliances to
assess internal network devices, systems and web applications. To configure
Scanner appliance navigate to Scans \> Appliance and Select option.

![](images/c1e91eaaf0b84acbcddea6b8dba1242e.png)

**Qualys Virtual Scanner Appliance**

The Qualys Virtual Scanner Appliance has multiple distributions to support
deployments on a variety of virtualization platforms.  However, the Qualys
Virtual Scanner Appliance is sold as a single product with a single SKU.  Each
purchased license entitles the user to one *active* Qualys Virtual Scanner
Appliance.

The Qualys Virtual Scanner Appliance acts as an extension of the customer's
solution subscriptions on the Qualys Cloud Platform and is not a standalone
solution.  Using the same license, customers are free to delete an instance of
the Qualys Virtual Scanner Appliance at any time and redeploy another instance
(of any distribution) in its place or in an entirely different location.

**Configure and activate your scanner**

![](images/6fded6356d5026bb8c768bdf31a55610.png)

Add Your Virtual Scanner
========================

**Step 1 - Start the Wizard**

Go to Scans \> Appliances and select New \> Virtual Scanner Appliance. Click
Start Wizard

**Step 2 - Choose your virtualization platform.**

Give your scanner a name and tell the virtualization platform you’d like to use.

![](images/d607127079938fc6204358f39935e3ca.png)

**Step 3 - Download the Image**

This step applies to virtualization platforms with a scanner appliance image
download (i.e. for VMware, Citrix XenServer, etc). Locate the Virtual Scanner
image on your local system.

![](images/9170dccdd241ae2a775b0b1d9091c2c5.png)

**Step 4 - Get your Personalization Code**

Copy the code to a safe place (need it later).

![](images/112dcb63e1c0021cef1f883ca4056bbf.png)

**Step 5 - Personalize Your Scanner Local system or server**

These steps apply when you have downloaded a scanner appliance image (i.e. for
VMware, Citrix XenServer, etc). You’ll use Virtual Scanner Console running on
your virtualization software to complete these steps.

Configure a virtual scanner using Microsoft Hyper-V
===================================================

Follow steps to configure a virtual scanner appliance using Microsoft Hyper-V.
Once you've successfully configured your scanner it'll be ready for scanning.

**Assumptions** - 1) Downloaded the virtual scanner image
(*qVSA-2.0.13-1-vhd.zip* or later) and

>   2) Obtained a personalization code.

**Step 1: Start the virtual scanner machine**

-   Unzip the download file  qVSA.i386-2.4.26-11.vhd.zip to obtain the virtual
    hard disk file *qVSA.i386-2.4.26-11.vhd.zip* Log in to the Hyper-V server.
    Go to Manager \> Hyper-V Manager and add a new Virtual Machine.

-   Provide a name for the scanner.

-   Configure the memory. Recommended is 2048 MB or more.

-   Configure the networking as appropriate so the network adapter on the
    scanner can use a virtual network for communication.

-   For the virtual hard disk configuration, select “Use an existing virtual
    hard disk” and provide the location of the .vhd file (obtained from the
    download .zip file).

-   Click Next and then Finish.

**Step 2: Press the Right arrow to select “Personalize this scanner”**

![](images/0a12bfe2fc2229b08fc93ef804b0e299.png)

The virtual scanner will use DHCP without proxy configuration, unless you make
custom settings first. For custom configuration: Go to “Set up network” by
pressing the Down arrow one time and then the Right arrow one time.

**Step 3: Enter your personalization code**

One activation code is used to activate one virtual scanner. After entering the
code the activation process starts and the service reports the progress.
Activation may take a few minutes to complete.

![](images/df3c1e9924faabac07c39b3525c85b9c.png)

**Step 4: Wait until activation completes**

The virtual scanner attempts to make a connection to the Qualys Cloud Platform
using its current configuration (network and proxy settings). Upon success, the
scanner’s friendly name and IP address appear and the scanner is ready to be
used for scanning. Press Enter to go to the main menu.

![](images/b2825f52bd359dd43d634f15dac5e196.png)

**AUTOMATICALLY CHANGE PASSWORDS AFTER EACH SCAN**

You can leverage Secret Server’s Check Out feature to ensure that passwords used
for authenticated scanning are changed after use. This is an important measure
in protecting your privileged accounts from “Pass-the-Hash” attacks, because it
means that the password hash stored in each machine from use during scanning
will no longer be valid once the password has been changed in Active Directory.
Check Out with Change Password on Check In means that the password for your
domain account will be changed automatically after scanning is complete.

**Note** Check Out requires Enterprise or Enterprise Plus edition.

**Enable Password Changing on Check In**

To verify that **Password Changing on Check In** is enabled, use the following
instructions:

1. Navigate to **Remote Password Changing** from the **ADMIN** menu.

2. If **Enable Password Changing on Check In** is set to **No** or doesn’t
appear, click **Edit** and ensure that the **Enable Remote Password Changing**
and **Enable Password Changing on Check In** check boxes are both selected. .
Click **Save**.

![](images/e69f0f395cbf8dde3c2e3c0cb20929a2.png)

*Figure Remote Password Changing settings*

**Configure a Secret for Check Out**

Enable Check Out with Change Password on Check In to ensure that the password
for your privileged account is changed after each use. To do so, use the
following steps:

1. Find your **privileged account Secret** and click **View**.

2. Click the **Security** tab and then click **Edit**.

3. Select the Require **Check Out check box**, and then select the **Change
Password On Check In** check box as well.

4. Click **Custom**, and enter **a period of time** that you estimate will allow
enough time for authenticated scanning to complete.

5. Click **Save**.

![](images/d42ecb7e289ceda547b6543c7db5a386.png)

*Figure Enabling Check Out for a Secret*