Fixed Issues since Mint 16 RC

All editions
------------
	[RFT] apps/drivers: some packages (wine for instance) can't be installed after using the xorg-edgers PPA (caused by priority 700 on PPA)	
	[RTF] mintupdate: not visible in Startup Applications
	[Fix pending] system: crashes/freezes	due to /run/user/<uid>/dconf/user being owned by root - https://bugzilla.redhat.com/show_bug.cgi?id=753882
	[Fixed] mintdrivers: doesn't apply ATI icon to "Advanced Micro Devices, Inc. [AMD/ATI]: Wrestler [Radeon HD 6290]"	
	[Fixed] mintdrivers: Nvidia drivers dont automaticaly install nvidia-settings (Tested with nvidia-319 and nvidi-319-updates)

Cinnamon Edition
----------------
	[Fixed in Git] nemo: Use sudo/gksu/gksudo to "open as root" instead of pkexec? to work around the XDG_RUNTIME_DIR bug?
	[Fixed in Git] cinnamon: User applet: name/pic are centered, should be left-aligned (shows with small gecos)
	[Fixed in Git] cinnamon: cinnamon-desktop-editor Choose an icon dialog does not have image previews
    [Fixed in Git] cinnamon: Changing default applications does nothing
    [Fixed in Git] cinnamon-settings: Network module crash, new kernels use rfkill types. https://mail.gnome.org/archives/commits-list/2013-May/msg04543.html
	[Fixed in Git] cinnamon-settings: “Date & Time” module name not translated, and months in combo not translated
	[Fixed in Git] cinnamon-settings: missing timezone selection
	[Fixed in Git] nemo: mime commands show up in the menu (add nodisplay)
	[Fixed in Git] nemo: Set folders to open each in their own window. Open a folder that has several sub-folders. Lasso two or more sub-folders in that window.  Right-click and choose Open. Nemo crashes!	
	[Fixed in Git] mint-themes-gtk3: nemo sidebar buttons are too large
	[Fixed in Git] Account details is in the appearance section of the control center... I would have thought it would be in preferences or administration.	
	[Fixed in Git] cinnamon: tooltip on Power applet says "Keyboard" or "Mouse"

MATE Edition
------------
	[RFT] mate: Use generic names in MATE packages
