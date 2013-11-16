Fixed Issues since Mint 16 RC
======================

All editions
------------

Cinnamon Edition
----------------

MATE Edition
------------

Confirmed Issues
=============

System
------	
	apturl/firefox: apturl missing support in Firefox
	Shutdown sequence in live-session is all black	
	cinnamon: inserting an Audio CD suggests Brasero and VLC, not Banshee
	libdvdcss2: DVD Playback doesn't work with new gstreamer: The stream is in the wrong format (using Totem).. works with VLC	
	mint4win: can't find CD (using autorun)
	mint4win: shows version 14 instead of 16	
	banshee: tries to rip a CD to FLAC by default
	mintdesktop/mintsystem: port mintfortune to filesystem flag and away from gsettings
    brasero: Brasero Wont open after burning a disk

Mint Tools
----------		
	mintstick: progress bar isn't fixed yet		
	mintdrivers: doesn't apply ATI icon to "Advanced Micro Devices, Inc. [AMD/ATI]: Wrestler [Radeon HD 6290]"

Cinnamon
--------	
	nemo: Use sudo/gksu/gksudo to "open as root" instead of pkexec? to work around the XDG_RUNTIME_DIR bug?
	User applet: name/pic are centered, should be left-aligned (shows with small gecos)
	Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)		
	Calendar applet should link to "cinnamon-settings calendar"
    Changing default applications does nothing
    When a maximized window is minimized, and you activate the hot corner or expo, it makes a split second glitch view of that window
    The mint logo is a bitmap(png) and is blurry when the panel is resized, it should be svg
    Mounted disks shouldest show by default one the desktop?
    Cannot Middle click most toolbar items in Nemo    
    Copying large files (< 200mb), nemo reports 99% the whole time.
    Changing Wallpaper sometimes freezes cinnamon
	Moving applets in cinnamon panel edit mode on, glitches out systray icons when it is shifted    
	mint-themes-gtk3: nemo sidebar buttons are too large
	
MATE
----		
	mate: Use generic names in MATE packages	
	mintmenu: category didn't appear (M64), did when clicked "Reload plugins"	
	mintmenu: show duplicates when item is in multiple categories (LibreOffice, gnome-disks)	
	mintmenu: pull requests		

KDE
---
	rel_notes: Add samba-mounter to new features page for KDE
	ubiquity: clicking on "Release notes" link opens an error dialog saying "can't launch Firefox"
	mintstick KDE action shows also for DVD and floppy disks

Xfce
----
	VLC missing             

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

New Bug Reports
=============

All editions
-------------
	there’s no “United States” setting available in “Cinnamon Settings/Regional Settings” under the “Format” tab and it can’t be added via the “+” button
- Nvidia drivers dont automaticaly install nvidia-settings (Tested with nvidia-319 and nvidi-319-updates)
- Banshee will segfault after playing ~30 mp3 songs


Cinnamon Edition - 
----------------
- Cinnamon Settings is advanced mode by default always
- cinnamon-desktop-editor Choose an icon dialog does not have image previews
- Having links of files/folders on desktop from another hardrive at startup, then mounting the drive will usually crash then restart Cinnamon

MATE Edition
------------


Triaged Reports
============

Not a bug 
---------
- Git is not installed by default

Outside of the scope
--------------------

- Magnet links for torrents are not working in Firefox

Not enough info
---------------

- On/Off switch for networking applet is visually glitchy

Upstream won't fix
------------------



MATE Edition
------------
