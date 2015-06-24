Maintenance
-----------
	Update tapatalk API on forums.

KDE/Xfce
--------
	common:
		OK (maybe) - When logging in an existing session, doesn't unlock xscreensaver / of KDE screensaver.

	Xfce:
		Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
		Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!).
		indicator-applet patch: https://bugzilla.gnome.org/show_bug.cgi?id=726030.
		xfce 4.12.
		consider this http://forums.linuxmint.com/viewtopic.php?f=152&t=195431.

	KDE:
		consider Plasma 5.

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
	common:
		32-bit isolinux linux is one line short (have to scroll to see Boot from Hard Drive)
		update rel notes and new features to talk about prime support
		Segfaults in FF/TB after upgrading linux-libc-dev
		update translations
		mint-X: add grey variation

	Cinnamon:
		When attempting to connect to a WPA/WPA2-Enterprise network using either the NetworkManager panel applet or Network Settings dialogue. Expected behavior is that a configuration dialogue for security settings (identity, password, CA cert, etc.) should pop up, allowing user to configure network. NM should then connect to the network. Actual behavior is that NM displays the “connecting to network” animation but never connects, pops up the security dialogue, or gives any error message (at least in the GUI). However, configuring the same WPA2 Enterprise connection through the “Connect to a Hidden Network” dialogue (i.e., manually) works as expected.
		[Fixed] libgtkmm-2.4-1c2a is not in Cinnamon-64 post-install (it's there in the 32bit edition and in MATE 64) - This missing lib causes invisible menu options in VMware and custom themes.

	MATE:
		epub support in atril
		mate-terminal: transparency in default profile
