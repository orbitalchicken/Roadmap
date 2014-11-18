Backports
---------
	x-caja-desktop fix for Maya
	LO 4.3?
	KDE 4.14

Maintenance
-----------
	Update tapatalk API on forums
	pkgs: unity-greeter pkg
	rel notes: no network after suspending? https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1286552	
	upgrade inxi to 2.1.28
	

KDE/Xfce Mint 17.1
------------------
	common:
		When logging in an existing session, doesn't unlock xscreensaver / of KDE screensaver		
	kde
		MintXKDE.colors https://dl.dropboxusercontent.com/u/11675431/MintXKDE.colors http://forums.linuxmint.com/viewtopic.php?f=153&t=61241
		[RFT] kde 4.14
		black screen on logout?
	xfce
		revive xfapplet
		upgrade xfce4-whiskermenu-plugin to 1.4.0?
		compiz support ootb?
		Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
		Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!)
		switch datetime applet to Clock applet
		indicator-applet patch: https://bugzilla.gnome.org/show_bug.cgi?id=726030	

		

Consider for Mint 17.1
----------------------
	
	[Can't reproduce] Regression in Nemo: Umounting dual-partitioned HDD freezes Nemo
	inserting live-stick, stick isn't mounted automatically in /media

Release Mgmt + Post-RC Mint 17.1
--------------------------------	
	[RFT] rephrase OEM isolinux/grub option --> s/Start Linux Mint/Preinstall Linux Mint/g
	implement visual upgrade path for Mint 17 users (use mint-meta as a precondition)
	cinnamon:
		Regression: DND minifreezes..
		Regression in Network Settings: Not possible to setup mobile broadband? https://github.com/linuxmint/Cinnamon/issues/3640
		[RFT] Regression in Nemo: Misplaced rename text entry https://github.com/linuxmint/nemo/issues/757
		Nemo: Zoom level changes over time on its own
		[RFT] Regression in Nemo: When switching the sidebar view to tree view and back, some entries in the “Devices” category are displaced/displayed incorrectly. On mouse-over they display correctly again.


Todo for Mint 17.1
------------------

	cinnamon		
		using CPU?

	artwork		
		tomboy systray icon is black

	nemo-emblems
		hide ubuntuone, dropbox icons		

	mate				
		[Fred] be able to provide /etc/apt/preferences.d in ISO
		[Fred] rsync-packages sync
		-- brightness OSD doesn't work (with Marco)
	
	mint-mirrors

Done:
-----

	kde
		pam_kwallet support in MDM

LMDE
----
	update virtualbox
	update synaptic adjustment in mintsystem for lmde
	live-installer: turn avatar selector into a nicer widget ala cinnamon-settings account details
	live-installer: check free space on /target before installing
	glib 2.41 regression on mutex, PRs for mint tools and/or fix in GTK 3.14.1 and waiting for GTK2 fix https://github.com/GNOME/gtk/commit/fbf38d16bcc26630f0f721d266509f5bc292f606
	gtk 3.12+
		 invisible checkboxes, too thin horizontal progressbar, and gtk-warnings about symbolic icons in an "open file" dialog.
		 fix ugly dialogs https://github.com/mate-desktop/marco/commit/42c63250abf2b4c7b1c704c907301bb5a5920b6e
		 muffin: do we need this https://git.gnome.org/browse/metacity/commit/?id=a6b29b2d2f6a7787c59cfffdc2bed1b5b5b99244	
	gtk 3.14
		https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=766100
	bring back totem-mozilla or find alternative