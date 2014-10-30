
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

KDE
---
	mdm: When loging in an existing session, doesn't unlock kde screensaver

Xfce
----
	mdm: When loging in an existing session, doesn't unlock xscreensaver

Next Release
------------
	Consider adding pipelight
	Consider porting cinnamon-bluetooth into gnome-bluetooth-frontend, for use in MATE and Xfce
	fonts: try fonts-noto
	fonts: Would Linux Mint mind changing the default CJK font in the future release?like Adobe’s source han sans. As a Traditional Chinese user, the default font Linux Mint now using is pretty awkward, and even didn’t follow the hand writing rules and education standard. The fedora team changed their default font to Adobe”s source han sans and it’s great.
	fonts: ship with fonts-unfonts-core by default? Fixes https://code.google.com/p/chromium/issues/detail?id=82400
	oem: rephrase isolinux/grub option --> s/Start Linux Mint/Preinstall Linux Mint/g
	see if we can make life easier for people using nonPAE kernels (live/boot args, and take kernel updates into account)
	kde: MintXKDE.colors https://dl.dropboxusercontent.com/u/11675431/MintXKDE.colors http://forums.linuxmint.com/viewtopic.php?f=153&t=61241
	xfce: revive xfapplet
	xfce: Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
	xfce: Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!)
	xfce: switch datetime applet to Clock applet	
	hexchat: implement PR for /etc/hexchat for distro to set default list of networks https://github.com/hexchat/hexchat; http://anonscm.debian.org/cgit/collab-maint/hexchat.git/ (sney mailto:drubo@drubo.net)
	indicator-applet patch: https://bugzilla.gnome.org/show_bug.cgi?id=726030
	nemo: remove duplication between Eject and Safely Remove (for removable devices)	
	ubiquity: https://bugs.launchpad.net/linuxmint/+bug/1325786	
	ubiquity: keyboard layout selection sets itself back to EN when no click is done in the table
	ubiquity: import upstream fixes
	ubiquity: fix installation for Swiss German users (fixed upstream https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1182784)
	ubiquity: make sure LC_TIME follows language choice, not timezone selection
	mint 17 mate 32 edition: screensaver kicks in during install... port this to Mint https://github.com/linuxmint/live-installer/blob/master/usr/lib/live-installer/frontend/gtk_interface.py#L196		
	mintinstall: should show licenses
	mintinstall: should separate impacts between installs and removals
	mintstick: Add % completion to window title
	mintsystem: add APT priority definitions for known PPAs and repositories
	mintsystem: make "apt download" download dependencies to the ./pkgname directory		
	cinnamon: fix spacing between systray icons
	cinnamon: improve network settings
	mate: http://mate-desktop.org/blog/2014-09-29-mate-1-8-updated/
	mate: make compiz work out of the box?
	consider installing timeshift
	grub background and full screen?
	full screen bootsplash? check how it's done in Ubuntu	
	muffin: do we need this https://git.gnome.org/browse/metacity/commit/?id=a6b29b2d2f6a7787c59cfffdc2bed1b5b5b99244
	mintinstall: removing gnupg removes apt.. the info is there but it's far from obvious enough!
	[RFT] firefox: don't preset browser.showQuitWarning

	inconsistent names (menu vs cinnamon-settings):
		Accessibilité (dans paramètres systèmes) → Accès universel (menu)
		Programmes au démarrage (dans paramètres systèmes) → Applications au démarrage (menu)
		Affichage (dans paramètres systèmes) → AffichageS (menu)
		CouleurS (dans paramètres systèmes) → Couleur (menu)
		Tablette graphique (dans paramètres systèmes) → Graphics Tablet (menu)
		Pilotes de périphériques (dans paramètres systèmes) → Gestionnaire de pilotes (menu)
		Écran de connexion (dans paramètres systèmes) → Fenêtre de connexion (menu)
		Sources de mise à jour (dans paramètres systèmes) → Sources de logiciels (menu)

	gtk 3.12+
		 invisible checkboxes, too thin horizontal progressbar, and gtk-warnings about symbolic icons in an "open file" dialog.
		 fix ugly dialogs https://github.com/mate-desktop/marco/commit/42c63250abf2b4c7b1c704c907301bb5a5920b6e

	done:
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
			3 finger touchpad support
			all cs icons in mint-x icon theme
			multiple panel launchers
			remove logout countdown			
			new background selection + slideshow support + slideshow applet
			configurable fonts in screensaver
			startup animation
			privacy settings
			notification settings
			disabling compositing for fullscreen windows OFF by default and now configurable
			super+e opens home
			desktop font configurable
		nemo
			highlight icons on hover in sidebar
			toolbar UI changes
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