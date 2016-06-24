New bug reports in Linux Mint 18 BETA

All editions
------------

	Update translations
	Could you update virtualbox-guest packages from Debian sid repo (5.0.2 versions) for solving 3D acceleration.
	update mint-mirrors
	pix: Doesn't seem to generate thumbnails until view is scrolled
	[Fixed in git] xed: in gedit, and in pluma, you can select text and move it by dragging it with the mouse. That doesn't work in xed.
	network-manager 1.9:
		After I resume from suspend NetworkManager seems to work fine, Wifi connection is maintained, but nm-applet shows Wi-Fi Networks and other things grayed out. Running ‘pkill nm-applet’ and then ‘nm-applet’ fixes this.
		Can't join WPA network (password not being passed), 3 people have this problem
		nm-applet shows ethernet icon instead of wifi for connections?
		nm connecting via WPA doesn't connect (no password passed).. using network connections to save the password -> works. Tested with MATE edition on a Lenovo Yoga 500.
		Intel Dual Band Wireless-AC 7265: unsupported splx structure --> fixed by network-manager 1.2
			progress on moving NM to 1.2.0:
				http://packages.ubuntu.com/search?suite=xenial&arch=any&searchon=sourcenames&keywords=network-manager
				http://packages.ubuntu.com/search?suite=xenial-updates&arch=any&searchon=sourcenames&keywords=network-manager
	mdm:
		[Fixed in git] wait for plymouth-quit
		[Fixed in git] don't conflict with getty@tty0
		support pam_kwallet5
		set XDG_RUNTIME_DIR http://bazaar.launchpad.net/~lightdm-team/lightdm/trunk/revision/2272
		login screen, no user selected, username don't show up very well on some of the backgrounds
	hardware:
		Wifi:
			Qualcomm Atheros Device 0042 (rev 30) --> fixed by linux-firmware 1.157.1
		Boot:
			Intel Corporation Haswell-ULT Integrated Graphics Controller --> can't boot without recovery mode
			Dell Inspiron 15  i7-6700HQ Processor 6th Generation Intel Core (Skylake) 16 GB memory 128 GB SSD + 1TB HDD -> boots to black screen
			soft lookup cpu3 stuck for 22s, laptop is PE60 6QE, cpu is i7-6700HQ, vga card is Nvidia GTX 960M 2G (all worked fine in 17.3) (works with (acpi=off))
		Suspend:
			Lenovo G50 80, core i5 broadwell, 2.2 ghz, GPU AMD Radeon 2GB, 500GB SSHD and 12GB of RAM. -> can't suspend -> black screen and never wakes up.
		Other:
			ASRock skylake gpe6F bug: /var/log/syslog and var/log/kern.log are flooded with hundreds of gpe6F errors per second until the root partition runs out of space. Its a known issue with ASRock skylake boards. The workaround is o add [code] echo “disable” > /sys/firmware/acpi/interrupts/gpe6F [/code] to rc.local. more info at https://forums.linuxmint.com/viewtopic.php?f=49&t=223180
			HP LaserJet 5000 on parallel port – Device URI: parallel:/dev/lp0 Buffer overflow error when printing. hpcups 3.16.3. Works in Mint 13 and 15, but not in 17.x/18.
		intel:
			mouse cursor disappears (switch user with mdmflexiserver, log back in) https://bugs.launchpad.net/ubuntu/+source/xserver-xorg-video-intel/+bug/1568604, "gsettings set org.gnome.settings-daemon.plugins.cursor active false" helps??
	artwork:
		mint-x: The xed editor has the icons in grey using the Mint-X icons so you don’t know if they are disabled or what

Cinnamon Edition - last processed comment: #676
-----------------------------------------------


MATE Edition - last processed comment: #356
-------------------------------------------
	very frequent “at-spi-registryd.desktop not responding” error at reboot/shutdown and it’s associated very slow reboot/shutdown

KDE Edition - last processed comment: #0
-----------------------------------------

Xfce Edition - last processed comment: #0
------------------------------------------
