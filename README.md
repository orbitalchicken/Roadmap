Fixed Issues since Mint 16 RC
======================

All editions
------------
	[RFT] apps/drivers: some packages (wine for instance) can't be installed after using the xorg-edgers PPA (caused by priority 700 on PPA)	
	[RTF] mintupdate: not visible in Startup Applications

Cinnamon Edition
----------------

MATE Edition
------------
	[RFT] mate: Use generic names in MATE packages

Confirmed Issues
=============

System
------	
	upgrade notes: Explain how to remove priority 700 for PPA
	apturl/firefox: apturl missing support in Firefox
	Shutdown sequence in live-session is all black	
	cinnamon: inserting an Audio CD suggests Brasero and VLC, not Banshee
	libdvdcss2: DVD Playback doesn't work with new gstreamer: The stream is in the wrong format (using Totem).. works with VLC	
	mint4win: can't find CD (using autorun)
	mint4win: shows version 14 instead of 16	
	banshee: tries to rip a CD to FLAC by default
	mintdesktop/mintsystem: port mintfortune to filesystem flag and away from gsettings
    brasero: Brasero Wont open after burning a disk
    Update all translations
    mdm: sets locale incorrectly (breaks apps like radiotray)
    mdm: mdm-theme-emulator provides no icon and places itself in "other" in menu
    mdm: nvidia-319 installed, login works fine. Log out and different user logs in --> blank screen with a mouse pointer. Switch users works ok.

Mint Tools
----------		
	mintstick: progress bar isn't fixed yet		
	mintdrivers: doesn't apply ATI icon to "Advanced Micro Devices, Inc. [AMD/ATI]: Wrestler [Radeon HD 6290]"	

Cinnamon
--------	
	[Fixed in Git] nemo: Use sudo/gksu/gksudo to "open as root" instead of pkexec? to work around the XDG_RUNTIME_DIR bug?
	nemo: Set folders to open each in their own window. Open a folder that has several sub-folders. Lasso two or more sub-folders in that window.  Right-click and choose Open. Nemo crashes!	
	nemo: could not install nemo-dropbox. downloads, displays “100%”, hangs. I was able to install dropbox from dropbox.com	
	muffin: delete file on desktop, confirmation dialog doesn't show in middle of the primary screen, but in middle of the workspace (i.e. if you have two screens, it shows on the right hand side of the left screen)
	cinnamon: sometimes icons change from default Mint icons to some other (maybe some fallback icons?)
	User applet: name/pic are centered, should be left-aligned (shows with small gecos)
	Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)		
	Calendar applet should link to "cinnamon-settings calendar"
    Changing default applications does nothing
    When a maximized window is minimized, and you activate the hot corner or expo, it makes a split second glitch view of that window
    The mint logo is a bitmap(png) and is blurry when the panel is resized, it should be svg
    Mounted disks shouldest show by default one the desktop?
    Cannot Middle click most toolbar items in Nemo    
    Copying large files (< 200mb), nemo reports 99% the whole time.
    Changing Wallpaper sometimes freezes cinnamon
	Moving applets in cinnamon panel edit mode on, glitches out systray icons when it is shifted    
	mint-themes-gtk3: nemo sidebar buttons are too large
	Account details is in the appearance section of the control center... I would have thought it would be in preferences or administration.
	tooltips in Cinnamon settings “jump” from left top corner of screen (created there and then moved to the right place)
	"Send by email" is showing when right clicking Computer, Home, Trash or removable drives icons on Desktop (also another really minor issue is that “Send by email” and “Format” should have “…” on the end)
	tooltip on Power applet says “Keyboard” (I am using wireless Keyboard)
	I miss the working WIN+D keyboard shortcut to go to desktop.
	remove certifications from spices
	cinnamon menu doesn't listen to menu changes outside /usr/share/applications? install shotwell for instance (uses /usr/share/menu)	
	mint-x (metacity): 1 px frame around windows prevents the rightmost pixel of the right scroll bar from being clickable. Open nemo full screen, with Adwaita you can throw your mouse to the right edge of the screen and start scrolling, with mint-x you need to move 1px left

MATE
----			
	mintmenu: category didn't appear (M64), did when clicked "Reload plugins"	
	mintmenu: show duplicates when item is in multiple categories (LibreOffice, gnome-disks)	
	mintmenu: pull requests		

KDE
---
	rel_notes: Add samba-mounter to new features page for KDE
	ubiquity: clicking on "Release notes" link opens an error dialog saying "can't launch Firefox"
	mintstick KDE action shows also for DVD and floppy disks

