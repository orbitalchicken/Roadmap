Bugs depending on apps outside of Mint team, many of these are solvables by the team but some others might depend on member of the other projects

Upstream bugs
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
		- mcc->notifications->help button doesn't work
	- Compiz GTK decorator segfaults in Virtualbox
	- kde:
		- problem with CalDAV/CardDAV-Servers… If I create an event in KOrganizer, it only works once and then is broken (no syncing) until I delete the calendar and add it again. Works fine in 17, using tine 2.0 WebDAV-Server - https://forum.kde.org/viewtopic.php?f=261&t=124072
	- whiskermenu:
		- lorsque je veux mettre un programme depuis le menu sur le bureau j’ai droit au popup qui veux que je mette ce raccourci en tant qu’exécutable… Dommage pour les néophyte… --> https://github.com/gottcode/xfce4-whiskermenu-plugin/pull/100
		- Only the items on the right-hand side of the menu can be selected with my keyboard. https://github.com/gottcode/xfce4-whiskermenu-plugin/issues/101
	- QT5: Dropbox icon is not displayed in the panel, but Dropbox daemon loads and functions as usual. I’ve seen this elsewhere, and seen numerous similar complains. I suspect it’s related to the new QT-based Dropbox release. https://www.dropboxforum.com/hc/communities/public/questions/201545695-After-upgrade-to-3-x-the-dropbox-tray-icon-is-missing-XFCE-Xubuntu-14-04-1-x64-?locale=en-us