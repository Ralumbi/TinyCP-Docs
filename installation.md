# Installation

The installation process of TinyCP is fairly easy, when you're not experienced follow the process carefully. We split the installation into a few parts.

* Essentials before installing
* Installation of TinyCP
* How to access TinyCP after installation

## \# Essentials

Before you should start the installation of TinyCP, update and upgrade your Operating System\(OS\) of the server. You can do this by typing into the terminal:

* Ubuntu: `sudo apt update && sudo apt upgrade -y`
* Debian: `sudo aptitude update && sudo aptitude full-upgrade -y`

### \# Starting the installation

Splitting this into two parts Ubuntu and Debian starting with Ubuntu

### \# Ubuntu:

* `sudo apt install gnupg ca-certificates`
* `sudo apt-key adv --fetch-keys http://repos.tinycp.com/ubuntu/conf/gpg.key`
* `sudo echo "deb http://repos.tinycp.com/ubuntu all main" | sudo tee /etc/apt/sources.list.d/tinycp.list`
* `sudo apt-get update`
* `sudo apt-get install tinycp -y`

### \# Debian:

* `sudo apt install gnupg ca-certificates`
* `sudo apt-key adv --fetch-keys http://repos.tinycp.com/ubuntu/conf/gpg.key`
* `sudo echo "deb http://repos.tinycp.com/ubuntu all nightbuild" | sudo tee /etc/apt/sources.list.d/tinycp.list`
* `sudo apt-get update`
* `sudo apt-get install tinycp -y`

During the installation process of TinyCP you will be asked to enter a password which will be the Admin password to login to your Tiny Control Panel.

## \# Completed

Now you can now login to your personal Tiny Control Panel using the information shown in the terminal. You must save this information on a secure place! \(we'd advice to write it down on paper\)

### \# How to connect

| Information |
| :--- |
| URL: [http://192.168.2.1:63232](http://192.168.2.1:63232) \(this address is different for everyone\) |
| LOGIN: admin |
| PASSWORD: 123123 \(this is the password you have entered at the end of the installation\) |

Goto the URL given in your installation and you will be able to start your journey in TinyCP!

