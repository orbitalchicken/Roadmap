Triaged reports

Not a bug 
---------
	system: Git is not installed by default
	mdm: displays both the user name and real name. (ok because the user can choose other themes)
	system: have installed openvpn, when I click on on “configure a VPN” from the wireless applet, then on the “Add” but I cant see any option for creating a “OpenVPN” connection type. (solved by installing network-manager-openvpn and network-manager-openvpn-gnome)
	cinnamon-settings: the network manager hasn’t any ability to add ADSL connection. (go to menu->network connections and then click Add and choose DSL) 
	translations: I can only find one translation of “Login Screen” in Cinnamon in Launchpad and that is “Login-skærm”, so where does this “Logind-skærm” come from? (comes from mdm)
	I think libnss3-1d:i386 should be installed by default in the final release if possible so that we can install adobeair without having to muck around in random forums and xchat to find this solution. 
	Two ‘Network’ items in mate-session-properties. (It's there as a workaround to force the upstream nm-applet to work with MATE)
	mate: In mintmenu, “Applications” is badly translated in french. It should be replaced by “Logiciels” instead of “Applications” that means nothing. ("Application" est Francais, provient du Latin, est courrament utilise en informatique (on parlait d'applis deja dans les annees 90 quand j'etais petit) et signifie: Programme ou ensemble de programmes destiné à aider l'utilisateur d'un ordinateur pour le traitement d'une tâche précise.). 
	mate: I cannot set the pointer size. The slider in Appearance/Customize/Pointer is greyed out (this features is available on cursor themes which support it)

Outside of the scope
--------------------
	mint-x (metacity): 1 px frame around windows prevents the rightmost pixel of the right scroll bar from being clickable. Open nemo full screen, with Adwaita you can throw your mouse to the right edge of the screen and start scrolling, with mint-x you need to move 1px left
	Magnet links for torrents are not working in Firefox
	Still no wacom tablet support?
	include a powerful search (like in Windows) in Cinnamon without using Synapse. As you type, it will automatically display the files that you’re looking for.	
	The side panel (for thumbnails, index, etc.) in the version of evince included in petra is very large and cannot be resized below 15cm on my computer screen.
	spices: Coverflow extension configure button does nothing

Can't reproduce
---------------------------------
	l10n: “Enter your password to perform administrative tasks” isn't l10n'd (not enough info)
	apps/drivers: Brasero Wont open after burning a disk
	mdm: always uses English keyboard layout? (flag indicates locale, not keyboard layout)
	mintdrivers: Driver manager list is always empty even Nvidia-319 driver installed (works fine)				
	system: No support for AMD Kabini chipset or embeded video output on 64 bit edition, both mint and cinn. For ref. ubuntu does have the support in all since 12.04 (need more info)
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
    cinnamon: When a maximized window is minimized, and you activate the hot corner or expo, it makes a split second glitch view of that window
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
	system: apt-get dist-upgrade wants to install shim*, it's for secure boot, i don't think, it should be available for installation
	gparted is missing on the live DVD.
	cinnamon: any choice of the ‘suspend when inactive for’ parameter lets the computer never go to suspend mode
	cinnamon: any choice of the ‘when the lid is closed’ parameter: the computer always suspends
	cinnamon: any choice of ‘power button action’ leads to an immediate shutdown when pressed
	cinnamon: The keyboard shortcut for “hide all normal windows” is broke. I can’t get any shortcut to work with it. The ubuntu website shows that there are issues going on with some keyboard shortcuts not working right. 
	cinnamon: Tapping showed as being enabled in control panel. Ran dconf-editor and found that tap-to-click wasn’t checked, once I checked it I was able to tap again.	
	system: Mint Splash screen is not appearing, and seems to be defaulting to the Ubuntu 13.10 splash screen.
	cinnamon: Icons keep disappearing from desktop especially when I log out then log in!!		
	mate: nm-applet crashed, stopped working
	I’ve installed LM16 Cinnamon twice now on 2 separate machines and both times the Icon “LM” picture disappears where the Menu button is… (probably due to existing /home configuration)
	After all upgrades from Mint 15 to 16, Mate doesn’t work. There is a message in the window, something like: Missing row “Exec” in file mate-session.
	installed driver for my nvidia 210 using mintdrivers - looking at system info it looks like it made it i can go into admin/nvidia x server settings and it shows BUT if i click it nothing happens ( doesn’t launch the nvidia control panel) - i use system monitor and shows processor activity for just a sec then flat lines
	mate: mate panel doesn’t do autohide after locking and unlocking screen.
	mate: x-caja-desktop issue when opening “Trash” from the menu. (probably related to xdg_runtime_dir issue, fixed in systemd update)
	mate: Could not install network printer.
	mate: network settings forgets DNS entries
	mate: Regardless how I set the screen shut down in Power Management, it always shuts down after a very short time. I tried ‘Never” and ’1 hour” but it did not work.
	mate: Mate power manager doesn’t force computer to suspend / hibernate when running on battery and the settings are set to sleep after a set period of time. This feature does work when running on a/c.
	mate: Mintmenu has a scrolling problem when the ALL-Tab was clicked and dragged quickly. This is a small problem.	
	mate: The notification will sometimes appear in the bottom right corner of the screen in a position it will be invisible
	mate: If you add a few keyboard layouts and set the CapsLock key to switch them, after reboot CapsLock stops switching the layouts.	(works fine, tested with fr and ie)
	mate: sound preview not work correctly, bug is like on LMDE before some package updates – file manager just disappear and sound continues play.
	mintmenu: show duplicates when item is in multiple categories (LibreOffice, gnome-disks)	

Upstream
--------
	synaptic: crashes when you try to delete any repository - http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=720605
	moc: segmentation fault - https://bugs.launchpad.net/ubuntu/+source/librcc/+bug/1183580
	gtkam: crashes on launch.
	vlc: In Virtualbox plays videos in monochrome when GPU enabled and black when disabled (solved by changing VLC video plugin to X11)
	banshee: segfaults after playing ~30 mp3 songs (disable plugins you don't need, reduces the probability of crashes)
	amd driver: AMD 13.11 (13.25.18) Beta Drivers refuses to build. I use the command “./amd-catalyst-13.11-beta6-linux-x86.x86_64.run –buildpkg Ubuntu/saucy” and I get comments replying back saying that the distro unsupported however it is supported because I have installed the 13.11 drivers on Ubuntu saucy several times and on linux mint 16 rc I cant for some reason.	(AMD needs to add support for Mint codenames saucy -> petra, LSB returns Petra here)
	font viewer:  4 font files (bold, Normal, Italic, bold-italic)...  choose them all and open in font viewer. They open in the same window.. with 4 install/back/info buttons i.imgur.com/EMbzh9v.png
	cups-pdf produces only a blank pdf page when I print to PDF
	system-config-lvm: invoke-rc.d: unknown initscript, /etc/init.d/lvm2 not found.	
	When battery charges to 100% it displays 0% and sends the laptop to hibernate - fixed in upower 0.9.22-1ubuntu2 - https://bugs.launchpad.net/ubuntu/+source/upower/+bug/1240673
