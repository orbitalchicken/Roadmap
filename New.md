New bug reports in Linux Mint 19 BETA

All editions - last processed comment: June 12, 2018 at 2:50 pm
---------------------------------------------------------------

- check that ISO installed in BIOS mode (USB stick)
- Gnome calendar does not have an icon on the top left in the new Gnome decorations, only a cog icon is shown.
- update inxi

slick:
  - On a VirtualBox setup with three users, if any user but the first is auto given focus, the username is present but the box only has half height, cut off with no password entry lower half. You can type where that password entry half of the box would be , and it works, but the characters don't show, so it's a visual display problem, only apparently happening on boot.

artwork:
  - improve status icons: nm-signal-, volume-audio-, power icons
  - [FIXED In GIT] .deb icon
  - slideshow: old screenshots, still using mint-x.
  - mint-y-icons: yellow folders missing.
  - filesystem icon looks like an ipod (in thunar, when small enough)
  - The progress indicator in the panel should be the same color as the chosen theme. Not just green.
  - start-here-symbolic.svg was missing in Mint-X icon set. So I copied /usr/share/icons/Mint-X/places/scalable/start-here-linux-mint-symbolic.svg to /usr/share/icons/Mint-X/places/scalable/start-here-symbolic.svg. Then I updated icon-cache file: sudo gtk-update-icon-cache -f '/usr/share/icons/Mint-X' Now: https://imgur.com/ftlrKXL
  - In the default theme, approximately one pixel of the taskbar near the edge of the screen cannot properly select and switch the task list.
  - Mint-Y showing incorrect icons in check-boxes. Example: Nemo Preferences, select "Show advanced permissions in the file property dialogue". Now view the properties of a directory containing files. Initially, the file permissions will show [-] (correct).  But clicking to change permissions results in [ ] -&gt; [🗸] -&gt; [🗸] (blank, check, check).  The dash never shows up again leading one to think they enabled the permission, which they didn't.

blueberry:
  - won't launch in VM (Xfce): "bt-adapter -i" hangs and then segfaults
  - possible to turn OFF completely? (systemd might fail to rfkill, but our systray option should at least be preserved)

mint tools:
  - Bash completion doesn't work with all apt commands https://github.com/linuxmint/mintsystem/issues/73
  - mintupdate:
    - conflicts with VM guest pkgs... installing them removes mintupdate (and mintwelcome)
    - systray doesn't move to green check mark after all updates are applied

ubiquity:
  - click rel notes, nothing happens

base:
  - Shutdown takes forever: “A stop job is running for Cryptography Setup for cryptoswap1” takes over 5 minutes
  - systemd-udev cause high cpu: https://bugs.launchpad.net/ubuntu/+source/udev/+bug/1767968?comments=all
  - Boot hangs 1 minute with “gave up waiting for suspend/resume device”
		there seems to be a wrong uuid for resume in initramfs.
		Temporarily solution is here: https://askubuntu.com/questions/1013830/slow-boot-long-kernel-load-time-due-to-wrong-resume-device

timeshift:
  - /swapfile should be excluded
  - wizard, the tooltip incorrectly states "Create snapshots using RSYNC" when you hover over BTRFS?
  - Users tab, the headings for the radio buttons are named "Exclude Apps", "Include Hidden Items" and (once again) "Exclude Apps".
  - First time Timeshift was used the Warning and Disclaimer text sections appeared blank (image link), next use the fields were populated. http://pasteall.org/pic/show.php?id=61509d64959391182648fdff247804e6

xplayer:
  - In fullscreen mode, it starts misbehaving after a while. Video freezes/goes black, sound is still there. Keyboard is lost. Mouse pointer moves, but no action can be taken. Reset button on box only option.
  - 'Fit Window to Movie' does not work.
  - In some videos with subtitles, Xplayer does not show them, even if I select them in the menu. It happened to me in a .mkv file, but I do not know if it happens in other types of files. In these cases, I use VLC.
  - Booted from the LM19 live CD (linuxmint-19-mate-32bit-beta.iso), installed smplayer (%sudo apt-get install --install-recommends smplayer).
		Marco: smplayer displays .flv and .mp4 videos correctly.
		Marco Compositing: smplayer displays .flv and .mp4 videos as described previously.
		Marco Compton: smplayer displays .flv and .mp4 videos as described previously.
		Metacity: smplayer displays .flv and .mp4 videos correctly.
		Metacity Compositing: smplayer displays .flv and .mp4 videos as described previously.
		Metacity Compton: smplayer displays .flv and .mp4 videos as described previously.
		Compiz: smplayer displays .flv and .mp4 videos correctly.
		AOpen MX4SG-4DN motherboard, Intel 865G Graphics Memory Controller Hub.
		xplayer segfaults in all cases above ^^

