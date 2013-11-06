Repository
----------
	Pin all missing upstream packages
	
Infra	
-----
	Add Petra rel notes
	Add Petra new features page
	rel_notes point to rel_petra_cinnamon.php
	rel_notes explain about apt recommends

Translations
------------
	Update cinnamon translations
	Update mint translations
	Update mint-slideshow translations
	
MDM
---		
	theme isn't completely l10n'd
	
System
------		
	EFI booth path isn't standard (EFI installation in Virtualbox works fine, but upon reboot it loses its NVRAM and isn't able to find the EFI boot files)
	Update mint-mirrors
	[Fixed] KDE apps get installed during the installation (k3b, nepomuk..etc)
	
Cinnamon
--------
	Launching keepass + xsel freezes Cinnamon [wrouesnel]	
	[Fixed in git] bg rendering delay
	[Fixed in git] squary window borders on tiled/snapped windows
	Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)

Mint Tools
----------
	mintInstall improvements
	review pending pull requests
	Review mintWelcome look and feel
	mintStick progress bar isn't fixed yet
	mintmenu show duplicates when item is in multiple categories (LibreOffice, gnome-disks)
	
MATE
----
	[Fixed] nm-applet isn't started automatically
	[Fixed] use generic names in MATE packages
	x-caja-desktop windows bug at session start --> try to apply patch: https://github.com/clefebvre/caja/commit/e916c945e86842b63e17c322b76ab47e1538c233

KDE
---
	[Fixed] In "system-config-samba" desktop file needs to use kdesudo and needs to be shown in KDE
	Add samba-mounter to new features page for KDE
	Missing comments in KDE menu items for mintinstall, mintupdate, mintstick-format and mintstick-iso

Look and Feel
-------------	
	[Fixed] Remove fuzzy border in mdm's mint-x?
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
