# Using Vagrant

This is a Vagrant umbrella document, containing general information related to Vagrant use.

*Use of proprietary software*

This guide refers to and uses [Microsoft](www.microsoft.com) software. I encourage you to read and follow their licensing rules in order to have the best user experience.


## Create a Windows 2012R2 VM using VirtualBox

### Virtual machine details

|Item | Value |
|-----|-------|
| Host | Ubuntu 14.04 64bits, 16Gb memory |
| VirtualBox | v 4.3.24 |
| VM name | win2012r2 |
| CPU quantity | 2|
| Memory | 3600MB |

### Additional Configuration

When starting the machine in the first time, received message "Your PC needs to restart".
```
VBoxManage setextradata win2012r2 VBoxInternal/CPUM/CMPXCHG16B 1
```


#### References
- [Windows 2012 Server R2 preview installation fails: Your PC needs to restart | Please hold down the power button | Error Code 0x000000C4](https://www.virtualbox.org/ticket/11899)


### Windows Installation

|Item | Value |
|-----|-------|
| OS | Windows 2012 R2 Standard (Server with a GUI)|
| Machine Name | win2012dev |
| Administrator password | Vagrant01 |
| vagrant user password | Banana01 |

### SQL Server Installation


|Item | Value |
|-----|-------|
| SQL Server | SQL Server 2012 |
| SQL Server sa password | Banana01 |
| SQL Server admins | Administrator, vagrant |
| Analysis Services admins | Administrator, vagrant |

*Before Installing*

- Enable NetFx3. In Windows, have the installation cd loaded, then in command prompt:
```
dism /online /enable-feature /featurename:netfx3 /all /source:<dvd installer drive>\sources\sxs
```


*Notes*

- You should use a secure password, I put mine here as an example. For Vagrant, it is common to have a user vagrant, with password = vagrant.


## Create a Vagrant box

See http://docs.vagrantup.com/v2/boxes/base.html

Base Windows Configuration

- Turn off UAC
- Disable complex passwords
- Disable "Shutdown Tracker".
- Disable "Server Manager" starting at login (for non-Core)
- In Virtualbox, go to the VM, change Network Adapter 1 to NAT
- Take note of the Mac Address


```
vagrant package --base <vm name>
```

```
vagrant box add windows2012 package.box
vagrant init windows2012
vagrant up
```

## Get a Vagrant box from a repository

The url for a box follows the pattern:

```
https://vagrantcloud.com/USERNAME/boxes/BOXNAME/versions/VERSION/providers/PROVIDER.box
```

Example: suppose you want this box https://atlas.hashicorp.com/lmayorga1980/boxes/windows-2008r2, which offers virtualbox; select a version, then run:

```
vagrant box add lmayorga1980/windows-2008r2 https://atlas.hashicorp.com/lmayorga1980/boxes/windows-2008r2/versions/0.1.0/providers/virtualbox.box
``
