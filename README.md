Maintenance
-----------
	Update tapatalk API on forums.
	hplip: https://bugs.launchpad.net/hplip/+bug/1442734
	gnome-terminal/mate-terminal: bring back menubar by default
	mdm 2.0.4 (fixed FR comment)

	mate:
		caja: clicking on home [compact view] in sidebar then on filesystem [icon view], back and forth, eventually dir names disappear
		make transitional packages for:
			mate-dialogs -> zenity
			mate-calc -> gcaltool
			mate-system-tools -> gnome-system-tools

	mintupdate: failed: float division by zero when size of package is 0
	the xfce4-whiskermenu-plugin is not installed through the meta-package

LMDE
----
	Add va-driver-all to the list of installed packages (fixes black bands with Intel GPUs).
	upgrade path:
		/etc/plymouth/plymouthd.conf -->  [Daemon]  Theme=mint-logo
		logind.conf
	history and completion in bashrc

Common
------
	hplip: https://bugs.launchpad.net/hplip/+bug/1442734
	mintsources: window too wide in russian locale

KDE
---

Xfce
----

Next Release
------------

	common:
		add network-manager-openvpn-gnome
		add mmcblk support (so we can install on sd card)?

	Cinnamon:
		cjs: Don't crash when applets call non-existing functions

	mintsources:
		check that the added PPA supports the base codename (trusty for instance)

	mintwelcome:
		Point to mintdrivers

	mintupload: FTPS




