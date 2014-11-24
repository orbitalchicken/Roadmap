Triaged reports

Not a bug
---------
	- settings/backgrounds Consider aligning the dropdown boxes for Gradient and Picture Aspect to each other.
	- If changing the mouse pointer from default white to black (e.g Adwaita), it shows up as white during startup. After login, it changes to black.
	- uim and uim-byeoru combination give us a good process but , uim installs only uim itself , we need key instance to define keys to input language. installing other packages supported by uim category , it install 19 more packages we just need one more package “uim-byeoru” with “uim”

Outside of the scope
--------------------


Can't reproduce
---------------
	- mdm: The login screen always defaults to “Login” rather than the user. In my case I have one user on the system and it should default to that user so I don’t have to continually click on my user to input the password.
	- The wireless signal strength of the networks shown changes constantly and the percentage is almost all the time wrong (weak signal networks are shown with 80+% strength and strong signal ones with low percentage).
	- caja exits (“normally”) on clicking “smb-network”.
	- mate: Audio-preview causes the window in question to freeze, requiring the user to forcibly close it. Just moving the mouse pointer over the audio file is enough to cause it to lock up at times. Happens 25-50% of the time.
	- mate: Movie Player closes without an error message when switching from full-screen. This happens with both audio & video files and whether you double-click on Movie Player or select ‘Leave Fullscreen’. Happens about 50% of the time.

Upstream
--------
	- ubiquity: Selecting Encrypted Home Folder Always Breaks Swap https://bugs.launchpad.net/linuxmint/+bug/1367392
	- caribou: the tray button does not send the keyboard to the tray, otherwise the applet works fine.
	- pidgin: status icon is not showing even if in the settings it’s set to always show.
	- Add some template such as Writer, Calc, Presentation on context R_click (need ability to define system-wide templates for nemo/caja, but we also need them to be translatable..)
	- Could you add nabi as input method to mintlocale? (it needs to be supported by im-config first)
	- gcin couldn’t apply the change of its input method settings, and also the CTRL+SPACE(combine keys that used change bwtween English and Chinese input method) didn’t work well seems these could be fixed by simply update the gcin to ver 2.8.2 --> Please create an issue on github.com/linuxmint/mintlocale. We need directions to reproduce this.
	- mate:
		- alt-mouse wheel desktop zoom
		- Flash video in website doesn't inhibit monitor turning itself off	(https://github.com/mate-desktop/mate-screensaver/issues/57)
		- brightness OSD doesn't work (with Marco) https://github.com/mate-desktop/mate-power-manager/issues/110
		- Movie Player’s screensaver/display-sleep-inhibit feature (still) doesn’t work. When enabled, either the screensaver and/or Powermanager’s display-sleep feature cuts in on queue.
	- Compiz GTK decorator segfaults in Virtualbox
