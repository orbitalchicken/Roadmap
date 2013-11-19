Triaged reports

Not a bug 
---------
	system: Git is not installed by default
	mdm: displays both the user name and real name. (ok because the user can choose other themes)
	system: have installed openvpn, when I click on on “configure a VPN” from the wireless applet, then on the “Add” but I cant see any option for creating a “OpenVPN” connection type. (solved by installing network-manager-openvpn and network-manager-openvpn-gnome)

Outside of the scope
--------------------
	Magnet links for torrents are not working in Firefox
	Still no wacom tablet support?
	include a powerful search (like in Windows) in Cinnamon without using Synapse. As you type, it will automatically display the files that you’re looking for.	
	The side panel (for thumbnails, index, etc.) in the version of evince included in petra is very large and cannot be resized below 15cm on my computer screen.
	spices: Coverflow extension configure button does nothing

Can't reproduce
---------------------------------	
    apps/drivers: radiotray doesn't start (probably because of wrong locale setup, check with "locale" command)
	apps/drivers: Minitube window control and menu bar moved to the right side!!!	
	apps/drivers: Please, add bcmwl-kernel-source_6.30.223.30+bdcom-0ubuntu3_amd64	(already there on the live medium)
	apps/drivers: gnome-system-monitor: in at least 64 bits to see in System Monitor have a high consumption of CPU (2) and Memory
	apps/drivers: editing the software sources via Synaptic ends up in corrupted software sources.	
	apps/drivers: Wine doesn’t work. Tried to install Picasa through Playonlinux, but the installation has failed. When I try to launch some wine application, I see the program window without any text and warning window without a text and then all this crashes. But there are no problem with ubuntu 13.10 at work at all. (possibly due to PPA 700 priority)
	system: Sometimes the ethernet network connection is lost without any evident reason.		
	Integrity check give no result. After the check process, no ‘ok’ or ‘error’ message, only ‘press any key to reboot’ message visible.
	mdm: Login window does not have focus on startup (You have to click into the window before you can type the password in)	
	mdm: No login screen has no where to put in login information. Background, works.
	apps/drivers: When using full screen mode in Chromium or Virtualbox (non-free) it is impossible return to the window mode.	
	apps/drivers: Why does Chrome render fonts differently in Linuxmint than it does Ubuntu 13.10?
	apps/drivers: Netflix will not load in Mint 16. probably because of missing gecko (should be fixed with fixes to ppa priority)
	apps/drivers: Problems with gnome15.org drivers. (Application does not start after installation – worked with Mint 15 (regressions?))	
	spices: I open the list of downloadable applets, the “more info” link for each applet is not clickable (this should be fixed).	
	spices: many of them cause crashes and hangs when attempting to use them because they haven’t been updated alongside the new desktop. ClockTow for example, froze my desktop entirely. Is there a way to ensure that the user can only download certified 2.0 applets and desklets etc, to avoid any problems? I personally don’t feel these extensions and suchlike should be available and visible to the end user if they can cause problems.
	mintinstall: removing programs from Software Manager doesn’t work (it says it is removed but program is still installed)
	mintinstall: Getting “The package x could not be installed” “check internet connection” when installing packages. Packages ARE successfully installed, however.	
	nemo: Nemo will open 3 instances of the new-launcher action when activated in the context menu	
	cinnamon-settings: Cinnamon Settings is advanced mode by default always
	cinnamon-settings: When I choose custom sounds (I used .wav files and they worked for a bit as they should), it does not remember them.
	cinnamon: The sound applet does not close Banshee by clicking on the close icon.	
	cinnamon: When I press Super_L (Windows key) to open the mint-menu, the menu opens, but the overview of workspaces (which should actually open via Ctrl+Alt+Up and does this, too) opens, too. So it is not possible to enter something into the menus search field. I already checked thed the shortcut for the workspace overview in the cinnamon settings, but there is only Ctrl+Alt+Up written.	
	cinnamon: The cursor can be scrolled way past the right border of the screen. On the left side, it stops at the edge.
	cinnamon: Using the keyboard brightness adjuster causes cinnamon to crash, then restart and use a different resolution. (Acer Aspire 5742G)
	cinnamon: menu requires Logout/restart before new application links are displayed.
	cinnamon: After resizing Synaptic Package Manager window, the mouse cursor froze in resize style. I could not click on any window any more. (looks like known systemd bug)
	cinnamon: Alt-Tab Icons and Window preview – black background has bad gradient (seems to happen only when using external monitor)
	cinnamon: Press alt-tab to bring up the program switcher, you can move the mouse cursor over the icons in the switcher but clicking on them does nothing, in LM15 you could click an icon to bring up the corresponding program.
	cinnamon: Press alt-tab to bring up the program switcher then roll the mouse wheel. The selector always moves to the right with wheel-up or wheel-down, in LM15 the selector would move in relation to the wheel direction (wheel up = selector left)(wheel down = selector right).
	system: the update manager loads at startup even after it has been removed from the startup list 
	apps/drivers: The following packages have unmet dependencies: libgl1-mesa-glx:i386 : Depends: libglapi-mesa:i386 (= 9.2.0~git20131002+9.2.2eb55601-0ubuntu0sarvatt) but it is not going to be installed E: Unable to correct problems, you have held broken packages. When attempting to install libglapi-mesa:i386, many of the default packages are removed.	

Upstream
--------
	synaptic: crashes when you try to delete any repository - http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=720605
	moc: segmentation fault - https://bugs.launchpad.net/ubuntu/+source/librcc/+bug/1183580
	gtkam: crashes on launch.
	vlc: In Virtualbox plays videos in monochrome when GPU enabled and black when disabled (solved by changing VLC video plugin to X11)
	banshee: segfaults after playing ~30 mp3 songs (disable plugins you don't need, reduces the probability of crashes)
	amd driver: AMD 13.11 (13.25.18) Beta Drivers refuses to build. I use the command “./amd-catalyst-13.11-beta6-linux-x86.x86_64.run –buildpkg Ubuntu/saucy” and I get comments replying back saying that the distro unsupported however it is supported because I have installed the 13.11 drivers on Ubuntu saucy several times and on linux mint 16 rc I cant for some reason.	(AMD needs to add support for Mint codenames saucy -> petra, LSB returns Petra here)
