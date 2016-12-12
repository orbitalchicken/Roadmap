Triaged reports

Not a bug
---------
    mintlocale: I installed (64 bit) with German language. After booting the installed system I find in the language settings the message about incomplete language packs for 4 English and 2 German language variants. The annoying thing is, that each of those 6 language packs have to get installed separately, so this really wastes some time. I did several installs of Serena and found the problem reproducible.

Outside of the scope
--------------------
    In live session, a restart causes the screen to hang on shut down. --> long standing issue on some hardware.
    “Show icons in menus” works with xed, but “Toolbar button labels” does not --> changes in GTK3 regarding menu icons force applications to enforce their presence

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

Upstream
--------
    gnome-terminal: the command to close all terminals in the file menu only closes all tabs.
    ubiquity: in user details screen, enter your name, then press tab all the way to the password field (using defaults for username and hostname), the text in the username entry stays selected.
    mate-control-center: Some colors are hardcoded, visible with Mint-Y Dark theme
    vmware: windows are translucent -> https://github.com/linuxmint/Cinnamon/issues/4870
    deja-dup: since Linux Mint 18 MATE there is a issue with the tray-icon of deja-dup: deja-dup works like it should, but the tray-icon (to show progress, pause/resume, skip) is not visible… the notification area is extended but you see just the normal panel-background. in Linux Mint MATE prior to 18.x, Linux Mint Xfce 18 and Ubuntu MATE 16.04 the tray-icon is shown, so it unfortunately hast to do with Mint MATE! --> deja-dup needs to check for XDG_CURRENT_DESKTOP instead of creating race conditions with DBUS.. this issue is reported on so many DEs..
    kernel: Unrecognized audio devices “Dummy output”. ProBook 470 G4. Audio was fine in Sarah.