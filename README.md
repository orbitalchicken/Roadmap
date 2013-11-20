Confirmed issues

System
------		
	upgrade notes: Explain how to remove priority 700 for PPA
	apturl/firefox: apturl missing support in Firefox
	Shutdown sequence in live-session is all black	
	cinnamon: inserting an Audio CD suggests Brasero and VLC, not Banshee
	libdvdcss2: DVD Playback doesn't work with new gstreamer: The stream is in the wrong format (using Totem).. works with VLC	
	mint4win: can't find CD (using autorun)
	mint4win: shows version 14 instead of 16	
	banshee: tries to rip a CD to FLAC by default
	mintdesktop/mintsystem: port mintfortune to filesystem flag and away from gsettings
    brasero: Brasero Wont open after burning a disk
    Update all translations
    mdm: nvidia-319 installed, login works fine. Log out and different user logs in --> blank screen with a mouse pointer. Switch users works ok.

Mint Tools
----------		
	mintstick: progress bar isn't fixed yet		
	mintdrivers: doesn't apply ATI icon to "Advanced Micro Devices, Inc. [AMD/ATI]: Wrestler [Radeon HD 6290]"	

Cinnamon
--------	
	nemo: could not install nemo-dropbox. downloads, displays “100%”, hangs. I was able to install dropbox from dropbox.com	
	muffin: delete file on desktop, confirmation dialog doesn't show in middle of the primary screen, but in middle of the workspace (i.e. if you have two screens, it shows on the right hand side of the left screen)
	cinnamon: sometimes icons change from default Mint icons to some other (maybe some fallback icons?)
	Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)		
    The mint logo is a bitmap(png) and is blurry when the panel is resized, it should be svg
    Mounted disks shouldest show by default one the desktop?
    Cannot Middle click most toolbar items in Nemo    
    Copying large files (< 200mb), nemo reports 99% the whole time.
    Changing Wallpaper sometimes freezes cinnamon
	Moving applets in cinnamon panel edit mode on, glitches out systray icons when it is shifted    
	tooltips in Cinnamon settings “jump” from left top corner of screen (created there and then moved to the right place)
	"Send by email" is showing when right clicking Computer, Home, Trash or removable drives icons on Desktop (also another really minor issue is that “Send by email” and “Format” should have “…” on the end)
	I miss the working WIN+D keyboard shortcut to go to desktop.
	remove certifications from spices
	cinnamon menu doesn't listen to menu changes outside /usr/share/applications? install shotwell for instance (uses /usr/share/menu)	
	mint-x (metacity): 1 px frame around windows prevents the rightmost pixel of the right scroll bar from being clickable. Open nemo full screen, with Adwaita you can throw your mouse to the right edge of the screen and start scrolling, with mint-x you need to move 1px left

MATE
----			
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
