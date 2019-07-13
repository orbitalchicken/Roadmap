Done
====

mintreport:
    sysinfo tab
    migrate to systemd-coredump (to make it compatible with LMDE
    better layout

mintinstall/mintbackup:
    use common cache to know all manually installed packages, not just the ones installed via mintinstall (only in Mint, not LMDE)

mintinstall:
    spinner while searching
    support for low resolution screens

Cinnamon 4.2:
    - enable recent by default
    - preferred apps: Added an option for PDF reader
    - simplified docinfo
    - simplified appsys
    - cmenus ported to meson
    - background slideshow applet shows filename
    - faster input lag
    - faster menu
    - printer applet
    - vsync can be switched without restarting
    - configurable vsync method
    - nemo conditional actions, exec condition https://github.com/linuxmint/nemo/pull/2056
    - nemo pinned items
    - menu no more duplicated names
    - natural scrolling for mice (not just touchpad)
    - cmenus ported to meson
    - screensaver no longer fades
    - screensaver on-screen keyboard
    - better samba support (check full permissions, warns about encrypted directories, fills rules for UFW)
    - session manager:
        don't let inhibitors stop a forced logout
        port to gdbus
    - connectivity checking in privacy

mintupdate:
    able to blacklist a specific version
    detects apt lock and delays refresh instead of failing
    automated autoremove of kernels and packages
    inhibit shutdown/reboot during automation
    persistent and logrotate for /var/log/mintupdate.log
    auto-refresh is now configurable

mintupdate
    refreshes automatically when apt cache changes
    add man pages
    warns that reboot is required after kernel update
    info dialog updates in real time
    refresh mechanism uses timestamp, no longer impacted by suspends, can be configured to periods longer than the session
    warns 90 days before distro reaches EOL
    retire level and obsolete options
    checkAPT no longer run as root
    kernel series supported
    multiples can be installed/removed (queued operations)
    kernels show their EOL
    status page when mintupdate needs to update itself
    refresh page
    mintupdate page

mintmenu:
    configurable tooltips
    configurable search bar position
    performance improvements
    preferences rewrite using xapp gsettings widgets
    recent -> documents first
    removed obsolete code
    added support for icon name in applet button

artwork:
    mint-y:
        improved contrast in nemo sidebar
    switch to ubuntu fonts
    improved contrast (more saturation, less value)
    improved progressbars
    less transparency in terminal
    clear and dark action icons
    remove noto-sans, noto-sans-hinted, noto-sans-unhinted? (create stuttering in chromium)
    currently debating mint-y-darker
    package mint-y variations into flathub

blueberry:
    ability to connect/disconnect paired devices in systray
    migrated to python3

xed:
    print preview fixes
    toggle comments

wine:
    wine-installed + wine-desktop-files
    winehq-stable in repos
    mintinstall support for wine-installer
    rel notes
    desktop-file-utils

python-xapp
    GSettings widgets

dev guide

xreader:
    optional zoom factor indicator
    ported to meson
    no recent documents screen

xapps:
    ctrl+w/q

lightdm-settings
    autologin delay (timeout)

mintdesktop
    use xapp.GsettingsWidgets
    Button layout for CSD windows

mintsystem
    search is more visible
    apt showsrc command

mintsources
    add missing keys
    remove duplicate sources

system
    boot repair

Linux Mint 19.2 BETA bugs
=========================

    HiDPI
        mintlocale flags
        mintsources flags
        cinnamon theme settings

    mate:
        caja
            wrong icon in engrampa compress action
            wrong icon in change color action
        theme settings
            folder icons too big
            mint-x background too dark
        hidpi
            titlebar buttons are blurry

    xfce
        mintdesktop doesn't run

    artwork:
        missing yellow icons

Maintenance
===========

    update mirrors
    update translations for installation guide
    advertise community website in get involved page
    add sum to download page directly

Linux Mint 19.3
===============

    favorite/starred documents (nemo, xapps)

    https/apt:
        add https support for packages.linuxmint.com
        switch to https by default?
        add feature in mintsources to list https mirrors only?

    system:
        add CLI support for foreign packages list/removal/downgrade

    artwork:
        new logo
            branded backgrounds
            splash screens
            isolinux/grub menu
        new website theme
        use dark-variants for dark apps (xplayer..etc) in Mint-Y (needs fixes in mint-themes and marco)
        icons
            grey-on-grey icons (many in cinnamon-settings)
            review color variations in mint-y
        update MATE metathemes

    mintlocale:
        ability to set time: https://github.com/linuxmint/mintlocale/issues/36

    mintupdate:
        safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).

    timeshift: after restoration and before reboot, run hooks (could be used to adjust grub menu)

