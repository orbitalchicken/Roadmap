Backports
---------
	Maya
		x-caja-desktop fix
		MDM session limiting
	17.x
		libreoffice 4.4 in 17.x
		inkscape 0.9.1


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
	Cinnamon: factorize GVC code across multiple projects
	kdeenlive: missing german translations
	mintupdate: possibility to turn on a automatic disapear of the Update Manager window after it's successful done
	kodi/xbmc instructions tell people to install python-software-properties and software-properties-common

KDE/Xfce Mint 17.1
------------------
	common:
		When logging in an existing session, doesn't unlock xscreensaver / of KDE screensaver

	xfce
		Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
		Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!)
		indicator-applet patch: https://bugzilla.gnome.org/show_bug.cgi?id=726030

LMDE
----
	COMMON
		[Fixed] gtk apply 17.x sauce
		gtk filechooser dialogs, too much vertical space between elements in the sidebar
	    libpam-systemd runtime dir collisions: (caja:10507): dconf-CRITICAL **: unable to create file '/run/user/1000/dconf/user': Permission non accordée.  dconf will not work properly.
	    missing plymouth-text theme

	CINNAMON SPECIFIC
		port cinnamon-bluetooth

	MATE SPECIFIC
	    Relogin in MDM doesn't unlock mate-screensaver

17.2
----
	Firefox
		disable telemetry/reset/etc notifications
	update bash.bashrc and .bashrc
	support broadcom ootb
	xfce 4.12
