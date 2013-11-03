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
	Review ubuntu-updates (systemd, upower) changes

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
	[Fixed] Remove btrfs-tools and make sure ubiquity doesn't list it as an option
	EFI Installation is broken (possible leads: check if efibootmgr and grub-efi install properly)
	Update mint-mirrors	
	
Cinnamon
--------
	[Fixed] cinnamon-settings: if we're the live session user, start in advanced mode	
	[Fixed] bg drawing is buggy in VB with no 3D accel
	Launching keepass + xsel freezes Cinnamon [wrouesnel]	

Mint Tools
----------
	mintInstall improvements
	review pending pull requests
	Review mintWelcome look and feel
	mintStick progress bar isn't fixed yet
	
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
	[Fixed] Backgrounds: Review selection and default choice
	[Fixed] Background: optimize for size/quality	
	[Fixed] Added mint-x cinnamon theme
	Mintupdate: update icons



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
