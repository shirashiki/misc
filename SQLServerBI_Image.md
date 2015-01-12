## SQL Server BI Development Environment

### About this document

This document describes how to setup a development environment using DevOps tools such as Vagrant. It assumes you own the necessary installers and licenses from Microsoft.

When developing Microsoft Business Intelligence applications, developers are confronted with the task of preparing a development machine. If they prepare the machine manually, they may miss the installation of certain libraries, tools, or install the wrong versions. This guide shows how to create development vm images using scripts, providing developers a uniform development environment.  

I am adding the scripts I am running, please check the references for complete, up-to-date information.


### Environment

Component | Description
----------|------------
Host | Ubuntu Desktop 14.04 amd64
VirtualBox | 4.3


### Steps

#### VirtualBox installation

Install VirtualBox running:

```
sudo sh -c "echo 'deb http://download.virtualbox.org/virtualbox/debian '$(lsb_release -cs)' contrib non-free' > /etc/apt/sources.list.d/virtualbox.list" && wget -q http://download.virtualbox.org/virtualbox/debian/oracle_vbox.asc -O- | sudo apt-key add - && sudo apt-get update && sudo apt-get install virtualbox-4.3 dkms
```

#### Vagrant installation

* Install Vagrant *

```
sudo apt-get install vagrant
```

* Install Vagrant plugins *

```
vagrant plugin install vagrant-windows
```

* Get a Vagrant Box *
http://blog.syntaxc4.net/post/2014/09/03/windows-boxes-for-vagrant-courtesy-of-modern-ie.aspx


* Add the downloaded box to Vagrant*

Open a shell, go to the directory where you downloaded the box and run:

```
vagrant box add windows7 IE11.Win7.For.Vagrant.box
```

This will add to Vagrant a box called "windows7" (you can use other name). Result:

```
Downloading box from URL: file:/home/chugaboo/IE11.Win7.For.Vagrant.box
Extracting box...te: 96.5M/s, Estimated time remaining: 0:00:01)
Successfully added box 'windows7' with provider 'virtualbox'!
```

#### Create a Vagrant Project







### Misc

#### Setting Up Windows 2008 R2 in VirtualBox 

* Setting Up the VM *

- Use IDE Instead Of SATA. In VM Settings > Storage, put your disk under an IDE controller. Controller IDE config: Type = PIIX4, Use Host I/O Cache = On
- In VM Settings > Processor > Extended Features > Enable PAE/NX = On


* Adding Host-Only networking *

You can add new adapter at File - Preferences - Network.



### References
- [Create a windows base box for vagrant](http://www.thomasvjames.com/2013/09/create-a-windows-base-box-for-vagrant/)
- [Installing Vagrant and Virtual box on Ubuntu 14.04 LTS](http://www.olindata.com/blog/2014/07/installing-vagrant-and-virtual-box-ubuntu-1404-lts)
- [VirtualBox Installation](https://help.ubuntu.com/community/VirtualBox/Installation)
- [Virtualize Your Windows Development Environments with Vagrant, Packer, and Chocolatey, Part 1](http://www.developer.com/net/virtualize-your-windows-development-environments-with-vagrant-packer-and-chocolatey-part-1.html)

