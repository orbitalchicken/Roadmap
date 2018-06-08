New bug reports in Linux Mint 19 BETA

All editions
------------

artwork:
  - Firefox bookmarks don’t use the folder color picked in the Cinnamon theme setting.
  - slideshow: old screenshots, still using mint-x.
  - mint-y-icons: yellow folders missing.
  - mint-y-dark (and dark variants of light themes): xed right margin is barely visible, current line highlighting is grey on top of grey.
  - provide network/sound panel icons

mint tools:
  - mintinstall: does only wait and not warn if synaptic is open.
  - mintupdate: conflicts with VM guest pkgs... installing them removes mintupdate (and mintwelcome)
  - [FIXED in GIT] mintupdate: On first time use, the preferences section “jumps” on the screen.

ubiquity:
  - When installing to internal 16GB SSD and with option “Something else” using the whole SSD for mountpoint root, installation always hangs in both XFCE 64 and Cinnamon 64. Ubuntu 18.04 installer with same options has no problem.

base:
  - Shutdown takes forever: “A stop job is running for Cryptography Setup for cryptoswap1” takes over 5 minutes
  - systemd-udev cause high cpu: https://bugs.launchpad.net/ubuntu/+source/udev/+bug/1767968?comments=all
  - Boot hangs 1 minute with “gave up waiting for suspend/resume device”
		there seems to be a wrong uuid for resume in initramfs.
		Temporarily solution is here: https://askubuntu.com/questions/1013830/slow-boot-long-kernel-load-time-due-to-wrong-resume-device

Cinnamon Edition - last processed comment: June 5, 2018 at 5:18 pm
------------------------------------------------------------------

artwork:
  - cinnamon themes hardcode the font

settings:
  - [confirmed] ccc: in color plugin, add a profile, browse it and click "View details". If gnome-color-manager is not installed, the plugin should ask packagekit (over dbus) to install it. This doesn't work.

csd:
  - If the screen is rotated, then the touch screen digitiser and trackpad both move the cursor in a direction mirrored to what is expected ie move your finger to the left on the screen and the cursor moves to the right. This works properly in Gnome.

other:
  - Cinnamon setting to disable the touch pad while typing does not work, which makes typing on the laptop pretty annoying.
  - machine will not hibernate, (either from the power button (the hibernate option is selected) or from the exit menu) the screen blanks for a couple of seconds then returns to the session)
  - Even after authorize Samba in gufw, Nemo doesn’t show the local network and machine on it. I must manually type smb://user@ip to get in (after workgroup and password) In Mint 18 that was directly available.

MATE Edition - last processed comment: June 5, 2018 at 12:57 pm
---------------------------------------------------------------

- ubiquity: click rel notes, nothing happens
- screen goes blank during the install despite all screensaver/power management being turned OFF. Post-install, with everything OFF again, screensaver/power management are disabled properly.

Xfce Edition - last processed comment: June 5, 2018 at 9:42 am
--------------------------------------------------------------

panel/osd:
  - changing sound volume via hotkey shows two on-screen-displays
  - pulseaudio item has two onscreen notifications
  - panel date and time item is set as bitstream vera fonts, but bitstream vera fonts not installed
  - digital clock would not stay in the panel, only the analog version
  - editing the panel clock item in anyway it won’t display anymore user need to remove clock then add again
  - clock applet doesn't let you use custom format
  - too many notification and status notifiers panel items, don’t know which one to control, they all have the same basic options. https://i.imgur.com/fmyhhdp.png
  - After switching to a guest session and back to my session, the wifi indicator appeared twice in the notification area.

other:
  - Suspend worked, but would not ask for my password. I set screen lock in power manager, which I think fixed this in the past, but then it would not suspend at all.
