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

MATE
----
	When panel is at the top, notifications show on top of it. https://dl.dropboxusercontent.com/u/54450962/%ED%99%94%EB%A9%B4-5.png