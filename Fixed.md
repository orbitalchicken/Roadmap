Fixed Issues since Mint 17 RC

All editions
------------
	mdm: login screen freezes for German speaking users
	mdm: second login screen does not say “Please enter your password” – no instruction text appears.
	mintsources: unable to add PPAs.. print(" %s" % (ppa_info["description"].encode("utf-8") or "")) --> AttributeError: ‘NoneType’ object has no attribute ‘encode’
	mintsources: The button "No action required" is not aligned along the right boundary with the text window below it.
	mintdrivers: failed to start when connection to the Internet was slow
	mintlocale: No keyboard navigation
	mintinstall: don't allow installation of broken packages, or packages which don't install properly in mintinstall.
	system: support for NVIDIA Optimus cards with nvidia-prime
	skype: sound issues (added suggestion to install ia32-libs to release notes).
	vlc: suggested to use “/dev/sr0″ for DVD playback in release notes
	gksu: freezes/lags due to fade-out animation
	mint-x: black background in Evolution's toolbar
	file-roller: Only one instance can run at a time
	gtk: symbolic icons in open dialogs
	gtk: scrollbars should not warp

Cinnamon Edition
----------------
	cinnamon-settings: datetime module doesn't fit in window
	cinnamon: only 1 msgid for "Lock Screen" (action vs noun)	
	cinnamon-settings: lockscreen - make the “Show this message when the screen is locked” input box larger and on its own row below.	
	cinnamon-settings: can't set hours in datetime module
	cinnamon-settings: desklets - left-align the note underneath “Decoration of desklets”	
	In keyboard settings -> User defined keyboard shortcuts, three phrases are shown when hovering above the keyboard binding. The first is translated, but “Press Escape or click again to cancel the operation” and “Press Backspace to clear the existing keybinding” are not translated though they have been translated in Launchpad (Danish).
	chromium: After watching a full screen video (for example on Youtube) the panels are disappearing (the browser window hides them).	
	If Open menu when mouse hovers is selected, right-clicking the menu and moving the mouse upwards to select Configure often leads to the menu opening and the right-click menu disappears before it can be clicked. Doing it a couple of times in succession finally allows one to clicking Configure – it varies how may times I have to try before I succeed.
	Breadcrumbs in Nemo do not display correctly with Adwaita theme or High Contrast theme.

	
MATE Edition
------------
	

KDE Edition
-----------
	

Xfce Edition
------------
	