Fixed Issues since Mint 16 RC

All editions
------------
	apps/drivers: some packages (wine for instance) can't be installed after using the xorg-edgers PPA (caused by priority 700 on PPA)	
	mintupdate: not visible in Startup Applications	
	mintdrivers: doesn't apply ATI icon to "Advanced Micro Devices, Inc. [AMD/ATI]: Wrestler [Radeon HD 6290]"	
	mintdrivers: Nvidia drivers dont automaticaly install nvidia-settings (Tested with nvidia-319 and nvidi-319-updates)
	mdm: nvidia-319 installed, login works fine. Log out and different user logs in --> blank screen with a mouse pointer. Switch users works ok.
	apturl/firefox: apturl missing support in Firefox	
	[FIXED] plymouth-stop and hybrid-check don't listen to mdm events in upstart
	system: crashes/freezes	due to /run/user/<uid>/dconf/user being owned by root - https://bugzilla.redhat.com/show_bug.cgi?id=753882	
	gtk: dialogs use symbolic icons (offending code is in GTK3, won't fix. Small issue but linked to GTK3 becoming a GNOME Shell specific toolkit.)
	gtk: No padding in context menu leads to accidental operations (bug reported upstream in GTK3, temp workaround/fix unlikely/tedious)
	gtk: noDisplay=true desktop entries don't appear in MIME lists

Cinnamon Edition
----------------
	nemo: The spacing in the Nemo side bar between the folders such as Downloads, Documents etc seems to be a bit small.	
	mint-themes-gtk3: nemo sidebar buttons are too large
	gtk: tooltips in Cinnamon settings “jump” from left top corner of screen (created there and then moved to the right place)	
	[Fixed] cinnamon-control-center: Network module crash, new kernels use rfkill types. https://mail.gnome.org/archives/commits-list/2013-May/msg04543.html
	[Fixed] cinnamon-session: thinks MDM is using mdm_socket
	[Fixed] nemo-dropbox: could not install nemo-dropbox. downloads, displays “100%”, hangs. I was able to install dropbox from dropbox.com		
	[Fixed] cinnamon: “Date & Time” module name not translated, and months in combo not translated
	[Fixed] cinnamon: sometimes icons change from default Mint icons to some other (maybe some fallback icons?)	
	[Fixed] cinnamon: User applet: name/pic are centered, should be left-aligned (shows with small gecos)
	[Fixed] cinnamon: Account details is in the appearance section of the control center... I would have thought it would be in preferences or administration.		
	[Fixed] cinnamon: cinnamon-desktop-editor Choose an icon dialog does not have image previews	
    [Fixed] cinnamon: Changing default applications does nothing
    [Fixed] cinnamon: tooltip on Power applet says "Keyboard" or "Mouse"	
	[Fixed] cinnamon: missing timezone selection
	[Fixed] nemo: mime commands show up in the menu (add nodisplay)
	[Fixed] nemo: Set folders to open each in their own window. Open a folder that has several sub-folders. Lasso two or more sub-folders in that window.  Right-click and choose Open. Nemo crashes!			
	nemo: "Send by email" is showing when right clicking Computer, Home, Trash or removable drives icons on Desktop (also another really minor issue is that “Send by email” and “Format” should have “…” on the end)	
	[Fixed] muffin: When using full screen mode in Chromium or Virtualbox (non-free) it is impossible return to the window mode.	
	[Fixed] muffin: delete file on desktop, confirmation dialog doesn't show in middle of the primary screen, but in middle of the workspace (i.e. if you have two screens, it shows on the right hand side of the left screen)	

MATE Edition
------------
	[Fixed] mintdesktop/mintsystem: reinstate mintfortune
	[Fixed] mate: Use generic names in MATE packages
	