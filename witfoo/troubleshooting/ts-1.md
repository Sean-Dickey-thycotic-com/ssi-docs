[title]: # (Troubleshooting Configuration)
[tags]: # (witfoo,troubleshoot)
[priority]: # (501)
[display]: # (all)
# Troubleshooting the Configuration

If the WitFoo UI does not appear after configuration, follow these troubleshooting tips.

## Check if Superintendent Service is ON

To check whether superintendent service is ON, run the following command:

`service --status-all`

## Install JDK and Remove Apache2

To install JDK and remove Apache2, run the following commands:

```
sudo apt install default-jdk
sudo apt-get remove apache2
```

## Restart the Superintendent

To restart superintendent, run the following command:

`sudo service superintendent restart`

## Check if Docker is Configured

Check if Docker is configured. If not, run the following commands:

```
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64]
https://download.docker.com/linux/ubuntu

$(lsb_release -cs) stable"

sudo apt-get update

sudo apt-get install -y docker-ce
```

## Check the Registration IP

Check if you can see the WitFoo GUI by entering the URL: `https://<ipaddrs>/register` in the browser. If not, run the following commands:

```
sudo service superintendent stop

sudo apt-get remove default-jdk

sudo apt-get install openjdk-8-jre-headless openjdk-8-jdk

sudo service superintendent start
```

It takes 30-60 minutes for the code (via Docker containers) to download and start. You will now be able to access `https://<ipaddrs>/register` to create the first account.

>**Note**: \<ipaddrs\> is the IP of the configured machine.

## Progress Monitoring

Run the following command to monitor the progress

`tail -f /var/log/witfoo-superintendent/status.log`
