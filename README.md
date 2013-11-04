Repository
----------
	Pin all missing upstream packages
	[Fixed] Mintify and pin unity-greeter
	
Infra	
-----
	Add Petra rel notes
	Add Petra new features page
	rel_notes point to rel_petra_cinnamon.php
	Make sure firefox and firefox-locale-xx match post-install (Live features FF 25, FF-locale-en 25, cache thinks FF-locale-fr is at 24)

Translations
------------
	Update cinnamon translations
	Update mint translations
	Update mint-slideshow translations
	
MDM
---	
	Bugs with user preselection, needs testing/fixing, the greeter gets confused sometimes
	New theme + remove cloudGL	
	
System
------	
	[Fixed] Remove btrfs support in ubiquity
	[Fixed] EFI: Set GRUB_DISTRIBUTOR to Ubuntu
	[Fixed] Switch DDG to HTTPS
	Check EFI booth path
	Update mint-mirrors	
	
Cinnamon
--------
	Launching keepass + xsel freezes Cinnamon [wrouesnel]	

Mint Tools
----------
	mintInstall improvements
	review pending pull requests
	Review mintWelcome look and feel
	[Fixed] mintStick progress bar isn't fixed yet
	
MATE
----
	nm-applet isn't started automatically
	use generic names in MATE packages
	x-caja-desktop windows bug at session start	

KDE
---
	[Fixed] In "system-config-samba" desktop file needs to use kdesudo and needs to be shown in KDE
	Add samba-mounter to new features page for KDE
	Missing comments in KDE menu items for mintinstall, mintupdate, mintstick-format and mintstick-iso

Look and Feel
-------------	
	Mintupdate: update icons
	[Fixed] cinnamon-themes: don't use OFF/ON switches



Need to reproduce again
-----------------------
	No sound in session (seems fixed by MDM)
	Menu->Quit proceeds to shutdown instead of showing Quit dialog (seems fixed by MDM)
	Driver falls back to llvmpipe half of the time (seems fixed by MDM)
	Alt+Fx switches tty...	(seems fixed by MDM)	

Minor
-----
	Pixelated alt-tab icon for mintupload file-uploader
	mint-themes-gtk3: No padding in context menu leads to accidental operations

De-scoped
---------	
	gksu covers cinnamon panel and clutter layer (offending code is in libgksu, won't fix, likely to migrate to pkexec instead)
	GTK dialogs use symbolic icons (offending code is in GTK, won't fix. Small issue but linked to GTK3 becoming a GNOME Shell specific toolkit. Long run decision on whether to patch/freeze gtk or to migrate to a fork/alternative toolkit. No action taken in this cycle.)
	gnome-calculator menubar (minor cosmestic issue, won't fix)
	Support for Wacom tablet (configurable via the command line, will need to join forces with Xfce/MATE if we want to develop a cross DE UI. This doesn't justify pulling resources to make a Cinnamon specific solution)
	Snapped/tiled window keep rounded corners against the edge (2.2)
