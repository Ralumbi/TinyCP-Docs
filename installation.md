# Installation

The installation process of TinyCP is fairly easy, when you're not experienced follow the process carefully. We split the installation into a few parts.

* Preperation
* Installation
* Access TinyCP

## \# Preperation

Before you should start the installation of TinyCP, update and upgrade your Operating System\(OS\) of the server. You can do this by typing into the terminal:

```bash
sudo apt update && sudo apt upgrade -y
```

### \# MariaDB & PHP Repository

To get the latest versions of PHP and MariaDB for Ubuntu / Debian, you need to include third party sources before installing TinyCP. The following section explains how you can implement this.

#### \# Ubuntu

##### \# PHP

Run the following commands to add the PHP repository for Ubuntu

```bash
sudo apt install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
```

##### \# MariaDB

Run the following commands to add the MariaDB repository for Ubuntu. Replace **{UBUNTU_VERSION}** with your Ubuntu version, for example **focal**

```bash
sudo apt-get install software-properties-common
sudo apt-key adv --fetch-keys 'https://mariadb.org/mariadb_release_signing_key.asc'
sudo add-apt-repository 'deb [arch=amd64,arm64,ppc64el] https://mariadb.mirror.iphh.net/repo/10.6/ubuntu {UBUNTU_VERSION} main'
```

#### \# Debian

##### \# PHP

Run the following commands to add the PHP repository for Debian

```bash
apt install -y lsb-release ca-certificates apt-transport-https software-properties-common
echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | tee /etc/apt/sources.list.d/sury-php.list
wget -qO - https://packages.sury.org/php/apt.gpg | apt-key add -
apt update
```

##### \# MariaDB

Run the following commands to add the MariaDB repository for Debian. Replace **{DEBIAN_VERSION}** with your Debian version, for example **bullseye**

```bash
apt-get install -y software-properties-common dirmngr
curl -LsSO https://mariadb.org/mariadb_release_signing_key.asc
chmod -c 644 mariadb_release_signing_key.asc
mv -vi mariadb_release_signing_key.asc /etc/apt/trusted.gpg.d/
add-apt-repository 'deb [arch=amd64,arm64,ppc64el] https://mariadb.mirror.iphh.net/repo/10.6/debian {DEBIAN_VERSION} main'
```

>You can also add these sources later, but then you have to run a `sudo apt upgrade -y` to upgrade the already installed packages.

### \# Starting the installation

Splitting this into two parts Ubuntu and Debian starting with Ubuntu

### \# Ubuntu:

```bash
sudo apt install gnupg ca-certificates
sudo apt-key adv --fetch-keys http://repos.tinycp.com/ubuntu/conf/gpg.key
sudo echo "deb http://repos.tinycp.com/ubuntu all main" | sudo tee /etc/apt/sources.list.d/tinycp.list
sudo apt-get update
sudo apt-get install tinycp -y
```

### \# Debian:

```bash
apt install gnupg ca-certificates
apt-key adv --fetch-keys http://repos.tinycp.com/ubuntu/conf/gpg.key
echo "deb http://repos.tinycp.com/ubuntu all nightbuild" | sudo tee /etc/apt/sources.list.d/tinycp.list
apt update
apt install tinycp -y
```

During the installation process of TinyCP you will be asked to enter a password which will be the Admin password to login to your Tiny Control Panel.

###   _\# Tip:_ 

You can pre-setup a few variables in the installation.
```bash
TINYCP_USER="admin" TINYCP_PASS="secretpass" TINYCP_PORT="55555" apt-get install tinycp -y
```

This do mean that you will need to replace the last part of the installation. As is described above.

## \# Completed

Now you can now login to your personal Tiny Control Panel using the information shown in the terminal. You must save this information on a secure place! \(we'd advice to write it down on paper\)

### \# How to connect

| Information |
| :--- |
| URL: [http://192.168.2.1:63232](http://192.168.2.1:63232) \(this address is different for everyone\) |
| LOGIN: admin |
| PASSWORD: 123123 \(this is the password you have entered at the end of the installation\) |

Goto the URL given in your installation and you will be able to start your journey in TinyCP!

