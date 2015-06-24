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
	Improved EFI support (particularly on ASUS laptop) by upgrading grub

Cinnamon Edition
----------------
	dual monitors full screen issue: https://github.com/linuxmint/Cinnamon/issues/4215
	little issue with Settings stacks: https://github.com/linuxmint/cinnamon-control-center/issues/120
	keyboard applet: when flag doesn't exist.. latam for instance
	fixed cinnamon-settings-daemon crashing with some NVIDIA cards

MATE Edition
------------
	compiz decorations now work in Virtualbox.