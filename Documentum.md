### Documentum Development	

#### Development tools setup

##### Documentum Composer
This describes how to setup Composer in Eclipse.

Environment used

Item | Description
-----|--------
Documentum | Documentum Developer Edition (7.1)
Eclipse | Eclipse 3.7 Indigo, 32 bits
Java | JRE 6, 32 bits
OS | Windows 7

**Installation steps**
- If you already have a newer Eclipse, you need to install the old 3.7 to be able to use the Composer plugin.
- Install Java JRE 6, 32 bits
- Install Eclipse 3.7
- In eclipse.ini, add the following parameter after `openFile`:
```
-vm
C:\Program Files (x86)\Java\jre6\bin\javaw.exe
```
- Install composer plugin


**Sources**
http://paulcwarren.wordpress.com/2010/11/29/composer-on-helios/


#### Creating a new Documentum WDK application


#### Notes

The WDK programming model is based on the following technologies:

- XML Configuration
- JavaServer Pages
- Java Servlets
- Java EE security

BOF stands for (Documentum) Business Object Framework

UCF Applet (Unified Client Facilities)


WDK Customization 
You need to use the customization layer, which is under:
`virtual_dir/custom`

WDK Eclipse plugin
https://community.emc.com/docs/DOC-1286


#### Sources
- Web Development Kit 6.7 Development Guide. EMC Documentum
- Web Development Kit 6.7 Tutorial. EMC Documentum
