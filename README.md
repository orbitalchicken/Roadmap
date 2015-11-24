	18
	==

		artwork/config:
			review isolinux
			New artwork

		system:
			Restore brightness settings on reboot (killswitch does that for bluetooth state)

		mate 1.14:
			touchpad: tap actions should reflect click actions

		cinnamon 3.0:
			touchpad: tap actions should reflect click actions
	17.3
	=====

	release management:
		screenshots
		videos of each desktops

	17.3 BETA
	=========

	[GIT] Cinnamon Sound applet: Close menu after clicking X button

	sources:
		live.linuxmint.com might need priority over packages.linuxmint.com to keep FF locales in sync with live version of FF
		consider not using extra.linuxmint.com
		consider downgrading import/main priority to 500


	mintupdate:
		don't test up-to-date-ness if using packages.linuxmint.com..
		when testing up-to-date-ness, check mirror first, don't check packages.linuxmint.com if age is less than 2 days
		remember mint age across refreshes, only re-read it if up-to-date check fails for mirror

	mintdrivers:
		always mark bcmwl-kernel-source as recommended
		mark b43 options as needing a connection to the Internet
		maybe indicate a reboot is needed post-successful driver install

	mintwelcome:
		use semi-saturated icons, or use full-saturated icons with highlighted versions for hover

	mintinstall:
		when apt cache is missing, it just says not available. Instead it could tell the user or even help the user to refresh the cache.

	cinnamon:
		gnome-system-monitor moves out of place in Expo
		When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
		hovering over notifications which have buttons/widgets should not dim them ...
		hidpi issues:
			Windows previews are nice but they are too small (not sure if this is only on HiDPI) – is there a way to make them bigger?
			Top of mint menu is cut off in HiDPI (1920×1280)

	Xfce/KDE
	========

	xfce:
		the xfce4-whiskermenu-plugin is not installed through the meta-package
		exo-utils can't open paths with special chars in them: http://forums.linuxmint.com/viewtopic.php?f=47&t=202069
		replace thunar with filemanager in panel: http://i.imgur.com/h6ftheB.png

	kde:
		mint kde 17.2 with asus ux303LA. On HDMI, can't clone screens, can't play sounds on tv. Both problems are solved by installing kde-workspace-randr. See https://bugs.launchpad.net/ubuntu/+source/kscreen/+bug/1213753 for details.


	Other
	=====

	mate:
		make transitional packages for:
			mate-dialogs -> zenity
			mate-calc -> gcaltool
			mate-system-tools -> gnome-system-tools
		MATE/Xfce: provide QT5 override in /etc/X11/Xsession.d to make it use GTK style
		alt-tab thumbs cost perf..
		caja: clicking on home [compact view] in sidebar then on filesystem [icon view], back and forth, eventually dir names disappear
		md5sum action

	lmde:
		bashrc: # colored GCC warnings and errors --> export GCC_COLORS='error=01;31:warning=01;35:note=01;36:caret=01;32:locus=01:quote=01' (won't work until gcc 4.9)
		update grub (improves efi support)
		Add va-driver-all to the list of installed packages (fixes black bands with Intel GPUs).
		upgrade path:
			/etc/plymouth/plymouthd.conf -->  [Daemon]  Theme=mint-logo
			logind.conf
		history and completion in bashrc
		betsy, meld 3.12.1 doesn't work (shows a black background), upgrade it to 3.12.3
		install libhal1-flash by default
		consider activating http://backports.debian.org/changes/jessie-backports.html
		backport blueman 2.0.1

	website:
		switch sensitive parts to https (md5 in particular)
		Update tapatalk API on forums.
		handle utf-8 on spices, see comments on http://cinnamon-spices.linuxmint.com/applets/view/171

	PIA:
		command to set up connection
		ca.crt
		tutorial
		support for openvpn
