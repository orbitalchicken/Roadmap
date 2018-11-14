Linux Mint 19.1 DONE
====================

mintlocale im
    separate app
    cinnamon applet hides when fcitx is running
    clearer instructions, tells you what to use, how to switch methods
    UI revamp

mintsources
    UI revamp
    dbgsyms option
    duplicate entries

mintupdate
    kernel window supports mainline kernels

mintwelcome
    firewall configuration

cinnamon
    cjs GC improvements
    configurable vsync
    embedded clutter/cogl
    muffin improvements
    inhibit applet shows inhibitors
    highlight logout/shutdown button in session dialogs
    calculator configurable in preferred apps
    xscreensaver support removed from csr
    xlets can have custom widgets in their settings

nemo
    speed improvements https://github.com/linuxmint/nemo/commit/4f1af958b15aaf3c5e6221ae80f77c1b138a5c02 https://github.com/linuxmint/nemo/commit/98843e26b48cd3526cacfe90cfa4ba201d1f3aee https://github.com/linuxmint/nemo/commit/61368e3fc33c0d662f45731d6bbb2a28fc5023ca
    improvements to icon sizes and spacing
    prefs UI
    python extensions ported to python3
    desktop settings UI
    per folder thumbnails

libxapp
    sidebar with icons
    icon chooser button+dialog

xed
    show spaces/tabs in statusbar

xplayer
    moved to python3

symbolic status icons:
    mint-y -> new icons
    onboard
    redshift
    network-manager-gnome (network-manager-applet)
    mate-media (mate-volume-control-applet)

mint-y contrast
mint-y color variations

Linux Mint 19.1 TO BE DONE
===========================

print test page https://github.com/linuxmint/linuxmint/pull/77/files

system
    plymouth: center text, hide "None" value


update installation slideshow
    internet: flash/java
    movies: DVD
    connected: refs to ICQ..
    mint-y theme.

mintupdate:
    don't gather packages in checkAPT as root: https://github.com/linuxmint/mintupdate/issues/379
    safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).
    notice to reboot the computer when appropriate
    purge old kernels? https://github.com/Pjotr123/purge-old-kernels-2

artwork:
  - MyPaint and Pinta have the same icon
  - grey-on-grey icons (many in cinnamon-settings)
  - mint-y-icons: teal folders missing.

- slick greeter: On a VirtualBox setup with three users, if any user but the first is auto given focus, the username is present but the box only has half height, cut off with no password entry lower half. You can type where that password entry half of the box would be , and it works, but the characters don't show, so it's a visual display problem, only apparently happening on boot.

ubiquity:
    /target/swapfile appears in /etc/crypttab when installing with home dir encryption, causes swap to malfunction https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1759253 https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1670336

Non-blocking bugs
=================

artwork:
  - mintwelcome icon
  - cinnamon themes hardcode the font

cinnamon:
  - NFS mount not visible in Nemo left menu. How to reproduce: install nfs-common, mount NFS folder.
  - Even after authorize Samba in gufw, Nemo doesn’t show the local network and machine on it. I must manually type smb://user@ip to get in (after workgroup and password) In Mint 18 that was directly available.
  - If the screen is rotated, then the touch screen digitiser and trackpad both move the cursor in a direction mirrored to what is expected ie move your finger to the left on the screen and the cursor moves to the right. This works properly in Gnome.
  - When in tablet mode (that is, the screen is rotated and covering the keyboard) the RotateWindows key doesn't work anymore... It just does nothing...
  - menu-editor: picking a pixmap in /usr/share/pixmaps for a category results in no icon being shown in the menu.
  - Unable to unlock the screensaver via LDAP with libpam-ldap and nscd packages installed pointing to an openldap server.
  - csd power: https://github.com/GNOME/gnome-settings-daemon/commit/82af1816f32a26f28027ea7ce8edc79cd833bc76

- Gnome calendar does not have an icon on the top left in the new Gnome decorations, only a cog icon is shown.

Linux Mint 19.1
===============

    help
        rtd dev guide
        rtd security guide

    mate:
        consider brisk menu

    mintupdate:
        systray icon or infobar to notify user of new Mint versions
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

    cinnamon
        enable recent by default, fix mem leak https://github.com/linuxmint/cinnamon-desktop/commit/2015cc0f8a8fe46384225b0cf10df45f7d3d9315#diff-7ad95a88738c9b5cd253f469add87640

    slick
        would be nice to show release number

    xapps/cinnamon/nemo:
        don't ship icons with generic names in /usr/share/hicolor. All icons should be prefixed (cs-, xapp-, nemo-..etc..) so they don't conflict with other packages

Linux Mint 19.2
===============

cinnamon
    gtk windows
    merge appsys and cmenus
    ditch docinfo

nemo
    better navbar

LMDE 4
======

remove debian-multimedia

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
        migrate to systemd-coredump (to make it compatible with LMDE)
        systray support
        use systemd-coredump

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
