
Infra	
-----
	Add Petra rel notes
	Add Petra new features page
	rel_notes point to rel_petra_cinnamon.php
	rel_notes explain about apt recommends

System
------	
	apturl missing support in Firefox

Mint Tools
----------
	[Fixed] mintInstall improvements
	mintStick progress bar isn't fixed yet
	mintmenu show duplicates when item is in multiple categories (LibreOffice, gnome-disks)	

Look and Feel
-------------
	cinnamon-mint-x-theme: Check latest pull request from Bernard
	cinnamon-mint-x-theme: User applet shows username/gecos in white

Cinnamon
--------		
	Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)	
	
MATE
----	
	Use generic names in MATE packages
	x-caja-desktop windows bug at session start --> try to apply patch: https://github.com/clefebvre/caja/commit/e916c945e86842b63e17c322b76ab47e1538c233

KDE
---
	Add samba-mounter to new features page for KDE
	Ubiquity, clicking on "Release notes" link opens an error dialog saying "can't launch Firefox"
	Ubiquity shows "update installer"

Feedback from Corbin
--------------------
    Installing Nvidia drivers makes tty and boot screen lo-res (http://www.conanblog.me/it/how-to-get-the-high-resolution-for-tty-back-after-nvidia-driver-update-in-ubuntu/)    
    Brasero Wont open after burning a disk
    In Spices the "Updates Available!" button is visually glitchy
    Moving applets in cinnamon panel edit mode on, glitches out systray icons when it is shifted
    Cinnamon Settings start in advanced mode on fresh install even if not in admin mode
    Cannot Middle click most toolbar items in Nemo
    User Applet is visually off in MintX Cinnamon theme
    Changing Wallpaper somtimes freezes cinnamon
    Calender Applet should link to "cinnamon-settings calendar"
    When a maximized window is minimized, and you activate the hot corner or expo, it makes a split second glitch view of that window
    The mint logo is a bitmap(png) and is blurry when the panel is resized, it should be svg
    Mounted disks shouldest show by default one the desktop?
    In Applets/Desklet config, the more actions button icon makes no sense, should be cog
    Volume change sound is terribly high pitched, it should be the bubble sound
    LibreOffice Loading bar is orange
    Rename file/folder field can be hard to read in some cases, eg. the desktop
    Changing default applications does nothing
    Copying large files (< 200mb), nemo reports 99% the whole time.    
    gnome-disk-utility 3.8.2 is fugly

De-scoped
---------		
	Cinnamon: Launching keepass + xsel freezes Cinnamon [wrouesnel] (unknown cause/solution)	
	GTK3: dialogs use symbolic icons (offending code is in GTK3, won't fix. Small issue but linked to GTK3 becoming a GNOME Shell specific toolkit.)
	GTK3: No padding in context menu leads to accidental operations (bug reported upstream in GTK3, temp workaround/fix unlikely/tedious)
	GNOME: gnome-calculator menubar (minor cosmestic issue, won't fix)
	System: gksu covers cinnamon panel and clutter layer (offending code is in libgksu, won't fix, likely to migrate to pkexec instead)
	System: Support for Wacom tablet (configurable via the command line, will need to join forces with Xfce/MATE if we want to develop a cross DE UI. This doesn't justify pulling resources to make a Cinnamon specific solution)	
	System: EFI booth path isn't standard (EFI installation in Virtualbox works fine, but upon reboot it loses its NVRAM and isn't able to find the EFI boot files)
	MDM: l10n doesn't cover new features (MDM 1.4 is still using the l10n it inherited from GDM. Decision was taken to migrate MDM entirely to Mint/LP translations in 1.6, not just mdmwebkit/mdmsetup).
	MP3 online doesn't work (known limitation with totem)
