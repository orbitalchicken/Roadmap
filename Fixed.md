Fixed Issues since Linux Mint 17.3 BETA

All editions
------------
	upower: Logitech mice battery not detected: https://bugs.launchpad.net/ubuntu/+source/upower/+bug/1448834
	broadcom STA: Fix 4.2 compatibility and kernel crashes when switching APT
	live: live.linuxmint.com might need priority over packages.linuxmint.com to keep FF locales in sync with live version of FF
	live: don't remove security/updates from build list
	ubiquity: wrong version (16) of Linux Mint being reported
	ubiquity-slideshow-mint: update translations
	apt: downgrade import/main priority to 500
	repositories: added spotify-client
	repositories: added minecraft-installer
	mdm: Don't let users with an encrypted home directory use auto/timed login
	mdm: crash when selecting 'blank' primary monitor
	mintsources: Fixed up-to-date checks
	mintupdate: Setting broken icons breaks mintupdate
	mintupdate: shows corrupt msg instead of errors in case of mergelist issues
	mintupdate: when testing up-to-date-ness, check mirror first, don't check packages.linuxmint.com if age is less than 2 days
	mintlocale: fine-tune input method packages for Korean, Thai, Vietnamese, Japanese (was already done), Chinese (partial)
	mintlocale: when all im pkgs are installed, button has no label
	mintdrivers: always mark bcmwl-kernel-source as recommended
	mintdrivers: mark b43 options as needing a connection to the Internet
	mintdrivers: indicate a reboot is needed post-successful driver install
	mint-themes-gtk3: first tick in a treeview is blurry
	vino-preferences has a button which points to ubuntu-docs

Cinnamon Edition
----------------
	Windows previews are nice but they are too small (not sure if this is only on HiDPI) – is there a way to make them bigger?
	changing sound volume doesn't trigger sound event
	Cinnamon Sound applet: Close menu after clicking X button
	nemo: context menu doesn't update Open with action

MATE Edition
------------
	import latest fixes/translations for :
		atril
		mcc
		mate-desktop
		marco
		mpm
		caja
		mate-applets
	indicator-sound-gtk2: launch mate-volume-control when in MATE


KDE Edition
-----------
	mint kde 17.2 with asus ux303LA. On HDMI, can't clone screens, can't play sounds on tv. Both problems are solved by installing kde-workspace-randr. See https://bugs.launchpad.net/ubuntu/+source/kscreen/+bug/1213753 for details.
	plymouth text is 17.2
	ksplash is 17.2

Xfce Edition
------------
	upgraded whisker menu
	the xfce4-whiskermenu-plugin is not installed through the meta-package
	exo-utils can't open paths with special chars in them: http://forums.linuxmint.com/viewtopic.php?f=47&t=202069
	replace thunar with filemanager in panel: http://i.imgur.com/h6ftheB.png
	theme and icon improvements for Xfce
	VLC does not have icons in menus
	mid click on panel closes application
	Switching from xfwm4 to xfwm4+compositing does not turn on compositing (use xfconf-query to turn it on). And switching from xfwm4 to compiz doesn’t work too. Switching to compiz breaks very fast, no matter which wm you have chosen.
	refine UCA text and localization