New bug reports in Linux Mint 18.2 BETA

All editions
------------

    http://people.canonical.com/~ubuntu-security/cve/pkg/vlc.html

    microcode package description is misleading in driver manager, should it be removed?
    Codecs Installer is not in the menu after installation (tested with Xfce)
    the media codecs installer is laking some translations to german

Cinnamon Edition - last processed comment: #102
-----------------------------------------------
    bg gets erased after suspend? https://bugzilla.gnome.org/show_bug.cgi?id=739178
    would battery be better swapped with user applet?
    looking for display in menu shows color first
    display resolution change freezes cinnamon https://github.com/linuxmint/Cinnamon/issues/6224
    [FIXED IN GIT] screensaver should not activate for guest sessions

MATE Edition - last processed comment: #49
------------------------------------------
    The ‘netspeed-applet 1.18.1’ now continuously resizes as the bitrate changes. Installed between the ‘Clock’ and ‘Notification Area’ means all the icons in the notification area jump around a lot. Now that’s annoying! Hopefully this will be fixed.
    The ‘indicator-keylock 3.1.0’ app while ‘working’, i.e. when the the CapsLock key is pressed, a notification popup appears, at present in 18.2 the ‘indicator-keylock’ preference settings are not respected by the ‘mate-panel’. Previously, the ‘indicator-keylock’ icon would appear on the mate-panel, ONLY when the CapsLock key was pressed and disappear again when the CapsLock key was deactivated. Now the ‘indicator-keylock’ icon remains visible all the time. This may be a ‘mate-panel 1.18.2’ or lightdm issue, idk?
    Sticky Notes: no marking, copy possible – double clicking now opens “Sticky Notes Properties”
    nm-applet can't be left-clicked
    mate font viewer should be called font viewer, and its app icon isn't found.

Xfce Edition - last processed comment: #37
------------------------------------------
    xfce4-weather-plugin 0.8.6 seems to have stopped working. It either needs to be patched somehow or upgraded to 0.8.9 which seems to work fine
    High! Thunar crashes after rename (popular bug https://bugzilla.xfce.org/show_bug.cgi?id=12264). Fixed in Xenial proposed (https://launchpad.net/ubuntu/+source/thunar/1.6.11-0ubuntu0.16.10.2) Backport it to 18.2 please!

KDE Edition - last processed comment: #32
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