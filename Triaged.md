Triaged reports

Not a bug
---------
    lightdm-settings: It seems that the user-defined logo settings inside the login dialog have no effect right now. --> only visible with multiple monitors
    mate-control-center: appearance Interface tab Ticking and unticking “Show icons in menus” doesn’t change anything in the Preview below (same as option in mintdesktop, GTK3 requires explicit menu icon to be set, thus code changes as GNOME tried to obsolete the use of icons in menus)
    mate: Calendar doesn’t auto-close when losing focus like when clicking on the desktop.

Outside of the scope
--------------------


Can't reproduce
---------------
    Gufw Firewall does not start either using Firewall Configuration button or by terminal cmd gufw. I tried it several times
    Codecs Installer is not in the menu after installation (tested with Xfce)
    the media codecs installer is lacking some translations to german
    kde: There seems to be a bug in Desktop Settings > Wallpaper: when you scroll down the list of images, the cursor jumps back up on its own.

Upstream
--------
    indicator-keylock doesn't work properly, always shows whether a lock is enabled or not

    GNOME:
        gnome-system-tools: date-time, the Help show the option “choose the server” for NTP which no longer exists.

    KDE:
        https://bugs.launchpad.net/ubuntu/+source/kde-l10n-sr/+bug/1683607
        When bringing up a context menu on the desktop and choosing “Configure Desktop”, KDE brings up a dialog named “Folder View Settings.” When using that dialog to switch from Folder View layout to Desktop layout (and pressing the Apply button), or vice versa, the dialog box disappears. I have to bring it up again to use it.

    MATE:
        mate-applets:
            The ‘netspeed-applet 1.18.1’ now continuously resizes as the bitrate changes. Installed between the ‘Clock’ and ‘Notification Area’ means all the icons in the notification area jump around a lot.
            Sticky Notes: no marking, copy possible – https://github.com/mate-desktop/mate-applets/issues/236

        caja:
            list-view zoom issue https://github.com/mate-desktop/caja/issues/790
            file operations dialog queue/pause/play/cancel buttons need tooltips (queue button is far from explicit by itself)

        mate font viewer should be called font viewer, and its app icon isn't found.

        nm-applet (indicators in general) can't be left-clicked
