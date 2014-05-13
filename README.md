
Backports
---------
	x-caja-desktop fix for Petra and Maya


Mint 17
--------------------
	KDE: 
		The installer doesn't install language-pack-gnome-xx resulting in GTK apps/dialogs showing in English
		also xfce, mdm: When loggin in an existing session, doesn't unlock kde screensaver, xscreensaver or gnome-screensaver (works fine with cinnamon-screensaver and mate-screensaver)
		Consider not using oxygen for GTK (check with mintBackup filechooser)	
		mintbackup, mintnanny, mintupload, mintdrivers, mintsources: remove KDE adjustment, add a specific KDE .desktop file
		missing mint-mdm-themes-kde
	xfce: 
		doesn't seem to detect DVD insertion, doesn't run VLC (works in 32bit, not 64bit)
		Can't use the trash in live mode
		There are no GTK bookmarks by default
		missing indicator-sound indicator-sound-gtk2		

	MATE: 
		https://github.com/linuxmint/mintmenu/pull/89
		OK missing gnome-keyring				
			
	Other:
		unity-greeter pkg
		gedit-plugins pkg				
		mintlocale missing ibus activation support	
		update translations for mintdrivers

	RFT:
		OK applets: Can't minimize windows which have a modal dialog (for example: Synaptic while installing a package). It's possible via the titlebar, but not via the window list
		OK prefs: I miss the working WIN+D keyboard shortcut to go to desktop.

	done
		mintwelcome redesign
		mintlocale
		mintmenu: panel applet transparency, multiple bug fixes
		hexchat replaces xchat
		mintupdate: handle kernel upgrades (show more info to advanced users)
		mintupdate: redesign, no need to elevate user to root to see updates
		mintupdate: redesign startup delay
		mintdesktop simplified UI, detects Marco
		mintsources: consider changing the way opt-in works for romeo and backport
		regenerate desktop files post-translations
		mint-x: MATE Panel transparency
		mdm shutdown sequence
		mdm recovery

	maintenance:
		reopen LMDE rsyncd


	