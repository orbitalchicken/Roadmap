New bug reports in Linux Mint 19 BETA

All editions
------------

artwork:
	Firefox bookmarks don’t use the folder color picked in the Cinnamon theme setting.
	The slideshow that shows during installation shows screenshots from a previous release, which still uses mint-X, and is therefore inconsistent.
	Folder color yellow is missing (Mint-Y)

mint tools:
	mintinstall: does only wait and not warn if synaptic is open.
	mintupdate: conflicts with VM guest pkgs... installing them removes mintupdate (and mintwelcome)
	mintupdate: On first time use, the preferences section “jumps” on the screen.
	mint-common: uninstalling flatpak from menu doesn't work (tried with VLC)
	mintdrivers: The text in “Authenticate” window that comes up when i click on Driver Manager is not fully translated. I’m using it with PT-BR language. The only thing that is translated is the bold text that appears above the explanation text. Buttons, window title, explanation text and “Password” are not.

ubiquity: When installing to internal 16GB SSD and with option “Something else” using the whole SSD for mountpoint root, installation always hangs in both XFCE 64 and Cinnamon 64. Ubuntu 18.04 installer with same options has no problem.

base:
	Shutdown takes forever: “A stop job is running for Cryptography Setup for cryptoswap1” takes over 5 minutes
	systemd-udev cause high cpu: https://bugs.launchpad.net/ubuntu/+source/udev/+bug/1767968?comments=all
	wine doesn't work (upstream issue in 18.04)
	ms ttf fonts says it is installed but when i go to fonts to use arial black there are no fonts i fixed this by uninstalling from software manager reboot and reinstalling them then reboot then it works i like my arial black and 1 of the few reasons i use lm verses all other distros
	When using RTL language (in this case Hebrew) in the right click menu on the window header the icons and check boxes go over the text. https://imgur.com/a/fISEJJA
	Boot hangs 1 minute with “gave up waiting for suspend/resume device”
		there seems to be a wrong uuid for resume in initramfs.
		Temporarily solution is here: https://askubuntu.com/questions/1013830/slow-boot-long-kernel-load-time-due-to-wrong-resume-device
	Despite installing open-vm-tools-desktop window resizing does not work
	wifi dongle rtl8192eu is not being recognized, but the generic rtl8xxxu-driver is being loaded instead yielding a 1mbs connection speed
	Using a live boot session in VirtualBox no longer allows copy-and-paste between the host and the Linux Mint live boot session, and resizing the VirtualBox window for that session does not resize Linux Mint within that session. Version 18.2 and several prior versions would do both copy-and-paste (to and from the host) and resize the VirtualBox session window easily.
		I wrote up how and why to use this feature in a blog post a couple of years ago, and it has been quite helpful for myself and my readers.
		https://adventuresofwondergeek.wordpress.com/2016/03/16/safer-online-banking-for-windows/


package selection:
	The quick filter is missing in synaptic.
	What about Java software? It is not being installed by default during the installation (even if I selected to install additional 3-party software)? Anyway after manually installing the openjdk-8-jre or openjdk-11-jre, LibreOffice is not working properly (in the LO preferences Java is visible…) – mainly LibreOffice Base (creating database is not possible)… Could you please check this from your side?
	i can not read video like mpeg or mp4 (with ubuntu mate 18.04 live or xubuntu 18.04 live, i can, now mp3 and mp4 codec is public domain, that’s why, no need to install extra codec to read those ones 


Cinnamon Edition - last processed comment: June 5, 2018 at 5:18 pm
------------------------------------------------------------------

[FIXED IN GIT] When I edit an application in “Startup Applications”, and it has a delay, the seconds unit “s” disappears.
[FIXED IN GIT] cinnamon settings startup, edit item with no delay, save -> python exception

artwork:
	cinnamon themes hardcode the font

settings:
	backgrounds: On the left pane, you can’t select “Pictures” folder by clicking, you need to use the keyboard – Down key..
	power: No way to set brightness for battery VS AC power.
	menu-editor: when adding new Menu items to the Menu, The Icon’s won’t save.
	desklets: I found a little bug in the Desklet “Analog Chronometer”. I can not call the settings when I have downloaded and switched on the Chronometer.
	ccc: After adding a color profile, gnome-color-manager won’t auto install when I click “view details.” I have to install it manually in the terminal, software manager or synaptic.

network:
	Wireless not showing in Network Manager even though it appears in Network Manager Settings.

Cinnamon setting to disable the touch pad while typing does not work, which makes typing on the laptop pretty annoying.
machine will not hibernate, (either from the power button (the hibernate option is selected) or from the exit menu) the screen blanks for a couple of seconds then returns to the session)
terminal: Just installed it with Hebrew as the system language and there’s something really weird with the fonts on the terminal. https://imgur.com/a/OHjoBu8
Installing in VirtualBox give error “Running in software rendering mode”
Even after authorize Samba in gufw, Nemo doesn’t show the local network and machine on it. I must manually type smb://user@ip to get in (after workgroup and password) In Mint 18 that was directly available.