Ideas - Todos
==============

    fingerprint reader -> slick-greeter support
    https://askubuntu.com/questions/46501/why-can-other-users-see-the-files-in-my-home-folder

    artwork:
        revamp sound theme?
        cinnamon
            text-size to be configurable in panel zones?
            cinnamon/gtk mint-y: tooltips don't match theme

    help
        rtd security guide

    mate:
        consider brisk menu
        fix terminal apps not running (gnome-terminal --> mate-terminal)

    mintupdate:
        remember sorting of updates
        have an option for update manager to initiate a timeshift backup prior to applying upgrades?

    port mintstick to python3

    mintreport:
        detect missing l10n packages and hint at mintlocale
        warn about root password if not set

    artwork
        add dark variant support to Mint-Y (needs fixes in Caja/marco)
        cursor theme?
        sound theme?
        bump resolution of branded backgrounds

    slick
        would be nice to show release number

    xapps/cinnamon/nemo:
        don't ship icons with generic names in /usr/share/hicolor. All icons should be prefixed (cs-, xapp-, nemo-..etc..) so they don't conflict with other packages
        cinnamon-settings should use gsettingswidgets from xapp and retire its own

    xfce:
        consider backports https://blog.xfce.org/

    cinnamon
        gtk windows
        - When in tablet mode (that is, the screen is rotated and covering the keyboard) the RotateWindows key doesn't work anymore... It just does nothing...
        - menu-editor: picking a pixmap in /usr/share/pixmaps for a category results in no icon being shown in the menu.
        - Unable to unlock the screensaver via LDAP with libpam-ldap and nscd packages installed pointing to an openldap server.
        - csd power: https://github.com/GNOME/gnome-settings-daemon/commit/82af1816f32a26f28027ea7ce8edc79cd833bc76
        - in HiDPI, keyboard applet, the flags is not the proper size. Hovering it fixes it.
        - mounted volume applet: no notification when unmounting (as opposed to when it's done in nemo).
        - gwl: Enable "application name" label. Open FF, open at least two browser tabs. Close FF. The label slides over the icon and doesn't disappear: https://kepkuldes.com/image/UoNHl

    nemo
        better navbar
        consider sping loaded folders https://www.youtube.com/watch?v=gdUPrMjlLy8

    xed:
        option to remember past opened-documents

LMDE 4
======

remove debian-multimedia
add backports (priority 100)

Roadmap
=======

    main ideas
        mintsystem apt downgrade

    desktop-search:
        local files
        web engines
        recent
        apps
        dictionary
        translations

    mate:
        switch mozo for menulibre

    mintreport:
        dmesg errors
        foreign packages if pinned by mint
        wrong lsb info..etc.
        slow boot sequence
        slow shutdown sequence
        systray support

    mintupgrade
        list/address foreign packages post-upgrade

    implement an alarm clock

    cinnamon:
        cinnamon slow to start after boot --> delay execution of appsys/docinfo until the DE is loaded
        CSD: support mouse wheel speed? Evdev scrolling distance?
        preferences > keyboard > custom shortcuts. Used with a Spanish keyboard layout. Recorded: crtl+number and ctrl+Shift+number (e.g. ctrl+1 and ctrl+shift+1 = ctrl+!) they are recorded correctly. When using the shortcut the command defined in the shift combination is triggered with just ctrl+number (i.e. ctrl+1). The complete combination triggers nothing (i.e. ctrl+shift+1 does nothing) and the comand defined in ctrl+number can never be used. This worked in 17.3.
        track/troubleshoot shutdown sequence (user should know what is happening when shutdown isn't immediate)
        track/troubleshoot vsync, compositing, unredirected windows and policy
        todo list applet/desklet
        calendar events applet/desklet
        multiple clocks https://github.com/simonwiles/cinnamon_applets
        network applet: airplane mode (quick way to rfkill all)
        nemo: retire computer:/// place (which is completely useless) or revamp it into something better
        alt-tab and panel use icon provided by appsys, ignoring icon set by the application itself (example: a python window using widow.set_icon_name())
        actions in panel launchers aren't translated if not present in .desktop file
        When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
        Is there any reason why there are two names for the same item, eg. "Trash" and "Rubbish Bin"? Would it be better to standardise on only one name?
        add gnome-screenshot to panel, right-click and select "Take screenshot of a selected area". This runs gnome-screenshot -a.. it should work but it doesn't. Is it because of the panel launcher capturing the click event or something?

    xapps
        implement an app-sharing protocol to quickly move a document from one app to another

        gestures support:
            pinch:
                zoom document in pix
                zoom view in nemo

            swipe:
                previous/next document in pix

            scroll:
                sound-volume/seek in xplayer

            click:
                pause/resume in xplayer

            double-click:
                full-screen in xplayer
                full-screen in xviewer

        pix
            doesn't rotate videos when playing them
            vignettes should look better, and the same in all themes
            support prefer-dark-themes
            treeview in sidebar shows unecessary "(empty)" when dirs have no subdirs

    artwork:
        Tray icons are black with mint-y themes.
        mint-x-icons: network status icons have a dark background in panel 33px and bigger (sound icon looks wrong in 41px and bigger).
        mint-y The maximize/restore window control button doesn’t change visually between in maximized and restored state (default theme and Mint-Y-Dark)

    system:
        compiler optimization: consider optimizing compiled binaries for Cinnamon/Xapps

    HiDPI support:
        upstream apps using GTK2: Gimp, Hexchat, Tomboy.

R&D
===

    system
        consider enabling recommends

    network discovery:
        easy out-of-the-box interactions (messaging/presence/file-sharing) over the LAN
