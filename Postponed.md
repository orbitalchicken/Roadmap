Improvements selected for the future
=====================================

Mint 17.x
---------
	common:
		new users: perms at 750 by default? http://www.techrepublic.com/blog/it-security/managing-default-unix-file-permissions-with-adduser-and-umask/.
		for non-english speaking people, it is not possible to change language, nor keyboard settings, when starting livemedia.
		backport VLC 3

	nemo:
		remove duplication between Eject and Safely Remove (for removable devices).
		[Can't reproduce] Regression in Nemo: Umounting dual-partitioned HDD freezes Nemo.
		video thumbnails are blurry https://github.com/linuxmint/nemo/issues/825.

	internet/network:
		hexchat: implement PR for /etc/hexchat for distro to set default list of networks https://github.com/hexchat/hexchat; http://anonscm.debian.org/cgit/collab-maint/hexchat.git/ (sney mailto:drubo@drubo.net).
		remove modemmanager?
		mirrors: implement mirmon? http://salixos.org/mirmon.html

	mintupdate:
		safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).

	mintupload:
		ftps support

	others:
		kde: New icon theme / UI look and feel.
		mdm: stopping the MDM service prevents access to the TTYs. Using Ctrl+Alt+F2 only works when MDM is running. Thus, there’s no way to run anything in a TTY unless the X server is running.
		Can’t play TS video files.
		windows compatibility layer.
		pin base-files?
		inserting live-stick, stick isn't mounted automatically in /media

	mintbackup:
		consider using another alternative?

	mintwelcome:
		review UI

	mintmenu:
		After typing when the list of matches accidentally disappears (hovering the mouse in the menu while moving up) there is no way of making it appear again without retyping.
		Please add a "delete selection" Button for the Search-Field.
		Sometimes at first launch, icons don't appear.

	mintinstall:
		revamp UI.

	mdm:
		mdm in live mode: can't log in using Mint and blank password
		preselect user if only one user is present in the list
		configurable slideshow

