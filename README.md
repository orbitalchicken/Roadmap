Confirmed issues

System
------		
	[Major] rel notes: Announce that mint4win is discontinued
	[Major] upgrade notes: Explain how to remove priority 700 for PPA
	[Major] Update all translations		
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
	[Major] muffin: delete file on desktop, confirmation dialog doesn't show in middle of the primary screen, but in middle of the workspace (i.e. if you have two screens, it shows on the right hand side of the left screen)
	[Major] cinnamon: sometimes icons change from default Mint icons to some other (maybe some fallback icons?)	
	[Medium] Clock says 15:38. Go to time settings. Turn off network time. Turn it back on. Wait for 10 seconds or so.. time updates to correct time and says 16:38. (either Cinnamon loses track of ntp when disconnected/reconnected to network, or it fails to use it at login time)		
    [Medium] Changing Wallpaper sometimes freezes cinnamon 	
	[Minor] remove certifications from spices
	[Minor] cinnamon menu doesn't listen to menu changes outside /usr/share/applications? install shotwell for instance (uses /usr/share/menu)	
	[Major] gtk: tooltips in Cinnamon settings “jump” from left top corner of screen (created there and then moved to the right place)	
	[Minor] gtk: dialogs use symbolic icons (offending code is in GTK3, won't fix. Small issue but linked to GTK3 becoming a GNOME Shell specific toolkit.)
	[Minor] gtk: No padding in context menu leads to accidental operations (bug reported upstream in GTK3, temp workaround/fix unlikely/tedious)
	[Minor] gtk: noDisplay=true desktop entries don't appear in MIME lists

MATE
----			
	[Medium] mintmenu: category didn't appear (M64), did when clicked "Reload plugins"	
	[Medium] mintmenu: pull requests
	[Minor] mintmenu: show duplicates when item is in multiple categories (LibreOffice, gnome-disks)	

KDE
---
	rel_notes: Add samba-mounter to new features page for KDE
	[Fixed] ubiquity: clicking on "Release notes" link opens an error dialog saying "can't launch Firefox"
	[Fixed] mintstick KDE action shows also for DVD and floppy disks

Xfce
----
	VLC missing             
