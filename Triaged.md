Triaged reports

Not a bug
---------
	nmap scan found the microsoft-ds ports, open 445 (samba)
	cinnamon: Notifications always appear in the panel even though they are disabled.
	cinnamon: Update shield became so small --> will move to new libindicator eventually
	mate: https://github.com/mate-desktop/caja/issues/569
	libmad0 is illegal in the U.S. and Japan --> No it's not (https://gstreamer.freedesktop.org/data/doc/gstreamer/head/faq/html/chapter-legal.html)
	installing HP Linux Printing Service HPLIP. It wants a library item libtool, which is already installed (I did sudo apt-get install libtool to verify). The HPLIP site is http://hplipopensource.com/hplip-web/index.html --> already packaged and installed by default in Mint 18.
	kde: ufw-kde does not work (in 17.x works) --> the gtk frontend is provided as default
	kde: please remove anything remotely related to akonadi. It is an abomination.
	kde: tray:  Very big icons and text tip fonts. If you add a pager to maneuver multiple desktops, for example, the remaining space available for the task manager itself becomes limited, almost half of the total screen width (height can be modified if needed).

Outside of the scope
--------------------
	xplayer + marco: while in full screen mode does not play video smoothly (use compton + mpv for better performance)
	mate clock applet: font and color is not customizable
	kde: can you include kolor-manager?

Can't reproduce
---------------
	Videos (Xplayer) window cannot be maximized (other windows can);
	mate: snap terminal right (ie drag to take up the right half of the screen) and the text is too far to the left to read the first character in each line.
	mate: control Center > Keyboard > Layouts “Choose a layout” window is gigantic and unresizable
	mate: Firefox Search Engines are missing and cannot add new one. In Cinnamon that works ok.
	mintmenu: when I install a piece of software it doesn’t show up until I log out from the desktop session and log back again, is it something normal or not?
	mozo: sliding an entry between a submenu to another crashes the menu editor and corrupts the menu (all applications disappear). Same problem when deleting a shortcut in the “other” submenu.
	mate: Mate System Monitor was not visible in any of the Mate menus in my installation. It was however accessible through mate-system-monitor command. “apt reinstall mate-system-monitor” solved the problem (application showed up in the menus).
	Steam will not work at all in MATE.
	cinnamon: Battery applet seems to stay at ‘charged ‘ even after power cord is removed, it MAY stay showing on charge or it may show on battery, its unpredictable.
	mintlocale: Tried adding support for iBus and FCITX (in Languages > Input Method) -> broken packages
	cinnamon: When using the Laptop with external Monitor, it isn’t possible to maximize windows on laptop panel. They will always maximize on the HDMI monitor instead. Same behaviour I had on my 17.3 Setup
	Can't switch sound to HDMI
	In /boot, Memtest86+ version is 4.20 but the last version of Memtest86+ is 5.10. (version is 5.01, like in the repositories)
	in the new ubuntu 16.04, touchegg works with 3 finger gestures, if I put synclient disable ClickFinger3 & TapButton3, however, in linux mint it’s not recognizing it..! (seems to work more or less, need more accurate issue description)
	cinnamon: I can disable mobile broadband using the switch in network preferences but it does have any effect. Next time I open up network preferences it is enabled again. I guess this could be a upstream problem though.
	Why did you change from Noto Sans to Noto Sans Regular? Letters now look short and stretched. They are much more elegant on 17.3. (some tools went from GTK2 to GTK3, noto changed slightly, other than that...?)
	cinnamon panel unresponsive when using nvidia 304 drivers?
	mintinstall http://imgur.com/a/oh56T
	mint-y update issue: http://imgur.com/a/B14wG
	mdm: autologin fails randomly (race condition at boot time?)
	kernel updates wipe the vbox dkms module?
	xfce: Whisker menu buttons are highlighted bugzilla.xfce.org/show_bug.cgi?id=12402 (already fixed)
	xfce: libindicator-plugin.so uses 10/20% CPU at idle. Removing the applet from the panel --> CPU usage goes down.
	xfce: Mint-Y theme Desktop Icons-text is not centered (Mint-X theme is OK).
	xfce: if I set it in Power Manager to just turn off screen or lock screen, when I open it back it works once BUT if I then close and open it again – the screen never comes back on and sometimes it seems whole system freezes( and other times it seems that just the screen doesn’t lit up, as it reacts to power button pressed).
	xfce: ALWAYS happens, regardless what settings I have on closing the lid: after opening the lid back the system opens Display preferences.
	kde:
		Whenever I selected to install 3rd party package, it stayed in that screen with wait cursor. Clicking back button didn’t bring it back to previous setup screen.
		The installer says that VLC is included. It is not.
		After adding any widget in desktop, desktop looks freeze for sometime.
		When I shutdown the session using K-Menu->Leave->Shutdown, the computer simply reboots.
		kwallet: Some sort of conflict between KDE wallet and the network manager. If KDE wallet is disabled passwords can’t be made persistent, you’ll have to type them every time you start. Similar if I recall to Kubuntu, but not in Manjaro KDE 32 bit.
	 	kwallet: every time you log into the session kded5 application asks to enter wi-fi password for kwallet. I tried to disable kwallet and even delete it, but the problem remained. Did I do something wrong to do to set up? But in the previous version(17.x) and in other distributions KDE (Kubuntu, KDE neon) had no such problems.
	 	kwallet: Found a cure for Kwallet and WiFi. Before you connect to your WiFi open Kwallet and disable it. Once disabled you can connect to your WiFi, enter your password then click on connect. It will now save your WiFi password and enable it each time you boot up without having to put in the password.
	 	The default GTK3 theme is set to Mint-X instead of “Breeze”
	 	The screenlocker is broken and unlocking is not possible anymore.
	 	“Show desktop” widget/hot corner does not hide “Desktop Settings” window.
	 	unable to download new themes “Loading of providers from http://download.kde.org/ocs/providers.xml failed”
	 	desktop effects hot corners are not work
	 	crash when blender is launched
	 	konversation shows duplicate entry for “spell checking language” options. Screenshot http://i.imgur.com/yIvT4x3.png
	 	The function key of the touchpad works, but there is no indication.
		When adding a user, the existing home directory is not chowned. KDE will not start complaining about wrong permissions in .kde and .config directories.
		changing to another user -> can't remember wifi password (asked twice)
		dolphin still not automount iphones? works in nemo.
		New bug just began yesterday. Opening MintUpdate and clicking refresh crashes Kwin.
		Weather widget has stopped working; just sits there listing the target city name but no long shows weather details popup upon click.

