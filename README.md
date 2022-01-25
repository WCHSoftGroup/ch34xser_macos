# ch34xser_macos
## ***\*Introduction\****

This installation guide document shows the procedure of installing the macOS driver for the WCH USB-to-SERIAL devices. The driver can be downloaded from the website:
Link: http://www.wch.cn/downloads/CH34XSER_MAC_ZIP.html

## ***\*System Requirement\****

- OS X 10.9 to OS X 10.15
- OS X 11.0(Big Sur) and above

## ***\*Chip Model Support\****

- CH340/CH341/CH343/CH9101/CH9102/CH9143 (USB to Single Serial Port)
- CH342/CH344/ CH344/CH347/CH9103 (USB to Multi Serial Ports)

## ***\*Installation\****

1. Download the driver from the website and unzip the file to a local installation directory.

2. Click on the driver file and continue to proceed step by step.

![img](README.assets/wpsFC5A.tmp.jpg) 



![img](README.assets/wpsFC5B.tmp.jpg) 

When using OS X 11.0 and above, you need to perform the following additional operation:

Open “LaunchPad” and find “CH34xVCPDriver” Application, open the App and click the “Install” button.

![img](README.assets/wpsFC5C.tmp.png) 

When using OS X 10.9 to OS X 10.15, you need to click “Restart” to restart your computer, then perform the following steps after restarting.

![img](README.assets/wpsFC5D.tmp.jpg) 

3. When plug the USB-to-SERIAL device into the USB port, you can open “System Report”->Hardware->USB, the right side is “USB Device Tree” and you will find a device whose “Vendor ID” is **[0x1a86]** if USB device is working properly.

![img](README.assets/wpsFC5E.tmp.jpg) 

4. Open Terminal program under Applications-Utilities folder and type the command “ls /dev/tty*”.

![img](README.assets/wpsFC5F.tmp.jpg) 

You should see the “tty.wchusbserialx” where “x” is the assigned device number similar to Windows COM port assignment. 

 

## ***\*Note:\****

Mac OS High Sierra 10.13 introduces a new feature that requires user approval before loading new third-party kernel extensions. Go to System Preferences - Security & Privacy and click Allow. 

Link: https://developer.apple.com/library/content/technotes/tn2459/_index.html

Please enter “System Preferences”->“Security & Privacy”->“General” page, below the title “Allow apps downloaded from:” choose the choice 2->”Mac App Store and identified developers” so that driver will work normally.

![img](README.assets/wpsFC70.tmp.png) 

## ***\*Uninstall Driver\****

- Mac OS X 10.9~10.15 

Open "Terminal" program under Applications-Utilities folder and type the following commands:

***\*sudo rm -rf  /Library/Extensions/CH34xVCPDriver.kext\****

***\*sudo rm –rf /var/db/receipts/\*CH34xVCPDriver\*.\*\**** 

- Mac OS X 11.0 and above

1. Remove the Application to “Trash” to uninstall.

2. Restart the computer again before reinstalling the driver.

 
