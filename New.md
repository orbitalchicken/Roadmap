New bug reports in Mint 16 RC

All editions
-------------	
	can't install in EFI mode without Internet connection
	system: grub/efi: UEFI boot and GPT partition tables, the installer crashes when installing grub. I have installed Ubuntu 13.10 on both of those UEFI systems with no problem.	
	system: grub/efi: Mint16 cannot install package grub-efi-amd64-signed. Why it try to do that if I have not EFI, UEFI and so on? Also I can’t install grub after from terminal but receiving other errors (something about “unable to determine /cow path”)
	system: apt-get dist-upgrade wants to install shim*, it's for secure boot, i don't think, it should be available for installation
	system:	Xorg does not start on my ati r128 video card. This seems to be an upstream issue in xorg 1.14, but you did mention the b43 hang issue in Maya.	 	
	apps/drivers: synaptic: Synaptic issues: [1] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1178024 [2] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1135687 [3] https://bugs.launchpad.net/ubuntu/+source/libgksu/+bug/1216045 [4] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1135687/comments/6			
	In Petra’s new MDM version, stopping the MDM service prevents access to the TTYs. Using Ctrl+Alt+F2 only works when MDM is running. Thus, there’s no way to run anything in a TTY unless the X server is running.
	system-config-lvm worked in Olivia, but crashes in Petra on startup up with the message: invoke-rc.d: unknown initscript, /etc/init.d/lvm2 not found.
	Can’t play TS video files
	mdm: Cant set login screen time to 24hr (changing the option doesnt work)
	Package ‘mintsources’ should depend on ‘python-pycurl’, as line 14 of ‘/usr/lib/linuxmint/mintSources/mintSources.py’ imports ‘pycurl’.	
	I think libnss3-1d:i386 should be installed by default in the final release if possible so that we can install adobeair without having to muck around in random forums and xchat to find this solution. Since all adobeair forums, bulletions, and information is so badly outdated. I thank you much if this happens.
	installing in russian doesn't apply locale properly


Cinnamon Edition - last processed comment: #433
----------------
	cinnamon: Having links of files/folders on desktop from another hardrive at startup, then mounting the drive will usually crash then restart Cinnamon
	cinnamon: Icons keep disappearing from desktop especially when I log out then log in!!		
	cinnamon: The Mint logo/icon that should appear next to the “Start” menu disappeared from the panel after the first reboot.	
	system: Mint Splash screen is not appearing, and seems to be defaulting to the Ubuntu 13.10 splash screen.
	icons pixelated in alt-tab or panel after a suspend-resume
	llvmpiped session after a suspend-resume
	Open GIMP, open a dropdown menu, e.g. the ‘Edit’ menu. Press the Print Screen button on the keyboard – no screenshot is taken while a menu is open.
	Cinnamon menu: When creating a new menu item the icon does not appear. It is ok in the menu editor.
	Tapping showed as being enabled in control panel. Ran dconf-editor and found that tap-to-click wasn’t checked, once I checked it I was able to tap again.
	The keyboard shortcut for “hide all normal windows” is broke. I can’t get any shortcut to work with it. The ubuntu website shows that there are issues going on with some keyboard shortcuts not working right. 
	When my battery charges to 100% its actually displayed at 0% (its displayed correctly when its under 99% and under). If I then remove the power cable the laptop hibernates as it thinks it has no power in the battery. Im running on a Compaq Presario C740. It sounds like this very old bug https://bugs.launchpad.net/ubuntu/+source/upower/+bug/583271 where the figures residing somehwere in /sys/class/power_supply/BAT0 are not correct, eg energy_full shows 3518000 and energy_now shows 4610000 (ie a higher figure for the current energy than its actually possible). https://bugs.launchpad.net/ubuntu/+source/kde-baseapps/+bug/1235633
	In gThumb, select a picture, right-click on it, select “Set as Desktop Background”, once applied, click the “Preferences” button on the green banner that just appeared at the bottom of the gThumb window and you’ll get the error message “Failed to execute child process “gnome-control-center” (No such file or directory)”
	If click “Lock screen” in Cinnamon, background don’t show full name year (only 20 without end) PL language
	any choice of the ‘suspend when inactive for’ parameter lets the computer never go to suspend mode
	any choice of the ‘when the lid is closed’ parameter: the computer always suspends
	any choice of ‘power button action’ leads to an immediate shutdown when pressed
	When I right-click an item, the menu entry “Send by Email” is not translated.
	“Enter your password to perform administrative tasks” isn't l10n'd
	In System Settings\Windows the options (Toggle Shade etc.) for the first four entries are not translated.
	In System Settings\Fonts “None”, “Greyscale”, “Slight”, “Medium” and “Full” are not translated to Danish though Danish is 100% translated.
	In System Settings\Applets on the Tab “Get more online” the middle button (Select updated) is not translated.

MATE Edition - last processed comment: #165
------------
	marco: Java apps are almost unusable when maximized. http://forums.linuxmint.com/viewtopic.php?f=47&t=112470&p=709183 https://bugzilla.redhat.com/show_bug.cgi?id=918055	
	nm-applet crashed, stopped working
	Login Window for pw on encrypted disks starts too far left with ***,,,should be centered
	mate-system-monitor under recourses doesn’t look great with the default GTK theme
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
	Mintmenu has a scrolling problem when the ALL-Tab was clicked and dragged quickly. This is a small problem.
	In the Mint menu, “Applications” is still badly translated in french. It should be replaced by “Logiciels” instead of “Applications” that means nothing. In the other applet menu (not default Mint menu), the translation is fine, see http://nsa33.casimages.com/img/2013/05/01/130501011029467213.png
	If you add a few keyboard layouts and set the CapsLock key to switch them, after reboot CapsLock stops switching the layouts.
	If you set a black wallpaper, the text below desktop icons becomes unvisible after reboot or logout and login. It appears even in LiveCD mode (set black wallpaper, logout, wait for login, see).
	Two ‘Network’ items in mate-session-properties.
	1. Open caja window 2. Click right mouse to some file or dir, select Properties. 3. Go to Emblems tab, enable some emblem, press Close. 4. Click right mouse to the file/dir, select Properties. 5. Go to Emblems tab, disable the enabled emblem, press Close. 6. Caja is crashed.
	i dont see dng and raw images thumbnails in caja
	network settings forgets DNS entries
	Major issue: gparted is missing on the live DVD. In the past, even though gparted was not installed in an initial install to a hard disk, it was present on the live DVD. gparted is an essential tool for checking or preparing a drive for a new installation, and for using the live dvd for troubleshooting and maintenance tasks, such as copying, moving, and resizing partitions. I would really, really like to see it back on the live DVD
	I cannot set the pointer size. The slider in Appearance/Customize/Pointer is greyed out
	Regardless how I set the screen shut down in Power Management, it always shuts down after a very short time. I tried ‘Never” and ’1 hour” but it did not work.
	Could not install network printer.
	mate panel doesn’t do autohide after locking and unlocking screen.