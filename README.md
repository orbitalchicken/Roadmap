Confirmed issues

KDE
---
	rel_notes: Add samba-mounter to new features page for KDE
	[Fixed] mintstick KDE action shows also for DVD and floppy disks
	[Fixed] Mint bgs authors should be "Linux Mint"
	[Fixed] bgs capitalization
	[Fixed] mintinstall: in app view, main icon can be huge (check filezilla for instance)
	[Fixed] icons: use oxymentary instead of oxygen
	[Fixed] apps sorted alphabetically in menu
	[Fixed] menu -> show apps by name
	[Fixed] add libreoffice
	[Fixed] mintbackup in menu

Xfce
----
    Xfce doesn't seem to detect DVD insertion, doesn't run VLC
	Can't use the trash in live mode
    [Fixed] gnome-screensaver is installed and should be removed    
    [Fixed] Missing space char in volume ID
    [Fixed] Thunar now features a delete option, we no longer need "Permanently Remove".    
    [Fixed] catfish missing
    [Fixed] remove print thunar action
    [Fixed] use std md5 action

Mint 17
-------	
	mdm: In OEM mode, MDM preselects the "oem" user (user no longer active but still present in AccountsServices) :)
	mdm: When loggin in an existing session, doesn't unlock kde screensaver, xscreensaver or gnome-screensaver (works fine with cinnamon-screensaver and mate-screensaver)
	system: switch to adobe-flashplugin
	banshee: use mp3 decoding by default
	cinnamon: enable touchpad tapping by default
	mintbackup, mintnanny, mintupload, mintdrivers, mintsources: remove KDE adjustment, add a specific KDE .desktop file
	mintdesktop: When Compiz is active with MATE, WM preferences have to go to Metacity gconf settings instead of Marco ones to work.
