Confirmed issues

Mint 17
-------	
	KDE: The installer doesn't install language-pack-gnome-xx resulting in GTK apps/dialogs showing in English
	mdm: In OEM mode, MDM preselects the "oem" user (user no longer active but still present in AccountsServices) :)
	mdm: When loggin in an existing session, doesn't unlock kde screensaver, xscreensaver or gnome-screensaver (works fine with cinnamon-screensaver and mate-screensaver)
	mdm: dep on numlockx... when numlockx gets installed it activates numlock. Cinnamon remembers that state. On laptop this results in the inability to login or to use some keys on the keyboard. not all laptops have an obvious num lock indicator/switch. Consider removing that feature or enabling it as an opt-in. Right now, although the feature is disabled by default, it does bring numlockx as a dependency.
	mdm: Allow logins without a password? http://forums.linuxmint.com/viewtopic.php?f=90&t=127829 --- check lightdm's postinst, it creates the nopasswdlogin user group
	mdm: should depend on mdm-themes... in Mint, we should use our themes, so make mint-mdm-themes provide mdm-themes.
	mdm: When the specified theme isn't found, don't default to circles, use the GTK greeter!
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
	mintmenu: panel applet transparency
	mintsources: consider changing the way opt-in works for romeo and backport
	cinnamon: add major version deps on various components (libmuffin in particular)
	cinnamon: consider using "XDG_MENU_PREFIX=cinnamon- alacarte" instead of cme - coordinate with upstream to get cme improvements into alacarte
	cinnamon-bluetooth: bring compatibility to GNOME 3.10
	