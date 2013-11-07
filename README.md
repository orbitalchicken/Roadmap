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
	
System
------		
	[Fixed] KDE apps get installed during the installation (k3b, nepomuk..etc)
	EFI booth path isn't standard (EFI installation in Virtualbox works fine, but upon reboot it loses its NVRAM and isn't able to find the EFI boot files)
	Update mint-mirrors	
	
Cinnamon
--------
		
	[Fixed in git] bg rendering delay
	[Fixed in git] squary window borders on tiled/snapped windows
	[Fixed in Git] tiled window keep rounded corners
	Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)
	

Mint Tools
----------
	[Fixed] Pixelated alt-tab icon for mintupload file-uploader
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
	
De-scoped
---------		
	Cinnamon: Launching keepass + xsel freezes Cinnamon [wrouesnel] (unknown cause/solution)	
	GTK3: dialogs use symbolic icons (offending code is in GTK3, won't fix. Small issue but linked to GTK3 becoming a GNOME Shell specific toolkit.)
	GTK3: No padding in context menu leads to accidental operations (bug reported upstream in GTK3, temp workaround/fix unlikely/tedious)
	GNOME: gnome-calculator menubar (minor cosmestic issue, won't fix)
	System: gksu covers cinnamon panel and clutter layer (offending code is in libgksu, won't fix, likely to migrate to pkexec instead)
	System: Support for Wacom tablet (configurable via the command line, will need to join forces with Xfce/MATE if we want to develop a cross DE UI. This doesn't justify pulling resources to make a Cinnamon specific solution)	
	MDM: l10n doesn't cover new features (MDM 1.4 is still using the l10n it inherited from GDM. Decision was taken to migrate MDM entirely to Mint/LP translations in 1.6, not just mdmwebkit/mdmsetup).
