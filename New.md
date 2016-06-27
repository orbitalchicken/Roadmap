New bug reports in Linux Mint 18 BETA

All editions
------------

	[done] wifi: Qualcomm Atheros Device 0042 (rev 30) --> fixed by linux-firmware 1.157.1
	[done] upgrade to nm 1.2
	[done] update live repo and sign, with latest FF at time of release.

	rel notes:
		ASRock skylake gpe6F bug: /var/log/syslog and var/log/kern.log are flooded with hundreds of gpe6F errors per second until the root partition runs out of space. Its a known issue with ASRock skylake boards. The workaround is o add [code] echo “disable” > /sys/firmware/acpi/interrupts/gpe6F [/code] to rc.local. more info at https://forums.linuxmint.com/viewtopic.php?f=49&t=223180
		hardware issues -> use Mint 17 until they're ironed out
		add info on "apt download mint-meta-codecs"
		intel uxa (tearing and mouse cursor)
		pavucontrol for sound and input

Cinnamon Edition - last processed comment: #789
-----------------------------------------------
	nemo: Prefs > Display > Icon Caption > first option SIZE, and Prefs > Preview > Folders > options NEVER ---> results in "–" showing under directories (tested in icon view).

MATE Edition - last processed comment: #440
-------------------------------------------

KDE Edition - last processed comment: #0
-----------------------------------------
	mdm:
		support pam_kwallet5
		set XDG_RUNTIME_DIR http://bazaar.launchpad.net/~lightdm-team/lightdm/trunk/revision/2272

Xfce Edition - last processed comment: #0
------------------------------------------
