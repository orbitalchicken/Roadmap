New bug reports in Linux Mint 18.2 BETA

All editions
------------

    update translations
    FF 54 in live repo
    ensure broadcom driver is properly installed post-install

Cinnamon Edition - last processed comment: #177
-----------------------------------------------
    would battery be better swapped with user applet?

MATE Edition - last processed comment: #124
------------------------------------------
    The ‘netspeed-applet 1.18.1’ now continuously resizes as the bitrate changes. Installed between the ‘Clock’ and ‘Notification Area’ means all the icons in the notification area jump around a lot. Now that’s annoying! Hopefully this will be fixed.
    The ‘indicator-keylock 3.1.0’ app while ‘working’, i.e. when the the CapsLock key is pressed, a notification popup appears, at present in 18.2 the ‘indicator-keylock’ preference settings are not respected by the ‘mate-panel’. Previously, the ‘indicator-keylock’ icon would appear on the mate-panel, ONLY when the CapsLock key was pressed and disappear again when the CapsLock key was deactivated. Now the ‘indicator-keylock’ icon remains visible all the time. This may be a ‘mate-panel 1.18.2’ or lightdm issue, idk?
    Sticky Notes: no marking, copy possible – double clicking now opens “Sticky Notes Properties”
    nm-applet can't be left-clicked
    mate font viewer should be called font viewer, and its app icon isn't found.
    Battery may be broken notification is annoying.
    appearance Interface tab Ticking and unticking “Show icons in menus” doesn’t change anything in the Preview below.
    Calendar doesn’t auto-close when losing focus like when clicking on the desktop.
    Right-click on the desktop -> No templates installed
    Zoom-in/out by pressing CTR++/- in Caja with “List View” seems to be slow at updating the view.
    install menulibre by default with MATE, instead of mozo, to allow better configuration of the application menu?
    When adding “Workspace Switcher” to panel it displays in blue color and does not follow default theme color green?
    Date/Time in panel used to display in two lines when panel was larger than a certain size?
    Text in the panel seems to be in bold style when it should be normal style?
    File Operations dialog looks strange – it has an “Undo” arrow icon?
    I found that available desktop themes would not install. They populate the available list and download without issue, but would not install and shift to the active theme list.
    Mint y themes clock font is bold even though application font setting is not.
    the Help show the option “choose the server” for NTP which no more exists.
    mintmenu https://abload.de/img/lm182recentvisgb.jpg

Xfce Edition - last processed comment: #45
------------------------------------------


KDE Edition - last processed comment: #40
-----------------------------------------
    SDDM stays in autologin after OEM install
    There seems to be a bug in Desktop Settings > Wallpaper: when you scroll down the list of images, the cursor jumps back up on its own.
    Add kde-config-tablet_2.0-2_amd64.deb from trusty to add wacom support
    /var/cache/apt/archives/kde-l10n-sr_4%3a16.04.3-0ubuntu1~ubuntu16.04~ppa2_all.deb
        E: Sub-process /usr/bin/dpkg returned an error code (1)
        This started with last update for 18.1 (Plasma 5.8.7), where package ‘plasma-desktop-data’ could not be installed.
        For this I found workaround:
        sudo dpkg -i –force-overwrite /var/cache/apt/archives/plasma-desktop-data_4%3a5.8.7.1-0ubuntu1~ubuntu16.04~ppa1_all.deb
    When bringing up a context menu on the desktop and choosing “Configure Desktop”, KDE brings up a dialog named “Folder View Settings.” When using that dialog to switch from Folder View layout to Desktop layout (and pressing the Apply button), or vice versa, the dialog box disappears. I have to bring it up again to use it.