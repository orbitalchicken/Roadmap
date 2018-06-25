Fixed Issues since Linux Mint 19 BETA

All editions
------------

artwork:
  - mint-x:
    - no icons in Online accounts > Information about Gnome online accounts -> Gnome Contacts, Gnome Documents, Gnome Maps and Gnome Photos
    - visual glitches in mate-screensaver-preferences in the left pane (list of screensavers). Just move the mouse over that pane back and forth, without clicking. Doesn't happen with Mint-Y.
    - transparent menubar in mate-terminal
    - start-here-symbolic.svg missing
    - improve status icons: nm-signal-, volume-audio-, power icons
  - mint-y:
    - thunderbird icon isn't the same as its flatpak
    - in nemo additional pane, select a folder in the left page, click in the right pane. The selected folder in the left pane is white on grey, almost invisible.
    - video and subtitle icons are too similar
    - .deb icon
    - filesystem icon looks like an ipod (in thunar, when small enough)
  - with adwaita, missing icons for Settings/Seting Language, Accessories/USB Format, Accessories/USB Write Image

- ubiquity: click rel notes, nothing happens
- The fortune command says 'no fortunes found' -> leftover, fortune is now removed.
- gdebi doesn't install packages unless it's run from the terminal
- ia32-libs: depends on libesd0:i386 which is gone
- libreoffice-base can't open databases
- mint-common: uninstalling flatpak from menu doesn't work (tried with VLC)
- ms ttf fonts says it is installed but when i go to fonts to use arial black there are no fonts i fixed this by uninstalling from software manager reboot and reinstalling them then reboot then it works i like my arial black and 1 of the few reasons i use lm verses all other distros -> made it a manual install
- intel-microcode is missing https://bugs.launchpad.net/ubuntu/+source/ubuntu-drivers-common/+bug/1758689
- remove vino (upstream made vino useless outside of GNOME)
- GTK file chooser: org.gtk.Settings.FileChooser sort-directories-first should be true
- xreader crash when opening certain documents
- mintinstall: launch button should be highlighted blue or green.
- spotify depends on libcurl3
- blueberry won't launch in VM: "bt-adapter -i" hangs and then segfaults
- Bash completion doesn't work with all apt commands https://github.com/linuxmint/mintsystem/issues/73
- xplayer: 'Fit Window to Movie' does not work.
- machine will not hibernate, (either from the power button (the hibernate option is selected) or from the exit menu) the screen blanks for a couple of seconds then returns to the session) -> pm-hibernate fails, that's upstream. We were forcing the hibernation option to be present though, and that was fixed.

mintupdate:
  - I choosed the new «Auto-upgrade», but it did not start until I made /etc/cron.daily/mintupdate executable.
  - On first time use, the preferences section “jumps” on the screen.
  - mint-update-pkgcache errors are reported after 60s timeout
  - conflicts with VM guest pkgs... installing them removes mintupdate (and mintwelcome)
  - refreshing the mintinstall cache slows down checkAPT
  - https://github.com/linuxmint/mintupdate/issues/362

mintbackup:
  - restore packages with buggy names -> error, instead of ignoring buggy names
  - restore a package list, Uncheck some packages, Apply. Expected : only selected packages are installed. Observed : all packages are installed, including unchecked ones

login screen:
  - text cursor doesn't appear
  - doesn't notify that caps lock is active

mime:
  - Error in file "/usr/share/applications/org.gnome.font-viewer.desktop": "font/ttf" is an invalid MIME type ("font" is an unregistered media type)
  - Error in file "/usr/share/applications/org.gnome.font-viewer.desktop": "font/otf" is an invalid MIME type ("font" is an unregistered media type

timeshift:
  - /swapfile should be excluded
  - wizard, the tooltip incorrectly states "Create snapshots using RSYNC" when you hover over BTRFS?
  - Users tab, the headings for the radio buttons are named "Exclude Apps", "Include Hidden Items" and (once again) "Exclude Apps".

Cinnamon Edition
----------------

- When I edit an application in “Startup Applications”, and it has a delay, the seconds unit “s” disappears.
- cinnamon settings startup, edit item with no delay, save -> python exception
- cinnamon fallback -> muffin_no_shadows=1
- skype systray duplicated: https://github.com/linuxmint/Cinnamon/issues/7588
- cmenu: doesn't show some newly installed apps (slack-desktop, ppa:4kvideodownloader, pysolfc), others show up just fine (filezilla, ppa:qbittorrent, ppa:woeusb).
- Wireless not showing in Network Manager even though it appears in Network Manager Settings.
- goa: ubuntu SSO isn't functional -> it won't work without snapd, and it's useless for anything else. Ubuntu non-gnome users auth in snapd CLI anyway, so this should be removed. We don't need it, it's not necessary and it won't work OOTB.
- desklets: I found a little bug in the Desklet “Analog Chronometer”. I can not call the settings when I have downloaded and switched on the Chronometer.
- When trying to (samba) share a folder in nemo, i have an option to install samba, but it fails to install. After installing samba from packetmanager it works.
- csd-power: https://github.com/linuxmint/cinnamon-settings-daemon/issues/209
- With panel set to “smart hide”: if panel was never hidden since the beginning of the session, the status of mintupdate is working as expected. Once panel is hidden (by maximizing a window) the mintupdate tray icon remains static for the rest of the session.
- nm applet resets to 0%

MATE Edition
------------

hidpi:
  - blurry titlebar buttons
  - grey tooltips

- mintlocale im has no window icon
- mintlocale has no window icon
- hide compton menuitem
- onboard isn't selected as a preferred apps
- mintmenu spamming the logs
- When I want to shut down, the dialog offers «Hibernate» (which I never tried, because it could not work with a small swap-file). But when I first log out and login as another user, the computer remembers that there is an file /var/lib/polkit-1/localauthority/10-vendor.d/com.ubuntu.desktop.pkla, which disable the hibernation. Afterwards the quit-dialog will never show to hibernate until reboot. I did not noticed this effect on Ubuntu Mate 18.04 on the same machine (hibernation is still disabled).

Xfce Edition
------------

- xfburn removed
- mintdesktop shows a sidepanel with only one item in it
- Touchpad tap would not work until I installed synaptics touchpad -> synaptics added to Xfce edition
- changing sound volume via hotkey shows two on-screen-displays
- After switching to a guest session and back to my session, the wifi indicator appeared twice in the notification area.
- applet icons are too big
- Suspend worked, but would not ask for my password. I set screen lock in power manager, which I think fixed this in the past, but then it would not suspend at all.

Manual steps for upgraders
--------------------------

apt install libreoffice-sdbc-hsqldb sessioninstaller

apt remove fortune-mod

in Xfce:
    apt install xserver-xorg-input-synaptics

remove/reinstall mint-meta-codecs

edit /etc/systemd/logind.conf
remove plka
