New bug reports in Linux Mint 18 BETA

All editions
------------

	Update translations
	kernel updates wipe the vbox dkms module?
	Could you update virtualbox-guest packages from Debian sid repo (5.0.2 versions) for solving 3D acceleration.
	hardware:
		Does not support Netgear A6210 wifi adapter.
		Laptop is Alienware 13′ with Skylake CPU -> touchscreen isn't working
		Laptop is Alienware 13′ with Skylake CPU -> wifi is not working
		Intel Corporation Haswell-ULT Integrated Graphics Controller --> can't boot without recovery mode
		Surface 4 Pro: Type Cover and Touchpad not working properly. Works from time to time. If I unplug the cover, both doesen't work any more.
		Surface 4 Pro: Wlan not working -&gt; tries to connect but with no success. Asking for Passprase again and again. USB Wlan Dongle works
		Surface 4 Pro: Touchscreen/pen not working
		ASRock skylake gpe6F bug: /var/log/syslog and var/log/kern.log are flooded with hundreds of gpe6F errors per second until the root partition runs out of space. Its a known issue with ASRock skylake boards. The workaround is o add [code] echo “disable” > /sys/firmware/acpi/interrupts/gpe6F [/code] to rc.local. more info at https://forums.linuxmint.com/viewtopic.php?f=49&t=223180
		Intel Dual Band Wireless-AC 7265: unsupported splx structure
		soft lookup cpu3 stuck for 22s, laptop is PE60 6QE, cpu is i7-6700HQ, vga card is Nvidia GTX 960M 2G (all worked fine in 17.3)
		HP LaserJet 5000 on parallel port – Device URI: parallel:/dev/lp0 Buffer overflow error when printing. hpcups 3.16.3. Works in Mint 13 and 15, but not in 17.x/18.
		Am testing on a lenovo w530. Bluetooth applet cant seem to pick any device. It will just display searching for devices and either provide an empty list or list devices i cannot setup. On 17.3 it worked like a charm
		3c:00.0 Network controller: Qualcomm Atheros QCA6174 802.11ac Wireless Network Adapter (rev 32), "wireless unavailable"
		Fatal resolution problem with all 16.04 derivatives https://answers.launchpad.net/ubuntu/+question/292402
		Lenovo Y700 no sound
	artwork:
		Tray icons are black with mint-y themes.
		Mint-Y themes Shade option is unavailable
		Black Themed Bar: Icons not vertically centered.
		Mint-Y needs a tiny window border or drop shadow. It can be very difficult to distinguish where one window ends and another begins.
		login screen, no user selected, username don't show up very well on some of the backgrounds

Cinnamon Edition - last processed comment: #86
----------------------------------------------
	changing desktop font size segfaults nemo
	Touch screen clicks are not working in the icon and compact view section of Nemo, everywhere else seems fine.
	Context menu “Open with>other application…” displays duplicate applications.
	I can disable mobile broadband using the switch in network preferences but it does have any effect. Next time I open up network preferences it is enabled again. I guess this could be a upstream problem though.
	white font? http://imgur.com/QBEM48H
	http://imgur.com/GdexG27
	When connecting with PEAP authentication, the network manager applet just gets stuck instead of prompting for credentials.
	cinnamon panel unresponsive when using nvidia 304 drivers?
	When using the Laptop with external Monitor, it isn’t possible to maximize windows on laptop panel. They will always maximize on the HDMI monitor instead. Same behaviour I had on my 17.3 Setup

MATE Edition - last processed comment: #142
-------------------------------------------
	network-manager | nm-applet:
		After I resume from suspend NetworkManager seems to work fine, Wifi connection is maintained, but nm-applet shows Wi-Fi Networks and other things grayed out. Running ‘pkill nm-applet’ and then ‘nm-applet’ fixes this.
		Can't join WPA network (password not being passed), 3 people have this problem
		after updates nm-applet shows ethernet icon instead of wifi for connections?
		nm connecting via WPA doesn't connect (no password passed).. using network connections to save the password -> works. Tested with MATE edition on a Lenovo Yoga 500.
		Another NetworkManager bug. Just tried to run the mint 18 MATE live on an old pc in my home and it wouldn’t recognize my Wi-Fi at all. It just looked as if I didn’t have Wi-Fi. Killing and restarting nm-applet didn’t help in this case, so the bug must be deeper. Sadly, this is a bug I’ve read about in Ubuntu MATE 16.04 so again, this might be a bug from upstream. For comparison, I had no problem of this sort when running mint cinnamon 18 live on this pc, and it is running mint Xfce (first 17.2, upgraded to 17.3) for a while and never had this problem.
	mintmenu:
		[Fixed in Git] use custom color should be disabled by default (it makes mintmenu look really bad with mint-y-dark)
		transparent only one after reboot (first click on menu). Next click menu show not transparent
		weird org.mate.panel.applet.MintMenuAppletFactory in syslog when running synaptic
	very frequent “at-spi-registryd.desktop not responding” error at reboot/shutdown and it’s associated very slow reboot/shutdown
	In the prefered applications(menu Preferences, “Prefered applications”), Caja isn’t the File manager by default. Must add it manually.
	when changing the appearance to Mint-Y-Dark the background in caja doesn’t change! you have to go to “Edit” -> “Backgrounds and Emblems” and reset it once manually. now it changes every time with the theme.

KDE Edition - last processed comment: #0
-----------------------------------------

Xfce Edition - last processed comment: #0
------------------------------------------
