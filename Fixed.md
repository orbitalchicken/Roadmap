Fixed Issues since Mint 16 RC

All editions
------------
	[RFT] apps/drivers: some packages (wine for instance) can't be installed after using the xorg-edgers PPA (caused by priority 700 on PPA)	
	[RTF] mintupdate: not visible in Startup Applications

Cinnamon Edition
----------------
	[Fixed in Git] nemo: Use sudo/gksu/gksudo to "open as root" instead of pkexec? to work around the XDG_RUNTIME_DIR bug?
	[Fixed in Git] cinnamon: User applet: name/pic are centered, should be left-aligned (shows with small gecos)
	[Fixed in Git] cinnamon: cinnamon-desktop-editor Choose an icon dialog does not have image previews
    [Fixed in Git] cinnamon: Changing default applications does nothing
    [Fixed in Git] cinnamon-settings: Network module crash, new kernels use rfkill types. https://mail.gnome.org/archives/commits-list/2013-May/msg04543.html
	[Fixed in Git] cinnamon-settings: “Date & Time” module name not translated, and months in combo not translated
	[Fixed in Git] cinnamon-settings: missing timezone selection

MATE Edition
------------
	[RFT] mate: Use generic names in MATE packages
