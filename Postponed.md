De-scoped
---------		
	GNOME: gnome-calculator menubar (minor cosmestic issue, won't fix)
	System: Support for Wacom tablet (configurable via the command line, will need to join forces with Xfce/MATE if we want to develop a cross DE UI. This doesn't justify pulling resources to make a Cinnamon specific solution)	
	System: EFI boot path isn't standard (EFI installation in Virtualbox works fine, but upon reboot it loses its NVRAM and isn't able to find the EFI boot files)
	MDM: l10n doesn't cover new features (MDM 1.4 is still using the l10n it inherited from GDM. Decision was taken to migrate MDM entirely to Mint/LP translations in 1.6, not just mdmwebkit/mdmsetup).
	MP3 online doesn't work (known limitation with totem)	

Improvements selected for the future
=====================================

Mint 17
-------
	mintsources: doesn’t show any progress bar and it seems to test mirrors one by one instead of doing it in parallel.
	system: migrate from gksu/kdesu to pkexec
	ubiquity-slideshow: In the “Install Software” slide of the installation slideshow, it shows Picasa under “Features software”, but Google dropped Picasa for Linux a little over a year ago
	mintdrivers: broadcom wireless chipset is recognize well, but I can’t choose the upper button (it always go back to “do not use this device”) http://www.imagebanana.com/view/jx2lm7vz/drivermanager.jpg
	apps/drivers: im-config should not be installed by default (agreed, but it's needed by language-selector-gnome, we'll replace both in Mint 17)	
	Shutdown sequence in live-session is all black	
	mdm: Cant set login screen time to 24hr (changing the option doesnt work)
	mdm: stopping the MDM service prevents access to the TTYs. Using Ctrl+Alt+F2 only works when MDM is running. Thus, there’s no way to run anything in a TTY unless the X server is running.
	Can’t play TS video files	
	cinnamon: inserting an Audio CD suggests Brasero and VLC, not Banshee
	banshee: tries to rip a CD to FLAC by default

Cinnammon
---------	
	cinnamon-settings: Cinnamon Regional settings is completely broken/useless/unintuitive, redesign from scratch in 2.2
	cinnamon-settings: 12vs24 hour clock, easier custom format selection
	cinnamon-settings: Add sound events for logout
	applets: Even after setting org.cinnamon.desktop.lockdown.disable-lock-screen to true, the lock button still appears on cinnamon menu applet…
	applets: The mint logo is a bitmap(png) and is blurry when the panel is resized, it should be svg
	applets: when I click on the window list to minimize and maximize sometimes the windows don’trespond and so I have to maximize another window so that I can mainimize or maximize the previous one!!	
	applets: Can't minimize windows which have a modal dialog (for example: Synaptic while installing a package). It's possible via the titlebar, but not via the window list
	applets: On/Off switch for networking applet is visually glitchy
	applets: Moving applets in cinnamon panel edit mode on, glitches out systray icons when it is shifted		
	prefs: I miss the working WIN+D keyboard shortcut to go to desktop.
	spices: removing extensions, themes, desklets, applets is only possible using right click (maybe it would be better to have button for that in future relases)
	spices: If I select the radio box to choose an applet and then I’ll click the button to install it, the applet is installed but it’s not active: maybe a new user expects to have it immediately in the panel after the download… in fact forcing the user to come back in the list of the installed applet to enable the just downloaded applet is not user friendly, in my opinion.
	nemo: if I press ALT+F2 and then enter “nemo ftp://ftp.mydomain.xyz” to access to my personal ftp server trough nemo, I’ll get a request of username and password: it’s OK. The problem is that if I select the option to remember forever the username and password, it will not have effect: if I reboot Linux Mint, the next time I’ll try to access my ftp trough nemo I’ll get the request of username e password. So… nemo doesn’t remember my credentials… it’s frustrating.
	nemo: Entering the folder of long name , the path disappeared screen capture 1) it shows a folder of longname https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A19.png screen capture 2) entering the long name folder , meeting disappeared folder path of long name folder https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A18%3A34.png screen capture 3) But Actually It was still dsiplayed at max window https://dl.dropboxusercontent.com/u/54450962/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%2C%202013-11-18%2002%3A19%3A13.png	
	nemo: package description for nemo-data it reads  "Nemo is the official file manager and graphical shell for the GNOME desktop."
	cinnamon: Onscreen keyboard activates when clicking the menu on the panel because text entry is focused... if onboard is used, entry should not focus when showing the menu	
	cinnamon: Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)		
    cinnamon: changing Wallpaper sometimes freezes cinnamon	
	cinnamon: menu doesn't listen to menu changes outside /usr/share/applications? install shotwell for instance (uses /usr/share/menu)
	Keyboard settings allow adding duplicate key combination for Cinnamon “Toggle Scale” and “Toggle Expo” (found these, didn’t go through all actions, most of them ok)
	nemo: Create a thumbnailer in usr/share/thumbnailers for MimeType inode/directory – when you try to run Nemo, it crashes with the error:  (nemo:9078): CinnamonDesktop-WARNING **: Error reading from file:///home/simon/Desktop: Error reading from file descriptor: Is a directory Installing cover-thumbnailer is an easy way to reproduce it.
	nemo-preview (not installed by default), doesn’t work: http://pastebin.com/Uaci0mzC
	cinnamon-settings: in French http://imagebin.org/277997
	Creating a user without password (stupid but nothing prevents it): impossible for that user to set one himself in Account Details.
	In the “Users and Groups”, when on “Groups” tab, it could be great to have a way to see the members of a selected group and add new members to the group as well. Currently, we can only edit the group name…
 	In Setting-Display no information about screen frequency (Hz) and click “Detect Display” showing nothing (1 or 2 connected monitors)
 	Feature request: if a create a luncher on my desktop, I can select an icon for it (with preview)… instead, if a modify a launcher in the menu with the “menu editor”, I can select a different icon but without preview. Can you please add the preview feature?
	if a launch from a bash script nemo to open an ftp server more than one time, with a command such as “nemo ftp://ftp.xxx.xyz“, I can get a duplicate icon on my desktop, see screenshot: https://dl.dropboxusercontent.com/u/573922/Schermata%20del%202013-11-21%2012%3A25%3A31.png 	
	1. Open nemo (unminimised)  2. Copy some files so that the transfer window is present 3. Open another program (unminimised) and in front of nemo such as firefox 4. If the transfer window is open (maximised) in front of the other program (firefox for example) and you click to minimise the transfer window, nemo will automatically pop up in front of the other program. Not a major bug but annoying from a window management point of view.
	Open GIMP, open a dropdown menu, e.g. the ‘Edit’ menu. Press the Print Screen button on the keyboard – no screenshot is taken while a menu is open.
	icons pixelated in alt-tab or panel after a suspend-resume
	llvmpiped session after a suspend-resume
	In gThumb, select a picture, right-click on it, select “Set as Desktop Background”, once applied, click the “Preferences” button on the green banner that just appeared at the bottom of the gThumb window and you’ll get the error message “Failed to execute child process “gnome-control-center” (No such file or directory)”	
	cinnamon: Having links of files/folders on desktop from another hardrive at startup, then mounting the drive will usually crash then restart Cinnamon
	Cinnamon menu: When creating a new menu item the icon does not appear. It is ok in the menu editor.
	l10n: In System Settings\Windows the options (Toggle Shade etc.) for the first four entries are not translated.
	l10n: In System Settings\Fonts “None”, “Greyscale”, “Slight”, “Medium” and “Full” are not translated to Danish though Danish is 100% translated.
	cinnamon-screensaver: If click “Lock screen” in Cinnamon, background don’t show full name year (only 20 without end) PL language

