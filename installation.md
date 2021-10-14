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

### \# Installation

The following steps describe the installation of TinyCP on Ubuntu and Debian.

#### \# Ubuntu:

```bash
sudo apt install gnupg ca-certificates
sudo apt-key adv --fetch-keys http://repos.tinycp.com/ubuntu/conf/gpg.key
sudo echo "deb http://repos.tinycp.com/ubuntu all main" | sudo tee /etc/apt/sources.list.d/tinycp.list
sudo apt-get update
sudo apt-get install tinycp -y
```

#### \# Debian:

```bash
apt install gnupg ca-certificates
apt-key adv --fetch-keys http://repos.tinycp.com/ubuntu/conf/gpg.key
echo "deb http://repos.tinycp.com/ubuntu all nightbuild" | sudo tee /etc/apt/sources.list.d/tinycp.list
apt update
apt install tinycp -y
```
During the TinyCP installation process, you will be prompted to enter a password, which is the admin password for logging into your Tiny Control Panel.

>You can preset some variables during installation to fully automate the installation process
```bash
TINYCP_USER="admin" TINYCP_PASS="secretpass" TINYCP_PORT="55555" apt install tinycp -y
```
Please replace the command described above accordingly.

##### \# Important!

Now you can log into your personal Tiny Control Panel with the data displayed in the terminal. You should save the login data immediately. There is no possibility to display them again.

## \# Access TinyCP

| Data | Value |
| :--- |:---|
| URL: | **http://YOUR_IP:63232** (The port is assigned dynamically with each installation.)|
| LOGIN: | **admin** |
| PASSWORD: | **The password you assigned during installation** |

Goto the URL given in your installation and you will be able to start your journey in TinyCP!

