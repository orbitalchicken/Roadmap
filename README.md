Fixed Issues since Mint 16 RC
======================

All editions
------------

Cinnamon Edition
----------------

MATE Edition
------------

Confirmed Issues
=============

System
------	
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

Mint Tools
----------		
	mintstick: progress bar isn't fixed yet		
	mintdrivers: doesn't apply ATI icon to "Advanced Micro Devices, Inc. [AMD/ATI]: Wrestler [Radeon HD 6290]"

Cinnamon
--------	
	nemo: Use sudo/gksu/gksudo to "open as root" instead of pkexec? to work around the XDG_RUNTIME_DIR bug?
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
	Account details is in the appearance section of the control center…I would have thought it would be in preferences or administration.
	tooltips in Cinnamon settings “jump” from left top corner of screen (created there and then moved to the right place)

	
MATE
----		
	mate: Use generic names in MATE packages	
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
	System: gksu covers cinnamon panel and clutter layer (offending code is in libgksu, won't fix, likely to migrate to pkexec instead)
	System: Support for Wacom tablet (configurable via the command line, will need to join forces with Xfce/MATE if we want to develop a cross DE UI. This doesn't justify pulling resources to make a Cinnamon specific solution)	
	System: EFI booth path isn't standard (EFI installation in Virtualbox works fine, but upon reboot it loses its NVRAM and isn't able to find the EFI boot files)
	MDM: l10n doesn't cover new features (MDM 1.4 is still using the l10n it inherited from GDM. Decision was taken to migrate MDM entirely to Mint/LP translations in 1.6, not just mdmwebkit/mdmsetup).
	MP3 online doesn't work (known limitation with totem)

New Bug Reports
=============

All editions
-------------
	mintdrivers: Nvidia drivers dont automaticaly install nvidia-settings (Tested with nvidia-319 and nvidi-319-updates)
 	mintdrivers: broadcom wireless chipset is recognize well, but I can’t choose the upper button (it always go back to “do not use this device”) http://www.imagebanana.com/view/jx2lm7vz/drivermanager.jpg
	banshee: Banshee will segfault after playing ~30 mp3 songs
	wine: Installed Wine, few other packages, when I go to open a windows app (civ2 for the record), it opens the wine gecko installer, and then that window turns “clear” and I just see the desktop behind it.
	gnome-system-monitor: in at least 64 bits to see in System Monitor have a high consumption of CPU (2) and Memory
	efi: UEFI boot and GPT partition tables, the installer crashes when installing grub. I have installed Ubuntu 13.10 on both of those UEFI systems with no problem.
	mdm: There appears to be a bug when logging out then back in as another user – the system just hangs
	synaptic: Synaptic issues: [1] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1178024 [2] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1135687 [3] https://bugs.launchpad.net/ubuntu/+source/libgksu/+bug/1216045 [4] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1135687/comments/6
	wine: Same issue with Wine in Mate as in Cinnamon. Installer pops up some dialogs, they are transparent, and then crash. The Wine issue I reported disappears when I switch from multimonitor mode to single monitor. Haven’t tested that in Cinnamon. To replicate, create a multi-monitor setup where one monitor is ABOVE the other, and then run some wine apps. Haven’t tried to setup side by side.
	Wine doesn’t work. Tried to install Picasa through Playonlinux, but the installation has failed. When I try to launch some wine application, I see the program window without any text and warning window without a text and then all this crashes. But there are no problem with ubuntu 13.10 at work at all.
	Update manager, Software Manager and some other applications that ask for password, when they open they make the system freeze for 30” and then they ask the password.
	language input short cut is terrible as it did on the saucy salamander If our linux mint is not going to focus on the ubuntu-tablet then I suggest to our linux mint team to abandon this very uncomfortable input method for other non-english countries including Korea super + space brings malfunction for menu, everytime I input super + space for type in korean then I meet menu pops up , and even it works not welll either.
	apt-get dist-upgrade wants to install shim*, it's for secure boot, i don't think, it should be available for installation
	No support for AMD Kabrini chipset or embeded video output on 64 bit edition, both mint and cinn. For ref. ubuntu does have the support in all since 12.04
	have installed openvpn, when I click on on “configure a VPN” from the wireless applet, then on the “Add” but I cant see any option for creating a “OpenVPN” connection type. This did work fine in Linux Mint 15, do you have any ideas?
	Java apps are almost unusable when maximized. http://forums.linuxmint.com/viewtopic.php?f=47&t=112470&p=709183 https://bugzilla.redhat.com/show_bug.cgi?id=918055
	In the “Install Software” slide of the installation slideshow, it shows Picasa under “Features software”, but Google dropped Picasa for Linux a little over a year ago
	editing the software sources via Synaptic ends up in corrupted software sources.
	mouse stays “busy” more than it should when opening applications that need Root rights (Login window, Driver manager, Users & groups …)	
	removing programs from Software Manager doesn’t work (it says it is removed but program is still installed)
	Driver manager list is always empty even Nvidia-319 driver installed (I’m also not sure if it should allow installation for detected hardware)
	Mint16 cannot install package grub-efi-amd64-signed. Why it try to do that if I have not EFI, UEFI and so on? Also I can’t install grub after from terminal but receiving other errors (something about “unable to determine /cow path”)
	AMD 13.11 (13.25.18) Beta Drivers refuse to build. I use the command “./amd-catalyst-13.11-beta6-linux-x86.x86_64.run –buildpkg Ubuntu/saucy” and I get comments replying back saying that the distro unsupported however it is supported because I have installed the 13.11 drivers on Ubuntu saucy several times and on linux mint 16 rc I cant for some reason.
	gksu causes a big hang/freeze for several seconds on the default drivers shipped with Linux Mint 16 RC. On other drivers, such as the AMD 13.6 beta it seems to perform fine.
	Switching users works but logging out of one user and logging in as another, the display turns black and just hangs there. The mouse is still movable though and the “rolling” wait icon is still spinning.	
	I am running Mint 16-RC 64 bit, with an Nvidia card (I have installed driver Nvidia-319; I get the same problem with Nvidia-319-updates). One user can log on and use the system fine. If they then log out and a different user logs in they simply get a blank screen with a mouse pointer. If I ctrl-alt-F1 I can log on in a text window and see that their start up applications are running. Just no display. It works fine if I simply lock screen then switch user.
	With nvidia-current installed attempting to shutdown or restart from mdm hangs with black screen. Have to shutdown with the power button. 64 bit Mint Cinnamon
	The following packages have unmet dependencies: libgl1-mesa-glx:i386 : Depends: libglapi-mesa:i386 (= 9.2.0~git20131002+9.2.2eb55601-0ubuntu0sarvatt) but it is not going to be installed E: Unable to correct problems, you have held broken packages. When attempting to install libglapi-mesa:i386, many of the default packages are removed.
	Why does Chrome render fonts differently in Linuxmint than it does Ubuntu 13.10?
	Minitube window control and menu bar moved to the right side!!!
	In this release it is impossible to install PlayOnLinux after adding xorg-edgers PPA (I am using Nvidia driver from there). In Ubuntu 13.10 there is no such problem. I found out experimentally what causes this problem – this is system improvement “Higher APT priority, out of the box support for PPA repositories”. After the removal of 12-15 lines from the file /etc/apt/preferences.d/official-package-repositories.pref PlayOnLinux has been successfully installed. 
	My 32 bit install problems were also solved by removing the 700 pinning for ppa.launchpad.net. It seems pinning the xorg-edgers ppa breaks alot of things. I am now able to install wine on the 64 bit version of mint 16 cinnamon.
	Please, add bcmwl-kernel-source_6.30.223.30+bdcom-0ubuntu3_amd64
	Login window does not have focus on startup (You have to click into the window before you can type the password in)
	MDM always uses English keyboard layout?

Cinnamon Edition - last processed comment: #218
----------------

	cinnamon-desktop-editor Choose an icon dialog does not have image previews
	Having links of files/folders on desktop from another hardrive at startup, then mounting the drive will usually crash then restart Cinnamon
	changing default applications don’t work (after setting VLC for video files, videos continue to open in Videos application)
	cinnamon settings (changing default applications) doesn’t recreate mimapps.list, maybe expected behaviour (if deleted only setting new association in Nemo creates file)
	Installed Cinnamon and could not install nemo-dropbox. It downloads, but after displaying “100%”, it hangs. I was able to install dropbox from dropbox.com – even though it said it would work with thunar ( and I had nemo). I tried to install gnome, but it errored out: “Could not apply changes. Fix broken packages first.”
	Onscreen keyboard activates when clicking the menu on the panel
	the update manager loads at startup even after it has been removed from the startup list 
	the network manager hasn’t any ability to add ADSL connection. From the pop-up list i can chose vpn only. https://bugs.launchpad.net/community.linuxmint.com/+bug/1251530 When you open network manager – standing in wired – click on options – then you seeing window “Editing wired”, but if you don’t close this window and click on “options” one more – it will be opened another window “Network connections”. Where i was able to set my dsl settings. But, in LM 16 it doesn’t work, the second window with “Network connections” doesn’t appear.
	menu requires Logout/restart before new application links are displayed.
	installing nemo-dropbox sends cinnamon into meltdown. If you restart Cinnamon afterwards, or log out and back in, or reboot, Cinnamon crashes, and resorts to software rendering permananently. It just won’t restart. Uninstalling nemo-dropbox, sets things back to normal again, and cinnamon works fine.
	when I click on the window list to minimize and maximize sometimes the windows don’trespond and so I have to maximize another window so that I can mainimize or maximize the previous one!!
	Icons keep disappearing from desktop especially when I log out then log in!!
	radio tray and kazam are not working. i can’t say why and if this thing has something to do with the system or only with cinnamon 2.
	Logout sound missing from the sound events
	remove certifications from spices
	cant access the settings for Network, every time i click on it, its appears shortly and crashes…
	it’s probably individual extension fault but clicking on Configure in Cinnamon settings/Extensions for Coverflow Alt-Tab extension does nothing
	when emptying trash from right click menu on Trash icon, dialog for confirmation was always showing snapped to the right side of screen, after restart was ok
	Alt-Tab Icons and Window preview – black background has bad gradient (seems to happen only when using external monitor)
	sometimes icons change from default Mint icons to some other (maybe some fallback icons?), issue also on Linux Mint 15
	Synaptic Package Manager – cannot minimize it by clicking on panel item (toggle maximize/minimize) while installation in progress (dialog shown)
	“Send by email” is showing when right clicking Computer, Home, Trash or removable drives icons on Desktop (also another really minor issue is that “Send by email” and “Format” should have “…” on the end)
	tooltip on Power applet says “Keyboard” (I am using wireless Keyboard)
	removing extensions, themes, desklets, applets is only possible using right click (maybe it would be better to have button for that in future relases)
	The cursor can be scrolled way past the right border of the screen. On the left side, it stops at the edge.
	Set folders to open each in their own window. Open a folder that has several sub-folders. Lasso two or more sub-folders in that window.  Right-click and choose Open. Poof!
	I miss the working WIN+D keyboard shortcut to go to desktop.
	Add a logout sound event
	cinnamon settings – select Networking /usr/lib/cinnamon-settings/modules/cs_user.py:112: Warning: g_object_unref: assertion ‘G_IS_OBJECT (object)’ failed network-cc-panel:ERROR:rfkill-glib.c:83:type_to_string: code should not be reached Aborted New kernels use rfkill types. This bug is related to the confirmed and solved RFkill issue see the following links for details: https://lkml.org/lkml/2013/5/27/386 https://mail.gnome.org/archives/commits-list/2013-May/msg04543.html https://bugzilla.redhat.com/show_bug.cgi?id=969784 committed fix (and patch) from the Ubuntu side. https://bugs.launchpad.net/ubuntu/+source/gnome-control-center/+bug/1209092 commit from gnome side: https://mail.gnome.org/archives/commits-list/2013-May/msg04543.html
	Using the keyboard brightness adjuster causes cinnamon to crash, then restart and use a different resolution. (Acer Aspire 5742G)
	I open the list of downloadable applets, the “more info” link for each applet is not clickable (this should be fixed).
	If I double click on an applet name, nothing happens.
	If I select the radio box to choose an applet and then I’ll click the button to install it, the applet is installed but it’s not active: maybe a new user expects to have it immediately in the panel after the download… in fact forcing the user to come back in the list of the installed applet to enable the just downloaded applet is not user friendly, in my opinion.
	Mint Splash screen is not appearing, and seems to be defaulting to the Ubuntu 13.10 splash screen.
	The Mint logo/icon that should appear next to the “Start” menu disappeared from the panel after the first reboot.
	Press alt-tab to bring up the program switcher, you can move the mouse cursor over the icons in the switcher but clicking on them does nothing, in LM15 you could click an icon to bring up the corresponding program.
	Press alt-tab to bring up the program switcher then roll the mouse wheel. The selector always moves to the right with wheel-up or wheel-down, in LM15 the selector would move in relation to the wheel direction (wheel up = selector left)(wheel down = selector right).
	There seems to be a tiny 1 pixel frame around windows that prevents the rightmost pixel of the right scroll bar from being clickable. For example LM15: open Nemo, go to a folder with a lot of files like /usr/bin/, throw the mouse cursor all the way to the right edge of the screen and click on the scrollbar = windows scrolls. LM16 doing the same thing will cause the scrollbar to do nothing until you move the mouse cursor a pixel to the left. An easy way to see the comparison in LM16 is to install chromium and change (settings) > (appearance) > (use system title bar and borders), using system borders will cause the rightmost pixel to be unclickable.
	When I choose custom sounds (I used .wav files and they worked for a bit as they should), it does not remember them.
	Nemo will open 3 instances of the new-launcher action when activated in the context menu
	When using full screen mode in Chromium or Virtualbox (non-free) it is impossible return to the window mode.
	The sound applet does not close Banshee by clicking on the close icon.
	if I press ALT+F2 and then enter “nemo ftp://ftp.mydomain.xyz” to access to my personal ftp server trough nemo, I’ll get a request of username and password: it’s OK. The problem is that if I select the option to remember forever the username and password, it will not have effect: if I reboot Linux Mint, the next time I’ll try to access my ftp trough nemo I’ll get the request of username e password. So… nemo doesn’t remember my credentials… it’s frustrating.
	I fired up Cinnamon Settings after a fresh install and decided to try out a number of my favourite desktop toys, but many of them cause crashes and hangs when attempting to use them because they haven’t been updated alongside the new desktop. ClockTow for example, froze my desktop entirely. Is there a way to ensure that the user can only download certified 2.0 applets and desklets etc, to avoid any problems? I personally don’t feel these extensions and suchlike should be available and visible to the end user if they can cause problems.
	When I press Super_L (Windows key) to open the mint-menu, the menu opens, but the overview of workspaces (which should actually open via Ctrl+Alt+Up and does this, too) opens, too. So it is not possible to enter something into the menus search field. I already checked thed the shortcut for the workspace overview in the cinnamon settings, but there is only Ctrl+Alt+Up written.
	The spacing in the Nemo side bar between the folders such as Downloads, Documents etc seems to be a bit small.
	There are a few issues with the translations (Danish, which is 100% translated): - In System Settings “Date & Time” is in English – In “Date & Time” the months are in English as well - If I go to Menu/Administration there is a “program” called “Logind-skærm”. However, if I go to System Settings the same “program” is called “Login-skærm”. I can only find one translation of “Login Screen” in Cinnamon in Launchpad and that is “Login-skærm”, so where does this “Logind-skærm” come from? Also, the tab names are in English.
	Running Mint in a Virtualbox here. Videos played in VLC are monochrome when GPU enabled and black when it’s disabled. GPU is Nvidia GTX650Ti. No problems with Mint 13 under the same conditions.
	Entering the folder of long name , the path disappeared screen capture 1) it shows a folder of longname https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A19.png screen capture 2) entering the long name folder , meeting disappeared folder path of long name folder https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A34.png screen capture 3) But Actually It was still dsiplayed at max window https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A19%3A13.png
	Getting “The package x could not be installed” “check internet connection” when installing packages. Packages ARE successfully installed, however.
	The side panel (for thumbnails, index, etc.) in the version of evince included in petra is very large and cannot be resized below 15cm on my computer screen.
	Netflix will not load in Mint 16. I am using Cinnamon by the way. It works great in Mint 15, but when I try to open it in Mint 16, it doesn’t do anything. It doesn’t give me an error message, it doesn’t open, nothing. It appears that Gecko isn’t installed and when I try to install it manually by following suggestions from the Ubuntu forums, it doesn’t work.
	Problems with gnome15.org drivers. (Application does not start after installation – worked with Mint 15 (regressions?))
	Shotwell goes to /usr/share/menu, but that doesn’t get it immediately shown or shown at all in the menu, without manual intervention.


