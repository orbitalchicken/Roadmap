New bug reports in Linux Mint 18.1 BETA

All editions
------------
	mdm: Webkit preview, process doesn't die when window is closed
	mdm: Webkit preview, mint-X doesn't show anything, only background
	“unattended-upgrades” is installed by default. Why is this package running everyday, searching for packages in improperly-formated repos and fails every day as seen in ‘/var/log/unattended-upgrades’? This needs to be uninstalled or set the correct variables in /etc/apt/apt.conf.d/50unattended-upgrades!!
	Still cannot mousewheel across tabs in Xed
	kernel:
		check critical bugs against -45/-47 or consider Dirty Cow patch in -31
		consider offering 4.8?
	mintupdate:
		‘Most stable recommendation’ is poor English
		creates objects with wrong ownership. See https://github.com/linuxmint/mintupdate/issues/169
	check continue button greyed out if not enough HDD space?
	ubiquity: If I come to the last dialog during the installer of Mint (Name, Computer name, Password) I enter at first my name, than I press several times the tab key, leaving computer name and user name at the prefilled values. If I am now in the first field for entering my password the field with the user name gets and stays completely marked, but this should not be the case.
	I installed (64 bit) with German language. After booting the installed system I find in the language settings the message about incomplete language packs for 4 English and 2 German language variants. The annoying thing is, that each of those 6 language packs have to get installed separately, so this really wastes some time. I did several installs of Serena and found the problem reproducible.
	in xed, when you have more than a page, scrolling down (or up) with the down (or up) arrow creates a jerky display; similarly, with a large document, going from the top to the bottom with Ctrl-End (or vice-versa with Ctrl-Home) seems to have an intermediate stage where it is displaying text from somewhere in the middle of the document; reminds me of “smooth” scrolling in Firefox; makes xed unusable for me except for short periods of time or for very short files
	gnome-calculator takes way to long to exit (for a calculator); it also seems to be thrashing my HDD when it exits
	Having more than one terminal open the command to close all terminals in the file menu (or shortcut ctrl-shift-q) does not work as expected. Only the current terminal gets closed, all the others remain open.
	steam doesn't run out of the box.


Cinnamon Edition - last processed comment: #64
-----------------------------------------------
	nemo: Prefs > Display > Icon Caption > first option SIZE, and Prefs > Preview > Folders > options NEVER ---> results in "–" showing under directories (tested in icon view).
	Right-click an icon on the panel, select “options”, then “edit”. Try to choose a new icon. The new icon shows in the window. Try to click “OK”. It won’t click and the icon won’t change.
	msgids:
		"Layout and content" isn't present in LP?
		screensaver: “Please enter your password” screenshot – https://goo.gl/nXU73n
		nemo: “Click on a file’s name twice to rename it”.
	screensaver:
		please make clock jumping less frequent (5 seconds right now?)
		If the display for the time gets disabled, also the absence message does not get shown. I think, both should be independent from each other.
	Is the speed of the mouse pointer finally changable via the settings? This did not work for years now
	When running cinnamon live session, attempting to do a restart via the button on the cinnamon menu causes the screen to hang on the cinnamon logo as the system begins to shut down.
	By default the file name for the sound is my username (without ending like .oga). This file does not exist, so that by simply turning the option to play the notification sound will do nothing. Looks like a forgotten default value.
	If in panel edit mode right clicking the panel doesn’t do anything. This means, that you cannot turn off panel edit mode.
	upload sysinfo crash when offline
	The option to go up one level by double clicking an empty place (a very welcomed feature) doesn’t work at all. I tried it with some empty folders (e.g. Desktop), but nothing happens at all. Also logging out and back into the user account does not help.
	when installing themes https://justpaste.it/110ba
	Configuration option for the menu urgently missed:
		Until Mint 18 Sarah there was for the menu the option “menu hover delay”. This is not the same as the option with the same name in 18.1 Serena, as also the tool tip reveals, if you hover the option.
		The new option delays the appearance of the menu, if you have the option to open the menu by hovering it in the panel activated.
		The old option delayed switching the categories. This means, if you have selected a category and want now to move the pointer to the menu entry to the right, you can (with the delay set to e.g.150 ms) move the mouse diagonally over other categories without activating them by doing so. Without the delay the categories, touched by the mouse pointer get at once activated and the command in the right column is not more there.
		This leads to the result, that without the delay you have to move the mouse at first properly to the right and then up or down to the needed command; diagonal (and far quicker and more logical) movements are without the delay not possible.
		As this category delay has now been (erroneously?) removed the menu in 18.1 appears as a regression in usability. Please restore this option.
	Bug Found: 24 hour format won’t change to 12 hour in vertical panel mode
		To reproduce: Change panel to vertical panel, then change clock from 24 hour to 12 hour, the clock will display in 24 hour format still. If you change panel to horizontal, time will be correct, change back to vertical and it changes back to 24 hour format, but settings still say 12 hour

MATE Edition - last processed comment: #26
------------------------------------------

Xfce Edition - last processed comment: #0
-------------------------------------------

KDE Edition - last processed comment: #0
-----------------------------------------

