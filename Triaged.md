Triaged reports

Not a bug
---------
	nmap scan found the microsoft-ds ports, open 445 (samba)
	cinnamon: Notifications always appear in the panel even though they are disabled.
	cinnamon: Update shield became so small --> will move to new libindicator eventually
	mate: https://github.com/mate-desktop/caja/issues/569
	libmad0 is illegal in the U.S. and Japan --> No it's not (https://gstreamer.freedesktop.org/data/doc/gstreamer/head/faq/html/chapter-legal.html)
	installing HP Linux Printing Service HPLIP. It wants a library item libtool, which is already installed (I did sudo apt-get install libtool to verify). The HPLIP site is http://hplipopensource.com/hplip-web/index.html --> already packaged and installed by default in Mint 18.

Outside of the scope
--------------------
	xplayer + marco: while in full screen mode does not play video smoothly (use compton + mpv for better performance)
	mate clock applet: font and color is not customizable

Can't reproduce
---------------
	Videos (Xplayer) window cannot be maximized (other windows can);
	mate: snap terminal right (ie drag to take up the right half of the screen) and the text is too far to the left to read the first character in each line.
	mate: control Center > Keyboard > Layouts “Choose a layout” window is gigantic and unresizable
	mate: Firefox Search Engines are missing and cannot add new one. In Cinnamon that works ok.
	mintmenu: when I install a piece of software it doesn’t show up until I log out from the desktop session and log back again, is it something normal or not?
	mozo: sliding an entry between a submenu to another crashes the menu editor and corrupts the menu (all applications disappear). Same problem when deleting a shortcut in the “other” submenu.
	mate: Mate System Monitor was not visible in any of the Mate menus in my installation. It was however accessible through mate-system-monitor command. “apt reinstall mate-system-monitor” solved the problem (application showed up in the menus).
	Steam will not work at all in MATE.
	cinnamon: Battery applet seems to stay at ‘charged ‘ even after power cord is removed, it MAY stay showing on charge or it may show on battery, its unpredictable.
	mintlocale: Tried adding support for iBus and FCITX (in Languages > Input Method) -> broken packages
	cinnamon: When using the Laptop with external Monitor, it isn’t possible to maximize windows on laptop panel. They will always maximize on the HDMI monitor instead. Same behaviour I had on my 17.3 Setup
	Can't switch sound to HDMI
	In /boot, Memtest86+ version is 4.20 but the last version of Memtest86+ is 5.10. (version is 5.01, like in the repositories)
	in the new ubuntu 16.04, touchegg works with 3 finger gestures, if I put synclient disable ClickFinger3 & TapButton3, however, in linux mint it’s not recognizing it..! (seems to work more or less, need more accurate issue description)
	cinnamon: I can disable mobile broadband using the switch in network preferences but it does have any effect. Next time I open up network preferences it is enabled again. I guess this could be a upstream problem though.
	Why did you change from Noto Sans to Noto Sans Regular? Letters now look short and stretched. They are much more elegant on 17.3. (some tools went from GTK2 to GTK3, noto changed slightly, other than that...?)
	cinnamon panel unresponsive when using nvidia 304 drivers?
	mintinstall http://imgur.com/a/oh56T
	mint-y update issue: http://imgur.com/a/B14wG
	mdm: autologin fails randomly (race condition at boot time?)
	kernel updates wipe the vbox dkms module?

