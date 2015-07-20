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


Common
------
	hplip: https://bugs.launchpad.net/hplip/+bug/1442734
	mintsources: window too wide in russian locale

KDE
---
	kinfocenter shows wrong version (4.13.2) for KDE SC
	[Fixed] added missing baloo4

Xfce
----


Next Release
------------

	common:
		add network-manager-openvpn-gnome
		add mmcblk support (so we can install on sd card)?

	Cinnamon:
		cjs: Don't crash when applets call non-existing functions

	mintwelcome:
		Point to mintdrivers




