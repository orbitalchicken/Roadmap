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
	mint-themes-gtk3: No padding in context menu leads to accidental operations     
	nemo: when renaming a file, the extension is hard to read
	dialog windows use symbolic icons (to reproduce: connect to ssh in terminal, close terminal)
	
Package selection
-----------------
	[Fixed] Remove lintian
	[Fixed] Remove gnome-control-center
	[Fixed] Remove ndisgtk
	[Fixed] Remove gparted post-install
	[Fixed] Remove olivia backgrounds
	[Fixed] Remove aptoncd
	[Fixed] Remove yelp or hide « Help » in menu	
	[Fixed] Remove zeitgeist and activity log manager
	[Fixed] Remove unity	
	[Fixed] Hide OpenJDK Java7 Policy Tool and IcedTea Web Control Panel from menus
	[Fixed] Remove ubuntu-system-settings
	
Missing
-------
	Mintify and pin unity-greeter
	Add cinnamon-bluetooth
	Support for Wacom tablet missing
	Add 32bit Flash support for Steam out of the box
	
System
------	
	Power button shuts down computer instead of showing quit dialog (in /etc/acpi/powerbtn.sh, the file checks for gnome-settings-daemon... add support for MATE and Cinnamon there)
	Yelp should be more selective to show help for selected items and redirect to linuxmint.com for others
	Add missing search engines
	xhost+ and ctrl_alt_backspace have no description in xdg autostart
	Review linux-kernel and which kernel to point to.
	Review uefi compatibility and efi boot path
	Update mint-translations
	Upgrade webkitgtk to v2.x
	Update mint-mirrors
	command-not-found looks in /etc/apt/sources.list, should be fixed
	Priority 700 for ppas and known 3rd party sources (getdeb, mate-desktop?)
	ll alias to ls
	Move adjustment for ATI amdccle from KDE to all editions?
	ls colors? https://github.com/linuxmint/community.linuxmint.com/issues/120
	Add libimobiledevice-utils and ifuse?
	
Cinnamon
--------
	[Fixed] Notifications show 2nd string twice. Reproduce with « notify-send 'Wireless Networks Available' 'Use the network menu to connect to one of them.' »
	[Fixed] Applet API : put a gap between icon and text in TextIconApplet
	[Fixed] changing panel size resets the menu icon
	[Fixed] background draw faulty in VB
	[Fixed] Cinnamon-screensaver shows last used custom msg when activated by csd
	Cinnamon-screensaver : date is not 12H.	
	Cinnamon-settings : test sound doesn't work (same in gcc, probably missing a package or something)
	[Fixed in git] Show week numbers should be in calendar's settings, not in cinnamon-settings
	Calendar would be better named Date and Time and use the Faenza icon for it
	[Fixed in git] Cinnamon-settings : Firewall should be in Administration section
	[Fixed in git] Cinnamon-settings : If user is a sudoer/admin, start in advanced mode
	User applet : clicking on avatar/name should launch « cinnamon-settings user »
	update cinnamon-translations
	if an icon is used in an applet context menu item, it looks out of place and clashes in alignment with "Configure..."	
	panel hides during gksu dialogs
	mintupload file-uploader icon in alt-tab is pixelated
	snapped/tiled window keep rounded corners against the edge

MATE
----
	[Fixed] nm-applet isn't started automatically
	x-caja-desktop windows bug at session start
	use generic names in MATE packages

KDE
---
	In "system-config-samba" desktop file needs to use kdesudo and needs to be shown in KDE
	
GNOME/GTK
---------
	[Fixed] extend Canonical patch to all DE for gnome-calculator (menubar regression)
	[Fixed] evince downgraded to 3.6 (menu + UI regressions)
	[Fixed] file-roller downgraded to 3.6 (menubar)	
	[Fixed] gnome-system-log downgraded to 3.4 (menu + UI)
	[Fixed] gnome-system-monitor downgraded to 3.6 with system tab removed (menu + UI)	
	[Fixed] gedit icon in about dialog
	[Fixed] gedit generic name in menu
	gnome-terminal resets position / crashes when cinnamon restarts
	
Mint Tools
----------
	[Fixed] mintwelcome crashes
	mintInstall improvements
	review pending pull requests
	Review mintWelcome look and feel
	