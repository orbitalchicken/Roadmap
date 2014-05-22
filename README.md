
Backports
---------
	x-caja-desktop fix for Petra and Maya


All Editions
------------
	OK - slideshow: Xchat still shown in the installer slideshow
	pkgs: unity-greeter pkg
	pkgs: gedit-plugins pkg
	update translations
	mintdrivers: remove the apt-cdrom repository when exiting
	mint-mirrors: update list of mirrors
	FF News Link points to var/www/syscpwebs/lm/planet
	
Cinnamon
--------
	OK - tomboy is missing
	cinnamon: regenerate cs desktop files with new translations	

MATE
----
	OK - gparted is missing
	OK - Remove mate-user-share? In Control Center, Shared Folders and User Share seem to duplicate and don't work well together. I have noticed that Shared Folders (from the Control Centre) will not save any shares I add.
	OK - mint-meta-mate package still depends on mate-doc-utils, which has been replaced by yelp-tools in MATE 1.8.
	OK - remove ugly minimize effect "org.mate.interface enable-animations"
	OK - trackpad should have tap-to-click enabled.
	OK - When you open Banshee, and close the window, a notification is shown beyond borders of desktop. You can see only top left corner of notification.
	OK - going CTRL-I (keyboard hotkey for the line selection tool) crashes pluma 1.8.0, but there is a new 1.8.1 pluma tag that fixes this.	
	OK - mintmenu: multiple issues with compiz		
	OK - mintmenu: Multiple Menu Entries – The menu has two entries for gnome-disk, libreoffice draw, and mate-volume-control in the ‘All’ category. This will appear when you first log into the system, but will disappear if you search through the menu and then look in the ‘All’ category
	caja-dropbox depends on dropbox, which is missing in repository	

KDE
---
	OK - Consider not using oxygen for GTK (check with mintBackup filechooser)	
	OK - missing mint-mdm-themes-kde
	The installer doesn't install language-pack-gnome-xx resulting in GTK apps/dialogs showing in English
	also xfce, mdm: When loggin in an existing session, doesn't unlock kde screensaver, xscreensaver or gnome-screensaver (works fine with cinnamon-screensaver and mate-screensaver)	
	mintbackup, mintnanny, mintupload, mintdrivers, mintsources: remove KDE adjustment, add a specific KDE .desktop file
	
Xfce
----
	doesn't seem to detect DVD insertion, doesn't run VLC (works in 32bit, not 64bit)
	Can't use the trash in live mode
	There are no GTK bookmarks by default
	missing indicator-sound indicator-sound-gtk2		

 