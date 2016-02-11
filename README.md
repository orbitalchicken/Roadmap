	Linux Mint 18 Sarah
	===================

        Look and feel:
            isolinux theme
            plymouth theme
            GTK 3.18 support in Mint-X
                Sidebar issues
                Pathbar buttons (visible in nemo)
                Context menus don't look good
            new GTK theme
            new icon theme
            consider making it easy to switch to old theme? (maybe a meta-theme and support for it in cinnamon?).
            website revamp

        X-Apps:
            [done] xed
            [done] xplayer
            [done] xviewer
            [done] xreader
            xar
            xapps support in Cinnamon
            xapps support in MATE
            xapps support in MIME defaults

        Regressions:
            GTK/Cinnamon: window is mapped to top-left and then moves in position when minimizing and then restauring from the panel window list
            GTK/Nemo: text entry out of place when renaming a file
            GTK: Overlay scrollbars hide content (for instance the last line of text in a text editor when wrapping is disabled)

        Mint apps:
            review python shebangs:
                [done] mint-common
                [done] mintdesktop
                [done] mintsystem
                [done] mintwelcome
                [done] mintinstall
                [done] mintmenu
                [done] mintsources
                [done] mintstick
                [done] mintupdate
                [done] mintupload
                [done] mintnanny
                [done] mintbackup
                mintdrivers
                mintlocale
                mint-dev-tools
            gtk3:
                [done] mintdesktop
                [done] mintsystem
                [done] mintwelcome
                [done] mintlocale
                [done] mintdrivers
                [done] mintnanny
                [done] mintstick
                [done] mint-common
                [glebihan] mintupdate
                mintbackup
                mintinstall
                mintsources
                mintupload
            hidpi:
                mintwelcome uses 32px png icons
                mintlocale uses fixed-size flag icons
            Full black-box testing on xenial:
                mintdesktop
                mintsystem
                mintwelcome
                mintinstall
                mintmenu
                mintsources
                mintstick
                mintupdate
                mintupload
                mintbackup
                mintdrivers
                mintlocale
                mintnanny

        Software selection:
            consider replacing/removing mintbackup
            consider replacing/removing gthumb

		System:
			Restore brightness settings on reboot (killswitch does that for bluetooth state)
			add "pwfeedback" to Defaults line in sudoers file, to show *** feedback when typing password
            Upgrade path from Mint 17.3

		mate 1.14:
			touchpad: tap actions should reflect click actions
			mcc: replace sound themes with sound events
			multi-monitor: caja doesn't always show the desktop on the primary monitor (using a laptop as main/left monitor, and HDMI screen with higher res on the right, it surprisingly ends up showing icons on the right screen)

		cinnamon 3.0:
			touchpad: tap actions should reflect click actions
			multi-monitor: add an option to suspend on lid-close EVEN when external monitors are plugged
			sound: add an option to switch sound to HDMI when an HDMI output device is plugged
			menu: search on non-accentuated versions (for instance, "method" should find mintlocale's im in French)
			hidpi issues: top of mint menu is cut off in HiDPI (1920×1280)
			gnome-system-monitor moves out of place in Expo
			when battery is very low, battery icon isn't red.. 2% charge, with less than 5 minutes to go, still not red.. bar is red in CCC, icon is red in notification.. but not in applet (and also not in the CCC icon itself either)
			When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
			hovering over notifications which have buttons/widgets should not dim them ...
			accessibility: ability to select files by hovering them

		mintupdate:
			unattended updates? at least provide a CLI to do it via cron?
			fix mergelist issues directly in mintupdate or checkAPT

		mintinstall: when apt cache is missing, it just says not available. Instead it could tell the user or even help the user to refresh the cache.
		mintmenu: dark themes https://github.com/linuxmint/mintmenu/issues/87
        mintsystem: review /usr/bin/apt and add missing features (list, search etc..)

		people are led to believe the community website is the place for support:
			change the order in FF bookmarks -> place Community at the end, after Forums/Blog.
			place an info message in the sidebar (or headerbar), and on the registration page to explain the forums are the place to be.

		gthumb tries to launch gnome-control-center when applying a background

		hexchat: add notifications, hide in/out messages, by default

        Ready:
            mintsources: add-apt-repository now supports --remove

	17.3
	=====

    Cinnamon point releases

	MATE updates:
		http://pastebin.com/yELMqEz2

	release management:
		screenshots
		videos of each desktops
	update listing on website from mintinstall
	upgrade LO to 5.0.4

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