Cinnamon Edition
----------------

artwork:
  - cinnamon themes hardcode the font

settings:
  - [confirmed] ccc: in color plugin, add a profile, browse it and click "View details". If gnome-color-manager is not installed, the plugin should ask packagekit (over dbus) to install it. This doesn't work.

csd:
  - If the screen is rotated, then the touch screen digitiser and trackpad both move the cursor in a direction mirrored to what is expected ie move your finger to the left on the screen and the cursor moves to the right. This works properly in Gnome.
  - Another problem: When in tablet mode (that is, the screen is rotated and covering the keyboard) the RotateWindows key doesn't work anymore... It just does nothing...
  - csd-power: https://github.com/linuxmint/cinnamon-settings-daemon/issues/209

other:
  - machine will not hibernate, (either from the power button (the hibernate option is selected) or from the exit menu) the screen blanks for a couple of seconds then returns to the session)
  - Even after authorize Samba in gufw, Nemo doesn’t show the local network and machine on it. I must manually type smb://user@ip to get in (after workgroup and password) In Mint 18 that was directly available.

- removing favorites isn't intuitive, there should be a context menu option
- Can't delete a user. Delete button doesn't delete.
- Effects "Unmaximize Window" behavior does not change with change in settings regardless of effect type or time setting.
- After the updates last night I am no longer able to drag maximized windows bu the title bar in Cinnamon.  To clarify the drag of maximized windows, Firefox and Nemo will not drag when maximized, Thunderbird will drag when maximized
- NFS mount not visible in Nemo left menu. How to reproduce: install nfs-common, mount NFS folder.
- steam has to be exited twice from systray?
- Using Vivaldi (1.15.1147.42 (Stable channel) (64-bit)) I downloaded a picture (jpg) from Facebook to my desktop. The download created a file (filename).jpg.crdownload. Once the picture was downloaded completely this file remained on my desktop. I can select it and check its properties, but I cannot delete it. I get an error message saying that the object does not exist.
- With panel set to “smart hide”: if panel was never hidden since the beginning of the session, the status of mintupdate is working as expected. Once panel is hidden (by maximizing a window) the mintupdate tray icon remains static for the rest of the session.
- Wanting to add a new custom Menu category to adding ones own Items to a category is like pulling teeth. Icon's don't save, Can't arrange Items and etc. No way to add desktop Files to the menu after they have already been created.
- Application switcher items are not properly selected https://github.com/linuxmint/Cinnamon/issues/7623
- NTFS pen drive is not mounting
- When trying to (samba) share a folder in nemo, i have an option to install samba, but it fails to install. After installing samba from paketmaneger it works.
- Unable to unlock the screensaver via LDAP with libpam-ldap and nscd packages installed pointing to an openldap server.


MATE Edition
------------

- screen goes blank during the install despite all screensaver/power management being turned OFF. Post-install, with everything OFF again, screensaver/power management are disabled properly.
- When I want to shut down, the dialog offers «Hibernate» (which I never tried, because it could not work with a small swap-file). But when I first log out and login as another user, the computer remembers that there is an file /var/lib/polkit-1/localauthority/10-vendor.d/com.ubuntu.desktop.pkla, which disable the hibernation. Afterwards the quit-dialog will never show to hibernate until reboot. I did not noticed this effect on Ubuntu Mate 18.04 on the same machine (hibernation is still disabled).
- Custom actions created with Caja Actions are not appearing in Caja's context menu, whereas they did in Mint 18.3. Is there some reason this might be occurring?

Xfce Edition
------------

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
