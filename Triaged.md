Triaged reports

Not a bug 
---------
	L5 updates listed in the Update Manager, which others have already mentioned. Probably due to the fact that they are listed as security updates, that they are overriding the Visibility settings
	The “tab” key cannot be used for keyboard shortcuts (as in Ctrl+Tab). Instead of registering as a shortcut, the tab key press moves the cursor focus out of the “Pick an accelerator” box, and down to the “Add custom shortcut” button.
	cinnamon-settings: themes - inconsistent aspect ratios for thumbnails
	Modem manager: is evil and often delays shutdown – should it be disabled by default?

Outside of the scope
--------------------
	virt-manager did not have the packages it needed on first boot.
	Dolphin Wii Emulator is not in the repos.

Can't reproduce
---------------
	when modifying settings in the Security Centre, I noticed that some minimized windows could not be maximized again. They were visible in the task bar but could not be selected.
	cinnamon : the battery icon doesn’t show the percentage on the panel and i have to always click on the battery icon to show me the percentage.
	HP D630 - Firefox address bar, the letters are replaced by grey and black squares.	
	mate: firefox suggests mintinstall for tgz
	mate: I can’t get any workspace switcher
	mate: When printing something, print queue icon appears in the ‘notification area’ as expected. But then… The print queue icon gets ‘stuck’ in the notification area and becomes totally unresponsive (i.e., useless). Left or right clicks using the mouse yeild no result. Killing the ‘/usr/bin/python /usr/share/system-config-printer/scp-dbus-service.py’ process is the only way I’ve figured to get rid of the printer icon.
	mate: You cant set display brightness on battery power mode, just on AC
	mate: The white on black background menu is not good for anyone with other than 20/20.
	mintlocale: mintlocale: Apply System-Wide Language – It is always displayed as ‘English, United States’, even if you change it in the list (try with Arabic - UAE)	
	is DNS lost after suspending?
	the data at /media/user/ doesn’t get deleted automatically when you eject the CD

Upstream
--------		
	ubiquity: I tried installing Qiana RC Cinnamon from a USB drive using the “Erase everything” partitioning option. It erased everything all right: including the USB drive it was installing from
	ubiquity: The installer (LM16 RC 64bit) seems to be failing during this kind of install:  Manual, / onto sdd, Mounting /home (LUKS encrypted) from hdd. It just sits there without any cpu usage or anything after putting in the username and password page. Didn’t touch the existing install at all. Did the exact same thing with the 16 64bit previously which worked flawlessly.
	ubiquity: LUKS password steps precedes keyboard layout selection.. leading to the user blindly inputting a password that doesn't correspond to what he thinks he's typing.	
	cairo-dock: Cairo Dock doesn’t select the openGL backend when adding to startup, even if you tell it to remember your choice when it asks. I had to manually go into Startup Applications and edit the command with cairo-dock -o for it to work
	chromium: After each restart of the system Chromium can’t play Flash and I have to reinstall the plugin.
	guvcview:  doesn’t record video. It just records weird stop motion kind of stuff.
	mate: mate-calc 1.8.0, mode advanced, not calculation correct. Example (1×10^-1)/(1×10^-2)= 10. This calculate correct. Bud 1×10^-1 / 1×10^-2 = 0.001 this is not correct, because 1×10^-1 is one number on science notation ( 1 plus function x10^y plus -1 )
	mate: Power Management Preferences Tabs – I think the ‘General’ tab should be the first tab, rather than the third.
	mate: ‘Copy To’ Removable Drive – I plugged in my usb drive and it would be great to be able to right-click on a file and find the removable drive in the ‘copy to’ sub menu
	mate: System Settings > Display won’t let me set the one on the right as primary. The “Set as Primary” button is grayed. It’s connected as DVI. The other monitor’s “Set as Primary” is not grayed. It’s connected as VGA.
	mate: no OSD when changing brightness
	pidgin: status icon is not showing (only a placeholder) even if in the settings it’s set to always show. (I use Mint-X dark icon theme). I found a workaround for it: I have to go to Pidgin settings and then set “Never show” and “Show always” again.		
	themes: cinnamon-screensaver: If using dark theme (I’m FlatStudioDark and I already tried with other dark theme too), there is black/dark horizontal box surrounding the clock and lock dialog. http://i.imgur.com/jrW5DoA.jpg <-- probably the theme specifying a background color for event-boxes or other containers such as gtk.Box
	Can't install epson printer https://bugs.launchpad.net/linuxmint/+bug/1320644
	
Upstream critical
-----------------	
	Hard freeze:
		NVIDIA Corp c51(Geforce 6150 LE) Hard freeze
		NVIDIA GeForce 6150SE nForce 430 (rev a2) hard freeze
		Nvidia 256 dedicated Geforce 6150SE nForce 430 Hard freeze
		System lock ups with NVIDIA Corporation C61 [GeForce 7025 / nForce 630a] (rev a2) --> have to use nouveau.noaccel=1
		NVIDIA Corporation C61 [GeForce 7025 / nForce 630a] (rev a2)
	
	computer reboots:
		AMD CPU + MSI Card - computer reboots https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1309578

	mouse/keyboard freeze
		I believe I found the fix: https://bugs.launchpad.net/ubuntu/+source/nfs-utils/+bug/1270445
		I had to blacklist rpcsec_gss_krb5. Since blacklisting and rebooting I have not had any freezes. So Happy, everything else appears to be working good.
	