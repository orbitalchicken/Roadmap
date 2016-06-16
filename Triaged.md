Triaged reports

Not a bug
---------
	nmap scan found the microsoft-ds ports, open 445 (samba)
	cinnamon: Notifications always appear in the panel even though they are disabled.



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
	mdm: Auto login fails (After testing, it works both from installer and from Login Window. Might not be obvious to users that they can't be auto-logged in if their home dir is encrypted..)
	cinnamon: When using the Laptop with external Monitor, it isn’t possible to maximize windows on laptop panel. They will always maximize on the HDMI monitor instead. Same behaviour I had on my 17.3 Setup
	Can't switch sound to HDMI

Upstream
--------
	grub: 32bit version doesn’t support 32bit UEFI
	samba: ‘Failed to retrieve share list from server’
	gtk (levelbar): Microphone level meter has color reverse. Shows red when low level and green when picking at high level. This is with build in microphone on Lenovo Carbon X1 4th generation 2016.