Upstream
--------
	grub: 32bit version doesn’t support 32bit UEFI
	samba: ‘Failed to retrieve share list from server’
	gtk (levelbar): Microphone level meter has color reverse. Shows red when low level and green when picking at high level. This is with build in microphone on Lenovo Carbon X1 4th generation 2016.
	gdebi: http://oi66.tinypic.com/2s9yqg5.jpg (https://bugs.launchpad.net/ubuntu/+source/gdebi/+bug/1581425)
	libgtksourceview: in xed with the classic and default (tango) color-scheme there is nearly no differentiation (color or border) between the text and the line-numbers; and at the latest working on a file with numbers at the beginning of the lines this is a disaster.
	mate: In the prefered applications(menu Preferences, “Prefered applications”), Caja isn’t the File manager by default. Must add it manually.
	caja: I can’t find hidden files in Caja file manager.
	caja: I noticed that search result doesn’t appear till the end of search, this may take some time. it would be nice to improve search behavior like the search in nautilus so that the search results in the current folder appears instantly.
	mate-control-center: when using ‘Mint-Y-Dark’ theme, and then pressing an item in the ‘Groups’ menu (such as ‘Hardware’), it paints the group-block in a very light-green color, so the white text is not readable.
	mate-control-center: install gnome-system-tools, items aren't l10nd.
	mate-notification: “connection established..” message always on front. no way to close
	mate-panel lacks borders: https://github.com/mate-desktop/mate-panel/issues/344
	mate: If a launcher is created from the desktop of type “application in terminal”, any command and attempting to execute the launcher results in the following error: “Details: Failed to execute child process “xterm” (No such file or directory)”
	intel: mouse cursor disappears (switch user with mdmflexiserver, log back in) https://bugs.launchpad.net/ubuntu/+source/xserver-xorg-video-intel/+bug/1568604
	Printer driver requires "lsb" package https://bugs.launchpad.net/ubuntu/+source/lsb/+bug/1536353 (being fixed upstream)
	hardware:
		Surface Pro: Type cover/touchpad/Touchscreen/pen not working -> https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1504618
		Fatal resolution problem with all 16.04 derivatives https://answers.launchpad.net/ubuntu/+question/292402
		Qualcomm Atheros QCA6174 802.11ac Wireless Network Adapter (rev 32), "wireless unavailable" --> https://bugs.launchpad.net/ubuntu/+source/linux-firmware/+bug/1520343
		Ethernet - no connection - Realtek Semiconductor Co., Ltd. RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller (rev 0c) --> http://askubuntu.com/questions/763080/no-wifi-in-qualcom-atheros-ubuntu-16-04-acer-aspire-e-15
		Does not support Netgear A6210 wifi adapter.
		WIFI issues with RTL8191SU (Rosewill-Wireless Lan-USB 2.0 Adapter-Model No. RNX-N180UBE)-(LSUSB-Bus 005 Device 003: ID 0bda:8172 Realtek Semiconductor Corp. RTL8191SU 802.11n WLAN Adapter)
		Bluetooth on Lenovo w530. Bluetooth applet cant seem to pick any device. It will just display searching for devices and either provide an empty list or list devices i cannot setup. On 17.3 it worked like a charm
		Lenovo Y700 no sound
		Onboard audio for an Intel DQ965GF motherboard is not working.
		No sound (worked in 17.3): Audio: Card-1 Intel 8 Series/C220 Series High Definition Audio Controller, driver: snd_hda_intel bus-ID: 00:1b.0 Sound: Advanced Linux Sound Architecture v: k4.4.0-24-generic
		My mic is not working. Lenovo C-440
		HP LaserJet 5000 on parallel port – Device URI: parallel:/dev/lp0 Buffer overflow error when printing. hpcups 3.16.3. Works in Mint 13 and 15, but not in 17.x/18.
		suspend: Lenovo G50 80, core i5 broadwell, 2.2 ghz, GPU AMD Radeon 2GB, 500GB SSHD and 12GB of RAM. -> can't suspend -> black screen and never wakes up.
		Intel Corporation Haswell-ULT Integrated Graphics Controller --> can't boot without recovery mode
		Dell Inspiron 15  i7-6700HQ Processor 6th Generation Intel Core (Skylake) 16 GB memory 128 GB SSD + 1TB HDD -> boots to black screen
		soft lookup cpu3 stuck for 22s, laptop is PE60 6QE, cpu is i7-6700HQ, vga card is Nvidia GTX 960M 2G (all worked fine in 17.3) (works with (acpi=off))
	update virtualbox-guest to Debian sid 5.0.2 to solve 3D acceleration?
	mint-x/mint-y: buttons aren't themed in gelemental
	xfce:
		Keyboard Layouts Text-font SIZE is not working (you can change the font of this task-bar applet but not its size).
		clock applet: can't change settings (deletes configuration)
		Thunar crashes when rename files. bugzilla.xfce.org/show_bug.cgi?id=12264
		Thunar crashes sometimes when copy and paste files
		Xfce4-task-manager toolbar style “Small” looks much better (maybe change default conf)
	kde:
		When changing resolution, after you press apply, there’s no confirmation window
		Clicking on the clock brings up the calendar but I can’t enter anything into the calendar?
		Under Virtualbox with 3D acceleration, parts of systemsettings are just black and fail to render (for instance Appearance)
		Only right mouse button opens indicators
		kwallet: If I set Gigolo to auto start and connect to five drives on my NAS, it starts before Wallet. I then have to enter my user name and password five times in Gigolo and once in Wallet. Disabling Wallet in settings then has the result of me needing to enter my wireless password every…..single….time. Why is Wallet needed?
		kwallet: i create my own keyring with my gpg key. 1. Although the wallet itself (hopefully) works,the systray icon never shows up 2. I have “Allow always”-ed a few apps, chromium, networkmanager, kwalletmanager5, konversation. But “allow” is remembered only for single session. How do i permanently allow above apps to access wallet ?
		Really Really missing the “Different Widgets for each desktop” option
		In LibreOffice, toolbar icons are not displayed correctly. They look like skeletons and are hard to distinguish.
		I can’t tell the difference between my desktops because they all have the same wallpaper
		kmail: crashes mainly when I delete some messages
		kmail: I can’t send email. Messages are moved to “Outgoing” and stuck there. In other distros, the solution was instalation of newer version of Kmail.
		kmail: color scheme of white text on light background makes message headers impossible to read.
		sddm does not display my profile pic at login. I have ensured/made the following changes without success – content in /var/lib/AccountsService/* configured “icon”. Added “FacesDir=/var/lib/AccountsService/icons” in /etc/sddm.conf. “accounts-daemon.service” up and running.
		Video thumbnails do not work. Installing ffmpegthumbs/kdeffmpegthumbnailer does not help. Workaround: sudo ln -s /usr/lib/x86_64-linux-gnu/plugins/* /usr/lib/x86_64-linux-gnu/qt5/plugins/
		no thumbnails for camera RAW files.
		Installing different window decorations breaks the ability to resize windows.
		Desktop settings > get new wallpaper,results in a blank box and the message “Some categories are missing”.
		According to the Meta key does not open Kickoff. When installing ksuperkey problem is partially solved. Menu opens on the button, but do not closes when pressed again.
		I had to manually put the slideshow directory to /usr/share/backgrounds/linuxmint-sarah [launched from desktop menu icon to top left], as otherwise turning the background slideshow on just gave a black screen.
	indicator-cpufreq:
		in KDE indicator-cpufreq doesn't show me conservative and powersave options. These are here in Linuxmint 18 Cinnamon and XFCE versions.