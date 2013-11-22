Fixed Issues since Mint 16 RC

All editions
------------
	[Fixed] apps/drivers: some packages (wine for instance) can't be installed after using the xorg-edgers PPA (caused by priority 700 on PPA)	
	[Fixed] mintupdate: not visible in Startup Applications	
	[Fixed] mintdrivers: doesn't apply ATI icon to "Advanced Micro Devices, Inc. [AMD/ATI]: Wrestler [Radeon HD 6290]"	
	[Fixed] mintdrivers: Nvidia drivers dont automaticaly install nvidia-settings (Tested with nvidia-319 and nvidi-319-updates)
	[Fixed] mdm: nvidia-319 installed, login works fine. Log out and different user logs in --> blank screen with a mouse pointer. Switch users works ok.
	[Fixed] plymouth-stop and hybrid-check don't listen to mdm events in upstart
	[Fixed] system: crashes/freezes	due to /run/user/<uid>/dconf/user being owned by root - https://bugzilla.redhat.com/show_bug.cgi?id=753882
	[Fixed] mdm: With nvidia-current installed attempting to shutdown or restart from mdm hangs with black screen. Have to shutdown with the power button.		

Cinnamon Edition
----------------
	[Fixed] nemo: The spacing in the Nemo side bar between the folders such as Downloads, Documents etc seems to be a bit small.	
	[Fixed] mint-themes-gtk3: nemo sidebar buttons are too large
	[Fixed in Git] cinnamon-session thinks MDM is using mdm_socket
	[Fixed in Git] nemo: Use sudo/gksu/gksudo to "open as root" instead of pkexec? to work around the XDG_RUNTIME_DIR bug?
	[Fixed in Git] cinnamon: User applet: name/pic are centered, should be left-aligned (shows with small gecos)
	[Fixed in Git] cinnamon: cinnamon-desktop-editor Choose an icon dialog does not have image previews
    [Fixed in Git] cinnamon: Changing default applications does nothing
    [Fixed in Git] cinnamon-settings: Network module crash, new kernels use rfkill types. https://mail.gnome.org/archives/commits-list/2013-May/msg04543.html
	[Fixed in Git] cinnamon-settings: “Date & Time” module name not translated, and months in combo not translated
	[Fixed in Git] cinnamon-settings: missing timezone selection
	[Fixed in Git] nemo: mime commands show up in the menu (add nodisplay)
	[Fixed in Git] nemo: Set folders to open each in their own window. Open a folder that has several sub-folders. Lasso two or more sub-folders in that window.  Right-click and choose Open. Nemo crashes!		
	[Fixed in Git] Account details is in the appearance section of the control center... I would have thought it would be in preferences or administration.	
	[Fixed in Git] cinnamon: tooltip on Power applet says "Keyboard" or "Mouse"
	[Fixed in Git] "Send by email" is showing when right clicking Computer, Home, Trash or removable drives icons on Desktop (also another really minor issue is that “Send by email” and “Format” should have “…” on the end)
	[Fixed in Git] nemo: could not install nemo-dropbox. downloads, displays “100%”, hangs. I was able to install dropbox from dropbox.com		
	[Fixed in Git] muffin: When using full screen mode in Chromium or Virtualbox (non-free) it is impossible return to the window mode.	


MATE Edition
------------
	[Fixed] mate: Use generic names in MATE packages
	[Fixed] mintdesktop/mintsystem: reinstate mintfortune
