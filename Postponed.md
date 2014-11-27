Improvements selected for the future
=====================================

Mint 17.2
---------
	Consider adding pipelight or freshplayerplugin (https://github.com/i-rinat/freshplayerplugin)
	Consider porting cinnamon-bluetooth into gnome-bluetooth-frontend, for use in MATE and Xfce
	nemo: remove duplication between Eject and Safely Remove (for removable devices)
	hexchat: implement PR for /etc/hexchat for distro to set default list of networks https://github.com/hexchat/hexchat; http://anonscm.debian.org/cgit/collab-maint/hexchat.git/ (sney mailto:drubo@drubo.net)
	remove modemmanager?
	pin base-files?
	for non-english speaking people, it is not possible to change language, nor keyboard settings, when starting livemedia.
	- mintmenu:
		After typing when the list of matches accidentally disappears (hovering the mouse in the menu while moving up) there is no way of making it appear again without retyping.
		Please add a "delete selection" Button for the Search-Field.
		Sometimes at first launch, icons don't appear.
	mintupdate: safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages)
	[Can't reproduce] Regression in Nemo: Umounting dual-partitioned HDD freezes Nemo
	inserting live-stick, stick isn't mounted automatically in /media
	mirrors: implement mirmon? http://salixos.org/mirmon.html

Mint 17
-------
	mdm: stopping the MDM service prevents access to the TTYs. Using Ctrl+Alt+F2 only works when MDM is running. Thus, there’s no way to run anything in a TTY unless the X server is running.
	Can’t play TS video files
	windows compatibility layer

Cinnamon
--------
	cinnamon regressions in Network Settings:
		- I can view the various wireless networks that are available and when I select one from the applet the Networking windows is opened. All networks are shown with a ‘play’ button (arrow). When I select a protected network (mine), symbol turns infinitely without connecting. http://forums.linuxmint.com/viewtopic.php?f=53&t=182608
	session dialog runs timer even when it's disabled
	an option to change the mouse scroll speed for the middle wheel in Mouse and Touchpad preferences
	When I refresh the Applets cache, the progress windows does not appear correctly, it was just a tiny gray window in the top left corner.
	accessibility:
		Screen reader did not appear to do anything, even after installing orca.
		on screen keyboard is close to unusable, redesign needed.
	nemo: If I disable the desktop icons with the first checkbox in cinnamon-settings the right mousebutton does not work on the desktop anymore…
	settings/panel Under Auto-hide panel consider aligning the two input boxes to each other (+/- milliseconds input buttons) but keep Show Delay and Hide Delay aligned with each other on the left side.
	menu: keywords (for searching) aren't l10n'd
	hidpi: screensaver is all messed up
	hidpi: hidpi setting should be in Displays, not in General
	actual screensaver?
	fix spacing between systray icons
	don't show keybinding OSDs when notifications are off
	network applet, consider this https://forum.kde.org/viewtopic.php?f=285&t=119742&sid=031f412655735293e130867c0fb1dbde https://dot.kde.org/sites/dot.kde.org/files/networkmanager.jpg
	improve window animations, based on GNOME SHELL 3.14 (windowmanager.js)
	frequency in monitor settings
	search providers
	ibus support
	integrate workspace management in nemo, panel, window-list, applet, muffin, settings
	Cinnamon isn’t scaling user defined panel sizes properly. If I select Numix as my theme and set a customised panel size, when clicking Allow Cinnamon to Scale Panel Text and Icons, the text on the right side of the panel bar seems to go a bit blurry. This didn’t happen on the last release. The update shield sometimes goes wonky too which I assume is related.
	The cinnamon-sound-applet’s icon renders incorrectly in i3wm’s system tray (it was fine with the version of cinnamon that shipped with LM16 and the same version of i3 (4.7.2)). I was able to get it working via brute force specifying the path to the icon, but it would be nice if it worked out of the box.
	When trying to connect my ext.hard drive via smb when double clicking on the globe icon (workgroup) nemo closes down
	System Settings > Display won’t let me set the one on the right as primary. The “Set as Primary” button is grayed. It’s connected as DVI. The other monitor’s “Set as Primary” is not grayed. It’s connected as VGA. This is related to a very longstanding issue of Mint always opening dialogs on the left (wrong) monitor
	Network setting does not let me to set Proxy.. The button “set system wide” is not there.
	settings: The search box in System Settings displays “Search…” next to the magnifier.
	settings: mdm - The name of the login screen in the main Cinnamon Control Centre is different to the window when you open it (Login Screen in the main Cinnamon Control Centre vs Login Window Preferences). The names should be the same for consistency.
	settings: mouse - The Cinnamon drag threshold and GTK drag threshold input boxes are not aligned to each other but appended to the end of the wording. They should be aligned as per other similar examples in the Cinnamon Control Centre.
	settings:  workspaces - OSD duration, OSD horizontal position and OSD vertical position are not aligned.
	settings: Under Auto-hide panel, the input boxes for “show delay” and “hide delay” are not aligned. Many other such input boxes and drop down menu boxes are aligned with each other and not with the end of the text.
	applets: when I click on the window list to minimize and maximize sometimes the windows don’t respond and so I have to maximize another window so that I can mainimize or maximize the previous one!!
	spices: removing extensions, themes, desklets, applets is only possible using right click (maybe it would be better to have button for that in future relases)
	spices: If I select the radio box to choose an applet and then I’ll click the button to install it, the applet is installed but it’s not active: maybe a new user expects to have it immediately in the panel after the download… in fact forcing the user to come back in the list of the installed applet to enable the just downloaded applet is not user friendly, in my opinion.
	nemo: if I press ALT+F2 and then enter “nemo ftp://ftp.mydomain.xyz” to access to my personal ftp server trough nemo, I’ll get a request of username and password: it’s OK. The problem is that if I select the option to remember forever the username and password, it will not have effect: if I reboot Linux Mint, the next time I’ll try to access my ftp trough nemo I’ll get the request of username e password. So… nemo doesn’t remember my credentials… it’s frustrating.
	nemo: Entering the folder of long name , the path disappeared screen capture 1) it shows a folder of longname https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A19.png screen capture 2) entering the long name folder , meeting disappeared folder path of long name folder https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A34.png screen capture 3) But Actually It was still dsiplayed at max window https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A19%3A13.png
	cinnamon: menu doesn't listen to menu changes outside /usr/share/applications? install shotwell for instance (uses /usr/share/menu)
	Keyboard settings allow adding duplicate key combination for Cinnamon “Toggle Scale” and “Toggle Expo” (found these, didn’t go through all actions, most of them ok)
	nemo: Create a thumbnailer in usr/share/thumbnailers for MimeType inode/directory – when you try to run Nemo, it crashes with the error:  (nemo:9078): CinnamonDesktop-WARNING **: Error reading from file:///home/simon/Desktop: Error reading from file descriptor: Is a directory Installing cover-thumbnailer is an easy way to reproduce it.
	nemo-preview (not installed by default), doesn’t work: http://pastebin.com/Uaci0mzC
	consider using bernard's theme
	screenshot filenames aren't handy (Screenshot from 2014-02-17 14:46:32.png)
	Add common tiling options to window list context menu - Show Windows Side by Side, Cascade, Show windows stacked
	cinnamon-settings-users: add support for nopasswdlogin
	expo: set overview mode to true by default
	expo: lag on dnd
	network applet https://git.gnome.org/browse/gnome-control-center/commit/panels/network?id=63756458b2de0d730763cc2acbd510659e4d00a5
	cinnamon-screensaver dialog is all shrunk in hi-dpi
	Can the upstream fix maybe be included in Mint somehow? Commit at upstream Gnome is https://git.gnome.org/browse/network-manager-applet/commit/?id=c798c40c5dce3bc6d9b615621cefe59660b5a504.
	right-click Run/Open with blah in nemo, on executable files
	applets: Even after setting org.cinnamon.desktop.lockdown.disable-lock-screen to true, the lock button still appears on cinnamon menu applet...
	cinnamon: Onscreen keyboard activates when clicking the menu on the panel because text entry is focused... if onboard is used, entry should not focus when showing the menu
	cinnamon panel icon size sometimes show huge icons unless panel-scale-text-icons is set to true..
	Creating a user without password (stupid but nothing prevents it): impossible for that user to set one himself in Account Details.
	In the “Users and Groups”, when on “Groups” tab, it could be great to have a way to see the members of a selected group and add new members to the group as well. Currently, we can only edit the group name…
 	Feature request: if a create a luncher on my desktop, I can select an icon for it (with preview)… instead, if a modify a launcher in the menu with the “menu editor”, I can select a different icon but without preview. Can you please add the preview feature?
	if a launch from a bash script nemo to open an ftp server more than one time, with a command such as “nemo ftp://ftp.xxx.xyz“, I can get a duplicate icon on my desktop, see screenshot: https://dl.dropboxusercontent.com/u/573922/Schermata%20del%202013-11-21%2012%3A25%3A31.png
	1. Open nemo (unminimised)  2. Copy some files so that the transfer window is present 3. Open another program (unminimised) and in front of nemo such as firefox 4. If the transfer window is open (maximised) in front of the other program (firefox for example) and you click to minimise the transfer window, nemo will automatically pop up in front of the other program. Not a major bug but annoying from a window management point of view.
	icons pixelated in alt-tab or panel after a suspend-resume
	llvmpiped session after a suspend-resume
	In gThumb, select a picture, right-click on it, select “Set as Desktop Background”, once applied, click the “Preferences” button on the green banner that just appeared at the bottom of the gThumb window and you’ll get the error message “Failed to execute child process “gnome-control-center” (No such file or directory)”
	cinnamon: Having links of files/folders on desktop from another hardrive at startup, then mounting the drive will usually crash then restart Cinnamon
	Cinnamon menu: When creating a new menu item the icon does not appear. It is ok in the menu editor.
	ibus support
			http://pkgs.fedoraproject.org/cgit/cinnamon-settings-daemon.git/plain/keyboard.patch
			http://pkgs.fedoraproject.org/cgit/cinnamon-control-center.git/plain/region.patch
			http://pkgs.fedoraproject.org/cgit/cinnamon.git/plain/keyboard_applet.patch
			http://pkgs.fedoraproject.org/cgit/cinnamon-control-center.git/tree/region_cleanup.patch
			https://github.com/linuxmint/cinnamon-control-center/pull/51
		look and feel
			bumpmaps
			startup animation
		menu
			search providers

