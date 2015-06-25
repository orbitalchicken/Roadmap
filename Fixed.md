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

Cinnamon Edition
----------------
	dual monitors full screen issue: https://github.com/linuxmint/Cinnamon/issues/4215
	little issue with Settings stacks: https://github.com/linuxmint/cinnamon-control-center/issues/120
	keyboard applet: when flag doesn't exist.. latam for instance
	fixed cinnamon-settings-daemon crashing with some NVIDIA cards
	two-edge scrolling regression

MATE Edition
------------
	compiz decorations now work in Virtualbox.
	atril, mate-dict and mate-color-selector should go in Accessories
	epub support in atril
	mate-terminal: transparency in default profile
