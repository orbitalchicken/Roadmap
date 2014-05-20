
Backports
---------
	x-caja-desktop fix for Petra and Maya


All Editions
------------
	GIT - slideshow: Xchat still shown in the installer slideshow
	pkgs: unity-greeter pkg
	pkgs: gedit-plugins pkg					
	mintlocale: missing ibus activation support	
		illustration: I tried to install Japanese as extra language. I could install Japanese, but the option to select an input manager like Ibus is gone. When I installed IBUS, ibus-Anthy and Japanese Takao fonts like takao mincho, takako gothic, I still could not select the input method from Ibus itself. On mint 13 no problem, here I am a little lost.
	mintdrivers: update translations
	mintdrivers: remove the apt-cdrom repository when exiting			
	mint-mirrors: update list of mirrors			
	mintsources: The button “No action required” is not aligned along the right boundary with the text window below it.
	mdm: second login screen does not say “Please enter your password” – no instruction text appears.
	As Linux Mint comes with VLC preinstalled, should we advise people that if they use external optical disk drives, in VLC, they should go into Tools -> Preferences -> Input & codecs -> then under optical drive -> change “/dev/dvd” to to “/dev/sr0″	
	
Cinnamon
--------
	OK - tomboy is missing
	OK - libgksu: remove fade animation
	cinnamon: only 1 msgid for "Lock Screen" (action vs noun)
	cinnamon-settings: can't set hours in datetime module
	cinnamon-settings: datetime module doesn't fit in window
	cinnamon-settings: desklets - left-align the note underneath “Decoration of desklets”
	cinnamon-settings: themes - inconsistent aspect ratios for thumbnails
	cinnamon-settings: lockscreen - make the “Show this message when the screen is locked” input box larger and on its own row below.	
	Super+e should open file manager
	In keyboard settings -> User defined keyboard shortcuts, three phrases are shown when hovering above the keyboard binding. The first is translated, but “Press Escape or click again to cancel the operation” and “Press Backspace to clear the existing keybinding” are not translated though they have been translated in Launchpad (Danish).
	If Open menu when mouse hovers is selected, right-clicking the menu and moving the mouse upwards to select Configure often leads to the menu opening and the right-click menu disappears before it can be clicked. Doing it a couple of times in succession finally allows one to clicking Configure – it varies how may times I have to try before I succeed.

MATE
----
	OK - gparted is missing
	OK - Remove mate-user-share? In Control Center, Shared Folders and User Share seem to duplicate and don't work well together. I have noticed that Shared Folders (from the Control Centre) will not save any shares I add.
	mintmenu: https://github.com/linuxmint/mintmenu/pull/89
		Mint menu is uncklickable when using compiz. It will open through mouse click and shortcut, but clicking on an entry in the menu will just close the menu without any action.
		Using composition “When clicked”, the mintmenu feels like it is behind the panel. On the other hand the window of the panel indicators is above the panel. 
	mintmenu: Multiple Menu Entries – The menu has two entries for gnome-disk, libreoffice draw, and mate-volume-control in the ‘All’ category. This will appear when you first log into the system, but will disappear if you search through the menu and then look in the ‘All’ category
	caja-dropbox depends on dropbox, which is missing in repository
	When you open Banshee, and close the window, a notification is shown beyond borders of desktop. You can see only top left corner of notification.
	remove ugly minimize effect "org.mate.interface enable-animations"
	mint-meta-mate package still depends on mate-doc-utils, which has been replaced by yelp-tools in MATE 1.8.


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

 