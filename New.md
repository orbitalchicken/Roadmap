New bug reports in Linux Mint 18 BETA

All editions
------------
	mdm: Webkit preview, process doesn't die when window is closed
	mdm: Webkit preview, mint-X doesn't show anything, only background

Cinnamon Edition - last processed comment: #789
-----------------------------------------------
	nemo: Prefs > Display > Icon Caption > first option SIZE, and Prefs > Preview > Folders > options NEVER ---> results in "–" showing under directories (tested in icon view).

MATE Edition - last processed comment: #440
-------------------------------------------

Xfce Edition - last processed comment: #63
------------------------------------------
	- Thunar crashes when rename files. bugzilla.xfce.org/show_bug.cgi?id=12264
	- Thunar crahses sometimes when copy and paste files
	- Whisker menu buttons are highlighted bugzilla.xfce.org/show_bug.cgi?id=12402 Rebuild master or apply this commit please git. xfce. org/panel-plugins/xfce4-whiskermenu-plugin/commit/?id=4f732a1b63595aa6745409bd403e0ca098e20dcd
	- Banshee player is unusable (Can’t resize panel elements, window starts to drag). Maybe replace with Clementine or any gtk player.
	- Qt apps Look and feel has become broken again (clementine e. g.). The way to fix it – add env variable DESKTOP_SESSION=gnome . 
	- Xfce4-task-manager toolbar style “Small” looks much better (maybe change default conf)
	- changing clock format makes clock applet disappear (alternative clock available in xfce4-goodies)
	- libindicator-plugin.so uses 10/20% CPU at idle. Removing the applet from the panel --> CPU usage goes down.
	- If you select Compiz as window manager you only get the default (Adwaita) ugly window border, not the active theme gtk border as it should be (for example if the default Mint-X is used as main theme you should also get the window border associated with this theme). You always end up with the Adwaita border regardless of what theme that is selected. This makes windows look weird if Compiz is used as window manager.
	- Nautilus overwrites the desktop with its own settings, removing icons and background and the right click context menu.
	- qt4 apps look wrong (tested with backintime-qt4), you can change it by installing qtconfig-qt4


KDE Edition - last processed comment: #0
-----------------------------------------
	mdm:
		support pam_kwallet5