Xfce
----
	VLC missing             

De-scoped
---------	
	System: crashes/freezes	due to /run/user/<uid>/dconf/user being owned by root (upstream bug in systemd, affects all distributions. The decision was taken not to hack XDG_RUNTIME_DIR and not to hack /etc/pam.d.. i.e. bringing back xdg_support.so in replacement to systemd.so as it could create further regressions with systemd)
	Cinnamon: Launching keepass + xsel freezes Cinnamon [wrouesnel] (unknown cause/solution, could be related to XDG_RUNTIME_DIR bug)	
	GTK3: dialogs use symbolic icons (offending code is in GTK3, won't fix. Small issue but linked to GTK3 becoming a GNOME Shell specific toolkit.)
	GTK3: No padding in context menu leads to accidental operations (bug reported upstream in GTK3, temp workaround/fix unlikely/tedious)
	GNOME: gnome-calculator menubar (minor cosmestic issue, won't fix)
	System: Support for Wacom tablet (configurable via the command line, will need to join forces with Xfce/MATE if we want to develop a cross DE UI. This doesn't justify pulling resources to make a Cinnamon specific solution)	
	System: EFI boot path isn't standard (EFI installation in Virtualbox works fine, but upon reboot it loses its NVRAM and isn't able to find the EFI boot files)
	MDM: l10n doesn't cover new features (MDM 1.4 is still using the l10n it inherited from GDM. Decision was taken to migrate MDM entirely to Mint/LP translations in 1.6, not just mdmwebkit/mdmsetup).
	MP3 online doesn't work (known limitation with totem)

New Bug Reports
=============

All editions
-------------	
	system: grub/efi: UEFI boot and GPT partition tables, the installer crashes when installing grub. I have installed Ubuntu 13.10 on both of those UEFI systems with no problem.	
	system: grub/efi: Mint16 cannot install package grub-efi-amd64-signed. Why it try to do that if I have not EFI, UEFI and so on? Also I can’t install grub after from terminal but receiving other errors (something about “unable to determine /cow path”)	
	system: apt-get dist-upgrade wants to install shim*, it's for secure boot, i don't think, it should be available for installation
	system: No support for AMD Kabrini chipset or embeded video output on 64 bit edition, both mint and cinn. For ref. ubuntu does have the support in all since 12.04	
	system:	Xorg does not start on my ati r128 video card. This seems to be an upstream issue in xorg 1.14, but you did mention the b43 hang issue in Maya.
	mintdrivers: Nvidia drivers dont automaticaly install nvidia-settings (Tested with nvidia-319 and nvidi-319-updates)
 	mintdrivers: broadcom wireless chipset is recognize well, but I can’t choose the upper button (it always go back to “do not use this device”) http://www.imagebanana.com/view/jx2lm7vz/drivermanager.jpg	
	mintdrivers: Driver manager list is always empty even Nvidia-319 driver installed (I’m also not sure if it should allow installation for detected hardware)			
	apps/drivers: synaptic: Synaptic issues: [1] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1178024 [2] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1135687 [3] https://bugs.launchpad.net/ubuntu/+source/libgksu/+bug/1216045 [4] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1135687/comments/6
	apps/drivers: wine: Same issue with Wine in Mate as in Cinnamon. Installer pops up some dialogs, they are transparent, and then crash. The Wine issue I reported disappears when I switch from multimonitor mode to single monitor. Haven’t tested that in Cinnamon. To replicate, create a multi-monitor setup where one monitor is ABOVE the other, and then run some wine apps. Haven’t tried to setup side by side.
	apps/drivers: Wine doesn’t work. Tried to install Picasa through Playonlinux, but the installation has failed. When I try to launch some wine application, I see the program window without any text and warning window without a text and then all this crashes. But there are no problem with ubuntu 13.10 at work at all.
	apps/drivers: wine: Installed Wine, few other packages, when I go to open a windows app (civ2 for the record), it opens the wine gecko installer, and then that window turns “clear” and I just see the desktop behind it.
	apps/drivers: language input short cut is terrible as it did on the saucy salamander If our linux mint is not going to focus on the ubuntu-tablet then I suggest to our linux mint team to abandon this very uncomfortable input method for other non-english countries including Korea super + space brings malfunction for menu, everytime I input super + space for type in korean then I meet menu pops up , and even it works not welll either.	
	mdm: always uses English keyboard layout?		
	mdm: With nvidia-current installed attempting to shutdown or restart from mdm hangs with black screen. Have to shutdown with the power button.

Cinnamon Edition - last processed comment: #218
----------------
	cinnamon-settings: cant access the settings for Network, every time i click on it, its appears shortly and crashes…
	cinnamon-settings: changing default applications don’t work (after setting VLC for video files, videos continue to open in Videos application)
	cinnamon-settings: (changing default applications) doesn’t recreate mimapps.list, maybe expected behaviour (if deleted only setting new association in Nemo creates file)
	cinnamon-settings: select Networking /usr/lib/cinnamon-settings/modules/cs_user.py:112: Warning: g_object_unref: assertion ‘G_IS_OBJECT (object)’ failed network-cc-panel:ERROR:rfkill-glib.c:83:type_to_string: code should not be reached Aborted New kernels use rfkill types. This bug is related to the confirmed and solved RFkill issue see the following links for details: https://lkml.org/lkml/2013/5/27/386 https://mail.gnome.org/archives/commits-list/2013-May/msg04543.html https://bugzilla.redhat.com/show_bug.cgi?id=969784 committed fix (and patch) from the Ubuntu side. https://bugs.launchpad.net/ubuntu/+source/gnome-control-center/+bug/1209092 commit from gnome side: https://mail.gnome.org/archives/commits-list/2013-May/msg04543.html
	spices: it’s probably individual extension fault but clicking on Configure in Cinnamon settings/Extensions for Coverflow Alt-Tab extension does nothing
	spices: many of them cause crashes and hangs when attempting to use them because they haven’t been updated alongside the new desktop. ClockTow for example, froze my desktop entirely. Is there a way to ensure that the user can only download certified 2.0 applets and desklets etc, to avoid any problems? I personally don’t feel these extensions and suchlike should be available and visible to the end user if they can cause problems.
	cinnamon: Having links of files/folders on desktop from another hardrive at startup, then mounting the drive will usually crash then restart Cinnamon
	cinnamon: Icons keep disappearing from desktop especially when I log out then log in!!		
	cinnamon: The Mint logo/icon that should appear next to the “Start” menu disappeared from the panel after the first reboot.	
	system: Mint Splash screen is not appearing, and seems to be defaulting to the Ubuntu 13.10 splash screen.
	system: the network manager hasn’t any ability to add ADSL connection. From the pop-up list i can chose vpn only. https://bugs.launchpad.net/community.linuxmint.com/+bug/1251530 When you open network manager – standing in wired – click on options – then you seeing window “Editing wired”, but if you don’t close this window and click on “options” one more – it will be opened another window “Network connections”. Where i was able to set my dsl settings. But, in LM 16 it doesn’t work, the second window with “Network connections” doesn’t appear.	
	translations: There are a few issues with the translations (Danish, which is 100% translated): - In System Settings “Date & Time” is in English – In “Date & Time” the months are in English as well - If I go to Menu/Administration there is a “program” called “Logind-skærm”. However, if I go to System Settings the same “program” is called “Login-skærm”. I can only find one translation of “Login Screen” in Cinnamon in Launchpad and that is “Login-skærm”, so where does this “Logind-skærm” come from? Also, the tab names are in English.		

MATE Edition - last processed comment: #87
------------
	marco: Java apps are almost unusable when maximized. http://forums.linuxmint.com/viewtopic.php?f=47&t=112470&p=709183 https://bugzilla.redhat.com/show_bug.cgi?id=918055	
	nm-applet crashed, stopped working
	Login Window for pw on encrypted disks starts too far left with ***,,,should be centered
	mate-systm-monitor under recourses doesn’t look great with the default GTK theme
	After Installing an application, the category icons in mint-menu do not show
	mate-terminal still has a menu bar and is not transparent
	The notification will sometimes appear in the bottom right corner of the screen in a position it will be invisible
	installed driver for my nvidia 210 using mintdrivers - looking at system info it looks like it made it i can go into admin/nvidia x server settings and it shows BUT if i click it nothing happens ( doesn’t launch the nvidia control panel) - i use system monitor and shows processor activity for just a sec then flat lines
	Clicking “help” on most mate applications opens yelp to an error page
	MATE sound preview not work correctly, bug is like on LMDE before some package updates – file manager just disappear and sound continues play.
	Not yet fixed MATE mintMenu bug where it isn’t transparent when user set panel with solid color – all panel adjusts transparent but mintMenu remains with default gray color.
	Mate power manager doesn’t force computer to suspend / hibernate when running on battery and the settings are set to sleep after a set period of time. This feature does work when running on a/c.
	x-caja-desktop issue when opening “Trash” from the menu.
	After all upgrades from Mint 15 to 16, Mate doesn’t work. There is a message in the window, something like: Missing row “Exec” in file mate-session.

Triaged Reports
============

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

Can't reproduce
---------------------------------	
	apps/drivers: Minitube window control and menu bar moved to the right side!!!	
	apps/drivers: Please, add bcmwl-kernel-source_6.30.223.30+bdcom-0ubuntu3_amd64	(already there on the live medium)
	apps/drivers: gnome-system-monitor: in at least 64 bits to see in System Monitor have a high consumption of CPU (2) and Memory
	apps/drivers: editing the software sources via Synaptic ends up in corrupted software sources.	
	system: Sometimes the ethernet network connection is lost without any evident reason.		
	Integrity check give no result. After the check process, no ‘ok’ or ‘error’ message, only ‘press any key to reboot’ message visible.
	mdm: Login window does not have focus on startup (You have to click into the window before you can type the password in)	
	mdm: No login screen has no where to put in login information. Background, works.
	apps/drivers: When using full screen mode in Chromium or Virtualbox (non-free) it is impossible return to the window mode.	
	apps/drivers: Why does Chrome render fonts differently in Linuxmint than it does Ubuntu 13.10?
	apps/drivers: Netflix will not load in Mint 16. probably because of missing gecko (should be fixed with fixes to ppa priority)
	apps/drivers: Problems with gnome15.org drivers. (Application does not start after installation – worked with Mint 15 (regressions?))	
	spices: I open the list of downloadable applets, the “more info” link for each applet is not clickable (this should be fixed).	
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

Improvements selected for the future
=====================================

Mint 17
-------
	mintsources: doesn’t show any progress bar and it seems to test mirrors one by one instead of doing it in parallel.
	system: migrate from gksu/kdesu to pkexec
	ubiquity-slideshow: In the “Install Software” slide of the installation slideshow, it shows Picasa under “Features software”, but Google dropped Picasa for Linux a little over a year ago

Cinnammon
---------
	cinnamon-settings: Cinnamon Regional settings is completely broken/useless/unintuitive, redesign from scratch in 2.2
	cinnamon-settings: Time zone selection, 12vs24 hour clock, easier custom format selection
	cinnamon-settings: Add sound events for logout
	applet: Even after setting org.cinnamon.desktop.lockdown.disable-lock-screen to true, the lock button still appears on cinnamon menu applet…
	applets: when I click on the window list to minimize and maximize sometimes the windows don’trespond and so I have to maximize another window so that I can mainimize or maximize the previous one!!
	nemo: The spacing in the Nemo side bar between the folders such as Downloads, Documents etc seems to be a bit small.
	window-list: Can't minimize windows which have a modal dialog (for example: Synaptic while installing a package). It's possible via the titlebar, but not via the window list
	cinnamon: cinnamon-desktop-editor Choose an icon dialog does not have image previews
	applets: On/Off switch for networking applet is visually glitchy
	spices: removing extensions, themes, desklets, applets is only possible using right click (maybe it would be better to have button for that in future relases)
	spices: If I select the radio box to choose an applet and then I’ll click the button to install it, the applet is installed but it’s not active: maybe a new user expects to have it immediately in the panel after the download… in fact forcing the user to come back in the list of the installed applet to enable the just downloaded applet is not user friendly, in my opinion.
	nemo: if I press ALT+F2 and then enter “nemo ftp://ftp.mydomain.xyz” to access to my personal ftp server trough nemo, I’ll get a request of username and password: it’s OK. The problem is that if I select the option to remember forever the username and password, it will not have effect: if I reboot Linux Mint, the next time I’ll try to access my ftp trough nemo I’ll get the request of username e password. So… nemo doesn’t remember my credentials… it’s frustrating.
	nemo: Entering the folder of long name , the path disappeared screen capture 1) it shows a folder of longname https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A19.png screen capture 2) entering the long name folder , meeting disappeared folder path of long name folder https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A34.png screen capture 3) But Actually It was still dsiplayed at max window https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A19%3A13.png	
	nemo: package description for nemo-data it reads  "Nemo is the official file manager and graphical shell for the GNOME desktop."
	cinnamon: Onscreen keyboard activates when clicking the menu on the panel because text entry is focused... if onboard is used, entry should not focus when showing the menu

MATE
----
	When panel is at the top, notifications show on top of it. https://dl.dropboxusercontent.com/u/54450962/%ED%99%94%EB%A9%B4-5.png