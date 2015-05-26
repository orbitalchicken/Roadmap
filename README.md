Other Backports
---------
	Maya:
		x-caja-desktop fix.
		MDM session limiting.

Maintenance
-----------
	Update tapatalk API on forums.
	pkgs: unity-greeter pkg.
	rel notes: no network after suspending? https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1286552.
	upgrade inxi to 2.1.28.
	mate: The Mate Panel right side application indicator icons and clock, and when some other icons are pinned there scramble and get switched around and stay in the middle of the Panel sometimes – when changing Desktop resolution.
	MDM: reinterpret "default" session.. DESKTOP_SESSION should be set properly.
	nemo: can no longer handle desktop in root session.
	On MATE version I have trouble with the screenshot action.. when I press printscreen on my keyboard always freezing… same thing happen when I open screenshot app manually..
	Cinnamon: can't connect to WPA enterprise.
	Cinnamon: port this https://github.com/rgcjonas/gnome-shell-extension-appindicator.
	Cinnamon: factorize GVC code across multiple projects.
	kdeenlive: missing german translations.
	kodi/xbmc instructions tell people to install python-software-properties and software-properties-common.
	amdccle not starting from menu http://forums.amd.com/game/textthread.cfm?catid=488&threadid=186490, content is http://pastebin.com/PsSamJV6 (/usr/lib/fglrx/bin/amdxdg-su).

KDE/Xfce Mint 17.1
------------------
	common:
		When logging in an existing session, doesn't unlock xscreensaver / of KDE screensaver.

	Xfce:
		Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
		Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!).
		indicator-applet patch: https://bugzilla.gnome.org/show_bug.cgi?id=726030.

LMDE
----
	Add va-driver-all to the list of installed packages (fixes black bands with Intel GPUs).
	mintwelcome wants to install mint-meta-codecs instead of mint-meta-debian-codecs.
	nemo-preview should be rebuilt against jessie packages in order to depend on libmusicbrainz5-1 (instead of 5-0 which is not in jessie).
	upgrade path:
		Fix for gnome-terminal on hidpi https://github.com/linuxmint/gnome-apps/commit/32e30807f98c8a5caf2cf16aedda608101cda4bc
	debian-system-adjustments https://github.com/monsta/debian-system-adjustments/commits/master.
		/etc/plymouth/plymouthd.conf -->  [Daemon]  Theme=mint-logo
		logind.conf
		two nm-applet?
		10_linux

17.2
----
	Artwork:
		New backgrounds.
		New MDM theme.
		LO 4.4 theme.

	Common:
		mintupdate:
			option to hide/show UI after update.
			screen when all updates are done vs empty table.
			option to only show systray when updates are present.
			split kernel info away from mintupdate.
		mintinstall:
			revamp UI.
		software:
			add libreoffice-base (lo start app points to it).
			Firefox, disable telemetry/reset/etc notifications.
		system:
			support broadcom ootb.
			update bash.bashrc and .bashrc.
			libhal-flash - amazon instant video (turn off silverlight, enable flash).

	Backports:
		LibreOffice 4.4.
		Inkscape 0.9.1.
		HPLIP 3.15.2.
		ubuntu-drivers-common 0.2.94.7 (check http://bazaar.launchpad.net/~ubuntu-branches/ubuntu/trusty/ubuntu-drivers-common/trusty-updates/changes/62?start_revid=62 & https://github.com/linuxmint/ubuntu-drivers-common/commit/8677d116cc5da7facd6f170ef8b19f859be5cf5d at upstream).

	Xfce:
		xfce 4.12.
		consider this http://forums.linuxmint.com/viewtopic.php?f=152&t=195431.

	KDE:
		consider Plasma 5.

	MATE:
		MATE 1.10.
		use a configuration runtime switch for logind support.
		remove all help buttons.
		add context menu support for CSD headerbars in Marco.

	Cinnamon:
		Cinnamon 2.6:
			systray applet: pidgin status icon https://github.com/linuxmint/Cinnamon/issues/3223.
			cinnamon-settings-daemon: on shutdown, the icon theme reverts to gnome before shutting down
			sound applet: can update position seeker every 100th of a second?
