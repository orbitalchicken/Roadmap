	17.3
	=====

	system:
		ubiquity:
			crypted swap: http://forums.linuxmint.com/viewtopic.php?f=90&t=201025#p1050041
				replace
					# Add crypttab entry
					echo “cryptswap$i UUID=$uuid /dev/urandom swap,cipher=aes-cbc-essiv:sha256″ >> /etc/crypttab
				with
					# Add crypttab entry
					echo “cryptswap$i UUID=$uuid /dev/urandom swap,offset=8,cipher=aes-cbc-essiv:sha256″ >> /etc/crypttab
				without “offset=8″, a freshly installed Linuxmint finds the cryptswap and then destroys its UUID. On reboot, the UUID is gone and the swap partition cannot be found anymore. The offset should fix that problem.
			select fastest repositories based on location
			review upstream ubiquity patches
			review github issues
		[DONE] integrate nemo-preview
		ship with nemo extensions, disable them by default (using overrides)
		MATE/Xfce: provide QT5 override in /etc/X11/Xsession.d to make it use GTK style
		[DONE] fixed mint-common
		[DONE] restore menubar in terminals
		[DONE] add LO and KDE PPA to list of 700 priorities
		[DONE] apt memory fix: APT::Cache-Start "104857600"; https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=753941 or apply patch http://anonscm.debian.org/cgit/apt/apt.git/commit?id=4ea471ecb013d188d03a5c3efb9b21e58ef56065
		[DONE] add network-manager-openvpn-gnome
		[DONE] added orca
		[DONE] install compton by default in MATE/Xfce
		use LTS stack
		update kernel
		review/remove upstream pins no longer needed

	apps:
		hplip: https://bugs.launchpad.net/hplip/+bug/1442734
		vlc: upgrade to 2.2. It supports HEVC/h265 (same quality at half the file size). PPA available at ppa:mc3man/trusty-media
		[DONE] LO5

	mintbackup:
		consider using another alternative?

	mintwelcome:
		review UI

	cinnamon:
		window preview stuck: https://github.com/linuxmint/Cinnamon/issues/4750
		gnome-system-monitor moves out of the place in Expo
		When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
		hovering over notifications which have buttons/widgets should not dim them ...
		hidpi issues:
			Windows previews are nice but they are too small (not sure if this is only on HiDPI) – is there a way to make them bigger?
			Top of mint menu is cut off in HiDPI (1920×1280)

	mate:
		alt-tab thumbs cost perf..
		caja: clicking on home [compact view] in sidebar then on filesystem [icon view], back and forth, eventually dir names disappear
		md5sum action
		pass on translations

	artwork/config:
		update 17.3 background (doesn't look good)
		update backgrounds
		switch mdm slideshow to rosa

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
