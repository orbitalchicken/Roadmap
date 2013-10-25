Repository
----------
	Add Tomahawk
	Add Handbrake
	Add all known missing packages from import
	Pin all missing upstream packages
	
Infra	
-----
	Add Petra rel notes
	Add Petra new features page
	rel_notes point to rel_petra_cinnamon.php
	
MDM
---	
	[Fixed] 2 mdm instances, one is fine, the other launches mdmKeepsCrashing
	Bugs with user preselection, needs testing/fixing, the greeter gets confused sometimes

Possibly fixed by latest MDM (need to reproduce again)
-------------------------------------------------------
	In live mode mdm shows timed login even though it's configured for automatic login... auto should superseed timed and log in immediately
	No sound in session
	Menu->Quit proceeds to shutdown instead of showing Quit dialog
	Driver falls back to llvmpipe half of the time
	Alt+Fx switches tty...	
	
Look and Feel
-------------	
	No menu borders under llvmpipe	
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
	
Missing
-------
	[Fixed] Add cinnamon-bluetooth
	[Fixed] Add 32bit Flash support for Steam out of the box
	[Fixed] Add lintian (gdebi shows the lintian tab whether it's installed or not, so better show techie info than an error message)
	Mintify and pin unity-greeter
	Support for Wacom tablet missing	
	
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
	[Fixed] Show week numbers should be in calendar's settings, not in cinnamon-settings
	[Fixed] Cinnamon-settings : Firewall should be in Administration section
	[Fixed] Cinnamon-settings : If user is a sudoer/admin, start in advanced mode
	[Fixed] User applet : clicking on avatar/name should launch « cinnamon-settings user »
	[Fixed] Calendar would be better named Date and Time and use the Faenza icon for it
	[Fixed] if an icon is used in an applet context menu item, it looks out of place and clashes in alignment with "Configure..."	
	[Fixed] Cinnamon-settings : test sound doesn't work (same in gcc, probably missing a package or something)	
	[Fixed] Draw the background twice when launching session (immediately and then 3 sec later).
	[Fixed] Add icons to default applet context menu items
	Cinnamon-screensaver : date is not 12H.		
	update cinnamon-translations	
	panel hides during gksu dialogs
	mintupload file-uploader icon in alt-tab is pixelated
	snapped/tiled window keep rounded corners against the edge
	Launching keepass + xsel freezes Cinnamon [wrouesnel]	
	cinnamon-session-properties isn't visible in the menu (missing desktop file?)
	
MATE
----
	[Fixed] nm-applet isn't started automatically
	[Fixed] use generic names in MATE packages
	x-caja-desktop windows bug at session start	

KDE
---
	[Fixed] In "system-config-samba" desktop file needs to use kdesudo and needs to be shown in KDE
	Add samba-mounter to new features page for KDE
	Missing comments in KDE menu items for mintinstall, mintupdate, mintstick-format and mintstick-iso
	
GNOME/GTK
---------
	[Fixed] menubar in gnome-calculator
	[Fixed] gnome-terminal resets position / crashes when cinnamon restarts
	[Fixed] gnome-terminal : semi-transparent
	[Fixed] gnome-terminal : don't show menubar by default
	[Fixed] evince should be in accessories, not graphics and not office
	
Mint Tools
----------
	mintInstall improvements
	review pending pull requests
	Review mintWelcome look and feel
	