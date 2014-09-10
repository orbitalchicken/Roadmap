
Backports
---------
	x-caja-desktop fix for Maya

Investigating
-------------
	Cinnamon freezing sometimes when using meld
	Cinnamon freezing on background change
	mdm login resulting in black screen when gnome-keyring gets locked? https://github.com/linuxmint/mdm/issues/92

Maintenance
-----------
	Update tapatalk API on forums
	pkgs: unity-greeter pkg
	pkgs: gedit-plugins pkg https://bugs.launchpad.net/linuxmint/+bug/1186528
	modemmanager hangs at shutdown
	rel notes: no network after suspending? https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1286552	
	patch for MATE: https://github.com/linuxmint/mate-packages/pull/4
	upgrade inxi to 2.1.28
	upgrade xfce4-whiskermenu-plugin to 1.4.0?

Cinnamon
--------
	"Add to %s" for [desktop, panel, etc..] isn't translatable in some languages
	open with dialog does not set as default anymore. went to set an mp3 to open with vlc/banshee/clementine, click ‘set as default’, and the highlighted list item focus just jumps back to Videos under the Default Application header.
	play around with the fonts in cinnamon sooner or later (usually sooner) the desktop crashes.
	play around with the slider for panel size using the cursor keys for up and down making it bigger or smaller then sooner or later, usually quite quickly the whole desktop freezes.

KDE
---
	mdm: When loging in an existing session, doesn't unlock kde screensaver

Xfce
----
	mdm: When loging in an existing session, doesn't unlock xscreensaver

Next Release
------------		
	mintupdate: when Update Manager has done it’s job successfully, the disk stops rumbling and the window just vanishes… it looks like it crashed. A pop-up ‘Your System Is Now Up To Date’ for ten seconds would be nice.	
	Consider adding pipelight
	Consider porting cinnamon-bluetooth into gnome-bluetooth-frontend, for use in MATE and Xfce
	port mintmenu to gtk3
	mintinstall: should show licenses
	mintinstall: should separate impacts between installs and removals
	mate: make compiz work out of the box?
	ubiquity: https://bugs.launchpad.net/linuxmint/+bug/1325786	
	oem: rephrase isolinux/grub option --> s/Start Linux Mint/Preinstall Linux Mint/g
	artwork: provide mint-x in a variation of colors
	cinnamon: actual screensaver?
	cinnamon: flickr wallpapers, wallch features etc..	
	cinnamon: frequency in monitor settings
	cinnamon: improve network settings, applet
	cinnamon: search providers
	cinnamon: fade-in at startup, loading strings (ala Don't Starve) before session comes up?
	cinnamon: ibus support
	cinnamon: integrate workspace management in nemo, panel, window-list, applet, muffin, settings	
	cinnamon: world clock http://cinnamon-spices.linuxmint.com/applets/view/108
	xfce: revive xfapplet
	xfce: Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
	xfce: Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!)
	xfce: switch datetime applet to Clock applet
	hexchat: -help is below -chat
	mintstick: Add % completion to window title
	try fonts-noto
	see if we can make life easier for people using nonPAE kernels (live/boot args, and take kernel updates into account)
	mintsystem: add APT priority definitions for known PPAs and repositories
	mdm: new theme based on mdm-modern, with slideshow
	mdm: add a preview button to theme selection
	mintsystem: make "apt download" download dependencies to the ./pkgname directory
	user guide -> consider using LP/docbook/LaTeX
	nemo-emblems: translations
	hexchat: implement PR for /etc/hexchat for distro to set default list of networks https://github.com/hexchat/hexchat; http://anonscm.debian.org/cgit/collab-maint/hexchat.git/ (sney mailto:drubo@drubo.net)
	fonts: Would Linux Mint mind changing the default CJK font in the future release?like Adobe’s source han sans. As a Traditional Chinese user, the default font Linux Mint now using is pretty awkward, and even didn’t follow the hand writing rules and education standard. The fedora team changed their default font to Adobe”s source han sans and it’s great.
	live-installer: when no translation is found, we should revert to en_US, not default
	gtk: patch menu key cinnamon screensaver: https://bugs.launchpad.net/ubuntu/+source/gtk+3.0/+bug/1366790
	gtk: memory leak? https://bugzilla.gnome.org/show_bug.cgi?id=729670
	cinnamon: systray patch http://dpaste.com/1H2T699
	set up Rebecca	

	done:
		mintupdate: 
			kernel page redesign
			package descriptions are now complete and l10n'd
			proxy support in changelog retrieval: https://bugs.launchpad.net/linuxmint/+bug/1335116	
		mintsources:
			better repository names
			test mirrors in parallel
		cinnamon
			cjs rebase
			nemo emblem support
			nemo folder-color
			3 finger touchpad support
			all cs icons in mint-x icon theme
			multiple panel launchers
			remove logout countdown
			nemo toolbar UI changes
		mate
			folder-color
		mint-x
			blue, grey icon theme

LMDE
----
	update virtualbox
	update synaptic adjustment in mintsystem for lmde
	live-installer: turn avatar selector into a nicer widget ala cinnamon-settings account details
	live-installer: check free space on /target before installing
	mintsystem creates an order cycle when booting with systemd
	jessie: patch gtk3.12 http://redmine.audacious-media-player.org/boards/1/topics/1135