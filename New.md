New bug reports in Linux Mint 19.1 BETA

All editions
------------

mintdriver:
	After a standard install, I ran Driver Manager and chose to change from the default nouveau driver to the nvidia-590 driver. Rebooted and all good.
    I then switched back to the nouveau driver, and rebooted.
    When I now go into Driver Manager, it says I have manually installed a driver and it will not allow me to select either the nouveau or nvidia-590 driver.
    Screenshot: https://imgur.com/7EqM6M3

ubiquity:
	GRUB TIME OUT isn't set properly
	kabyle
	fcitx recommends

xapps don't react consistently to ctrl+q and ctrl+w

Cinnamon Edition
----------------

Booting from USB stick take pause for 10-30 seconds with no USB mouse light and no light on USB stick then light up boot continue. Pause for USB ports reset ?

nemo:
	- When I right click on the desktop and select ‘Customize’, my icons are automatically resorted.

gwl: Enable "application name" label. Open FF, open at least two browser tabs. Close FF. The label slides over the icon and doesn't disappear: https://kepkuldes.com/image/UoNHl

mounted volume applet: no notification when unmounting (as opposed to when it's done in nemo).

MATE Edition
------------

Xfce Edition
------------


rel notes
---------

	Samba changed their protocol to work with Windows 10. I don’t understand the details but if you edit (as root) /etc/samba/smb.conf and add the line “client max protocol = NT1” (without the quote marks) in the [global] section, save the file, and reboot, that should restore the Windows Networking
	The latest samba has changed to a protocol that breaks your network browsing.
For home users, the latest protocol is unlikely to be necessary, so a simple fix is:
As root, edit /etc/samba/smb.conf. Find the section “[global]” and underneath that heading add this line:
client max protocol = NT1
Then restart, and you should be ok.
This patch forces samba to use protocol version 1 instead of the latest version 3.