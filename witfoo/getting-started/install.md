[title]: # (Installation)
[tags]: # (introduction)
[priority]: # (4)
[display]: # (all)

# Installation

# Install and Configure Ubuntu 18.04 LTS

You must install Ubuntu, configure network, install-prep, and run register to
complete the integration of WitFoo virtual appliance with Secret Server.

1.  Download Ubuntu 18.04 LTS from <http://releases.ubuntu.com/18.04/>

1.  Install Ubuntu 18.04 LTS.

1.  To create a user as WitFoo Admin, at the command prompt, type the following:

>   sudo adduser witfooadmin ; sudo usermod -aG sudo witfooadmin

>   and press **Enter**.

1.  Log in as a witfooadmin.

1.  Type the following to install prerequisites:

>   curl -k -o
>   /tmp/witfoo-precinct.deb** **<https://www.witfoo.com/data/witfoo-precinct.deb>** ;
>   apt install -y -f /tmp/witfoo-precinct.deb**

and press **Enter**.

1.  Type the following to register:

sudo /home/witfooadmin/register

and press **Enter.**

1.  Enter the **license key** provided by WitFoo.

1.  For selecting the role for the virtual appliance type **1** and press
    **Enter**.

**Notes:** By selecting 1 you assign all the roles.

1.  Change the password.

>   WitFoo Precinct virtual appliance is configured. This process may take some time.

1.  Type the URL in the browser: https://\<IP address of the Ubuntu
    image\>/register

    The login page of WitFoo Precinct virtual appliance appears.

1.  Complete the registration.

1.  Log in to the WitFoo Precinct virtual appliance with the registered credentials.

1.  In the search bar enter the **IP address** of Secret Server.
