Fixed Issues since Linux Mint 17.2 RC

All editions
------------
	mintsources: New PPA archive package browsing. You don’t see if a package is already installed. Checkbox is always empty if you reopen the package list. No error when you install “again”.
	mintsources: PPA package list should be modal. One wrong click and the window is behind the non responding sources window.
	mintsources: Installed ppa:danielrichter2007/grub-customizer, then installed grub-customizer directly from the package list (works). Unabled PPA, downgrade foreign packages -> nothing to select from. Uninstalled PPA, refreshed APT cache -> still nothing to select from in downgrade foreign packages. Of course I can uninstall grub-customizer the old fashioned ways.
	NVIDIA 346 drivers backported
	MDM lets users switch NVIDIA Prime GPU via logout (as opposed to reboot)
	nvidia-prime systray support
	mintupdate: up-to-date screen hides otherwise visible, yet not-recommended, updates
	mintupdate: don't show level 4/5 updates by default (security or not)
	mintupdate: for visible levels, when security updates are set to non-visible but safe, they are not selected
	Improved EFI support (particularly on ASUS laptop) by upgrading grub
	MDM slideshow, don't show bright colors there
	MDM slideshow, black background
	mint-X: add grey variation
	mint-x: sharper window controls
	updated translations
	32-bit isolinux linux is one line short (have to scroll to see Boot from Hard Drive)

Cinnamon Edition
----------------
	dual monitors full screen issue: https://github.com/linuxmint/Cinnamon/issues/4215
	little issue with Settings stacks: https://github.com/linuxmint/cinnamon-control-center/issues/120
	keyboard applet: when flag doesn't exist.. latam for instance
	fixed cinnamon-settings-daemon crashing with some NVIDIA cards
	two-edge scrolling regression
	libgtkmm-2.4-1c2a is missing post-install, causing invisible menu options in VMware and custom themes.

MATE Edition
------------
	compiz decorations now work in Virtualbox.
	atril, mate-dict and mate-color-selector should go in Accessories
	epub support in atril
	mate-terminal: transparency in default profile
	mint-x: metacity-2 support

KDE Edition
-----------
	Fixed search not working in Dolphin

Xfce Edition
------------
	QT apps don't use GTK theme theme.. compile xfce4-session with legacy support
	keyboard shortcuts: adding a new command for an exiting keybinding works, removing it works as well.. but the command doesn't disappear from the settings window
	“search” contextual menu item doesn’t show the search box when you right-clic on file or folder
