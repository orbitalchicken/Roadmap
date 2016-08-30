New bug reports in Linux Mint 18 BETA

All editions
------------
	mdm: Webkit preview, process doesn't die when window is closed
	mdm: Webkit preview, mint-X doesn't show anything, only background

Cinnamon Edition - last processed comment: #789
-----------------------------------------------
	nemo: Prefs > Display > Icon Caption > first option SIZE, and Prefs > Preview > Folders > options NEVER ---> results in "–" showing under directories (tested in icon view).

MATE Edition - last processed comment: #440
-------------------------------------------

Xfce Edition - last processed comment: #106
-------------------------------------------

KDE Edition - last processed comment: #198
-----------------------------------------

	Thumbnails:
		Video thumbnails do not work. Installing ffmpegthumbs/kdeffmpegthumbnailer does not help. Workaround: sudo ln -s /usr/lib/x86_64-linux-gnu/plugins/* /usr/lib/x86_64-linux-gnu/qt5/plugins/

	System:
		oneconf (python -> help() -> modules) invalid distro: ‘LinuxMint’

	Mint:
		The installer says that VLC is included. It is not.
		Slideshow doesn’t use translated file (korean)
		plymouth theme doesn't show disk-encryption password field
		Changing Icon Theme to Mint-* results in missing icons in Dolphin.
		During install I opted in to install codecs. It did install. After install when I go to Software Centre, under recommended apps, it shows as codecs not installed?
		Whenever I selected to install 3rd party package, it stayed in that screen with wait cursor. Clicking back button didn’t bring it back to previous setup screen.

	KDE:
		When changing resolution, after you press apply, there’s no confirmation window
		Clicking on the clock brings up the calendar but I can’t enter anything into the calendar?
		In Systemsettings: When I try to change the Login-Screen, I can see just a black Login Screen on the Preview. The LoginScreen itselfs works great.
		in the “energy information” (KDE control module) the history graphs don’t show. Instead I get the message “This type of history is currently not available for this device”. works in manjaro.
		tray:  Very big icons and text tip fonts. If you add a pager to maneuver multiple desktops, for example, the remaining space available for the task manager itself becomes limited, almost half of the total screen width. Some other distros (e.g. Fedora 24 KDE) apparently corrected (reduced) the icon sizes and look much more elegant.
		Desktop settings > get new wallpaper,results in a blank box and the message “Some categories are missing”.
		ufw-kde does not work (in 17.x works).
		According to the Meta key does not open Kickoff. When installing ksuperkey problem is partially solved. Menu opens on the button, but do not closes when pressed again.
		sddm does not display my profile pic at login. I have ensured/made the following changes without success – content in /var/lib/AccountsService/* configured “icon”. Added “FacesDir=/var/lib/AccountsService/icons” in /etc/sddm.conf. “accounts-daemon.service” up and running.	
		konversation shows duplicate entry for “spell checking language” options. Screenshot http://i.imgur.com/yIvT4x3.png
		unable to download new themes “Loading of providers from http://download.kde.org/ocs/providers.xml failed”
		Nothing shows up on “History” in startmenu.
		“Show desktop” widget/hot corner does not hide “Desktop Settings” window.
		I can’t tell the difference between my desktops because they all have the same wallpaper;Boring!
		Installing different window decorations breaks the ability to resize windows.
		Not sure if its a Chrome/Chromium thing or a Mint thing – but I can’t seem to set Chrome as the default browser?
		When I shutdown the session using K-Menu->Leave->Shutdown, the computer simply reboots.
		System Settings | Workspace Theme | Look And Feel comes up with a dialog box area that is black, just black. Moving the mouse around gets a tooltip here and there for “Breeze” and “Breeze Dark.” They are selectable, but it is weird selecting something that cannot be seen.
	 	System Settings | Multimedia | Audio Volume comes up with a dialog box area that is black
		recents documents and applications are not working in menu. they are working in kaos and openmandriva Lx3.0
		Only right mouse button opens Mint Update on panel.
		I installed indicator-cpufreq to prevent notebook heat. I clicked indicator icon. I can’t see conservative and powersave options in small list. But there is no problem on Linuxmint 18 Cinnamon and XFCE versions.
		crash when blender is launched
		After adding any widget in desktop, desktop looks freeze for sometime.
		desktop effects hot corners are not work
		Weather widget has stopped working; just sits there listing the target city name but no long shows weather details popup upon click.
		The screenlocker is broken and unlocking is not possible anymore.
		When adding a user, the existing home directory is not chowned. KDE will not start complaining about wrong permissions in .kde and .config directories.
		changing to another user -> can't remember wifi password (asked twice)
		New bug just began yesterday. Opening MintUpdate and clicking refresh crashes Kwin.

	Kmail:
		Except kmail that crashes mainly when I delete some messages
		I can’t send email from Kmail. I have tried 3 different smtp serwers (google, gmx and my own server) and the result is always the same. Messages are moved to “Outgoing” and stuck there. I have in my mind, that I meet similar problem when I start testing Plasma 5 (with Kubuntu) about half year ago. The solution was instalation of newer version of Kmail.
		KMail color scheme of white text on light background makes message headers impossible to read.

	Wallet:
		KDE wallet. This has to be the most useless piece of software out there. If I set Gigolo to auto start and connect to five drives on my NAS, it starts before Wallet. I then have to enter my user name and password five times in Gigolo and once in Wallet. Disabling Wallet in settings then has the result of me needing to enter my wireless password every…..single….time. Why is Wallet needed?
		In addition to #31 regarding Kwallet – i create my own keyring with my gpg key. 1. Although the wallet itself (hopefully) works,the systray icon never shows up 2. I have “Allow always”-ed a few apps, chromium, networkmanager, kwalletmanager5, konversation. But “allow” is remembered only for single session. How do i permanently allow above apps to access wallet ?
		Some sort of conflict between KDE wallet and the network manager. If KDE wallet is disabled passwords can’t be made persistent, you’ll have to type them every time you start. Similar if I recall to Kubuntu, but not in Manjaro KDE 32 bit.
	 	every time you log into the session kded5 application asks to enter wi-fi password for kwallet. This latest offering from the outset 2 encryption type, and they are not activated. I tried to disable kwallet and even delete it, but the problem remained. Did I do something wrong to do to set up? But in the previous version(17.x) and in other distributions KDE (Kubuntu, KDE neon) had no such problems.
	 	Found a cure for Kwallet and WiFi. Before you connect to your WiFi open Kwallet and disable it. Once disabled you can connect to your WiFi, enter your password then click on connect. It will now save your WiFi password and enable it each time you boot up without having to put in the password.

	Software selection:
		please remove anything remotely related to akonadi. It is an abomination.
		For old KDE games to work users need to install “qml-module-org-kde-games-core”, for compatibility with QML.
		not decompressed ARK downloaded files from the web
		Ark (the KDE file archive manager) isn’t able to open ZIP files. The problem can be solved by installing “p7zip-full” (the base package “p7zip” is already installed).
		Impressed until I tried viewing Camera RAW files,no thumbnails. Required decoders etc have been installed and enabled in Dolphin Preview dialogue. Coincidentally i have the same problem with XFCE and Mate.An installation of UBUNTU KDE does not have same problem.
		dolphin still not automount iphones and idevices ???? Nemo in cinnamon just displays the file system and lets you drag and drop. But with dolphin i have to manually install things like libimobiledevice etc and then play around woth dolphon plugins.
		Please you can include kolor-manager package in the official repositories? as opensuse. I tried instal kolor-manager on linux mint KDE 17 and I could not. The colord-kde package is useless. Does not apply the icc color profile to calibrate monitor.

	Configuration:
		I had to manually put the slideshow directory to /usr/share/backgrounds/linuxmint-sarah [launched from desktop menu icon to top left], as otherwise turning the background slideshow on just gave a black screen.
		.deb files are open by default with Ark, they should be open with some software installer instead.
		The function key of the touchpad works, but there is no indication (in kubuntu and neon is present)
		The default GTK3 theme is set to Mint-X instead of “Breeze”
		In LibreOffice, toolbar icons are not displayed correctly. They look like skeletons and are hard to distinguish.
		it would a good idea to Turn OFF! the Screen Locker > located in Settings > Workspace > Desktop Behaviour > Screen Locking, as well the screen saver located in Settings > Hardware > Power Management

	Activities:
		cannot create new activities
		it doesn’t install kactivitymanagerd by default which is needed to be able to make/run activities.
		can’t edit activities. Trying to rename the current one or create a new one opens a dialog window, and clicking OK in it closes it but no changes are applied.
		When I go to System settings-power management and then activity settings, nothing shows up? Just a blank space. In Kubuntu 16.04.1 it does function.
		Really Really missing the “Different Widgets for each desktop” option
		I installed kactivitymanagerd and am able to add and edit activities. However, on the next boot plasmashell kept crashing. I used Alt+F2 to run commands. I had to killall kactivitymanagerd, then start plasmashell, and then start kactivitymanagerd again. My activities have been forgotten, though.

	Root dolphin:
		View Folder as Root – when viewing the boot EFI folders as root the folders are White and can not be seen (same color as background)
		installed all needed packages, updated mint-artwork-kde but still no icon when opening dolpin as root. writing this to open dolphin works: kdesudo -c “KDE_SESSION_VERSION=5 KDE_FULL_SESSION=true dbus-launch dolphin”