MATE Edition - last processed comment: #87
------------
	nm-applet crashed, stopped working
	Login Window for pw on encrypted disks starts too far left with ***,,,should be centered
	mate-systm-monitor under recourses doesn’t look great with the default GTK theme
	After Installing an application, the category icons in mint-menu do not show
	mate-terminal still has a menu bar and is not transparent
	The notification will sometimes appear in the bottom right corner of the screen in a position it will be invisible
	installed driver for my nvidia 210 using mintdrivers - looking at system info it looks like it made it i can go into admin/nvidia x server settings and it shows BUT if i click it nothing happens ( doesn’t launch the nvidia control panel) - i use system monitor and shows processor activity for just a sec then flat lines
	Clicking “help” on most mate applications opens yelp to an error page
	Xorg does not start on my ati r128 video card. This seems to be an upstream issue in xorg 1.14, but you did mention the b43 hang issue in Maya.
	MATE sound preview not work correctly, bug is like on LMDE before some package updates – file manager just disappear and sound continues play.
	Not yet fixed MATE mintMenu bug where it isn’t transparent when user set panel with solid color – all panel adjusts transparent but mintMenu remains with default gray color.
	Mate power manager doesn’t force computer to suspend / hibernate when running on battery and the settings are set to sleep after a set period of time. This feature does work when running on a/c.
	x-caja-desktop issue when opening “Trash” from the menu.
	After all upgrades from Mint 15 to 16, Mate doesn’t work. There is a message in the window, something like: Missing row “Exec” in file mate-session.


