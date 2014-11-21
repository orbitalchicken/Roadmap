Fixed Issues since Mint 17.1 RC

All editions
------------
	- when resizing Software Sources window, its scale up and never scale down!
	- LibreOffice theme is missing some sidebar icons
	- please bring back the “Mint-X-Dark” icon set. its important for dark themes..	
	- Help menu item launches linuxmint.com/documentation.php instead of mintdoc
	
Cinnamon Edition
----------------
	- expo trash icon isn't sized properly
	- cinnamon-themes to use noto fonts
	- nemo-emblems: hide ubuntuone, dropbox icons
	[Fixed in Git]
		- settings/backgrounds Gradient and Picture Aspect text not aligned on the left side.
		- settings/preferedapps Consider little bit more spacing under the Terminal dropdown to balance the window elements a bit.
		- Account details: Cinnamon 17, by default link: http://s26.postimg.org/armd84n21/Screenshot_from_2014_11_17_10_04_05.png, 17.1 by default: http://s26.postimg.org/gyxr8ait5/Screenshot_from_2014_11_17_10_35_12.png
		- Accessibility settings, typing, turning on-screen keyboard on or off does not appear to do anything. 
		- Usint mint-x aqua theme when you maximize windows they go behind panel. Default theme doesn’t do this. I haven’t tried others.
		- I disabled the recently used Files. After that the menu gets way to wide (it reach nearly to the 17.1 on the wallpaper. There is a text in the menu that says “recently used files are disabled…” (I don’t know the correct words, i use the german language)	?
		- systray icons (reproducible with mintupdate) in bottom panel does not scale with the size of the panel. Increasing the size of the panel does not increase the Update Manager icon (even when all the other icons increase in size…yes I ticked that box :) ).			
		- cinnamon-settings-users should not let root modify user's passwords when their home is crypted	
		- Regression in Nemo: Misplaced rename text entry https://github.com/linuxmint/nemo/issues/757
		- Regression in Nemo: When switching the sidebar view to tree view and back, some entries in the “Devices” category are displaced/displayed incorrectly. On mouse-over they display correctly again.
		- mdm:
			- mdmsetup Under the Welcome Message the text input area for Custom should align on the left hand side with the ‘Welcome’ text above it. Either ‘Welcome’ should be moved to the right or the text input area increased to the left to get the correct alignment.
			- mdm https://github.com/linuxmint/mdm/pull/127

	
MATE Edition
------------
	- Ctrl+Alt+Backspace doesn't do anything.
	- Caja still uses a 3 sec delay at launch. With partial fixes in systemd and caja on runtime dir issues we could probably remove this or reduce it to a single sec.	
	- Can't make CCSM changes stick	
	- mintdesktop: mate-wm-recovery doesn't always work....

KDE Edition
-----------

Xfce Edition
------------
	