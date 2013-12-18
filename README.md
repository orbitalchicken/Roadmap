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
    [Fixed] icons on the desktop have black font…and when I use a dark background I don’t see the text	
    [Fixed] Add xscreensaver-gl xscreensaver-gl-extra xscreensaver-data-extra
    [Fixed] ‘Super’ button does not open whisker menu. (add a shortcut to xfce4-popup-whiskermenu command)			
    [Fixed]: switch to system-wide configuration set 
	
Mint 17
-------	
	KDE: The installer doesn't install language-pack-gnome-xx resulting in GTK apps/dialogs showing in English
	mdm: In OEM mode, MDM preselects the "oem" user (user no longer active but still present in AccountsServices) :)
	mdm: When loggin in an existing session, doesn't unlock kde screensaver, xscreensaver or gnome-screensaver (works fine with cinnamon-screensaver and mate-screensaver)
	mdm: dep on numlockx... when numlockx gets installed it activates numlock. Cinnamon remembers that state. On laptop this results in the inability to login or to use some keys on the keyboard. not all laptops have an obvious num lock indicator/switch. Consider removing that feature or enabling it as an opt-in. Right now, although the feature is disabled by default, it does bring numlockx as a dependency.
	mdm: Allow logins without a password? http://forums.linuxmint.com/viewtopic.php?f=90&t=127829 --- check lightdm's postinst, it creates the nopasswdlogin user group
	mdm: should depend on mdm-themes... in Mint, we should use our themes, so make mint-mdm-themes provide mdm-themes.
	system: switch to adobe-flashplugin
	banshee: use mp3 decoding by default
	cinnamon: enable touchpad tapping by default
	mintbackup, mintnanny, mintupload, mintdrivers, mintsources: remove KDE adjustment, add a specific KDE .desktop file
	mintdesktop: When Compiz is active with MATE, WM preferences have to go to Metacity gconf settings instead of Marco ones to work.
	mintdrivers: should we re-add a systray icon to notify users at session startup?
	consider using https instead of http for Amazon queries			
	ubiquity: https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1038522
	cinnamon: option to disable HUD	
	xfce: doesn't seem to detect DVD insertion, doesn't run VLC (works in 32bit, not 64bit)
	xfce: Can't use the trash in live mode
	xfce: There are no GTK bookmarks by default