MATE
----
	hard to resize window or to grab border
	some of the MATE applications don’t have a mint-x icon. engrampa, eye of mate, atril. They could use the GNOME icons.
	mate-terminal still has a menu bar and is not transparent
	When panel is at the top, notifications show on top of it. https://dl.dropboxusercontent.com/u/54450962/%ED%99%94%EB%A9%B4-5.png
	Would be nice if the mouse preference panel in Mate included a “natural scrolling” option
	Add sound effects like in Cinnamon
	The MATE user admin program (mate-users-admin), when setting a user’s type to “Administrative”, does not add the user to the “sudo” group. The workaround is to explicitly add the user to the sudo group
	‘mate-screensaver’ still as flaky as it was in lm15 MATE 64-bit. Set to ‘Lock screen when screensaver is active’ sometimes upon resume after suspend I get a prompt for my password, other times NOT.
	MPRIS support
	mate-system-monitor under resourses doesn’t look great with the default GTK theme (need to give the notebook at widget class name or style name so we can make it flat in Mint-X, alternatively, we could try and make the cairo elements transparent)
	caja: If you set a black wallpaper, the text below desktop icons becomes unvisible after reboot or logout and login.
	caja: dng and raw images thumbnails in caja
	switch to default notification theme
	mintdesktop: Use radiobuttons for marco vs compiz, with labels like "Marco (No desktop effects, compatible with all hardware)", "Compiz (Desktop effects, requires compatible hardware)"

LMDE
----
	Review live-installer from Tanglu (https://gitorious.org/tanglu/tanglu-live-installer) and Manjaro (http://git.manjaro.org/core/live-installer)
	Review Cinnarch installer (https://github.com/Antergos/Cnchi) and Manjaro fork (https://github.com/manjaro/thus)
	Triple mint-fortune issue with bash.bashrc
	Systemd runtime dir with gksu/pkexec
	XFS won't boot because of missing fsck.xfs https://bugs.launchpad.net/bugs/1322164
	check fsck presence for ALL other FS'es

Post 17
--------
	revive Giver project?
