Confirmed issues

System
------		
	[Major] upgrade notes: Explain how to remove priority 700 for PPA
	[Major] Update all translations
	[Major] mdm: nvidia-319 installed, login works fine. Log out and different user logs in --> blank screen with a mouse pointer. Switch users works ok.
	[Major] mintdesktop/mintsystem: port mintfortune to filesystem flag and away from gsettings
	[Medium] apturl/firefox: apturl missing support in Firefox
	[Medium] Shutdown sequence in live-session is all black	
	[Medium] libdvdcss2: DVD Playback doesn't work with new gstreamer: The stream is in the wrong format (using Totem).. works with VLC	
	[Minor] cinnamon: inserting an Audio CD suggests Brasero and VLC, not Banshee		
	[Minor] banshee: tries to rip a CD to FLAC by default       

Mint Tools
----------		
	[Minor] mintstick: progress bar isn't fixed yet	

Cinnamon
--------	
	[Major] tooltips in Cinnamon settings “jump” from left top corner of screen (created there and then moved to the right place)
	[Major] nemo: could not install nemo-dropbox. downloads, displays “100%”, hangs. I was able to install dropbox from dropbox.com	
	[Major] muffin: delete file on desktop, confirmation dialog doesn't show in middle of the primary screen, but in middle of the workspace (i.e. if you have two screens, it shows on the right hand side of the left screen)
	[Major] cinnamon: sometimes icons change from default Mint icons to some other (maybe some fallback icons?)	
	[Medium] Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)		
    [Medium] Changing Wallpaper sometimes freezes cinnamon
    [Minor] The mint logo is a bitmap(png) and is blurry when the panel is resized, it should be svg
	[Minor] Moving applets in cinnamon panel edit mode on, glitches out systray icons when it is shifted	
	[Minor] "Send by email" is showing when right clicking Computer, Home, Trash or removable drives icons on Desktop (also another really minor issue is that “Send by email” and “Format” should have “…” on the end)
	[Minor] I miss the working WIN+D keyboard shortcut to go to desktop.
	[Minor] remove certifications from spices
	[Minor] cinnamon menu doesn't listen to menu changes outside /usr/share/applications? install shotwell for instance (uses /usr/share/menu)	
	[Minor] mint-x (metacity): 1 px frame around windows prevents the rightmost pixel of the right scroll bar from being clickable. Open nemo full screen, with Adwaita you can throw your mouse to the right edge of the screen and start scrolling, with mint-x you need to move 1px left

MATE
----			
	[Medium] mintmenu: category didn't appear (M64), did when clicked "Reload plugins"	
	[Medium] mintmenu: pull requests
	[Minor] mintmenu: show duplicates when item is in multiple categories (LibreOffice, gnome-disks)	

KDE
---
	rel_notes: Add samba-mounter to new features page for KDE
	ubiquity: clicking on "Release notes" link opens an error dialog saying "can't launch Firefox"
	mintstick KDE action shows also for DVD and floppy disks

Xfce
----
	VLC missing             
