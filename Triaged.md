Triaged reports

Not a bug
---------
    lightdm-settings: It seems that the user-defined logo settings inside the login dialog have no effect right now. --> only visible with multiple monitors


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
    KDE:
        https://bugs.launchpad.net/ubuntu/+source/kde-l10n-sr/+bug/1683607
        When bringing up a context menu on the desktop and choosing “Configure Desktop”, KDE brings up a dialog named “Folder View Settings.” When using that dialog to switch from Folder View layout to Desktop layout (and pressing the Apply button), or vice versa, the dialog box disappears. I have to bring it up again to use it.

    MATE:
        mate-applets:
            Calendar doesn’t auto-close when losing focus like when clicking on the desktop.
            The ‘netspeed-applet 1.18.1’ now continuously resizes as the bitrate changes. Installed between the ‘Clock’ and ‘Notification Area’ means all the icons in the notification area jump around a lot. Now that’s annoying! Hopefully this will be fixed.
            The ‘indicator-keylock 3.1.0’ app while ‘working’, i.e. when the the CapsLock key is pressed, a notification popup appears, at present in 18.2 the ‘indicator-keylock’ preference settings are not respected by the ‘mate-panel’. Previously, the ‘indicator-keylock’ icon would appear on the mate-panel, ONLY when the CapsLock key was pressed and disappear again when the CapsLock key was deactivated. Now the ‘indicator-keylock’ icon remains visible all the time. This may be a ‘mate-panel 1.18.2’ or lightdm issue, idk?
            Sticky Notes: no marking, copy possible – double clicking now opens “Sticky Notes Properties”

        mate-control-center:
            appearance Interface tab Ticking and unticking “Show icons in menus” doesn’t change anything in the Preview below.
            date-time: The Help show the option “choose the server” for NTP which no longer exists.

        caja:
            In list-view, zooming in/out with Ctrl++ or Ctrl-- updates the zoom level but doesn't seem to refresh the view immediately
            File Operations dialog looks strange – it has an “Undo” arrow icon?

        mate font viewer should be called font viewer, and its app icon isn't found.

        nm-applet (indicators in general) can't be left-clicked
