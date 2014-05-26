Fixed Issues since Mint 17 RC

All editions
------------
	mdm: login screen freezes for German speaking users
	mdm: second login screen does not say “Please enter your password” – no instruction text appears.
	mintsources: unable to add PPAs.. print(" %s" % (ppa_info["description"].encode("utf-8") or "")) --> AttributeError: ‘NoneType’ object has no attribute ‘encode’
	mintsources: The button "No action required" is not aligned along the right boundary with the text window below it.
	mintdrivers: failed to start when connection to the Internet was slow
	mintlocale: No keyboard navigation
	mintinstall: don't allow installation of broken packages, or packages which don't install properly in mintinstall.
	system: support for NVIDIA Optimus cards with nvidia-prime
	skype: sound issues (added suggestion to install ia32-libs to release notes).
	vlc: suggested to use “/dev/sr0″ for DVD playback in release notes
	gksu: freezes/lags due to fade-out animation
	mint-x: black background in Evolution's toolbar
	file-roller: Only one instance can run at a time
	gtk: symbolic icons in open dialogs
	gtk: scrollbars should not warp
	synaptic: freezes, and rendering issues
	network manager vpn: Unable to set up VPN or import a VPN config file
	network manager wpa: https://git.gnome.org/browse/network-manager-applet/commit/?id=c798c40c5dce3bc6d9b615621cefe59660b5a504
	FF News Link points to var/www/syscpwebs/lm/planet
	backgrounds: wrong author credited for "Flame" background	
	slideshow: Xchat still shown in the installer slideshow	
	The FFmpeg plugin for GStreamer 0.10 is not in the repository and it affects Firefox H.264 playback and other applications you can see http://www.webupd8.org/2014/04/10-things-to-do-after-installing-ubuntu.html for the PPA to install the package gstreamer0.10-ffmpeg all so included in that PPA is a much newer VLC version as well which is a extra bonus it is VLC 2.1.5		
	mintdrivers: remove the apt-cdrom repository when exiting

Cinnamon Edition
----------------
	cinnamon-settings: datetime module doesn't fit in window
	cinnamon: only 1 msgid for "Lock Screen" (action vs noun)	
	cinnamon-settings: lockscreen - make the “Show this message when the screen is locked” input box larger and on its own row below.	
	cinnamon-settings: can't set hours in datetime module
	cinnamon-settings: desklets - left-align the note underneath “Decoration of desklets”	
	In keyboard settings -> User defined keyboard shortcuts, three phrases are shown when hovering above the keyboard binding. The first is translated, but “Press Escape or click again to cancel the operation” and “Press Backspace to clear the existing keybinding” are not translated though they have been translated in Launchpad (Danish).
	chromium: After watching a full screen video (for example on Youtube) the panels are disappearing (the browser window hides them).	
	If Open menu when mouse hovers is selected, right-clicking the menu and moving the mouse upwards to select Configure often leads to the menu opening and the right-click menu disappears before it can be clicked. Doing it a couple of times in succession finally allows one to clicking Configure – it varies how may times I have to try before I succeed.
	Breadcrumbs in Nemo do not display correctly with Adwaita theme or High Contrast theme.
	tomboy is missing
	pidgin status icon is not displayed. I have to do Alt+F2 -> “r” to make it visible.	
	nopassdlogin support in cinnamon-settings-user
	Battery applet not showing time or percentage.
	battery applet tooltip is AC Adapter?
	
MATE Edition
------------
	pluma: crash when pressing CTRL+I
	dropbox: caja-dropbox not installable
	gparted is missing
	Remove mate-user-share? In Control Center, Shared Folders and User Share seem to duplicate and don't work well together. I have noticed that Shared Folders (from the Control Centre) will not save any shares I add.
	mint-meta-mate package still depends on mate-doc-utils, which has been replaced by yelp-tools in MATE 1.8.
	remove ugly minimize effect "org.mate.interface enable-animations"
	trackpad should have tap-to-click enabled.
	When you open Banshee, and close the window, a notification is shown beyond borders of desktop. You can see only top left corner of notification.	
	mintmenu: multiple issues with compiz
	mintmenu: Multiple Menu Entries – The menu has two entries for gnome-disk, libreoffice draw, and mate-volume-control in the ‘All’ category. This will appear when you first log into the system, but will disappear if you search through the menu and then look in the ‘All’ category	
	xdg-open /home --> opens Firefox instead of caja	

KDE Edition
-----------
	

Xfce Edition
------------
	