Triaged reports

Not a bug
---------
    mintlocale: I installed (64 bit) with German language. After booting the installed system I find in the language settings the message about incomplete language packs for 4 English and 2 German language variants. The annoying thing is, that each of those 6 language packs have to get installed separately, so this really wastes some time. I did several installs of Serena and found the problem reproducible.

Outside of the scope
--------------------
    In live session, a restart causes the screen to hang on shut down. --> long standing issue on some hardware.
    “Show icons in menus” works with xed, but “Toolbar button labels” does not --> changes in GTK3 regarding menu icons force applications to enforce their presence
    xfce:
        when I put the Xfce panel into kiosk mode, I lose all changes to the panel that I’ve made previously. Kiosk mode does work well in Xubuntu 16.04.x, with preservation of the changes I made. But not in Linux Mint 18.1 Xfce: it just falls back to the installation defaults. This is the method I use for kiosk mode for the Xfce panel: https://sites.google.com/site/easylinuxtipsproject/xfce#TOC-Lock-the-panels-kiosk-mode- (item 7, right column)
    kde:
        Enhanced Desktop colour consistency idea: Before http://pasteall.org/pic/show.php?id=111473, After http://pasteall.org/pic/show.php?id=111474. --> Good idea, but Breeze is going through important changes and we're not frozen on Plasma (PPA Scheme) so let's stick to upstream as much as possible right now.
        Wallpaper -> Positioning currently uses ‘Scaled’, may I recommend ‘Scaled and Cropped’ (matches Cinnamon’s ‘Picture aspect’ ‘Zoom’ functionality). Recommendation prevents image distortion for those using different aspect ratio display devices. --> Definitely, but this isn't directly configurable upstream without resorting to scripting.
        enable two things in Dolphin? 1. Make Tab switch between panes, as KDEneon does, 2. Disable single-click activation of items.

Can't reproduce
---------------
    xed: when you have more than a page, scrolling down (or up) with the down (or up) arrow creates a jerky display; similarly, with a large document, going from the top to the bottom with Ctrl-End (or vice-versa with Ctrl-Home) seems to have an intermediate stage where it is displaying text from somewhere in the middle of the document; reminds me of “smooth” scrolling in Firefox; makes xed unusable for me except for short periods of time or for very short files
    gnome-calculator: takes way to long to exit (for a calculator); it also seems to be thrashing my HDD when it exits
    nemo: The option to go up one level by double clicking an empty place (a very welcomed feature) doesn’t work at all. I tried it with some empty folders (e.g. Desktop), but nothing happens at all. Also logging out and back into the user account does not help.
    cinnamon:
        when installing themes https://justpaste.it/110ba
        If in panel edit mode right clicking the panel doesn’t do anything. This means, that you cannot turn off panel edit mode.
    nemo: Nemo/Cinnamon crash when browsing sftp://
    With VirtualBox 5.1.10 and VboxGuestAdditions (GA) installed race condition happens approximately 60% of the time after login (CSD high CPU usage).
        After around 1 min 45 sec of black screen and high CPU usage Cinnamon crashes, Gnome desktop appears, CPU usage remains high, at which point ran System Monitor and Top
        http://pasteall.org/pic/show.php?id=109572
        http://pasteall.org/pic/show.php?id=109574
        After around 9 minutes of high CPU usage the process reaches 3 GiB virtual memory then crashes, desktop resets and offending process memory drops to 1.5 KiB
    cinnamon: Qt 5.7 looks bad
    xfce:
        “xfwm4 + compositing” cause screen tearing, changing it to “xfwm4 + compton” fixes that in 18.0. However, in 18.1 beta, compton doesn’t work anymore (as in: screen tearing remains).
        Screensaver: setting ‘cycle after’ to 1 minute causes white screen, followed by lock-up.
Upstream
--------
    gnome-terminal: the command to close all terminals in the file menu only closes all tabs.
    ubiquity: in user details screen, enter your name, then press tab all the way to the password field (using defaults for username and hostname), the text in the username entry stays selected.
    mate-control-center: Some colors are hardcoded, visible with Mint-Y Dark theme
    vmware: windows are translucent -> https://github.com/linuxmint/Cinnamon/issues/4870
    deja-dup: since Linux Mint 18 MATE there is a issue with the tray-icon of deja-dup: deja-dup works like it should, but the tray-icon (to show progress, pause/resume, skip) is not visible… the notification area is extended but you see just the normal panel-background. in Linux Mint MATE prior to 18.x, Linux Mint Xfce 18 and Ubuntu MATE 16.04 the tray-icon is shown, so it unfortunately hast to do with Mint MATE! --> deja-dup needs to check for XDG_CURRENT_DESKTOP instead of creating race conditions with DBUS.. this issue is reported on so many DEs..
    kernel: Unrecognized audio devices “Dummy output”. ProBook 470 G4. Audio was fine in Sarah.
    firefox: issues with Mint-Y-Dark — on youtube, the number of thumbs up/down are *barely* visible