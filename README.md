# odroidxu4LinuxImage
[odroidxu4LinuxImage]
(ftp://ftp.imp.fu-berlin.de/pub/autonomos/data/modelcar/v3/system-images/)

Ubuntu 14.04, ros indigo 
To get started, first things first, after you plugged in the emmc chip through the converter, you open your terminal.

1. Step: Install

Navigate to /linux-image-for-odroid-xu3

with the command ls /dev/sd* you can view all devices available. 
You want to make sure you have choosen the right one before starting the installation, if you are uncertain unblug the chip and insert it again to un-/show the device.

Forexample the driver is /dev/sdb.

For installation use: sudo ./install.pl /dev/sdb
Be aware, if this is not the correct device, you should cancle (Ctrl+C) and change the device manually ('./install.pl /dev/sd[X]).

Be carefull, during the installation one step is going to format partitions, which may erase unwanted data, just make sure you are certain of the steps you choose. The countdown later showing up will still give you the time to cancel your doing if needed.

2. Configuration

Device Configuration

during the installion you will be asked to specify which configuration will be used. You should go ahead and choose your name from the list.

Network configuration

You can go through the default configuarations, or choose your own name, password, etc. 
(make sure to remember you will need it in later on)

explain each configuration here

You are done now and can remove the SD card.

Also remember to copy all required files over to the device.

3.

Put the emmc chip on the odriod.
You can find a switch on the odrid, choosing between  SD and eMMC, make sure it is turned to eMMC.
Now it is time to plug in the power and the lan to the odriod, it may take a while for the first boot. If the blue light next to the power is blinking you are fine.
Remember that during the first boot of the eMMC card some initialization will be done. This happens automatically but may take a minute or two. 

4. Connetct

You will need to create a connection, you want to make sure you are choosing a Ethernet. While doing your editing check under 'IPv4Settings' that your Method is DHCP (this should be automatically, but just in case please check). 
After you have saved your editing, add your network connection and connect yourself to it.

It is time to set the ssh, with 'ssh root@192.168.1.199 '(or your choosen Ethernet IP address) you can do so.

5. Setup

You may need to update you date-settings with ' date –set ''[year]-[month]-[day] [hour]:[minute]:[second]''  '
