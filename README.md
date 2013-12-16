Confirmed issues

KDE
---
	Upgrade note to explain about plasma-nm
	[Fixed] mintstick KDE action shows also for DVD and floppy disks	
	[Fixed] mintbackup doesn't run
	[Fixed] remove openssh
	[Fixed] network manager applet missing
	[Fixed] ~/.kde/env directory prevents login http://forums.linuxmint.com/viewtopic.php?f=109&t=143649

Xfce
----
    Xfce doesn't seem to detect DVD insertion, doesn't run VLC (works in 32bit, not 64bit)
	Can't use the trash in live mode    
	There are no GTK bookmarks by default

Mint 17
-------	
	KDE: The installer doesn't install language-pack-gnome-xx resulting in GTK apps/dialogs showing in English
	mdm: In OEM mode, MDM preselects the "oem" user (user no longer active but still present in AccountsServices) :)
	mdm: When loggin in an existing session, doesn't unlock kde screensaver, xscreensaver or gnome-screensaver (works fine with cinnamon-screensaver and mate-screensaver)
	mdm: dep on numlockx... when numlockx gets installed it activates numlock. Cinnamon remembers that state. On laptop this results in the inability to login or to use some keys on the keyboard. not all laptops have an obvious num lock indicator/switch. Consider removing that feature or enabling it as an opt-in. Right now, although the feature is disabled by default, it does bring numlockx as a dependency.
	system: switch to adobe-flashplugin
	banshee: use mp3 decoding by default
	cinnamon: enable touchpad tapping by default
	mintbackup, mintnanny, mintupload, mintdrivers, mintsources: remove KDE adjustment, add a specific KDE .desktop file
	mintdesktop: When Compiz is active with MATE, WM preferences have to go to Metacity gconf settings instead of Marco ones to work.
	mintdrivers: should we re-add a systray icon to notify users at session startup?
	consider using https instead of http for Amazon queries			
