<u>**MT7612U for Linux**</u>

Driver for 802.11ac USB Adapter with MT7612U chipset  
STA, AP and Monitor Modes are possible

This driver is **currently** under **heavy** development.  
cfg80211 is in testing for STA mode
BUG in notify code, will crash kernel

Tested on X86_64 platform(s) **only**,  
cross compile possible, but not fully tested.  

For compiling type  
`make`  
in source dir  

For install the driver use  
`sudo insmod mt7612u.ko`  

To Unload driver you need to disconnect the device

If the driver fails building consult your distro how to  
install the kernel sources and build an external module.
  
Questions about this will **silently** ignored !  
They are <u>plenty</u> information around the web.  

**NOTES**  
The original driver is a mess and **PITA**  
Both mt7610u and mt7612u <u>can</u> work with the  
same driver.  
Code which is missing in one driver, may found in the other driver.  
i.e STA, AP, RSSI, LED handling stuff  

**BUGS**  
- can't unload driver, must disconnect device(s) first  
- bug in cfg80211 notify code  
- missing led support, need code from mt7610u driver  
  

**TODO**, in order of no appearance ;-)
- fix the kernel crash  
- add led support
- remove stupid AP/STA switch  
- fix unloading driver  
- do more function typesafe  
- cross compile check with real hw on $target  
- strip fw files and use kernel firmware load  
- check for wrong typecasts  
- remove/strip hardcoded `RT2870STA.dat`  
- check for wrong variable sizes (driver was for 32bit)  
- update to more USB-IDs  
- check if monitor mode is working  
- more cleanup and other stuff  
- fix compile warnings  
- misc. other stuff  


Hans Ulli Kroll <ulli.kroll@googlemail.com>




