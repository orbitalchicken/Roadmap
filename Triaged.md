Triaged reports

Not a bug 
---------
	L5 updates listed in the Update Manager, which others have already mentioned. Probably due to the fact that they are listed as security updates, that they are overriding the Visibility settings
	The “tab” key cannot be used for keyboard shortcuts (as in Ctrl+Tab). Instead of registering as a shortcut, the tab key press moves the cursor focus out of the “Pick an accelerator” box, and down to the “Add custom shortcut” button.

Outside of the scope
--------------------
	virt-manager did not have the packages it needed on first boot.
	Dolphin Wii Emulator is not in the repos.

Can't reproduce
---------------
	when modifying settings in the Security Centre, I noticed that some minimized windows could not be maximized again. They were visible in the task bar but could not be selected.
	cinnamon : the battery icon doesn’t show the percentage on the panel and i have to always click on the battery icon to show me the percentage.
	HP D630 - Firefox address bar, the letters are replaced by grey and black squares.	

Upstream
--------
	Breadcrumbs in Nemo do not display correctly with Adwaita theme or High Contrast theme.
	chromium and muffin hate each others..
	I tried installing Qiana RC Cinnamon from a USB drive using the “Erase everything” partitioning option. It erased everything all right: including the USB drive it was installing from
	The installer (LM16 RC 64bit) seems to be failing during this kind of install:  Manual, / onto sdd, Mounting /home (LUKS encrypted) from hdd. It just sits there without any cpu usage or anything after putting in the username and password page. Didn’t touch the existing install at all. Did the exact same thing with the 16 64bit previously which worked flawlessly.
	LUKS password steps precedes keyboard layout selection.. leading to the user blindly inputting a password that doesn't correspond to what he thinks he's typing.
	If i watch a youtube video in full screen mode and come back to normal mode then my chrome is hiding the bottom panel/taskbar. This is not happening with firefox.
	Cairo Dock doesn’t select the openGL backend when adding to startup, even if you tell it to remember your choice when it asks. I had to manually go into Startup Applications and edit the command with cairo-dock -o for it to work
	After each restart of the system Chromium can’t play Flash and I have to reinstall the plugin.
	guvcview doesn’t record video. It just records weird stop motion kind of stuff.
	mate: mate-calc 1.8.0, mode advanced, not calculation correct. Example (1×10^-1)/(1×10^-2)= 10. This calculate correct. Bud 1×10^-1 / 1×10^-2 = 0.001 this is not correct, because 1×10^-1 is one number on science notation ( 1 plus function x10^y plus -1 )
	mate: Power Management Preferences Tabs – I think the ‘General’ tab should be the first tab, rather than the third.
	mate: ‘Copy To’ Removable Drive – I plugged in my usb drive and it would be great to be able to right-click on a file and find the removable drive in the ‘copy to’ sub menu
	mate: System Settings > Display won’t let me set the one on the right as primary. The “Set as Primary” button is grayed. It’s connected as DVI. The other monitor’s “Set as Primary” is not grayed. It’s connected as VGA.
	
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
	