New bug reports in Linux Mint 18 BETA

All editions
------------

	Update translations
	Does not support Netgear A6210 wifi adapter.
	mintbackup just hangs indefinitely when you try to restore software selection, terminal has no output, and mintbackup is using no cpu.
	nm connecting via WPA doesn't connect (no password passed).. using network connections to save the password -> works. Tested with MATE edition on a Lenovo Yoga 500.
	Laptop is Alienware 13′ with Skylake CPU -> touchscreen isn't working
	Laptop is Alienware 13′ with Skylake CPU -> wifi is not working
	nmap scan found the microsoft-ds ports, open 443
	login screen, no user selected, username don't show up very well on some of the backgrounds
	Intel Corporation Haswell-ULT Integrated Graphics Controller --> can't boot without recovery mode
	Black Themed Bar: Icons not vertically centered.
	Surface 4 Pro: Type Cover and Touchpad not working properly. Works from time to time. If I unplug the cover, both doesen't work any more.
	Surface 4 Pro: Wlan not working -&gt; tries to connect but with no success. Asking for Passprase again and again. USB Wlan Dongle works
	Surface 4 Pro: Touchscreen/pen not working
	Mint-Y needs a tiny window border or drop shadow. It can be very difficult to distinguish where one window ends and another begins.
	ASRock skylake gpe6F bug: /var/log/syslog and var/log/kern.log are flooded with hundreds of gpe6F errors per second until the root partition runs out of space. Its a known issue with ASRock skylake boards. The workaround is o add [code] echo “disable” > /sys/firmware/acpi/interrupts/gpe6F [/code] to rc.local. more info at https://forums.linuxmint.com/viewtopic.php?f=49&t=223180
	kernel updates wipe the vbox dkms module?
	Intel Dual Band Wireless-AC 7265: unsupported splx structure
	soft lookup cpu3 stuck for 22s, laptop is PE60 6QE, cpu is i7-6700HQ, vga card is Nvidia GTX 960M 2G (all worked fine in 17.3)
	Mint-Y themes Shade option is unavailable

Cinnamon Edition - last processed comment: #64
----------------------------------------------
	changing desktop font size segfaults nemo
	Touch screen clicks are not working in the icon and compact view section of Nemo, everywhere else seems fine.
	Context menu “Open with>other application…” displays duplicate applications.
	I can disable mobile broadband using the switch in network preferences but it does have any effect. Next time I open up network preferences it is enabled again. I guess this could be a upstream problem though.
	white font? http://imgur.com/QBEM48H
	http://imgur.com/GdexG27
	When connecting with PEAP authentication, the network manager applet just gets stuck instead of prompting for credentials.
	cinnamon panel unresponsive when using nvidia 304 drivers?
	Microphone level meter has color reverse. Shows red when low level and green when picking at high level. This is with build in microphone on Lenovo Carbon X1 4th generation 2016.

MATE Edition - last processed comment: #41
------------------------------------------

	mintmenu: use custom color should be disabled by default (it makes mintmenu look really bad with mint-y-dark)
	Control Center > Keyboard > Layouts “Choose a layout” window is gigantic and unresizable?
	panel applet which let us know the CPU and HDD/SSD devices’ temperature?
	Videos (xplayer), while in full screen mode does not play video smoothly, i.e. it has delays. I tried it with my favorite Korean drama in MP4 format. (placed in MATE because it could be due to the WM-fullscreen)
	After I resume from suspend NetworkManager seems to work fine, Wifi connection is maintained, but nm-applet shows Wi-Fi Networks and other things grayed out. Running ‘pkill nm-applet’ and then ‘nm-applet’ fixes this.

KDE Edition - last processed comment: #0
-----------------------------------------

Xfce Edition - last processed comment: #0
------------------------------------------
