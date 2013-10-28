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
	[Fixed] Backgrounds : change xxRapeKxx name to rapciu
	Mint-x-icons pull from corbin
	Update slideshow
	Cinnamon : Review default sounds	
	Backgrounds : Review selection and default choice
	Background : optimize for size/quality
	Mint-themes : remove highlight on hover for checkboxes and radio buttons
	Mintupdate : update icons
	In cinnamon-settings many widgets have a darker background
	Cinnamon theme "Linux Mint", window list, selected window isn't noticeable enough   
	mint-themes-gtk3: No padding in context menu leads to accidental operations     
	dialog windows use symbolic icons (to reproduce: connect to ssh in terminal, close terminal)
	
Missing
-------
	Mintify and pin unity-greeter	
	
System
------	
	[Fixed] remove gnome-session-common
	[Fixed] ll alias to ls
	[Fixed] ls colors? https://github.com/linuxmint/community.linuxmint.com/issues/120
	[Fixed] ctrl_alt_backspace have no description in xdg autostart
	[Fixed] remove xhost+?
	[Fixed] Yelp should be more selective to show help for selected items and redirect to linuxmint.com for others
	[Fixed] Power button shuts down computer instead of showing quit dialog (in /etc/acpi/powerbtn.sh, the file checks for gnome-settings-daemon... add support for MATE and Cinnamon there	
	Upgrade webkitgtk to v2.x	
	Add missing search engines
	Review linux-kernel and which kernel to point to.
	Review uefi compatibility and efi boot path
	Update mint-translations	
	Update mint-mirrors
	Priority 700 for ppas and known 3rd party sources (getdeb, mate-desktop?)	
	Move adjustment for ATI amdccle from KDE to all editions?	
	Add libimobiledevice-utils and ifuse?	
	
Cinnamon
--------
	[Fixed] cinnamon-bluetooth desktop file uses wrong icon
	[Fixed] cinnamon-session-properties isn't visible in the menu (missing desktop file?)
	[Fixed] Cinnamon-screensaver : date is not 12H.
	cinnamon-settings: if we're the live session user, start in advanced mode	
	update cinnamon-translations
	Pixelated alt-tab icon for mintupload file-uploader
	snapped/tiled window keep rounded corners against the edge
	Launching keepass + xsel freezes Cinnamon [wrouesnel]	
	bg drawing is buggy in VB with no 3D accel
	
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
	[Fixed] gnome-screenshot has a broken help button, remove it
	
Mint Tools
----------
	mintInstall improvements
	review pending pull requests
	Review mintWelcome look and feel
	mintStick progress bar isn't fixed yet

Might not happen (de-scope?)
----------------------------	
	Support for Wacom tablet

De-scoped
---------
	gksu covers cinnamon panel and clutter layer (offending code is in libgksu, won't fix, likely to migrate to pkexec instead)
	GTK dialogs use symbolic icons (offending code is in GTK, won't fix. Small issue but linked to GTK3 becoming a GNOME Shell specific toolkit. Long run decision on whether to patch/freeze gtk or to migrate to a fork/alternative toolkit. No action taken in this cycle.)
	gnome-calculator menubar (minor cosmestic issue, won't fix)