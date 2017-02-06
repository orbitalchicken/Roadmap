Fixed Issues since Linux Mint 18.1 BETA

All editions
------------
    “unattended-upgrades” should be removed by default.
    upgrade kernel to 4.4.0-53
    mintupdate:
        ‘Most stable recommendation’ is poor English
        kernel upgrades should take kernel series in consideration to recommend the right kernel
    mintstick: http://pasteall.org/pic/show.php?id=109579
    ttf-ancient-fonts-symbola added
    gdebi: http://pasteall.org/pic/show.php?id=109580
    gdebi: remove menu item
    When you open the calculator instead of saying “Calculator” on the panel, it says “gnome-calculator”.
    ttf-mscorefonts-installer fails to install
    steam doesn't run out of the box
    xed:
        typing shouldn't move to next result
        pressing case button should perform the search
    xplayer: https://github.com/linuxmint/xplayer/issues/53
    slideshow:
        pix icon is wrong
        remove banshee

Cinnamon Edition
----------------
    Support for RTL languages in vertical panels
    clock applet doesn't support custom formats in vertical mode
    use mate-panel in fallback mode
    notification sound, by default the file name for the sound is my username (without ending like .oga). This file does not exist.
    System Info (Upload System Information) “This includes no personal information”, possibly shorten to ‘Includes no personal information’, or ‘No personal information included’?
    window list applet -> ‘Close’ button should be near the panel
    multiple fixes in screensaver
    Right-click an icon on the panel, select “options”, then “edit”. Try to choose a new icon. The new icon shows in the window. Try to click “OK”. It won’t click and the icon won’t change.
    provide a sound file for notifications

MATE Edition
------------
    The brushed metal mintmenu background isn't set for some Mint-X color variants
    mate: when changing the track in rhythmbox: https://i.imgur.com/3ctHhPn.png (fixed in master, will come as an update with mate-notification-daemon 1.16.1)

Xfce Edition
------------
    mintupload: systray icon looks huge
    In “Removable Drives and Media”, multimedia tab, “play audio CD’s when inserted” should be “rhythmbox %d” or “vlc cdda:///dev/sr0/”
    Reduce notifications time to 5 seconds.
    The taskbar tray indicator icons become “janky” when you hover over them with the mint-y theme (dark or regular) selected

KDE Edition (Plasma 5.8)
------------------------
    theme needs support for logout/shutdown session background
    configure the SDDM theme background
    kmail fails because /var/lib/mysql-files doesn't exist
    installer: continue button greyed out when not enough HDD
