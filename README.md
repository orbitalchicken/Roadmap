
Backports
---------
	x-caja-desktop fix for Petra and Maya

Mint 17 [end of May]
--------------------
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
	mintupdate: redesign, no need to elevate user to root to see updates
	mintupdate: redesign startup delay
	mintinstall: chromium-browser should appear in search results, chromium-l10n should not appear in listings
	windows compatibility layer
	mint-x: MATE Panel transparency
	mintmenu pulls https://github.com/linuxmint/mintmenu/pulls
	update memtest on ISOs (version 1.07 --> 5.01), needed to test more than 2GB/4GB.
	make sure /etc/xdg/autostart/user-dirs-update-gtk.desktop works in MATE and Xfce (it uses OnlyShowIn)
	check APT to avoid mergelist issues - i.e. automatically delete/re-download corrupted files on apt-get update calls
	Can the upstream fix maybe be included in Mint somehow? Commit at upstream Gnome is https://git.gnome.org/browse/network-manager-applet/commit/?id=c798c40c5dce3bc6d9b615621cefe59660b5a504.

Cinnamon 2.2 [end of April]
---------------------------	 
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
		screenshot filenames aren't handy (Screenshot from 2014-02-17 14:46:32.png)
		Add common tiling options to window list context menu - Show Windows Side by Side, Cascade, Show windows stacked		
		add major version deps on various components (libmuffin in particular)
		consider using "XDG_MENU_PREFIX=cinnamon- alacarte" instead of cme - coordinate with upstream to get cme improvements into alacarte
		cinnamon-bluetooth: bring compatibility to GNOME 3.10
		cinnamon-settings-users: add support for nopasswdlogin		
		does CSD remember the brightness level across sessions?
		does CSD remember the sound level across sessions?
		inhibit systemd power management		
		cinnamon-screensaver: background doesn't show up		
		date gets revered automatically in cinnamon-settings, even when ntp is off
		tiling left tiles right-left
		port cinnamon-menu-editor fixes to alacarte upstream
		expo: set overview mode to true by default
		expo: lag on dnd
		nemo mounts as read-only after formatting a live stick back to vfat
	Done
		locales: remove region module
		locales: move keyboard layouts to keyboard settings
		date and time: 12vs24 hour clock, show seconds, show date		
		small things: stop using session-migration


LMDE
----
	Review live-installer from Tanglu (https://gitorious.org/tanglu/tanglu-live-installer) and Manjaro (http://git.manjaro.org/core/live-installer)
	Review Cinnarch installer (https://github.com/Antergos/Cnchi) and Manjaro fork (https://github.com/manjaro/thus)
	Triple mint-fortune issue with bash.bashrc
	Systemd runtime dir with gksu/pkexec