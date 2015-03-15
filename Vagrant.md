# Using Vagrant

## Creating a Windows 2012R2 VM using VirtualBox

### Virtual machine details

|Item | Value |
|-----|-------|
| Host | Ubuntu 14.04 64bits, 16Gb memory |
| VirtualBox | v 4.3.24 |
| VM name | Win2012R2 |
| CPU quantity | 2|
| Memory | 3600MB |

### Additional Configuration

When starting the machine in the first time, received message "Your PC needs to restart".
```
VBoxManage setextradata Win2012R2 VBoxInternal/CPUM/CMPXCHG16B 1
```


#### References
- [Windows 2012 Server R2 preview installation fails: Your PC needs to restart | Please hold down the power button | Error Code 0x000000C4](https://www.virtualbox.org/ticket/11899)



### Windows Installation

|Item | Value |
|-----|-------|
| OS | Windows 2012 R2 Standard (Server with a GUI)|


