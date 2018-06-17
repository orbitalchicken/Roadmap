Fixed Issues since Linux Mint 19 BETA

All editions
------------

artwork:
  - mint-x:
    - no icons in Online accounts > Information about Gnome online accounts -> Gnome Contacts, Gnome Documents, Gnome Maps and Gnome Photos
    - visual glitches in mate-screensaver-preferences in the left pane (list of screensavers). Just move the mouse over that pane back and forth, without clicking. Doesn't happen with Mint-Y.
    - transparent menubar in mate-terminal
  - mint-y:
    - thunderbird icon isn't the same as its flatpak
    - in nemo additional pane, select a folder in the left page, click in the right pane. The selected folder in the left pane is white on grey, almost invisible.
    - video and subtitle icons are too similar

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

mintupdate:
  - I choosed the new «Auto-upgrade», but it did not start until I made /etc/cron.daily/mintupdate executable.
  - On first time use, the preferences section “jumps” on the screen.
  - mint-update-pkgcache errors are reported after 60s timeout

mintbackup:
  - restore packages with buggy names -> error, instead of ignoring buggy names
  - restore a package list, Uncheck some packages, Apply. Expected : only selected packages are installed. Observed : all packages are installed, including unchecked ones

login screen:
  - text cursor doesn't appear
  - doesn't notify that caps lock is active

mime:
  - Error in file "/usr/share/applications/org.gnome.font-viewer.desktop": "font/ttf" is an invalid MIME type ("font" is an unregistered media type)
  - Error in file "/usr/share/applications/org.gnome.font-viewer.desktop": "font/otf" is an invalid MIME type ("font" is an unregistered media type

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

Xfce Edition
------------

- xfburn removed
- mintdesktop shows a sidepanel with only one item in it
- Touchpad tap would not work until I installed synaptics touchpad -> synaptics added to Xfce edition

Manual steps for upgraders
--------------------------

apt install libreoffice-sdbc-hsqldb

apt remove fortune-mod

in Xfce:
    apt install xserver-xorg-input-synaptics


remove/reinstall mint-meta-codecs