Cinnamon
--------
	accessibility:
		Screen reader did not appear to do anything, even after installing orca.

	hidpi and display settings:
		screensaver is all messed up
		hidpi setting should be in Displays, not in General
		frequency in monitor settings
		System Settings > Display won’t let me set the one on the right as primary. The “Set as Primary” button is grayed. It’s connected as DVI. The other monitor’s “Set as Primary” is not grayed. It’s connected as VGA. This is related to a very longstanding issue of Mint always opening dialogs on the left (wrong) monitor

	look and feel:
		fix spacing between systray icons
		cinnamon panel icon size sometimes show huge icons unless panel-scale-text-icons is set to true..
		icons pixelated in alt-tab or panel after a suspend-resume

	networking:
		network applet, consider this https://forum.kde.org/viewtopic.php?f=285&t=119742&sid=031f412655735293e130867c0fb1dbde https://dot.kde.org/sites/dot.kde.org/files/networkmanager.jpg
		Network setting does not let me to set Proxy.. The button “set system wide” is not there.
		network applet https://git.gnome.org/browse/gnome-control-center/commit/panels/network?id=63756458b2de0d730763cc2acbd510659e4d00a5
		regression, I can view the various wireless networks that are available and when I select one from the applet the Networking windows is opened. All networks are shown with a ‘play’ button (arrow). When I select a protected network (mine), symbol turns infinitely without connecting. http://forums.linuxmint.com/viewtopic.php?f=53&t=182608
		Can the upstream fix maybe be included in Mint somehow? Commit at upstream Gnome is https://git.gnome.org/browse/network-manager-applet/commit/?id=c798c40c5dce3bc6d9b615621cefe59660b5a504.
		When attempting to connect to a WPA/WPA2-Enterprise network using either the NetworkManager panel applet or Network Settings dialogue. Expected behavior is that a configuration dialogue for security settings (identity, password, CA cert, etc.) should pop up, allowing user to configure network. NM should then connect to the network. Actual behavior is that NM displays the “connecting to network” animation but never connects, pops up the security dialogue, or gives any error message (at least in the GUI). However, configuring the same WPA2 Enterprise connection through the “Connect to a Hidden Network” dialogue (i.e., manually) works as expected.

	nemo:
		review all usage of Gio/Glib
		re-add bg-change fade effect
		if I press ALT+F2 and then enter “nemo ftp://ftp.mydomain.xyz” to access to my personal ftp server trough nemo, I’ll get a request of username and password: it’s OK. The problem is that if I select the option to remember forever the username and password, it will not have effect: if I reboot Linux Mint, the next time I’ll try to access my ftp trough nemo I’ll get the request of username e password. So… nemo doesn’t remember my credentials… it’s frustrating.
		Entering the folder of long name , the path disappeared screen capture 1) it shows a folder of longname https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A19.png screen capture 2) entering the long name folder , meeting disappeared folder path of long name folder https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A34.png screen capture 3) But Actually It was still dsiplayed at max window https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A19%3A13.png
		Create a thumbnailer in usr/share/thumbnailers for MimeType inode/directory – when you try to run Nemo, it crashes with the error:  (nemo:9078): CinnamonDesktop-WARNING **: Error reading from file:///home/simon/Desktop: Error reading from file descriptor: Is a directory Installing cover-thumbnailer is an easy way to reproduce it.
		nemo-preview (not installed by default), doesn’t work: http://pastebin.com/Uaci0mzC
		1. Open nemo (unminimised)  2. Copy some files so that the transfer window is present 3. Open another program (unminimised) and in front of nemo such as firefox 4. If the transfer window is open (maximised) in front of the other program (firefox for example) and you click to minimise the transfer window, nemo will automatically pop up in front of the other program. Not a major bug but annoying from a window management point of view.
		When trying to connect my ext.hard drive via smb when double clicking on the globe icon (workgroup) nemo closes down
		If I disable the desktop icons with the first checkbox in cinnamon-settings the right mousebutton does not work on the desktop anymore…
		right-click Run/Open with blah in nemo, on executable files
		Feature request: if I create a launcher on my desktop, I can select an icon for it (with preview)… instead, if a modify a launcher in the menu with the “menu editor”, I can select a different icon but without preview. Can you please add the preview feature?
		if I launch from a bash script nemo to open an ftp server more than one time, with a command such as “nemo ftp://ftp.xxx.xyz“, I can get a duplicate icon on my desktop, see screenshot: https://dl.dropboxusercontent.com/u/573922/Schermata%20del%202013-11-21%2012%3A25%3A31.png
		If you plug in a USB, it auto mounts in a location on the desktop but if you unplug it, plug in another, and re-insert the first, the desktop icons overlap each other. I've noticed a similar issue in previous Mint releases. It would be great if the icons could auto position.
		small bug in all Linux Mint Cinnamon editions (maybe with Nemo). When I drag and drop some file(s) on an archive , my expectation is the files being added to it , but instead of that an error message pops out : “An error occurred while adding files to the archive. You can’t add an archive to itself.” . The Mate edition does not have this problem
		when no panels are present -> right-click the desktop -> Add a panel
		always handle the desktop (when no icons are to be shown, provide right-click features all the same)
		nemo context menus -> expand/collapse mini-button in the top-right corner of context menu, remember whether it's collapsed/expanded.
		If Nemo is open with 2 folder-panes the user can switch between both panes with F6, that is fine, if one uses the file-manager with keyboard only. The problem is, that F6 only works at once, if you have set Nemo to open with 2 panes. If Nemo opens with 1 pane (default setting) and the second pane gets opened via F3 (or menu), pressing F6 does at first nothing – no reaction at all. You can either click the second pane with the mouse (what is against a keyboard-only usage) or you have to navigate in the first pane anywhere (e.g. by pressing backspace), only after that F6 is reacting
		nemo: can no longer handle desktop in root session.
		in context menu, show expand/collapse button/arrow to toggle showing extra context menu options
		show icons per monitor..

	window management:
		expo: set overview mode to true by default
		integrate workspace management in nemo, panel, window-list, applet, muffin, settings
		Add common tiling options to window list context menu - Show Windows Side by Side, Cascade, Show windows stacked

	settings:
		don't show outdated spices
		cinnamon-settings: The search box in System Settings displays “Search…” next to the magnifier.
		cinnamon-settings: mdm - The name of the login screen in the main Cinnamon Control Centre is different to the window when you open it (Login Screen in the main Cinnamon Control Centre vs Login Window Preferences). The names should be the same for consistency.
		spices: removing extensions, themes, desklets, applets is only possible using right click (maybe it would be better to have button for that in future relases)
		spices: If I select the radio box to choose an applet and then I’ll click the button to install it, the applet is installed but it’s not active: maybe a new user expects to have it immediately in the panel after the download… in fact forcing the user to come back in the list of the installed applet to enable the just downloaded applet is not user friendly, in my opinion.
		keyboard: allow adding duplicate key combination for Cinnamon “Toggle Scale” and “Toggle Expo” (found these, didn’t go through all actions, most of them ok)
		mouse/touchpad: an option to change the mouse scroll speed for the middle wheel in Mouse and Touchpad preferences
		cinnamon-settings-users: Creating a user without password (stupid but nothing prevents it): impossible for that user to set one himself in Account Details.
		cinnamon-settings-users: In the “Users and Groups”, when on “Groups” tab, it could be great to have a way to see the members of a selected group and add new members to the group as well. Currently, we can only edit the group name…
		backgrounds: get more brackgrounds (find a way to make it easy to install more backgrounds)

	applets:
		menu: doesn't listen to menu changes outside /usr/share/applications? install shotwell for instance (uses /usr/share/menu)
		menu: keywords (for searching) aren't l10n'd
		menu: Even after setting org.cinnamon.desktop.lockdown.disable-lock-screen to true, the lock button still appears on cinnamon menu applet...
		menu: When creating a new menu item the icon does not appear. It is ok in the menu editor.
		sound: align close/raise buttons to the right

	other:
		screenshot filenames aren't handy (Screenshot from 2014-02-17 14:46:32.png)
		In gThumb, select a picture, right-click on it, select “Set as Desktop Background”, once applied, click the “Preferences” button on the green banner that just appeared at the bottom of the gThumb window and you’ll get the error message “Failed to execute child process “gnome-control-center” (No such file or directory)”
		refactor css theme to gain responsiveness.
		consider using search providers.

