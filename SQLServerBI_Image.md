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

'''
sudo sh -c "echo 'deb http://download.virtualbox.org/virtualbox/debian '$(lsb_release -cs)' contrib non-free' > /etc/apt/sources.list.d/virtualbox.list" && wget -q http://download.virtualbox.org/virtualbox/debian/oracle_vbox.asc -O- | sudo apt-key add - && sudo apt-get update && sudo apt-get install virtualbox-4.3 dkms
'''





### References
- [Installing Vagrant and Virtual box on Ubuntu 14.04 LTS](http://www.olindata.com/blog/2014/07/installing-vagrant-and-virtual-box-ubuntu-1404-lts)
- [VirtualBox Installation](https://help.ubuntu.com/community/VirtualBox/Installation)
