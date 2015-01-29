Backports
---------
	Maya
		x-caja-desktop fix
		MDM session limiting
	17.x
		libreoffice 4.3 in 17.x

Maintenance
-----------
	Update tapatalk API on forums
	pkgs: unity-greeter pkg
	rel notes: no network after suspending? https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1286552
	upgrade inxi to 2.1.28
	mate: The Mate Panel right side application indicator icons and clock, and when some other icons are pinned there scramble and get switched around and stay in the middle of the Panel sometimes – when changing Desktop resolution.
	MDM: reinterpret "default" session.. DESKTOP_SESSION should be set properly
	nemo: can no longer handle desktop in root session
	On MATE version I have trouble with the screenshot action.. when I press printscreen on my keyboard always freezing… same thing happen when I open screenshot app manually..
	Cinnamon: can't connect to WPA enterprise
	Cinnamon: port this https://github.com/rgcjonas/gnome-shell-extension-appindicator
	kdeenlive: missing german translations
	mintupdate: possibility to turn on a automatic disapear of the Update Manager window after it's successful done
	kodi/xbmc instructions tell people to install python-software-properties and software-properties-common

KDE/Xfce Mint 17.1
------------------
	common:
		When logging in an existing session, doesn't unlock xscreensaver / of KDE screensaver
		add support for KDE/Xfce for mint-backgrounds-*
		add support for KDE/Xfce for mint-backgrounds-maya

	xfce
		Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
		Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!)
		indicator-applet patch: https://bugzilla.gnome.org/show_bug.cgi?id=726030

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

	patch/remove/downgrade CSD applications
		gcalc
		evince
		system-monitor
		fileroller
	fix gedit-plugins
	live-installer
		PRs
		multi-hdd install
		Review live-installer from Tanglu (https://gitorious.org/tanglu/tanglu-live-installer) and Manjaro (http://git.manjaro.org/core/live-installer)
		Review Cinnarch installer (https://github.com/Antergos/Cnchi) and Manjaro fork (https://github.com/manjaro/thus)
	cinnamon
		settings->backgrounds doesn't list backgrounds
		muffin: context menu on CSD titlebars https://github.com/linuxmint/muffin/commit/57680ced5d0989ff0810317e4ff0e2333b449488
	packages
		backgrounds galore missing
	yahoo urls are obsolete
	imagemagik shows up in the menu
	gdebi is in the menu
	isolinux still points to initrd.img (we moved to lzma)
	Gtk
		Apply 17.x sauce
		Remove CSD from dialogs
	Fix yelp ala 17.x
	System
		grub title isn't right
		Add ecryptfs and other crypt packages?
		Triple mint-fortune issue with bash.bashrc
		check fsck presence for ALL other FS'es
		XFS won't boot because of missing fsck.xfs https://bugs.launchpad.net/bugs/1322164
		Don't show error codes in bash prompt
		isolinux: localboot won't work (chain it?)
		when live-installer removes live packages, it switches the init system from sysv to systemd
		installer seems to fail updating initramfs when the ISO is built with LZMA compression