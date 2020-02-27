[title]: # (Troubleshooting Configuration)
[tags]: # (witfoo,troubleshoot)
[priority]: # (501)
[display]: # (all)

# Troubleshooting Configuration

<!-- add troubleshooting topic and info -->

If the WitFoo UI does not appear after configuration, perform the following
steps.

1.  To check whether superintendent service is ON, run the following command:
    service --status-all

2.  To install JDK and remove Apache2, run the following commands:

-   sudo apt install default-jdk

-   sudo apt-get remove apache2

1.  To restart superintendent, run the following command:

-   sudo service superintendent restart

1.  Check if Docker is configured. If not, run the following commands:

-   sudo curl -fsSL
    [https://download.docker.com/linux/ubuntu/gpg](https://slack-redir.net/link?url=https%3A%2F%2Fdownload.docker.com%2Flinux%2Fubuntu%2Fgpg)
    \| sudo apt-key add -

-   sudo add-apt-repository "deb [arch=amd64]
    [https://download.docker.com/linux/ubuntu](https://slack-redir.net/link?url=https%3A%2F%2Fdownload.docker.com%2Flinux%2Fubuntu)

-   \$(lsb_release -cs) stable"

-   sudo apt-get update

-   sudo apt-get install -y docker-ce

1.  To restart superintendent, run the following command:

-   sudo service superintendent restart

1.  Check if you can see the WitFoo GUI by entering the URL: in the browser. If
    not, run the following commands:

-   sudo service superintendent stop

-   sudo apt-get remove default-jdk

-   sudo apt-get install openjdk-8-jre-headless openjdk-8-jdk

-   sudo service superintendent start

>   It takes 30-60 minutes for the code (via Docker containers) to download and
>   start. You will now be able to access to create the first account.

>   **Note**: \<ipaddrs\> is the IP of the configured Ubuntu machine.

1.  Run the following command to monitor the progress

-   tail -f /var/log/witfoo-superintendent/status.log
