New bug reports in Linux Mint 18.2 BETA

All editions
------------

	mintupdate:
		In the past when updating packages completed the ‘Details’ window would stay open until I clicked the ‘Closed’ button. This is no longer true.
		kernel headers for 4.4 confuse ppl
		update policy choice doesn't stick
		Clicking Linux kernel headers 4.4, and selecting ‘Ignore updates for this package’ has no effect. Understandable for newer kernel/kernel headers update?

	guest sessions:
		don't block mintmenu
		[FIXED in GIT] don't start mintupdate

	mintinstall:
		can't access office category

    Slick greeter / lightdm-settings:
        session badges look blurry in HiDPI
        [FIXED IN GIT] wrong logitech keyboard layout: https://github.com/linuxmint/slick-greeter/issues/46

    synaptic: https://github.com/linuxmint/synaptic/issues/12

    xplayer: wrong aspect ratio http://pasteall.org/pic/show.php?id=114543

Cinnamon Edition - last processed comment: #79
-----------------------------------------------
 	bg gets erased after suspend? https://bugzilla.gnome.org/show_bug.cgi?id=739178
 	[FIXED IN GIT] screensaver should not activate for guest sessions

MATE Edition - last processed comment: #49
------------------------------------------
	The ‘netspeed-applet 1.18.1’ now continuously resizes as the bitrate changes. Installed between the ‘Clock’ and ‘Notification Area’ means all the icons in the notification area jump around a lot. Now that’s annoying! Hopefully this will be fixed.
	The ‘indicator-keylock 3.1.0’ app while ‘working’, i.e. when the the CapsLock key is pressed, a notification popup appears, at present in 18.2 the ‘indicator-keylock’ preference settings are not respected by the ‘mate-panel’. Previously, the ‘indicator-keylock’ icon would appear on the mate-panel, ONLY when the CapsLock key was pressed and disappear again when the CapsLock key was deactivated. Now the ‘indicator-keylock’ icon remains visible all the time. This may be a ‘mate-panel 1.18.2’ or lightdm issue, idk?
	mate-panel:
		when applying a bg color, the “Window List” remains unchanged.
		freezes everytime I try to add or move a launcher (icon) to it.
	Sticky Notes: no marking, copy possible – double clicking now opens “Sticky Notes Properties”

Xfce Edition - last processed comment: #0
-------------------------------------------

KDE Edition - last processed comment: #0
-----------------------------------------
