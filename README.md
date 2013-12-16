Confirmed issues

KDE
---
	[Fixed] mintstick KDE action shows also for DVD and floppy disks	
	remove openssh
	consider using https instead of http for Amazon queries	
	After reboot, I can’t seem to find Update Manager icon.
	Can’t log out properly. It just goes to a black screen and all I can do is ctrl alt bksp and restart from the prompt.
	Just noticed a dead (sort of) link. When changing my Appearance, the Theme tab has a link “Get more themes online”, the url is https://wiki.gnome.org/Personalizationthemes/. That page gives you a nice message “This page does not exist yet.”
	The Network Management Icon in the System Tray doesn’t change when the network is disconnected.	
	plain text redirect of all Amazon search terms to the Mint server
	If ~/.kde/env directory exists I cannot log in. http://userbase.kde.org/Session_Environment_Variables The file ~/.kde/env/path.sh is no longer honored by the rewritten /usr/bin/startkde program. If I rename the env directory to env_hold, I can log in. If I rename it back to env, I get caught in the loop that asks me about qdbus again, and I cannot login. I looks as though the person who rewrote the startkde program was unable to completely test it. Posts from last August are here: http://forums.linuxmint.com/viewtopic.php?f=109&t=143649
	[127]mint@mint:~ > mintBackup You do not have the required dependencies Traceback (most recent call last): File “/usr/lib/linuxmint/mintBackup/mintBackup.py”, line 88, in class MessageDialog(apt.progress.gtk2.GOpProgress): AttributeError: ‘module’ object has no attribute ‘gtk2′ 
	Translation leak, install with non english language (I used spanish), once installed, open Firefox, go to File menu, Open file, the dialog box is not translated, not the places section, not even the buttons.

Xfce
----
    Xfce doesn't seem to detect DVD insertion, doesn't run VLC (works in 32bit, not 64bit)
	Can't use the trash in live mode    
	There are no GTK bookmarks by default

Mint 17
-------	
	mdm: In OEM mode, MDM preselects the "oem" user (user no longer active but still present in AccountsServices) :)
	mdm: When loggin in an existing session, doesn't unlock kde screensaver, xscreensaver or gnome-screensaver (works fine with cinnamon-screensaver and mate-screensaver)
	system: switch to adobe-flashplugin
	banshee: use mp3 decoding by default
	cinnamon: enable touchpad tapping by default
	mintbackup, mintnanny, mintupload, mintdrivers, mintsources: remove KDE adjustment, add a specific KDE .desktop file
	mintdesktop: When Compiz is active with MATE, WM preferences have to go to Metacity gconf settings instead of Marco ones to work.
	mintdrivers: should we re-add a systray icon to notify users at session startup?
