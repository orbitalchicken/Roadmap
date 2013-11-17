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
	Java apps are almost unusable when maximized. http://forums.linuxmint.com/viewtopic.php?f=47&t=112470&p=709183
	In the “Install Software” slide of the installation slideshow, it shows Picasa under “Features software”, but Google dropped Picasa for Linux a little over a year ago
	editing the software sources via Synaptic ends up in corrupted software sources.

Cinnamon Edition - last processed comment: #85
----------------
	cinnamon-desktop-editor Choose an icon dialog does not have image previews
	Having links of files/folders on desktop from another hardrive at startup, then mounting the drive will usually crash then restart Cinnamon
	I go to system settings to change the default applications to the ones of my choice but it does not work. I tried to change media application for music and video to VLC but Totem remains as the default media player.
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

MATE Edition - last processed comment: #65
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
	Cinnamon Regional settings is completely broken/useless/unintuitive, redesign from scratch in 2.2

Not enough info / Can't reproduce
---------------------------------

	On/Off switch for networking applet is visually glitchy
	No login screen has no where to put in login information. Background, works.
	Sometimes the ethernet network connection is lost without any evident reason.
	Cinnamon Settings is advanced mode by default always
	After resizing Synaptic Package Manager window, the mouse cursor froze in resize style. I could not click on any window any more. 

Upstream
--------
	Synaptic package manager crashes when you try to delete any repository - http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=720605
	MOC (music on console) does not work Segmentation fault - https://bugs.launchpad.net/ubuntu/+source/librcc/+bug/1183580