cinnamon:
	On Vivaldi when I full screen a youtube video, the dashboard always remains displayed. Same on Firefox.
	Some applications that I installed through additional ppa (like 4kvideodownloader), to open through the menu, I need to restart the computer. Other applications that I installed through additional ppa (like qbittorrent and woeusb) work without having to restart.
	Installing Pysolfc via Synaptic and also Software Manager. No Games directory added to the menu. Though game worked from within a terminal. Restarting the computer the Menu was properly populated.

csd:
	If the screen is rotated, then the touch screen digitiser and trackpad both move the cursor in a direction mirrored to what is expected ie move your finger to the left on the screen and the cursor moves to the right. This works properly in Gnome.

systray:
	The Telegram icon in the bottom right bar is too small, like Dropbox icon. But it works well.
	The Skype icon in the bottom right bar is a little deformed, but also works well.
	Two Skype icons are displayed on the panel near the time.
	After log-out & log-in back, the update manager icon stays there but nothing happens when you left or right click on it..
	The dropbox icon in the bottom right bar is too small.

MATE Edition - last processed comment: June 5, 2018 at 12:57 pm
---------------------------------------------------------------


Windows Manager Metacity+Compton puts red line around app window
provide network/sound panel icons
preferred apps: caja, onboard, orca aren't selected
ubiquity: click rel notes, nothing happens
update manager toolbar is too big
When installing beta 19 mate, from a live USB thumb drive version, my screen goes BLANK during the install to the hard drive in spite of the fact that I had turned off ALL screensaver and power management features on the live USB session. Once I got the install done to the hard drive and again turned off the screensaver and power management the problem did not repeat.

Xfce Edition - last processed comment: June 5, 2018 at 9:42 am
--------------------------------------------------------------

panel/osd
	changing sound volume via hotkey shows two on-screen-displays
	pulseaudio item has two onscreen notifications
	panel date and time item is set as bitstream vera fonts, but bitstream vera fonts not installed
	digital clock would not stay in the panel, only the analog version
	editing the panel clock item in anyway it won’t display anymore user need to remove clock then add again
	clock applet doesn't let you use custom format
	too many notification and status notifiers panel items, don’t know which one to control, they all have the same basic options. https://i.imgur.com/fmyhhdp.png
	After switching to a guest session and back to my session, the wifi indicator appeared twice in the notification area.

touchpad
	Elan touchpad’s ‘tap to click’ and ‘right click’ functions not working and can’t be set because they are not shown in touchpad settings (in cinnamon it’s fine and shown up).
	Touchpad tap would not work until I installed synaptics touchpad

software
	No pressure sensitivity when I tried Krita. Ugee’s graphics display pen not seen as mouse either. Both Krita and Ugee 2150 (and Huion) worked perfectly in Mint 18.1 and 18.3, Cinnamon/Mate versions.

mint tools
	mintdesktop shows a sidepanel with only one item in it
	can’t add any PPA

artwork
	Network Icon in Tray is not monochrome, like the rest of the Mint Y icons
	xed display right margin at column does nothing. in dark mode with classic and other themes highlight current line colors need to be inverted

can’t see the share remote desktop ….. i went to menu/preferences but then no desktop sharing was there

Suspend worked, but would not ask for my password. I set screen lock in power manager, which I think fixed this in the past, but then it would not suspend at all.

After installing Opera Browser, on first opening after login, I keep getting the message “The login keyring did not get unlocked when you logged into your computer”. Then it asks for my password (solution is to autostart  gnome-keyring-daemon -r)