MATE
----
	hard to resize window or to grab border
	some of the MATE applications don’t have a mint-x icon. engrampa, eye of mate, atril. They could use the GNOME icons.
	When panel is at the top, notifications show on top of it. https://dl.dropboxusercontent.com/u/54450962/%ED%99%94%EB%A9%B4-5.png
	Add sound effects like in Cinnamon
	The MATE user admin program (mate-users-admin), when setting a user’s type to “Administrative”, does not add the user to the “sudo” group. The workaround is to explicitly add the user to the sudo group
	‘mate-screensaver’ still as flaky as it was in lm15 MATE 64-bit. Set to ‘Lock screen when screensaver is active’ sometimes upon resume after suspend I get a prompt for my password, other times NOT.
	MPRIS support
	caja: If you set a black wallpaper, the text below desktop icons becomes unvisible after reboot or logout and login.
	caja: dng and raw images thumbnails in caja
    caja: renaming a file produces a black border
    use a configuration runtime switch for logind support.
	add context menu support for CSD headerbars in Marco.
	make MATE screensaver see OnlyShowIn=GNOME xscreensavers (/usr/share/applications/screensavers/*)

Post 17
--------
	revive Giver project?

LMDE
----
	add the ability to encrypt the home directory
    Localization of the installer slideshow
    Live media isn't ejected at live session shutdown
    compiz integration missing
    caja: it looks like caja briefly dies at session start just before reappearing again
	missing plymouth-text theme
	Marco doesn't provide WM context menu options for CSD apps
	iphones can't be mounted (need more info on how to pull this off and with which versions of iOS?)
	Set the default debian repository to http.debian.net/debian instead of ftp.us.debian.org, which results in better performance for all users outside of the US
	missing slovak language pack (something like thunderbird-l10n-sk) for Thunderbird mail client
	rfkill provides upstart config, but not init.d.. as a result RFKILL state isn't stored/restored
	integrity check warns about malformed header
	/.config/pulse present (found on MATE i386 ISO)
	gnome-power-statistics.desktop doesn't show up in Cinnamon
