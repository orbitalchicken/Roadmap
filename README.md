	system:
		hplip: https://bugs.launchpad.net/hplip/+bug/1442734
		add network-manager-openvpn-gnome
		add mmcblk support (so we can install on sd card)?
		ubiquity: crypted swap: http://forums.linuxmint.com/viewtopic.php?f=90&t=201025#p1050041
			replace
				# Add crypttab entry
				echo “cryptswap$i UUID=$uuid /dev/urandom swap,cipher=aes-cbc-essiv:sha256″ >> /etc/crypttab
			with
				# Add crypttab entry
				echo “cryptswap$i UUID=$uuid /dev/urandom swap,offset=8,cipher=aes-cbc-essiv:sha256″ >> /etc/crypttab
			without “offset=8″, a freshly installed Linuxmint finds the cryptswap and then destroys its UUID. On reboot, the UUID is gone and the swap partition cannot be found anymore. The offset should fix that problem.
		ubiquity: select fastest repositories based on location
		check if libgtkmm-2.4-1c2a should be installed (reported missing in Cinnamon 17.1 32-bit). Missing lib creates problems for VMware Player (missing menus) and changing Themes.
		integrate nemo-preview
		ship with nemo extensions, disable them by default (using overrides)
		restore menubar in terminals
		MATE/Xfce: provide QT5 override in /etc/X11/Xsession.d to make it use GTK style
		add LP PPA to list of 700 priorities
		bashrc: # colored GCC warnings and errors --> export GCC_COLORS='error=01;31:warning=01;35:note=01;36:caret=01;32:locus=01:quote=01' (won't work until gcc 4.9)
		apt memory fix: APT::Cache-Start "104857600"; https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=753941 or apply patch http://anonscm.debian.org/cgit/apt/apt.git/commit?id=4ea471ecb013d188d03a5c3efb9b21e58ef56065
		add orca (might have to hide its menu item)

	mdm:
		onscreen keyboard
		mdmflexiserver: in MATE (on a computer with cinnamon installed), mdmflexiserver launches cinnamon-screensaver instead of mate-screensaver

	apps:
		vlc: upgrade to 2.2. It supports HEVC/h265 (same quality at half the file size). PPA available at ppa:mc3man/trusty-media
		gnome-terminal/mate-terminal: bring back menubar by default
		LO5

	cinnamon:
		window preview stuck: https://github.com/linuxmint/Cinnamon/issues/4750
		gnome-system-monitor moves out of the place in Expo
		snap window on 2nd monitor, then try to a maximize another window on 2nd monitor -> broken window frame
		In 2.6 the sound applet successfully hid Amaroks tray icon, this is not the case anymore.
		When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
		hovering over notifications which have buttons/widgets should not dim them ...
		brightness and keyboard brightness OSDs not consistent with sound volume OSD
		hidpi issues:
			Windows previews are nice but they are too small (not sure if this is only on HiDPI) – is there a way to make them bigger?
			Top of mint menu is cut off in HiDPI (1920×1280)
			When HiDPI is off, logging in for the first time after comp startup happens within 1-3 seconds. With HiDPI it takes a clear 5-10 seconds. Is there a way to speed this up?

	mate:
		alt-tab thumbs cost perf..
		caja: clicking on home [compact view] in sidebar then on filesystem [icon view], back and forth, eventually dir names disappear
		make transitional packages for:
			mate-dialogs -> zenity
			mate-calc -> gcaltool
			mate-system-tools -> gnome-system-tools
		md5sum action, open-as-root, open-terminal?

	xfce:
		the xfce4-whiskermenu-plugin is not installed through the meta-package
		exo-utils can't open paths with special chars in them: http://forums.linuxmint.com/viewtopic.php?f=47&t=202069
		replace thunar with filemanager in panel: http://i.imgur.com/h6ftheB.png

	kde:
		mint kde 17.2 with asus ux303LA. On HDMI, can't clone screens, can't play sounds on tv. Both problems are solved by installing kde-workspace-randr. See https://bugs.launchpad.net/ubuntu/+source/kscreen/+bug/1213753 for details.

	mintbackup:
		consider using another alternative?

	mintwelcome:
		point to mintdrivers

	artwork/config:
		mint-themes-gtk3: fix gnome-calculator context-menu (right-click inside the calculator screen) being huge
		cinnamon: increase panel height by 3 pixels (to a value of 28) (makes apps less blurry) http://www.pasteall.org/pic/show.php?id=92723

	lmde:
		update grub (improves efi support)
		Add va-driver-all to the list of installed packages (fixes black bands with Intel GPUs).
		upgrade path:
			/etc/plymouth/plymouthd.conf -->  [Daemon]  Theme=mint-logo
			logind.conf
		history and completion in bashrc
		betsy, meld 3.12.1 doesn't work (shows a black background), upgrade it to 3.12.3
		install libhal1-flash by default
		consider activating http://backports.debian.org/changes/jessie-backports.html

	website:
		switch sensitive parts to https (md5 in particular)
		Update tapatalk API on forums.
		handle utf-8 on spices, see comments on http://cinnamon-spices.linuxmint.com/applets/view/171

	PIA:
		command to set up connection
		ca.crt
		tutorial
		support for openvpn
