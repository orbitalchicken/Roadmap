New bug reports in Linux Mint 18 BETA

All editions
------------

	Update translations
	Could you update virtualbox-guest packages from Debian sid repo (5.0.2 versions) for solving 3D acceleration.
	update mint-mirrors
	pix: Doesn't seem to generate thumbnails until view is scrolled
	[Fixed in git] xed: in gedit, and in pluma, you can select text and move it by dragging it with the mouse. That doesn't work in xed.
	boot time: remove samba (make sure NetworkManager-wait-online.service is inactive by default)
	mdm:
		[Fixed in git] wait for plymouth-quit
		[Fixed in git] don't conflict with getty@tty0
		support pam_kwallet5
		set XDG_RUNTIME_DIR http://bazaar.launchpad.net/~lightdm-team/lightdm/trunk/revision/2272
		login screen, no user selected, username don't show up very well on some of the backgrounds
	hardware:
		Ethernet:
			Ethernet - no connection - Realtek Semiconductor Co., Ltd. RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller (rev 0c)
		Wifi:
			Atheros wifi firmware did not load for install on Acer laptop. lspci = 03:00.0 Network controller: Qualcomm Atheros Device 0042 (rev 30) The fix is as follows: wget http://mirrors.kernel.org/ubuntu/pool/main/l/linux-firmware/linux-firmware_1.158_all.deb sudo dpkg -i linux-firmware_1.158_all.deb
			ath10k WiFi doesn’t work. 4.5 kernel needed (https://bugs.launchpad.net/ubuntu/+source/linux-firmware/+bug/1520343)
			Does not support Netgear A6210 wifi adapter.
			Surface 4 Pro: Wlan not working -&gt; tries to connect but with no success. Asking for Passprase again and again. USB Wlan Dongle works
			WIFI issues with RTL8191SU (Rosewill-Wireless Lan-USB 2.0 Adapter-Model No. RNX-N180UBE)-(LSUSB-Bus 005 Device 003: ID 0bda:8172 Realtek Semiconductor Corp. RTL8191SU 802.11n WLAN Adapter)
			Intel Dual Band Wireless-AC 7265: unsupported splx structure
			3c:00.0 Network controller: Qualcomm Atheros QCA6174 802.11ac Wireless Network Adapter (rev 32), "wireless unavailable"
		Bluetooth:
			Am testing on a lenovo w530. Bluetooth applet cant seem to pick any device. It will just display searching for devices and either provide an empty list or list devices i cannot setup. On 17.3 it worked like a charm
		Laptop is Alienware 13′ with Skylake CPU -> touchscreen isn't working
			Laptop is Alienware 13′ with Skylake CPU -> wifi is not working
		Boot:
			Intel Corporation Haswell-ULT Integrated Graphics Controller --> can't boot without recovery mode
			Dell Inspiron 15  i7-6700HQ Processor 6th Generation Intel Core (Skylake) 16 GB memory 128 GB SSD + 1TB HDD -> boots to black screen
			soft lookup cpu3 stuck for 22s, laptop is PE60 6QE, cpu is i7-6700HQ, vga card is Nvidia GTX 960M 2G (all worked fine in 17.3) (works with (acpi=off))
		Suspend:
			Lenovo G50 80, core i5 broadwell, 2.2 ghz, GPU AMD Radeon 2GB, 500GB SSHD and 12GB of RAM. -> can't suspend -> black screen and never wakes up.
		Touchscreen/touchpad:
			Surface 4 Pro: Touchscreen/pen not working
			Surface 4 Pro: Type Cover and Touchpad not working properly. Works from time to time. If I unplug the cover, both doesen't work any more.
		Sound:
			Lenovo Y700 no sound
			Onboard audio for an Intel DQ965GF motherboard is not working.
			No sound (worked in 17.3): Audio: Card-1 Intel 8 Series/C220 Series High Definition Audio Controller, driver: snd_hda_intel bus-ID: 00:1b.0 Sound: Advanced Linux Sound Architecture v: k4.4.0-24-generic
			My mic is not working. Lenovo C-440
		Other:
			ASRock skylake gpe6F bug: /var/log/syslog and var/log/kern.log are flooded with hundreds of gpe6F errors per second until the root partition runs out of space. Its a known issue with ASRock skylake boards. The workaround is o add [code] echo “disable” > /sys/firmware/acpi/interrupts/gpe6F [/code] to rc.local. more info at https://forums.linuxmint.com/viewtopic.php?f=49&t=223180
			HP LaserJet 5000 on parallel port – Device URI: parallel:/dev/lp0 Buffer overflow error when printing. hpcups 3.16.3. Works in Mint 13 and 15, but not in 17.x/18.
			Fatal resolution problem with all 16.04 derivatives https://answers.launchpad.net/ubuntu/+question/292402
		intel:
			mouse cursor disappears (switch user with mdmflexiserver, log back in) https://bugs.launchpad.net/ubuntu/+source/xserver-xorg-video-intel/+bug/1568604, "gsettings set org.gnome.settings-daemon.plugins.cursor active false" helps??
	artwork:
		mint-x: The xed editor has the icons in grey using the Mint-X icons so you don’t know if they are disabled or what

Cinnamon Edition - last processed comment: #676
-----------------------------------------------


MATE Edition - last processed comment: #356
-------------------------------------------
	network-manager | nm-applet:
		After I resume from suspend NetworkManager seems to work fine, Wifi connection is maintained, but nm-applet shows Wi-Fi Networks and other things grayed out. Running ‘pkill nm-applet’ and then ‘nm-applet’ fixes this.
		Can't join WPA network (password not being passed), 3 people have this problem
		after updates nm-applet shows ethernet icon instead of wifi for connections?
		nm connecting via WPA doesn't connect (no password passed).. using network connections to save the password -> works. Tested with MATE edition on a Lenovo Yoga 500.
		Another NetworkManager bug. Just tried to run the mint 18 MATE live on an old pc in my home and it wouldn’t recognize my Wi-Fi at all. It just looked as if I didn’t have Wi-Fi. Killing and restarting nm-applet didn’t help in this case, so the bug must be deeper. Sadly, this is a bug I’ve read about in Ubuntu MATE 16.04 so again, this might be a bug from upstream. For comparison, I had no problem of this sort when running mint cinnamon 18 live on this pc, and it is running mint Xfce (first 17.2, upgraded to 17.3) for a while and never had this problem.
	very frequent “at-spi-registryd.desktop not responding” error at reboot/shutdown and it’s associated very slow reboot/shutdown

KDE Edition - last processed comment: #0
-----------------------------------------

Xfce Edition - last processed comment: #0
------------------------------------------
