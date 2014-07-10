
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
	mint-mirrors: update list of mirrors
	modemmanager hangs at shutdown
	rel notes: no network after suspending? https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1286552	
	cinnamon 2.2.14, muffin 2.2.6, cinnamon-session 2.2.2, cinnamon-control-center 2.2.10, nemo 2.2.3
	patch for MATE: https://github.com/linuxmint/mate-packages/pull/4
	upgrade inxi to 2.1.28
	upgrade xfce4-whiskermenu-plugin to 1.4.0?


Cinnamon
--------		
	"Add to %s" for [desktop, panel, etc..] isn't translatable in some languages

KDE
---	
	mdm: When loging in an existing session, doesn't unlock kde screensaver
	mintBackup works in Qiana but a backport is needed in Petra https://bugs.launchpad.net/linuxmint/+bug/1261693	
	
Xfce
----
	mdm: When loging in an existing session, doesn't unlock xscreensaver	



Next Release
------------
	Consider adding pipelight
	Consider porting cinnamon-bluetooth into gnome-bluetooth-frontend, for use in MATE and Xfce
	port mintmenu to gtk3
	mintinstall: should show licenses
	mintinstall: should separate impacts between installs and removals
	mate: make compiz work out of the box?
	ubiquity: https://bugs.launchpad.net/linuxmint/+bug/1325786
	mintupdate: give kernel page a real table
	oem: rephrase isolinux/grub option --> s/Start Linux Mint/Preinstall Linux Mint/g
	artwork: provide mint-x in a variation of colors
	cinnamon: actual screensaver?
	cinnamon: flickr wallpapers, wallch features etc..
	cinnamon: all cs icons in mint-x icon theme
	cinnamon: 3 finger touchpad support
	cinnamon: frequency in monitor settings
	cinnamon: improve network settings, applet
	cinnamon: search providers
	cinnamon: fade-in at startup
	cinnamon: ibus support
	xfce: revive xfapplet
	xfce: Many config-type things in the menu are missing from xfce4-settings-manager. Examples are mdmsetup; Languages; and ‘Users and groups’.
	xfce: Menu doesn’t update automatically to include KDE applications. Installed kate and krusader (most useful file manager ever!)
	hexchat: -help is below -chat
	repository: provide translations or disable them?

LMDE
----
	update synaptic adjustment in mintsystem for lmde
	live-installer: turn avatar selector into a nicer widget ala cinnamon-settings account details
	live-installer: check free space on /target before installing