Upstream
--------
	grub: 32bit version doesn’t support 32bit UEFI
	samba: ‘Failed to retrieve share list from server’
	gtk (levelbar): Microphone level meter has color reverse. Shows red when low level and green when picking at high level. This is with build in microphone on Lenovo Carbon X1 4th generation 2016.
	gdebi: http://oi66.tinypic.com/2s9yqg5.jpg (https://bugs.launchpad.net/ubuntu/+source/gdebi/+bug/1581425)
	libgtksourceview: in xed with the classic and default (tango) color-scheme there is nearly no differentiation (color or border) between the text and the line-numbers; and at the latest working on a file with numbers at the beginning of the lines this is a disaster.
	mate: In the prefered applications(menu Preferences, “Prefered applications”), Caja isn’t the File manager by default. Must add it manually.
	caja: I can’t find hidden files in Caja file manager.
	caja: I noticed that search result doesn’t appear till the end of search, this may take some time. it would be nice to improve search behavior like the search in nautilus so that the search results in the current folder appears instantly.
	mate-control-center: when using ‘Mint-Y-Dark’ theme, and then pressing an item in the ‘Groups’ menu (such as ‘Hardware’), it paints the group-block in a very light-green color, so the white text is not readable.
	mate-control-center: install gnome-system-tools, items aren't l10nd.
	mate-notification: “connection established..” message always on front. no way to close
	mate-panel lacks borders: https://github.com/mate-desktop/mate-panel/issues/344
	mate: If a launcher is created from the desktop of type “application in terminal”, any command and attempting to execute the launcher results in the following error: “Details: Failed to execute child process “xterm” (No such file or directory)”
	intel: mouse cursor disappears (switch user with mdmflexiserver, log back in) https://bugs.launchpad.net/ubuntu/+source/xserver-xorg-video-intel/+bug/1568604
	Printer driver requires "lsb" package https://bugs.launchpad.net/ubuntu/+source/lsb/+bug/1536353 (being fixed upstream)
	hardware:
		Surface Pro: Type cover/touchpad/Touchscreen/pen not working -> https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1504618
		Fatal resolution problem with all 16.04 derivatives https://answers.launchpad.net/ubuntu/+question/292402
		Qualcomm Atheros QCA6174 802.11ac Wireless Network Adapter (rev 32), "wireless unavailable" --> https://bugs.launchpad.net/ubuntu/+source/linux-firmware/+bug/1520343
		Ethernet - no connection - Realtek Semiconductor Co., Ltd. RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller (rev 0c) --> http://askubuntu.com/questions/763080/no-wifi-in-qualcom-atheros-ubuntu-16-04-acer-aspire-e-15
		Does not support Netgear A6210 wifi adapter.
		WIFI issues with RTL8191SU (Rosewill-Wireless Lan-USB 2.0 Adapter-Model No. RNX-N180UBE)-(LSUSB-Bus 005 Device 003: ID 0bda:8172 Realtek Semiconductor Corp. RTL8191SU 802.11n WLAN Adapter)
		Bluetooth on Lenovo w530. Bluetooth applet cant seem to pick any device. It will just display searching for devices and either provide an empty list or list devices i cannot setup. On 17.3 it worked like a charm
		Lenovo Y700 no sound
		Onboard audio for an Intel DQ965GF motherboard is not working.
		No sound (worked in 17.3): Audio: Card-1 Intel 8 Series/C220 Series High Definition Audio Controller, driver: snd_hda_intel bus-ID: 00:1b.0 Sound: Advanced Linux Sound Architecture v: k4.4.0-24-generic
		My mic is not working. Lenovo C-440
		HP LaserJet 5000 on parallel port – Device URI: parallel:/dev/lp0 Buffer overflow error when printing. hpcups 3.16.3. Works in Mint 13 and 15, but not in 17.x/18.
		suspend: Lenovo G50 80, core i5 broadwell, 2.2 ghz, GPU AMD Radeon 2GB, 500GB SSHD and 12GB of RAM. -> can't suspend -> black screen and never wakes up.
		Intel Corporation Haswell-ULT Integrated Graphics Controller --> can't boot without recovery mode
		Dell Inspiron 15  i7-6700HQ Processor 6th Generation Intel Core (Skylake) 16 GB memory 128 GB SSD + 1TB HDD -> boots to black screen
		soft lookup cpu3 stuck for 22s, laptop is PE60 6QE, cpu is i7-6700HQ, vga card is Nvidia GTX 960M 2G (all worked fine in 17.3) (works with (acpi=off))