New bug reports in Linux Mint 18 BETA

All editions
------------

	*update translations
	*update mint-mirrors
	*[Fixed in git] xed: in gedit, and in pluma, you can select text and move it by dragging it with the mouse. That doesn't work in xed.
	*[Fixed in git] xplayer: inhibits on video but not on audio? (although it is selected to do so for “Video or Audio” and “org.x.player lock-screensaver-on-audio true” is set).
	*[Fixed in git] xviewer-plugins: couldn't load resource /org/x/viewer/plugins/exif-display/exif-display-config.ui (EXIF plugin)
	*mdm:
		[Fixed in git] wait for plymouth-quit
		[Fixed in git] don't conflict with getty@tty0
		support pam_kwallet5
		set XDG_RUNTIME_DIR http://bazaar.launchpad.net/~lightdm-team/lightdm/trunk/revision/2272
		login screen, no user selected, username don't show up very well on some of the backgrounds
	*wifi: Qualcomm Atheros Device 0042 (rev 30) --> fixed by linux-firmware 1.157.1
	update virtualbox-guest to Debian sid 5.0.2 to solve 3D acceleration?
	pix: Doesn't seem to generate thumbnails until view is scrolled

	rel notes:
		ASRock skylake gpe6F bug: /var/log/syslog and var/log/kern.log are flooded with hundreds of gpe6F errors per second until the root partition runs out of space. Its a known issue with ASRock skylake boards. The workaround is o add [code] echo “disable” > /sys/firmware/acpi/interrupts/gpe6F [/code] to rc.local. more info at https://forums.linuxmint.com/viewtopic.php?f=49&t=223180
		hardware issues -> use Mint 17 until they're ironed out
		add info on "apt download mint-meta-codecs"

	network-manager 1.9:
		After I resume from suspend NetworkManager seems to work fine, Wifi connection is maintained, but nm-applet shows Wi-Fi Networks and other things grayed out. Running ‘pkill nm-applet’ and then ‘nm-applet’ fixes this.
		Can't join WPA network (password not being passed), 3 people have this problem
		nm-applet shows ethernet icon instead of wifi for connections?
		nm connecting via WPA doesn't connect (no password passed).. using network connections to save the password -> works. Tested with MATE edition on a Lenovo Yoga 500.
		Intel Dual Band Wireless-AC 7265: unsupported splx structure --> fixed by network-manager 1.2
			progress on moving NM to 1.2.0:
				http://packages.ubuntu.com/search?suite=xenial&arch=any&searchon=sourcenames&keywords=network-manager
				http://packages.ubuntu.com/search?suite=xenial-updates&arch=any&searchon=sourcenames&keywords=network-manager

	artwork:
		mint-x/mint-y: buttons aren't themed in gelemental
		mint-x: The xed editor has the icons in grey using the Mint-X icons so you don’t know if they are disabled or what

Cinnamon Edition - last processed comment: #733
-----------------------------------------------
	nemo: Prefs > Display > Icon Caption > first option SIZE, and Prefs > Preview > Folders > options NEVER ---> results in "–" showing under directories (tested in icon view).

MATE Edition - last processed comment: #401
-------------------------------------------

KDE Edition - last processed comment: #0
-----------------------------------------

Xfce Edition - last processed comment: #0
------------------------------------------
