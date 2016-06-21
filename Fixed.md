Fixed Issues since Linux Mint 18 BETA

All editions
------------
	mintsources: warning text uses hardcoded color (looks wrong in mint-y-dark)
	mintsources: can't browse PPA (relies on lsb_release -u)
	mintdrivers: grey font not readable
	mintdrivers https://github.com/linuxmint/mintdrivers/issues/23
	Optimus Graphic: When right clicking on nvidia icon, the menu pops up in the top right
	mintbackup just hangs indefinitely when you try to restore software selection, terminal has no output, and mintbackup is using no cpu.
	add curl to default selection
	In the date/time configuration, trying to change Manual by Synchronisation with NTP server. ntp package is not installed.
	Cant seem to be able to set the clock, unlock the setting and set it but it doesn’t hold.
	mintupload: when editing a (non working – e.g. the default “suggested”) account, without changing something (and therefore closing the window with the top right X) the next time i just get an empty tiny Properties-window! you have close the Upload Manager (just the window – not even necessary to restart mintupload) and it is working again.
	mintlocale: Cannot change default System Locale by Language settings. Thus it can be changed manually by text editor. (file: /etc/default/locale)
	mintlocale: Failed to parse imconfig output
	banshee: will not import media form folders causing hard locks (disabled daap plugin to fix this)
	mintinstall: Missing emus in Software Manager under Games / Emulators: Higan is missing, but in synaptic Dolphin-emu is missing, but in synaptic
	Removed Skype via Software manager but the program still showing up in the Menu. Tried to uninstall it via the Menu but same results. Restarted the system and terminal is no longer works. Skype is still in the Menu but marked as “Install” in Software Manager.
	in Czech/Danish (and a few other languages), search in firefox does not work. Both from adress bar and from search bar. Search setting is unaccessible?
	At the top of xreader, it is shown how many pages the PDF file has. With Mint-Y-Darker Theme it is impossible to read.
	Mint-Y needs a tiny window border or drop shadow. It can be very difficult to distinguish where one window ends and another begins.
	Mint-Y:  I dislike these borderless windows. When I snap applications next to each other on the screen, the content just seems to run into eachother and almost looks cut off. I know it’s not actually being cut off, but without even a thin border it gives off that impression.
	no border for any opened window which makes it like it’s mixed with any other window if we use the new mint dark theme in cinnamon.

Cinnamon Edition
----------------
	nemo-terminal: E: Package ‘gir1.2-vte-2.90’ has no installation candidate
	white font? http://imgur.com/QBEM48H
	text in logout countdown isn't easily readable ... could be similar to Spices configuration module, when install 3rd party spices. Is it a missing style in Mint-X? To define the color of text in progress bars?
	“Automatically connect to VPN when using this connection” option for a WiFi network connection is failing upon startup. It then connects to the wifi without the VPN.

MATE Edition
------------
	when changing the appearance to Mint-Y-Dark the background in caja doesn’t change! you have to go to “Edit” -> “Backgrounds and Emblems” and reset it once manually. now it changes every time with the theme. (check gsettings set org.mate.caja.preferences background-set false)
	Can you somehow disable the audio file sound preview when you point your mouse pointer on it? It just often crashes the whole Caja file manager and the audio sometimes keeps playing even if I point mouse away from it (so i have to kill the proccess in proccess manager).
	Qt 5 apps use the Fusion theme by default rather than the GTK+ one.
	set as wallpaper doesn't work in pix and xviewer
	mintmenu: use custom color should be disabled by default (it makes mintmenu look really bad with mint-y-dark)
	mintmenu: transparent only once after reboot (first click on menu). Next click menu show not transparent
	mintmenu: The new MintMenu theme is supposed to have rounded corners, but the transparency is broken, leaving hideous white triangles where there ought to be transparency.

KDE Edition
-----------

Xfce Edition
------------