Triaged Reports
============

Not a bug 
---------
	Git is not installed by default
	The new login screen (Mint X default) looks really great but displays both the user name and real name. Is this intentional? (Yes, it's ok because the user can choose other themes, it wouldn't if MDM wasn't themeable)

Outside of the scope
--------------------

	Magnet links for torrents are not working in Firefox
	Still no wacom tablet support?
	include a powerful search (like in Windows) in Cinnamon without using Synapse. As you type, it will automatically display the files that you’re looking for.	

Not enough info / Can't reproduce
---------------------------------

	On/Off switch for networking applet is visually glitchy
	No login screen has no where to put in login information. Background, works.
	Sometimes the ethernet network connection is lost without any evident reason.
	Cinnamon Settings is advanced mode by default always
	After resizing Synaptic Package Manager window, the mouse cursor froze in resize style. I could not click on any window any more. 
	Integrity check give no result. After the check process, no ‘ok’ or ‘error’ message, only ‘press any key to reboot’ message visible.

Upstream
--------
	Synaptic package manager crashes when you try to delete any repository - http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=720605
	MOC (music on console) does not work Segmentation fault - https://bugs.launchpad.net/ubuntu/+source/librcc/+bug/1183580
	‘gtkam’ crashes on launch.

Improvements selected for the future
=====================================

Mint 17
-------
	mintSources has two annoying quirks: it doesn’t show any progress bar and it seems to test mirrors one by one instead of doing it in parallel.

Cinnammon
---------
	Cinnamon Regional settings is completely broken/useless/unintuitive, redesign from scratch in 2.2
	Time zone selection, 12vs24 hour clock, easier custom format selection

MATE
----
	When panel is at the top, notifications show on top of it. https://dl.dropboxusercontent.com/u/54450962/%ED%99%94%EB%A9%B4-5.png