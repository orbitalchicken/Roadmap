New bug reports in Linux Mint 19 BETA

All editions - last processed comment: June 12, 2018 at 2:50 pm
---------------------------------------------------------------

- check that ISO installed in BIOS mode (USB stick)
- update inxi
- update timeshift to 18.06

artwork:
  - improve status icons: nm-signal-, volume-audio-, power icons
  - slideshow: old screenshots, still using mint-x.

mint tools:
  - mintupdate:
    - conflicts with VM guest pkgs... installing them removes mintupdate (and mintwelcome)
    - refreshing the mintinstall cache slows down checkAPT
    - systray doesn't move to green check mark after all updates are applied
    - https://github.com/linuxmint/mintupdate/issues/362

ubiquity:
  - click rel notes, nothing happens

base:
  - Shutdown takes forever: “A stop job is running for Cryptography Setup for cryptoswap1” takes over 5 minutes
  - systemd-udev cause high cpu: https://bugs.launchpad.net/ubuntu/+source/udev/+bug/1767968?comments=all
  - Boot hangs 1 minute with “gave up waiting for suspend/resume device”
		there seems to be a wrong uuid for resume in initramfs.
		Temporarily solution is here: https://askubuntu.com/questions/1013830/slow-boot-long-kernel-load-time-due-to-wrong-resume-device

xplayer:
  - [FIXED IN GIT] 'Fit Window to Movie' does not work.

Cinnamon Edition
----------------

settings:
  - [confirmed] ccc: in color plugin, add a profile, browse it and click "View details". If gnome-color-manager is not installed, the plugin should ask packagekit (over dbus) to install it. This doesn't work.

csd:
  - If the screen is rotated, then the touch screen digitiser and trackpad both move the cursor in a direction mirrored to what is expected ie move your finger to the left on the screen and the cursor moves to the right. This works properly in Gnome.
  - Another problem: When in tablet mode (that is, the screen is rotated and covering the keyboard) the RotateWindows key doesn't work anymore... It just does nothing...
  - csd-power: https://github.com/linuxmint/cinnamon-settings-daemon/issues/209

other:
  - machine will not hibernate, (either from the power button (the hibernate option is selected) or from the exit menu) the screen blanks for a couple of seconds then returns to the session)
  - Even after authorize Samba in gufw, Nemo doesn’t show the local network and machine on it. I must manually type smb://user@ip to get in (after workgroup and password) In Mint 18 that was directly available.

- NFS mount not visible in Nemo left menu. How to reproduce: install nfs-common, mount NFS folder.
- With panel set to “smart hide”: if panel was never hidden since the beginning of the session, the status of mintupdate is working as expected. Once panel is hidden (by maximizing a window) the mintupdate tray icon remains static for the rest of the session.
- Wanting to add a new custom Menu category to adding ones own Items to a category is like pulling teeth. Icon's don't save, Can't arrange Items and etc. No way to add desktop Files to the menu after they have already been created.
- NTFS pen drive is not mounting
- Unable to unlock the screensaver via LDAP with libpam-ldap and nscd packages installed pointing to an openldap server.
- [FIXED] When trying to (samba) share a folder in nemo, i have an option to install samba, but it fails to install. After installing samba from packetmanager it works.

MATE Edition
------------

- screen goes blank during the install despite all screensaver/power management being turned OFF. Post-install, with everything OFF again, screensaver/power management are disabled properly.
- When I want to shut down, the dialog offers «Hibernate» (which I never tried, because it could not work with a small swap-file). But when I first log out and login as another user, the computer remembers that there is an file /var/lib/polkit-1/localauthority/10-vendor.d/com.ubuntu.desktop.pkla, which disable the hibernation. Afterwards the quit-dialog will never show to hibernate until reboot. I did not noticed this effect on Ubuntu Mate 18.04 on the same machine (hibernation is still disabled).
- Custom actions created with Caja Actions are not appearing in Caja's context menu, whereas they did in Mint 18.3. Is there some reason this might be occurring?

Xfce Edition
------------

- Suspend worked, but would not ask for my password. I set screen lock in power manager, which I think fixed this in the past, but then it would not suspend at all.