MATE
----
	mate-terminal still has a menu bar and is not transparent	
	Clicking “help” on most mate applications opens yelp to an error page (fixed in 1.7)
	When panel is at the top, notifications show on top of it. https://dl.dropboxusercontent.com/u/54450962/%ED%99%94%EB%A9%B4-5.png
	Would be nice if the mouse preference panel in Mate included a “natural scrolling” option
	Add sound effects like in Cinnamon
	The MATE user admin program (mate-users-admin), when setting a user’s type to “Administrative”, does not add the user to the “sudo” group. The workaround is to explicitly add the user to the sudo group
	‘mate-screensaver’ still as flaky as it was in lm15 MATE 64-bit. Set to ‘Lock screen when screensaver is active’ sometimes upon resume after suspend I get a prompt for my password, other times NOT.
	MPRIS support
	mintmenu: Not yet fixed MATE mintMenu bug where it isn’t transparent when user set panel with solid color – all panel adjusts transparent but mintMenu remains with default gray color.		
	marco: Java apps are almost unusable when maximized. http://forums.linuxmint.com/viewtopic.php?f=47&t=112470&p=709183 https://bugzilla.redhat.com/show_bug.cgi?id=918055 (won't fix in MATE, will try to convince the team or patch Marco in Mint 17)
	mate-system-monitor under resourses doesn’t look great with the default GTK theme (need to give the notebook at widget class name or style name so we can make it flat in Mint-X, alternatively, we could try and make the cairo elements transparent)
	caja: If you set a black wallpaper, the text below desktop icons becomes unvisible after reboot or logout and login.
	caja: dng and raw images thumbnails in caja