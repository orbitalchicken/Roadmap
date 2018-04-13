
Implemented
===========

cinnamon
    new combo options for spices settings (combo options, valid values)
    sound applet:
        can now also mute input on middle-click
        next/previous track on right/left scroll
        album art keep aspect ratio
    sound volume can go all the way to 150%
    better CSD windows support: titlebar click actions and button layouts
    faster to map windows
    better window animations
    better window list thumbnails
    notifications:
        can be shown at the bottom of the screen
        close button
        no more fade-effect
        no longer vanish when focusing caller app
    ability to show desklets on top of windows thanks to show-desklets applet, or Super+Tab

nemo:
    symbolic icons
    faster view render
    stronger extension code
    File search:
        async search
        simplify UI/features

improvements to mint-y-icons
    improved icons
    backports from moka
    crisper HiDPI with @2x icons

xreader
    recent view
    preferences, optional toolbar buttons
    remove annotations
    epub support (thumbs fixed, allow to save document)
    thumbnail zoom
    smooth scrolling

xed
    refined look/feel with GTK 3.22 support
    shortcuts window
    new preference window (from xapps)

mintsources:
    PPA: show already installed packages

mintupdate:
    can be backported (locales ...)
    shortcut window
    timeshift integration replace levels/policy
    kernel install rely on meta
    automatic updates

mintwelcome:
    new layout

pia-manager:
    remembers username/password/gateway

docs
    translation guide
    troubleshooting guide

hidpi:
    2x icons
    pkexec instead of gksu

Linux Mint 18.3
===============

    Release
        rel_notes
            Add instructions to upgrade to HWE Xorg 1.19

Maintenance
===========

    update cinnamon-translations

    mintinstall:
        continue to show window-progress even when app page isn't visible
        install flatpak deps via API to better report progress
        keyboard navigation issues

    mintreport:
        warn about root password if not set

Linux Mint 19
=============

    cinnamon:
        investigate https://www.phoronix.com/scan.php?page=news_item&px=GNOME-Post-3.28-Perf-Work

    make the GOA frontend an Xapp (it should be cross-DE), disable buggy/irrelevant services

    hidpi
        cinnamon startup apps icons are blurry

    redshift
        doesn't die when logging out

    Artwork
        would be nice if slick showed our release number
        remove preload of cinnamon themes

    desktop-search:
        local files
        web engines
        recent
        apps
        dictionary
        translations

    mintwelcome:
        write content and hint at things users might want to do (codecs, popular settings, popular apps etc..)

    mintreport:
        detect missing l10n packages and hint at mintlocale

    mintupdate:
        safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).
        notice to reboot the computer when appropriate
        purge old kernels? https://github.com/Pjotr123/purge-old-kernels-2
        systray icon or infobar to notify user of new Mint versions

    system:
        compiler optimization: consider optimizing compiled binaries for Cinnamon/Xapps

    cinnamon:
        cinnamon slow to start after boot --> delay execution of appsys/docinfo until the DE is loaded
        enable recent by default, fix mem leak https://github.com/linuxmint/cinnamon-desktop/commit/2015cc0f8a8fe46384225b0cf10df45f7d3d9315#diff-7ad95a88738c9b5cd253f469add87640

    nemo:
        Skip GVFS when possible
        Performance issues:
            File operations:
                Mouse-cursor lag
            Loading views:
                switching views is slower than reloading them
                existing thumbs are loaded asynchronously
                loading is slower than with ls (could be Gvfs, could be the way we render view in GTK. For 25k elements, 0.4s with ls, up to 6s in icon view for Nemo/Caja)
        video thumbnails are blurry

Roadmap
=======

    mintreport:
        dmesg errors
        foreign packages if pinned by mint
        wrong lsb info..etc.
        slow boot sequence
        slow shutdown sequence

    implement an alarm clock

    cinnamon:
        CSD: support mouse wheel speed? Evdev scrolling distance?
        menu keywords: looking for display in menu shows color first
        preferences > keyboard > custom shortcuts. Used with a Spanish keyboard layout. Recorded: crtl+number and ctrl+Shift+number (e.g. ctrl+1 and ctrl+shift+1 = ctrl+!) they are recorded correctly. When using the shortcut the command defined in the shift combination is triggered with just ctrl+number (i.e. ctrl+1). The complete combination triggers nothing (i.e. ctrl+shift+1 does nothing) and the comand defined in ctrl+number can never be used. This worked in 17.3.
        track/troubleshoot shutdown sequence (user should know what is happening when shutdown isn't immediate)
        track/troubleshoot vsync, compositing, unredirected windows and policy
        menu: consider adopting this layout (https://raw.githubusercontent.com/The-Panacea-Projects/Gnomenu/master/Screenshot.png), same as ours/mintmenu, only better.
        todo list applet/desklet
        calendar events applet/desklet
        multiple clocks https://github.com/simonwiles/cinnamon_applets
        network applet: airplane mode (quick way to rfkill all)
        nemo: retire computer:/// place (which is completely useless) or revamp it into something better
        alt-tab and panel use icon provided by appsys, ignoring icon set by the application itself (example: a python window using widow.set_icon_name())
        actions in panel launchers aren't translated if not present in .desktop file
        gnome-system-monitor moves out of place in Expo
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
        Mint-Y themes Shade option is unavailable
        mint-x-icons: network status icons have a dark background in panel 33px and bigger (sound icon looks wrong in 41px and bigger).
        mint-y The maximize/restore window control button doesn’t change visually between in maximized and restored state (default theme and Mint-Y-Dark)

R&D
===

    system
        consider enabling recommends

    review logind.conf changes in:
        MATE
        Xfce

    libindicator++?
        client-rendered icon/menu (ala libindicator)
        support all the features from GTK statusicon (tooltips, left/right clicks etc..)

    network discovery:
        easy out-of-the-box interactions (messaging/presence/file-sharing) over the LAN

    windows compatibility layer:
        seamless wine integration

    HiDPI support:
        upstream apps using GTK2: Gimp, Hexchat, VLC, Pidgin, Tomboy.
