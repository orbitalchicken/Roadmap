Linux Mint 19
=============

    gist-paste still used in xapps/mintsystem
    update translations
    update installation slideshow
    apt sandboxing warning https://bugs.launchpad.net/ubuntu/+source/synaptic/+bug/1522675

    gdebi
        pkexec doesn’t work when double-clicking from nemo https://bugs.launchpad.net/ubuntu/+source/gdebi/+bug/1760910 https://bugs.launchpad.net/ubuntu/+source/gdebi/+bug/1749728

    Artwork
        icons:
            thunar/caja -> use app icon? (is folder appropriate. doesn't currently change color with color variation)
            mimetypes
            actions (gtk-yes in ubiquity, white navigation in caja..etc)
            grey-on-grey icons (many in cinnamon-settings)
        gtk:
            folder-color restore button
            color variations
        tara backgrounds
        default look:
            slightly taller/darker panel?
            generic menu icon?

    mintwelcome:
        write content and hint at things users might want to do (codecs, popular settings, popular apps etc..)

    xfce:
        no sound indicator (xfce4-pulseplugin needs to be added)
        add notif and power plugins
        icons for plugins

    need_update:
        minecraft-installer
        whatsapp-desktop
        spotify-client
        dropbox
        google-earth-pro-stable
        skypeforlinux

    help
        rtd dev guide
        rtd security guide

    release upgrade tool
        migrate to pkexec
        make sure timeshift config is in place
        make sure mdm isn't in use anymore
        suggestions:
            Re-enable 3rd party repositories after upgrade. A backup of the APT sources gets stored in ~/Upgrade-Backup/APT but the tutorial didn't cover this or what to do with it (probably best to just find what the 3rd party repositories were and re-enable them manually from instructions on their website). Important for things like Google Chrome.
            mintupgrade replaces user modified configuration files in /etc without prompting, leaving *.dpkg-old files behind. Perhaps cover this tidbit in the tutorial.

    release notes
        warning about guest accounts not being confined
        warning about home directory encryption not unmounting on logout

LMDE 3
======

    lightdm asks username to be typed

    Backports
        flatpak/ostree/appstream?
        meson/debhelper/dh_autoreconf?

Linux Mint 19.1
===============

    mate:
        consider brisk menu

    mintupdate:
        safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).
        notice to reboot the computer when appropriate
        purge old kernels? https://github.com/Pjotr123/purge-old-kernels-2
        systray icon or infobar to notify user of new Mint versions

    mintreport:
        detect missing l10n packages and hint at mintlocale
        warn about root password if not set

    artwork
        add dark variant support to Mint-Y (needs fixes in Caja)
        mint-y lack of borders without compositing

    cinnamon
        enable recent by default, fix mem leak https://github.com/linuxmint/cinnamon-desktop/commit/2015cc0f8a8fe46384225b0cf10df45f7d3d9315#diff-7ad95a88738c9b5cd253f469add87640
        muffin to render titlebars with GTK themes (i.e. drop support for metacity themes)
        investigate https://www.phoronix.com/scan.php?page=news_item&px=GNOME-Post-3.28-Perf-Work
        PR on network applet to use libnm/libnma (needs fixes in Debian Stretch)
        nemo
            video thumbnails are blurry
    mate
        marco: add support for GTK dark variants

    system
        plymouth: center text, hide "None" value

    slick
        would be nice to show release number

    xapps/cinnamon/nemo:
        don't ship icons with generic names in /usr/share/hicolor. All icons should be prefixed (cs-, xapp-, nemo-..etc..) so they don't conflict with other packages

Roadmap
=======

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

    implement an alarm clock

    cinnamon:
        CSD/Cinnamon should set GtkSettings' gtk-print-preview-command to "xreader-previewer -u -p %s %f" (test by launching xreader from terminal, ask for a print preview and see error trying to launch evince on stdout)
        cinnamon slow to start after boot --> delay execution of appsys/docinfo until the DE is loaded
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

    make the GOA frontend an Xapp (it should be cross-DE), disable buggy/irrelevant services

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

        xreader
            xreader-previewer use full-color icons

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

artwork:
    symbolic icons

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
    word completion plugin

mint-tools:
    transition to aptdaemon/pkexec and gtk3/python3 (for remaining ones)

mintsources:
    PPA: show already installed packages

mintupdate:
    can be backported (locales ...)
    shortcut window
    timeshift integration replace levels/policy
    kernel install rely on meta
    automatic updates
    new type to mark updates from other PPA/repos
    switch type icons to symbolics
    mintupdate-tool -> mintupdate-cli
    support for lowlatency kernels

mintinstall:
    python3
    better keyboard navigation
    better search (search in categories, async)
    use internal cache for apt/flatpak with better abstraction (this can potentially be used in mintupdate at a later stage)
    numerous UI improvements and animations
    loading and activity indicators
    old screenshots are cleaned up
    flatpak support for .flatpakref/.flatpakrepo (can click from website etc..)
    flatpak size/version

mintstick:
    exfat support

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

software selection:
    pidgin removed
    ntp/ntpdate removed in Cinnamon (done by systemd)
    gnome-calendar added
    gnome-logs replaces gnome-system-logs in Cinnamon
    codecs now include ms fonts

slick-greeter:
    user can specify which monitor to use

xfce:
    whisker 2.1.7
    added gnome-logs