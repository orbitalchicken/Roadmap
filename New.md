New bug reports in Mint 16 RC

All editions
-------------	
	system: grub/efi: UEFI boot and GPT partition tables, the installer crashes when installing grub. I have installed Ubuntu 13.10 on both of those UEFI systems with no problem.	
	system: grub/efi: Mint16 cannot install package grub-efi-amd64-signed. Why it try to do that if I have not EFI, UEFI and so on? Also I can’t install grub after from terminal but receiving other errors (something about “unable to determine /cow path”)
	system: apt-get dist-upgrade wants to install shim*, it's for secure boot, i don't think, it should be available for installation
	system:	Xorg does not start on my ati r128 video card. This seems to be an upstream issue in xorg 1.14, but you did mention the b43 hang issue in Maya.	
 	mintdrivers: broadcom wireless chipset is recognize well, but I can’t choose the upper button (it always go back to “do not use this device”) http://www.imagebanana.com/view/jx2lm7vz/drivermanager.jpg	
 	mintdrivers: Driver manager list is always empty even Nvidia-319 driver installed (I’m also not sure if it should allow installation for detected hardware)				
	apps/drivers: synaptic: Synaptic issues: [1] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1178024 [2] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1135687 [3] https://bugs.launchpad.net/ubuntu/+source/libgksu/+bug/1216045 [4] https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1135687/comments/6	
	apps/drivers: language input short cut is terrible as it did on the saucy salamander If our linux mint is not going to focus on the ubuntu-tablet then I suggest to our linux mint team to abandon this very uncomfortable input method for other non-english countries including Korea super + space brings malfunction for menu, everytime I input super + space for type in korean then I meet menu pops up , and even it works not welll either.		
	apps/drivers: Brasero Wont open after burning a disk
	mdm: always uses English keyboard layout?
	mdm: With nvidia-current installed attempting to shutdown or restart from mdm hangs with black screen. Have to shutdown with the power button.	

Cinnamon Edition - last processed comment: #218
----------------
	cinnamon: Having links of files/folders on desktop from another hardrive at startup, then mounting the drive will usually crash then restart Cinnamon
	cinnamon: Icons keep disappearing from desktop especially when I log out then log in!!		
	cinnamon: The Mint logo/icon that should appear next to the “Start” menu disappeared from the panel after the first reboot.	
	system: Mint Splash screen is not appearing, and seems to be defaulting to the Ubuntu 13.10 splash screen.

MATE Edition - last processed comment: #87
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
