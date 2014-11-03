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
	mdm: When loging in an existing session, doesn't unlock xscreensaver / of KDE screensaver
	mate: make compiz work out of the box?
	Nemo conflicts with fcitx, the best chinese input method. I can’t rename anything in Nemo with fcitx.
	The power button set to “shut down immediately” still ‘asks’
	remove modemmanager?
	bring back hardinfo?

Todo for Mint 17.1
------------------
	artwork
		rebecca backgrounds
		grub background and full screen?
		full screen bootsplash? check how it's done in Ubuntu
	live
		rephrase OEM isolinux/grub option --> s/Start Linux Mint/Preinstall Linux Mint/g
		see if we can make life easier for people using nonPAE kernels (live/boot args, and take kernel updates into account)
		set up build system to build with updates
		guarantee the same version of Firefox-l10n as Firefox itself is installed post-install
		select the new kernel for Rebecca
	ubiquity
		https://bugs.launchpad.net/linuxmint/+bug/1325786	
		keyboard layout selection sets itself back to EN when no click is done in the table
		import upstream fixes
		fix installation for Swiss German users (fixed upstream https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1182784)
		make sure LC_TIME follows language choice, not timezone selection
	package selection / configuration
		switch to fonts-noto
		[RFT] firefox: don't preset browser.showQuitWarning
		consider installing timeshift

	cinnamon
		fix spacing between systray icons
		fix regression on umounting HDD in Nemo
		fix possible regression with mobile broadband? https://github.com/linuxmint/Cinnamon/issues/3640
		don't show keybinding OSDs when notifications are off
		muffin: do we need this https://git.gnome.org/browse/metacity/commit/?id=a6b29b2d2f6a7787c59cfffdc2bed1b5b5b99244
		inconsistent names (menu vs cinnamon-settings):
			Accessibilité (dans paramètres systèmes) → Accès universel (menu)
			Programmes au démarrage (dans paramètres systèmes) → Applications au démarrage (menu)
			Affichage (dans paramètres systèmes) → AffichageS (menu)
			CouleurS (dans paramètres systèmes) → Couleur (menu)
			Tablette graphique (dans paramètres systèmes) → Graphics Tablet (menu)
			Pilotes de périphériques (dans paramètres systèmes) → Gestionnaire de pilotes (menu)
			Écran de connexion (dans paramètres systèmes) → Fenêtre de connexion (menu)
			Sources de mise à jour (dans paramètres systèmes) → Sources de logiciels (menu)	
		l10n:
			System Settings -> Windows: The options in the four drop-down boxes “Action on title bar double-click”, “Action on title bar double-click”, “Action on title bar right-click” and “Window focus mode”.
			Language Settings: “Apply System-Wide”, “Install / Remove Languages”, the associated tool tips and all the text.
			System Settings -> Network -> Proxy: The options under Method.
			System Settings -> Graphics Tablet: “No tablet detected – please plug in or turn on your graphics tablet”
			System Settings -> Software Sources: Text in Maintenance button
			System Settings -> Fonts: Options in the two drop-down boxes Antialiasing and Hinting.
			System Settings -> Applets/Desklets/Extensions/Themes: Blue text “More info” (right-clicking opens a menu that is translated)
			System Settings -> Monitor: Options in the drop-down box Rotation
			System Settings -> Desklets: The buttons Highlight and Remove (configuring a desklet).
			Menu Editor: “Main Menu” (title bar), “New Menu”, New Item”, “Move Up”, “Move Down”, “Restore System Configuration”.
			In System Settings\Windows the options (Toggle Shade etc.) for the first four entries are not translated.
			In System Settings\Fonts “None”, “Greyscale”, “Slight”, “Medium” and “Full” are not translated to Danish though Danish is 100% translated.

	
	mate
		[RFT] mate 1.8.x
		mint 17 mate 32 edition: screensaver kicks in during install... port this to Mint https://github.com/linuxmint/live-installer/blob/master/usr/lib/live-installer/frontend/gtk_interface.py#L196

	kde
		[RFT] kde 4.14

	xfce
		Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
		Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!)
		switch datetime applet to Clock applet	

	indicator-applet patch: https://bugzilla.gnome.org/show_bug.cgi?id=726030	
		
	mint tools
		mintinstall: should show licenses
		mintinstall: should separate impacts between installs and removals
		mintinstall: removing gnupg removes apt.. the info is there but it's far from obvious enough!
		mintinstall "show all results" not l10n	
		mintstick: Add % completion to window title
		mintsystem: add APT priority definitions for known PPAs and repositories
		mintsystem: make "apt download" download dependencies to the ./pkgname directory		
		mintdoc: finish user guide, package it etc..
	
	docs
		rel_notes
		start page
		migrate documentation to mintdoc

	mate
		http://mate-desktop.org/blog/2014-09-29-mate-1-8-updated/
		
	upgrade path
		implement visual upgrade path for Mint 17 users
		folder-color-switcher
		user-guide
		nemo-emblems	

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
	mint-x
		color variations
	mdm
		better mdmsetup
		slideshow in mint-x
		.xsession-errors limit and filtering			
		include more HTML themes			
	user guide
	mintlocale
		new UI
		regional settings
		im support
		handle all locales, not just UTF-8

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