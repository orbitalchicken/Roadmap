New bug reports in Linux Mint 18.2 BETA

All editions
------------

    http://people.canonical.com/~ubuntu-security/cve/pkg/vlc.html

    microcode package description is misleading in driver manager, should it be removed?

    blueberry:
        [FIXED IN GIT] Button on popup to open/view file just received via Bluetooth is not translated
        [FIXED IN GIT] unicode issue when receiving file

    update translations
    FF 54 in live repo

    mintupdate:
        should kernel series col be asc or desc?
        [FIXED IN GIT] it would be better not to use Ctrl+C as shortcut to empty the list, as thus one cannot copy text e.g. from the description of changes
        [FIXED IN GIT] Firefox should be a security update

    lightdm-settings: It seems that the user-defined logo settings inside the login dialog have no effect right now.

    Xplayer has a weird and unexpected behavior with scroll wheel not controlling the volume like in VLC

    artwork:
        mint-y The maximize/restore window control button doesn’t change visually between in maximized and restored state (default theme and Mint-Y-Dark)
        [Joseph] mint-x-icons oversized icons
        [Joseph] xfce window buttons in mint-y

    synaptic: Start menu -> Sound & video -> Install Multimedia Codecs fails without internet connection. The first error message: synaptic (as superser) window title with “Could not download all repository indexes is way too tall on a 1366×768 laptop screen

    Gufw Firewall does not start either using Firewall Configuration button or by terminal cmd gufw. I tried it several times

    codecs:
        check that java isn't installed with codecs
        install mp3 support without codecs?
        gstreamer fails to install codecs
        Codecs Installer is not in the menu after installation (tested with Xfce)
        the media codecs installer is lacking some translations to german

    https://askubuntu.com/questions/800479/ubuntu-16-04-slow-boot-apt-daily-service

    xreader Next Page and Previous Page arrows do not work

    ensure broadcom driver is properly installed post-install


Cinnamon Edition - last processed comment: #177
-----------------------------------------------
    [Michael] bg gets erased after suspend? https://bugzilla.gnome.org/show_bug.cgi?id=739178
    would battery be better swapped with user applet?
    looking for display in menu shows color first
    preferences > keyboard > custom shortcuts. Used with a Spanish keyboard layout. Recorded: crtl+number and ctrl+Shift+number (e.g. ctrl+1 and ctrl+shift+1 = ctrl+!) they are recorded correctly. When using the shortcut the command defined in the shift combination is triggered with just ctrl+number (i.e. ctrl+1). The complete combination triggers nothing (i.e. ctrl+shift+1 does nothing) and the comand defined in ctrl+number can never be used. This worked in 17.3.
    In Mint menu Nemo (Files) is not translated
    screen rotates 90º counter-clockwise automatically.
    ccc display doesn't always show screen ID windows
    [Clem] can't run onboard in cinnamon -> hide it from menu and implement a menu entry for cinnamon's built-in keyboard

MATE Edition - last processed comment: #124
------------------------------------------
    The ‘netspeed-applet 1.18.1’ now continuously resizes as the bitrate changes. Installed between the ‘Clock’ and ‘Notification Area’ means all the icons in the notification area jump around a lot. Now that’s annoying! Hopefully this will be fixed.
    The ‘indicator-keylock 3.1.0’ app while ‘working’, i.e. when the the CapsLock key is pressed, a notification popup appears, at present in 18.2 the ‘indicator-keylock’ preference settings are not respected by the ‘mate-panel’. Previously, the ‘indicator-keylock’ icon would appear on the mate-panel, ONLY when the CapsLock key was pressed and disappear again when the CapsLock key was deactivated. Now the ‘indicator-keylock’ icon remains visible all the time. This may be a ‘mate-panel 1.18.2’ or lightdm issue, idk?
    Sticky Notes: no marking, copy possible – double clicking now opens “Sticky Notes Properties”
    nm-applet can't be left-clicked
    mate font viewer should be called font viewer, and its app icon isn't found.
    Battery may be broken notification is annoying.
    appearance Interface tab Ticking and unticking “Show icons in mens” doesn’t change anything in the Preview below.
    Calendar doesn’t auto-close when losing focus like when clicking on the desktop.
    Right-click on the desktop -> No templates installed
    Zoom-in/out by pressing CTR++/- in Caja with “List View” seems to be slow at updating the view.
    No virtual (on-screen) keyboard.
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
    xfce4-weather-plugin 0.8.6 seems to have stopped working. It either needs to be patched somehow or upgraded to 0.8.9 which seems to work fine
    High! Thunar crashes after rename (popular bug https://bugzilla.xfce.org/show_bug.cgi?id=12264). Fixed in Xenial proposed (https://launchpad.net/ubuntu/+source/thunar/1.6.11-0ubuntu0.16.10.2) Backport it to 18.2 please!
    consider installing light-locker-settings by default
    System requirements say Graphics card capable of 800×600 resolution, but the mintupdate window doesn’t fit into a screen with 800×600 resolution.

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