Repository
----------
	Add Tomahawk
	Add Handbrake
	Add all known missing packages from import
	Pin all missing upstream packages
	Mintify and pin unity-greeter
	
Infra	
-----
	Add Petra rel notes
	Add Petra new features page
	rel_notes point to rel_petra_cinnamon.php

Translations
------------
	Update cinnamon translations
	Update mint translations
	Update mint-slideshow translations
	
MDM
---	
	Bugs with user preselection, needs testing/fixing, the greeter gets confused sometimes
	In live mode mdm shows timed login even though it's configured for automatic login... auto should superseed timed and log in immediately
	New theme + remove cloudGL
	
System
------	
	[Fixed] Power button shuts down computer instead of showing quit dialog 
	[Fixed] Power button action should be ask by default
	[Fixed] Yelp shows debug notification
	[Fixed] Yelp doesn't work for ghelp:gedit
	[Fixed] Add libimobiledevice-utils, ideviceinstaller and ifuse
	[Fixed] Priority 700 for ppas and known 3rd party sources (getdeb, mate-desktop?)
	Add missing search engines
	Review uefi compatibility and efi boot path
	Update mint-mirrors	
	
Cinnamon
--------
	cinnamon-settings: if we're the live session user, start in advanced mode	
	Launching keepass + xsel freezes Cinnamon [wrouesnel]
	bg drawing is buggy in VB with no 3D accel

Mint Tools
----------
	[Fixed in Git] Pixelated alt-tab icon for mintupload file-uploader	
	mintInstall improvements
	review pending pull requests
	Review mintWelcome look and feel
	mintStick progress bar isn't fixed yet
	
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

Look and Feel
-------------	
	[Fixed] Update slideshow
	[Fixed] In cinnamon-settings many widgets have a darker background
	[Fixed] Cinnamon : Review default sounds	
	Backgrounds : Review selection and default choice
	Background : optimize for size/quality
	Mint-themes : remove highlight on hover for checkboxes and radio buttons
	Mintupdate : update icons
	Cinnamon theme "Linux Mint", window list, selected window isn't noticeable enough
	mint-themes-gtk3: No padding in context menu leads to accidental operations

Need to reproduce again
-----------------------
	No sound in session (seems fixed by MDM)
	Menu->Quit proceeds to shutdown instead of showing Quit dialog (seems fixed by MDM)
	Driver falls back to llvmpipe half of the time (seems fixed by MDM)
	Alt+Fx switches tty...	(seems fixed by MDM)
	Segfault in MDMWebkit when repeatedly switching languages (Fixed in Mint 15 by upgrading webkitgtk to v2.x, doesn't seem to happen in Mint 16)

De-scoped
---------
	gksu covers cinnamon panel and clutter layer (offending code is in libgksu, won't fix, likely to migrate to pkexec instead)
	GTK dialogs use symbolic icons (offending code is in GTK, won't fix. Small issue but linked to GTK3 becoming a GNOME Shell specific toolkit. Long run decision on whether to patch/freeze gtk or to migrate to a fork/alternative toolkit. No action taken in this cycle.)
	gnome-calculator menubar (minor cosmestic issue, won't fix)
	Support for Wacom tablet (configurable via the command line, will need to join forces with Xfce/MATE if we want to develop a cross DE UI. This doesn't justify pulling resources to make a Cinnamon specific solution)
	Snapped/tiled window keep rounded corners against the edge (2.2)
