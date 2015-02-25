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
		update synaptic adjustment in mintsystem for lmde
		fix gedit-plugins
		gtk apply 17.x sauce
		gtk filechooser dialogs, too much vertical space between elements in the sidebar
		yahoo urls are obsolete
		yahoo is missing in en_US (sometimes?)
		mintsources: doesn't know which country http://ftp.debian.org/debian is from
		mintsources: Common LMDE apt keys aren't added to mintsources configuration
		Remove mplayer
	    Downgrade totem
	    Quicktime playback not working
	    libpam-systemd runtime dir collisions: (caja:10507): dconf-CRITICAL **: unable to create file '/run/user/1000/dconf/user': Permission non accordée.  dconf will not work properly.
	    grub: menu name isn't right
	    help: User Guide is for Linux Mint 17
	    ff: start page should be betsy not debian
	    doc: rel and rel_new pages don't exist yet
	    No kernel metapackage and kernel selection in mintupdate isn't adapted to LMDE
	    Hexchat doesn't autoconnect to #linuxmint-help
	    plymouth: boot logo doesn't show up properly (might be specific to virtualbox)
	    [RFT] Add gnome-disk-utility
	    [RFT] packages: vim should be removed
	    [Fixed in Git, needs new version of live-installer and mint-translations] live-installer l10n: missing translations for:
	        [Fixed] Log in automatically on system boot
	        [Fixed] This will be shown in the About Me application
	        [Fixed] Please select a root (/) partition.
	        [Fixed] Please select an EFI partition.
	        [Fixed] Installation is now complete. Do you want..etc..
	        [Fixed] Browse for more pictures (possibly also the string used for webcam capture)
	        [Fixed] Click to change your picture
	        [Fixed] Edit (partitioning context menu)
	        [Fixed] Assign To (partitioning context menu)
	        [Fixed] GB (sizes unit in free space column and size colum)
	        [Fixed] Mount Point (edit dialog)
	        [Fixed] Format as (edit dialog)
	        [Fixed] Copying (in installation step)
	        [Fixed] Formatting (in installation step)
	    [Fixed] live-installer: Mode Expert button isn't aligned properly

	CINNAMON SPECIFIC
		port cinnamon-bluetooth

	MATE SPECIFIC
	    mint-x-theme: mate-system-monitor isn't properly themed
	    mate: preferred apps either not set or badly set
		[RFT] No such key 'menus-have-icons' in schema 'org.gnome.desktop.interface' as specified in override file '/usr/share/glib-2.0/schemas/mint-artwork-mate.gschema.override'; ignoring override for this key.
	    Relogin in MDM doesn't unlock mate-screensaver
	    Missing blueman (need to test on real HW without bt adapter, we don't want BT to show up when no adapters are present, this was the reason it wasn't present in Mint 17.x).
	    Missing mate-user-guide
	    [RFT] Add panel launchers (like in Cinnamon)
	    Some MATE applications don't use generic names
	    caja: renaming a file produces a black border
	    mime: text files are associated with LibreOffice by default
	    mime: html files open up with thunderbird
	    compiz integration missing
	    [RFT] bash: prompt isn't set properly
	    caja: it looks like caja briefly dies at session start just before reappearing again
	    marco: CSD are not properly rounded
	    [Fixed] mintmenu: one slot is empty in the favorites

17.2
----
	Firefox
		disable telemetry/reset/etc notifications
	update bash.bashrc and .bashrc
	support broadcom ootb