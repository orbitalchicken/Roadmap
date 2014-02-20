
Mint 17
-------	
	KDE: The installer doesn't install language-pack-gnome-xx resulting in GTK apps/dialogs showing in English
	mdm: When loggin in an existing session, doesn't unlock kde screensaver, xscreensaver or gnome-screensaver (works fine with cinnamon-screensaver and mate-screensaver)	 
	mdm: should depend on mdm-themes... in Mint, we should use our themes, so make mint-mdm-themes provide mdm-themes.
	mdm, upstart: Add a start condition on plymouth-ready, and drop conditions already handled by plymouth-splash (LP: #982889)?
	system: switch to adobe-flashplugin
	banshee: use mp3 decoding by default	
	mintbackup, mintnanny, mintupload, mintdrivers, mintsources: remove KDE adjustment, add a specific KDE .desktop file
	mintdesktop: When Compiz is active with MATE, WM preferences have to go to Metacity gconf settings instead of Marco ones to work.
	mintdrivers: should we re-add a systray icon to notify users at session startup?	
	ubiquity: https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1038522
	xfce: doesn't seem to detect DVD insertion, doesn't run VLC (works in 32bit, not 64bit)
	xfce: Can't use the trash in live mode
	xfce: There are no GTK bookmarks by default
	mintmenu: panel applet transparency
	mintsources: consider changing the way opt-in works for romeo and backport
	mintupload issues: https://github.com/linuxmint/mintupload/issues?state=open	
	integrate user guide in yelp help content
	upgrade translations
	replace gimp with pinta?	
	consider hexchat vs xchat
	consider mpv instead of totem
	mintupdate: handle kernel upgrades (show more info to advanced users)
	windows compatibility layer
	mint-x: MATE Panel transparency
	mintmenu pulls https://github.com/linuxmint/mintmenu/pulls
	mintlocale: set .pam_environment

Cinnamon 2.2
------------
	locales
		remove region module
		move keyboard layouts to keyboard settings
		12vs24 hour clock, easier custom format selection
	ibus support		
		http://pkgs.fedoraproject.org/cgit/cinnamon-settings-daemon.git/plain/keyboard.patch 
		http://pkgs.fedoraproject.org/cgit/cinnamon-control-center.git/plain/region.patch 
		http://pkgs.fedoraproject.org/cgit/cinnamon.git/plain/keyboard_applet.patch
		http://pkgs.fedoraproject.org/cgit/cinnamon-control-center.git/tree/region_cleanup.patch
		https://github.com/linuxmint/cinnamon-control-center/pull/51
	hidpi support
	look and feel
		logout sound
		bumpmaps
		consider using bernard's theme
		activate/discover hud and corner zones
		startup animation
	menu
		highlight newly installed items
		search providers
	little things
		stop using session-migration
		screenshot filenames aren't handy (Screenshot from 2014-02-17 14:46:32.png)
		Add common tiling options to window list context menu - Show Windows Side by Side, Cascade, Show windows stacked
		option to disable HUD	
		add major version deps on various components (libmuffin in particular)
		consider using "XDG_MENU_PREFIX=cinnamon- alacarte" instead of cme - coordinate with upstream to get cme improvements into alacarte
		cinnamon-bluetooth: bring compatibility to GNOME 3.10
		cinnamon-settings-users: add support for nopasswdlogin	
		cinnamon-settings-daemon: don't set locale / ditch org.cinnamon.locale.region in cinnamon-desktop
		