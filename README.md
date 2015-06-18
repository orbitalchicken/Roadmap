Maintenance
-----------
	Update tapatalk API on forums.
	pkgs: unity-greeter pkg.
	rel notes: no network after suspending? https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1286552.
	upgrade inxi to 2.1.28.
	mate: The Mate Panel right side application indicator icons and clock, and when some other icons are pinned there scramble and get switched around and stay in the middle of the Panel sometimes – when changing Desktop resolution.
	nemo: can no longer handle desktop in root session.
	On MATE version I have trouble with the screenshot action.. when I press printscreen on my keyboard always freezing… same thing happen when I open screenshot app manually..
	kdeenlive: missing german translations.

KDE/Xfce Mint 17.1
------------------
	common:
		OK (maybe) - When logging in an existing session, doesn't unlock xscreensaver / of KDE screensaver.

	Xfce:
		Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
		Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!).
		indicator-applet patch: https://bugzilla.gnome.org/show_bug.cgi?id=726030.

LMDE
----
	Add va-driver-all to the list of installed packages (fixes black bands with Intel GPUs).
	upgrade path:
		debian-system-adjustments https://github.com/monsta/debian-system-adjustments/commits/master.
		/etc/plymouth/plymouthd.conf -->  [Daemon]  Theme=mint-logo
		logind.conf
		two nm-applet?
		10_linux
	mate 1.10: add additional rename MATE desktop (take from ubuntu-system-adjustments)
	history and completion in bashrc

17.2
----
	eom and mate-color-selector should go in Accessories
	two-edge scrolling regression
	32-bit isolinux linux is one line short (have to scroll to see Boot from Hard Drive)


	Xfce:
		xfce 4.12.
		consider this http://forums.linuxmint.com/viewtopic.php?f=152&t=195431.

	KDE:
		consider Plasma 5.

	MATE:
		use a configuration runtime switch for logind support.
		remove all help buttons.
		add context menu support for CSD headerbars in Marco.
		make MATE screensaver see OnlyShowIn=GNOME xscreensavers (/usr/share/applications/screensavers/*)

