
Infra	
-----
	Add Petra rel notes
	Add Petra new features page	
	rel_notes explain about apt recommends	
	rel_notes explain systemd regression on pam / XDG_RUNTIME_DIR

System
------	
	apturl missing support in Firefox
	Shutdown sequence in live-session is all black	
	cinnamon: inserting an Audio CD suggests Brasero and VLC, not Banshee
	DVD Playback doesn't work with new gstreamer: The stream is in the wrong format (using Totem).. works with VLC	
	mint4win: can't find CD (using autorun)
	mint4win: shows version 14 instead of 16	
	Banshee tries to rip a CD to FLAC by default
	mintdesktop/mintsystem: port mintfortune to filesystem flag and away from gsettings

To be Fixed prior to RC
-----------------------		
	[Fixed] mdm: can't select another user
	[Fixed] cinnamon: menu and calendar applets, problem parsing file for menu@cinnamon.org while preparing to perform upgrade...
	[Fixed] mate: x-caja-desktop windows bug at session start	
	[Fixed] Menu entries for module names aren't localized (Network, Sound, Displays, Color, Firewall Configuration, Region & Language, Power)
	[Fixed] nemo: create new launcher (and other actions..) isn't l10n'd
	[Fixed] mintinstall uses network and takes time before showing package page	

Mint Tools
----------	
	mintStick progress bar isn't fixed yet
	mintmenu show duplicates when item is in multiple categories (LibreOffice, gnome-disks)	
	mintmenu pull requests	
	[Fixed] mintdesktop: remove mintfortune support
	[Fixed] mintsystem: remove mintfortune support

Look and Feel
-------------	
	[Fixed] mint-x-gtk3: Buttons default and hover effect look a bit glitchy
	[Fixed] mint-x-gtk3: radio-check buttons have outline on selection

Cinnamon
--------		
	Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)		
	
MATE
----	
	Use generic names in MATE packages	
	mintmenu category didn't appear (M64), did when clicked "Reload plugins"	
	use mint logo as mintmenu icon

KDE
---
	Add samba-mounter to new features page for KDE
	Ubiquity, clicking on "Release notes" link opens an error dialog saying "can't launch Firefox"
	Ubiquity shows "update installer"

Xfce
----
	VLC missing

Feedback from Corbin
--------------------
    Installing Nvidia drivers makes tty and boot screen lo-res (http://www.conanblog.me/it/how-to-get-the-high-resolution-for-tty-back-after-nvidia-driver-update-in-ubuntu/)    
    Brasero Wont open after burning a disk
    Cannot Middle click most toolbar items in Nemo    
    Calender Applet should link to "cinnamon-settings calendar"
    When a maximized window is minimized, and you activate the hot corner or expo, it makes a split second glitch view of that window
    The mint logo is a bitmap(png) and is blurry when the panel is resized, it should be svg
    Mounted disks shouldest show by default one the desktop?
    Changing default applications does nothing
    Copying large files (< 200mb), nemo reports 99% the whole time.    

Known Cinnamon bugs
-------------------
	Changing Wallpaper sometimes freezes cinnamon
	Moving applets in cinnamon panel edit mode on, glitches out systray icons when it is shifted

De-scoped
---------	
	System: crashes/freezes	due to /run/user/<uid>/dconf/user being owned by root (upstream bug in systemd, affects all distributions. The decision was taken not to hack XDG_RUNTIME_DIR and not to hack /etc/pam.d.. i.e. bringing back xdg_support.so in replacement to systemd.so as it could create further regressions with systemd)
	Cinnamon: Launching keepass + xsel freezes Cinnamon [wrouesnel] (unknown cause/solution, could be related to XDG_RUNTIME_DIR bug)	
	GTK3: dialogs use symbolic icons (offending code is in GTK3, won't fix. Small issue but linked to GTK3 becoming a GNOME Shell specific toolkit.)
	GTK3: No padding in context menu leads to accidental operations (bug reported upstream in GTK3, temp workaround/fix unlikely/tedious)
	GNOME: gnome-calculator menubar (minor cosmestic issue, won't fix)
	System: gksu covers cinnamon panel and clutter layer (offending code is in libgksu, won't fix, likely to migrate to pkexec instead)
	System: Support for Wacom tablet (configurable via the command line, will need to join forces with Xfce/MATE if we want to develop a cross DE UI. This doesn't justify pulling resources to make a Cinnamon specific solution)	
	System: EFI booth path isn't standard (EFI installation in Virtualbox works fine, but upon reboot it loses its NVRAM and isn't able to find the EFI boot files)
	MDM: l10n doesn't cover new features (MDM 1.4 is still using the l10n it inherited from GDM. Decision was taken to migrate MDM entirely to Mint/LP translations in 1.6, not just mdmwebkit/mdmsetup).
	MP3 online doesn't work (known limitation with totem)
