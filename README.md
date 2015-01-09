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

	[Fixed in Git] CS THEMES: breaks when thumbnails' permission is wrong (no right to read)
	[Fixed in Git] when I try to open cinnamon-settings (after the upgrade), I only get the message “cannot import name Notify”
	nemo: can no longer handle desktop in root session
	clicking on the base mirror in software sources does not work https://bugs.launchpad.net/linuxmint/+bug/1400096
	On MATE version I have trouble with the screenshot action.. when I press printscreen on my keyboard always freezing… same thing happen when I open screenshot app manually..
	Cinnamon: can't connect to WPA enterprise
	Cinnamon: port this https://github.com/rgcjonas/gnome-shell-extension-appindicator

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