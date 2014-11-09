Backports
---------
	x-caja-desktop fix for Maya
	LO 4.3?
	KDE 4.14

Maintenance
-----------
	Update tapatalk API on forums
	pkgs: unity-greeter pkg
	modemmanager hangs at shutdown
	rel notes: no network after suspending? https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1286552	
	patch for MATE: https://github.com/linuxmint/mate-packages/pull/4
	upgrade inxi to 2.1.28
	upgrade xfce4-whiskermenu-plugin to 1.4.0?

Consider for Mint 17.1
----------------------
	kde: MintXKDE.colors https://dl.dropboxusercontent.com/u/11675431/MintXKDE.colors http://forums.linuxmint.com/viewtopic.php?f=153&t=61241
	xfce: revive xfapplet
	mdm: When logging in an existing session, doesn't unlock xscreensaver / of KDE screensaver
	The power button set to “shut down immediately” still ‘asks’
	remove modemmanager?
	[Can't reproduce] Regression in Nemo: Umounting dual-partitioned HDD freezes Nemo

Todo for Mint 17.1
------------------

	artwork
		[RFT] mdm theme slideshow delay is too small
		[RFT] duplicate bgs in mint-backgrounds-retro vs olivia
		[RFT] default bgs still show qiana and 17
		mint-themes: eclipse UI https://bugs.launchpad.net/linuxmint/+bug/1168281

	live
		[Fred] rephrase OEM isolinux/grub option --> s/Start Linux Mint/Preinstall Linux Mint/g
		[Fred] see if we can make life easier for people using nonPAE kernels (live/boot args, and take kernel updates into account)
		pin base-files?
		inserting live-stick, stick isn't mounted automatically in /media
		security option not recognized

	cinnamon
		[RFT] Regression: custom keybindings lost during upgrade		
		Regression in Network Settings: Not possible to setup mobile broadband? https://github.com/linuxmint/Cinnamon/issues/3640
		Regression in Nemo: Misplaced rename text entry https://github.com/linuxmint/nemo/issues/757
		Regression in Nemo: When switching the sidebar view to tree view and back, some entries in the “Devices” category are displaced/displayed incorrectly. On mouse-over they display correctly again.
		Regression: DND minifreezes..
		update cinnamon-translations
			
	mate
		[RFT] mate 1.8.x http://mate-desktop.org/blog/2014-09-29-mate-1-8-updated/
		brightness OSD doesn't work (with Marco)

	kde
		[RFT] kde 4.14

	xfce
		Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
		Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!)
		switch datetime applet to Clock applet	

	indicator-applet patch: https://bugzilla.gnome.org/show_bug.cgi?id=726030	
		
	mint tools		
		mintsystem: add APT priority definitions for known PPAs and repositories
		mintdoc: finish user guide, package it etc..
		update mint-translations
		mintmenu PRs and issues
		mintsystem
		mint-mirrors
	
	docs
		rel_notes
		start page
		migrate documentation to mintdoc
		
	upgrade path
		implement visual upgrade path for Mint 17 users (use mint-meta as a precondition)		

Done:
-----
	mintupdate:
		kernel page redesign
		package descriptions are now complete and l10n'd
		proxy support in changelog retrieval
		handle source packages, not packages
		window no longer hides after installing updates
	mintsources:
		better repository names
		test mirrors in parallel
		retry mechanism on timeout, remove erroneous mirrors from the list
	mintsystem
		pastebin command
		search now uses current folder by default
	mintstick
		Added % completion in titlebar
	cinnamon
		cjs rebase
		super+e opens home
		new network settings
		screensaver
			custom date formats
			custom fonts and colors
		3 finger touchpad support
		smoother experience
			startup animation
			login sound in sync
			fixed a lot of memory leak
			moved commonly used icons to the icon theme (decreases latency)
			disabling compositing for fullscreen windows OFF by default and now configurable				
			many bug fixes
			many little UI refinements
			desktop font configurable
			cinnamon settings and menu categories are now sorted alphabetically

		multiple panel launchers
		new background selection + slideshow support + slideshow applet			
		privacy settings
		notification settings
		better theme settings						
	nemo
		smarter bookmark section in sidebar
		highlight icons on hover in sidebar
		new toolbar UI with configurable buttons
		folder-color
		emblem support
	caja
		folder-color
	mate
		compiz works out of the box, ability to switch between Marco and Compiz (on compatible GPUs, doesn't work in Virtualbox)
	mint-x
		color variations
	mdm
		better mdmsetup
		slideshow in mint-x
		.xsession-errors limit and filtering			
		include more HTML themes
		syndaemon called in Init
		filter and limit .xsession-errors
		pam_kwallet			
	user guide
	mintlocale
		new UI
		regional settings
		im support
		handle all locales, not just UTF-8
	mintinstall
		separates impacts between installs and removals
		warns about removals
	artwork
		Noto Fonts

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