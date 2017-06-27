Fixed Issues since Linux Mint 18.2 BETA

All editions
------------
    redshift-gtk should depend on geoclue-2.0
    onboard is not visible in the app menu

    guest sessions:
        don't start mintwelcome

    slick-greeter/lightdm-settings:
        background color doesn't seem to work
        padding issue when hovering session button
        wrong logitech keyboard layout

    pix:
        Support for Fujifilm RAW files
        Support for EXIF orientation in RAW files

    mintupdate:
        kernel headers for 4.4 confuse ppl
        Clicking Linux kernel headers 4.4, and selecting ‘Ignore updates for this package’ has no effect. Understandable for newer kernel/kernel headers update?
        update policy choice doesn't stick
        don't start mintupdate in guest sessions
        Don't use Ctrl+C as shortcut to empty the list (needed to copy text e.g. from the description of changes)
        Firefox should always be flagged as a security update
        Fit policy page within 800x600

    blueberry:
        add a way to disable the autostart
        Button on popup to open/view file just received via Bluetooth is not translated
        unicode issue when receiving file

    mintinstall:
        can't access office category (happens in MATE but not in Cinnamon, issue in Pixbuf SVG support..)

    codecs:
        remove xplayer-mozilla
        remove icedtea
        gstreamer fails to install codecs

    artwork:
        xfce window buttons in mint-y

Cinnamon Edition
----------------
    nemo-preview doesn't work
    screensaver should not activate for guest sessions
    In Mint menu Nemo (Files) is not translated
    can't run onboard in cinnamon -> hide it from menu and implement a menu entry for cinnamon's built-in keyboard


MATE Edition
------------
    guest session blocks mintmenu
    mate-panel:
        freezes everytime I try to add or move a launcher (icon) to it.
        when applying a bg color, the “Window List” remains unchanged.
    Battery may be broken notification is annoying.
    mintmenu https://abload.de/img/lm182recentvisgb.jpg
    mint-y-theme:
        When adding “Workspace Switcher” to panel it displays in blue color and does not follow default theme color green?
        Text in the panel (including window-list and clock applet) seems to be in bold style when it should be normal style?

Xfce Edition
------------
    install light-locker-settings by default


KDE Edition (Plasma 5.8)
------------------------
