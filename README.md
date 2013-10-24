Repository
----------
	Add Tomahawk
	Add Handbrake
	Add all known missing packages from import
	Pin all missing upstream packages
	
Infra	
-----
	Add Petra start page
	Add Petra rel notes
	Add Petra new features page
	Remove youtube from FF RSS feed ?
	rel_notes point to rel_petra_cinnamon.php
	
ISO	
---
	[Fixed] CAPS in isolinux
	[Fixed] CAPS in ISO name
	
MDM
---	
	2 mdm instances, one is fine, the other launches mdmKeepsCrashing
	Bugs with user preselection, needs testing/fixing, the greeter gets confused sometimes
	in live mode mdm shows timed login even though it's configured for automatic login... auto should superseed timed and log in immediately
	
Session issues	
--------------
	Menu->Quit proceeds to shutdown instead of showing Quit dialog
	Driver falls back to llvmpipe half of the time
	Alt+Fx switches tty...
	
Look and Feel
-------------	
	No menu borders under llvmpipe
	Gnome-terminal : semi-transparent
	Gnome-terminal : don't show menubar by default
	Mint-x-icons pull from corbin
	Update slideshow
	Cinnamon : Review default sounds
	Backgrounds : change xxRapeKxx name to rapciu
	Backgrounds : Review selection and default choice
	Background : optimize for size/quality
	Mint-themes : remove highlight on hover for checkboxes and radio buttons
	Mintupdate : update icons
	In cinnamon-settings many widgets have a darker background
	Cinnamon theme "Linux Mint", window list, selected window isn't noticeable enough        
	
Package selection
-----------------
	[Fixed] Remove lintian
	Remove yelp or hide « Help » in menu
	[Fixed] Remove gnome-control-center
	[Fixed] Remove ndisgtk
	Remove zeitgeist and activity log manager
	Remove unity
	[Fixed] Remove gparted post-install
	[Fixed] Remove olivia backgrounds
	[Fixed] Remove aptoncd
	Hide OpenJDK Java7 Policy Tool and IcedTea Web Control Panel from menus
	Remove ubuntu-system-settings
	
Missing
-------
	Mintify and pin unity-greeter
	Add cinnamon-bluetooth
	Support for Wacom tablet missing
	Add 32bit Flash support for Steam out of the box
	
System
------	
	Power button shuts down computer instead of showing quit dialog
	Yelp should be more selective to show help for selected items and redirect to linuxmint.com for others
	Add missing search engines
	xhost+ and ctrl_alt_backspace have no description in xdg autostart
	Review linux-kernel and which kernel to point to.
	Review uefi compatibility and efi boot path
	Update mint-translations
	Upgrade webkitgtk to v2.x
	Update mint-mirrors
	
Cinnamon
--------
	[Fixed in git] Notifications show 2nd string twice. Reproduce with « notify-send 'Wireless Networks Available' 'Use the network menu to connect to one of them.' »
	Cinnamon-screensaver : date is not 12H.
	[Fixed in git] Applet API : put a gap between icon and text in TextIconApplet
	[Fixed] Cinnamon-screensaver shows last used custom msg when activated by csd
	[Fixed in git] changing panel size resets the menu icon
	Cinnamon-settings : test sound doesn't work (same in gcc, probably missing a package or something)
	Show week numbers should be in calendar's settings, not in cinnamon-settings
	Calendar would be better named Date and Time and use the Faenza icon for it
	Cinnamon-settings : Firewall should be in Administration section
	Cinnamon-settings : If user is a sudoer/admin, start in advanced mode
	User applet : clicking on avatar/name should launch « cinnamon-settings user »
	update cinnamon-translations
	if an icon is used in an applet context menu item, it looks out of place and clashes in alignment with "Configure..."
	[Fixed in git] background draw faulty in VB
	panel hides during gksu dialogs

MATE
----
	nm-applet isn't started automatically
	x-caja-desktop windows bug at session start
	
GNOME/GTK
---------
	[Fixed in git] extend Canonical patch to all DE for gnome-calculator (menubar regression)
	[Fixed in git] evince downgraded to 3.6 (menu + UI regressions)
	[Fixed in git] file-roller downgraded to 3.6 (menubar)
	[Fixed in git] gnome-disk-utility downgraded to 3.0.2 (UI regression)
	[Fixed in git] gnome-system-log downgraded to 3.4 (menu + UI)
	[Fixed in git] gnome-system-monitor downgraded to 3.6 with system tab removed (menu + UI)	
	[Fixed in git] gedit icon in about dialog
	[Fixed in git] gedit generic name in menu
	gnome-terminal resets position / crashes when cinnamon restarts
	
Mint Tools
----------
	mintInstall improvements
	review pending pull requests
	Review mintWelcome look and feel
	[Fixed in git] mintwelcome crashes
