Triaged reports

Not a bug
---------
	nmap scan found the microsoft-ds ports, open 445 (samba)
	cinnamon: Notifications always appear in the panel even though they are disabled.
	cinnamon: Update shield became so small --> will move to new libindicator eventually

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
	mate-notification: “connection established..” message always on front. no way to close