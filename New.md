New bug reports in Linux Mint 18.2 BETA

All editions
------------

	http://people.canonical.com/~ubuntu-security/cve/pkg/vlc.html

	mintupdate:
		kernel headers for 4.4 confuse ppl
		Clicking Linux kernel headers 4.4, and selecting ‘Ignore updates for this package’ has no effect. Understandable for newer kernel/kernel headers update?
		[FIXED in GIT] update policy choice doesn't stick
		[FIXED in GIT] don't start mintupdate in guest sessions

	mintinstall:
		can't access office category (happens in MATE but not in Cinnamon, issue in Pixbuf SVG support..)

    Slick greeter / lightdm-settings:
        session badges look blurry in HiDPI
        [FIXED IN GIT] wrong logitech keyboard layout: https://github.com/linuxmint/slick-greeter/issues/46

    xplayer: wrong aspect ratio http://pasteall.org/pic/show.php?id=114543

Cinnamon Edition - last processed comment: #79
-----------------------------------------------
 	bg gets erased after suspend? https://bugzilla.gnome.org/show_bug.cgi?id=739178
 	would battery be better swapped with user applet?
    looking for display in menu shows color first
    display resolution change freezes cinnamon https://github.com/linuxmint/Cinnamon/issues/6224
    [FIXED IN GIT] screensaver should not activate for guest sessions

MATE Edition - last processed comment: #49
------------------------------------------
	The ‘netspeed-applet 1.18.1’ now continuously resizes as the bitrate changes. Installed between the ‘Clock’ and ‘Notification Area’ means all the icons in the notification area jump around a lot. Now that’s annoying! Hopefully this will be fixed.
	The ‘indicator-keylock 3.1.0’ app while ‘working’, i.e. when the the CapsLock key is pressed, a notification popup appears, at present in 18.2 the ‘indicator-keylock’ preference settings are not respected by the ‘mate-panel’. Previously, the ‘indicator-keylock’ icon would appear on the mate-panel, ONLY when the CapsLock key was pressed and disappear again when the CapsLock key was deactivated. Now the ‘indicator-keylock’ icon remains visible all the time. This may be a ‘mate-panel 1.18.2’ or lightdm issue, idk?
	mate-panel:
		when applying a bg color, the “Window List” remains unchanged.
	mint-x-icons: network status icons have a dark background in panel 33px and bigger (sound icon looks wrong in 41px and bigger).
	Sticky Notes: no marking, copy possible – double clicking now opens “Sticky Notes Properties”
	nm-applet can't be left-clicked
	mate font viewer should be called font viewer, and its app icon isn't found.

Xfce Edition - last processed comment: #0
-------------------------------------------

KDE Edition - last processed comment: #0
-----------------------------------------
	SDDM stays in autologin after OEM install
