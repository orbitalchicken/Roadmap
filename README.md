Implemented
===========

    Cinnamon:
        Support for HybridSleep
        network applet: Rescan for wireless network
        cinnamon-settings: spices revamp
        nemo-preview support animated gifs
        better translations for cinnamon-session, cinnamon-settings-daemon, nemo-extensions

    Slick:
        indicator tooltips
        support for numlockx
        optional panel indicators
        LDAP options (hiding user list, manual login)
        Added option for auto login

    mintsources ported to GTK3

    mintinstall:
        UI and nagivation revamp
        GTK3 + HiDPI
        User mode + aptdaemon backend
        speed improvements

    mintbackup:
        complete revamp
        user mode + aptdaemon backend
        revamped UI
        revamped threading and performance
        restricted to home dir
        always preserves perms/times

    Xapp window-progress now supported by:
        cinnamon
        nemo
        mintinstall
        mintstick
        mintdrivers
        mintbackup

    xplayer:
        removed xplayer-mozilla
        better fullscreen statusbar

Done - Awaiting repos/build
====================

    remove mintnanny and mintupload from default software selection
    cinnamon:
        enable hidpi by default

Linux Mint 18.3
===============

    implement an alarm clock
    add a dictionary
    install mp3 support without codecs?

    xed: support opening at particular line number, like sublime does

    nemo: ability to search string within files and open xed at line number

    mintbackup:
        place backups in .backup or exclude them by default?
        need user confirmation before overwriting existing files
        consider including some settings by default?

    cinnamon:
        settings: ability to enable hybrid sleep
        ccc: wacom - when no tablet is detected, remove fugly frame around content and fix bt settings button not linking towards blueberry
        menu keywords: looking for display in menu shows color first
        consider: notifications stay on desktop until mouse is moved + a few secs
        reconsider inhibiting onscreen keyboards (our keyboard doesn't do locales layouts and it's quite ugly)
        ccc display doesn't always show screen ID windows
        preferences > keyboard > custom shortcuts. Used with a Spanish keyboard layout. Recorded: crtl+number and ctrl+Shift+number (e.g. ctrl+1 and ctrl+shift+1 = ctrl+!) they are recorded correctly. When using the shortcut the command defined in the shift combination is triggered with just ctrl+number (i.e. ctrl+1). The complete combination triggers nothing (i.e. ctrl+shift+1 does nothing) and the comand defined in ctrl+number can never be used. This worked in 17.3.
        track/troubleshoot shutdown sequence (user should know what is happening when shutdown isn't immediate)
        nemo thumbnail error happens too often (too picky, does it always require root perms?)
        cinnamon slow to start after boot --> delay execution of appsys/docinfo until the DE is loaded
        track/troubleshoot vsync, compositing, unredirected windows and policy
        menu: consider adopting this layout (https://raw.githubusercontent.com/The-Panacea-Projects/Gnomenu/master/Screenshot.png), same as ours/mintmenu, only better.
        todo list applet/desklet
        calendar events applet/desklet
        multiple clocks https://github.com/simonwiles/cinnamon_applets
        menu: use search providers to search local files
        network applet: airplane mode (quick way to rfkill all)
        network applet: https://github.com/linuxmint/Cinnamon/issues/2746
        nemo: retire computer:/// place (which is completely useless) or revamp it into something better
        alt-tab and panel use icon provided by appsys, ignoring icon set by the application itself (example: a python window using widow.set_icon_name())
        actions in panel launchers aren't translated if not present in .desktop file
        sound: add an option to switch sound to HDMI when an HDMI output device is plugged
        hidpi issues: top of mint menu is cut off in HiDPI (1920×1280)
        gnome-system-monitor moves out of place in Expo
        When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
        Is there any reason why there are two names for the same item, eg. "Trash" and "Rubbish Bin"? Would it be better to standardise on only one name?
        add gnome-screenshot to panel, right-click and select "Take screenshot of a selected area". This runs gnome-screenshot -a.. it should work but it doesn't. Is it because of the panel launcher capturing the click event or something?
        In Nemo, right-click on "File System" -> "Properties" gives the details of the Home folder, not the File System, making it difficult to determine the overal disk space available.
        In Nemo, if i select a new tab, the folder name that appears in the tab appears with a separation line underneath, separating the tab name from the list of files in the folder. This style of separation is onconsistent to XED, where the Tab name and content under that tab have no such visible horizontal separation line.
        system settings modules should be singletons (only one possible instance) and have their window use their own icon (in alt-tab, and window list)
        [Michael] bg gets erased after suspend? https://bugzilla.gnome.org/show_bug.cgi?id=739178

    xviewer
        make the position (left/right, top/bottom won’t make much sense) of the sidebar configurable (like the gallery) at least via dconf!

    xapps
        add an option to blank other monitors when in full screen in xviewer/xreader/pix
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

    mintwelcome:
        consider accompanying the user and hinting at things he/she might want to do (codecs, popular settings, popular apps etc..)

    mintupdate:
        mint notices
        implement rules and notification system:
            dmesg errors
            foreign packages if pinned by mint
            wrong lsb info..etc.
            slow boot sequence
            slow shutdown sequence
        safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).
        notice to reboot the computer when appropriate
        kernelwindow: make kernel series column desc-sorted and select the active series

    mintdrivers:
        microcode package description is misleading in driver manager, should it be removed?

    mate 1.20
        sound events vs sound themes
        multi-monitor: caja doesn't always show the desktop on the primary monitor (using a laptop as main/left monitor, and HDMI screen with higher res on the right, it surprisingly ends up showing icons on the right screen)
        Right-click on the desktop -> No templates installed

    system:
        for non-english speaking people, it is not possible to change language, nor keyboard settings, when starting livemedia.
        implement a crash-intercepter
        compiler optimization: consider optimizing compiled binaries for Cinnamon/Xapps
        kernel 4.8: screen rotates 90º counter-clockwise automatically.

    artwork:
        Tray icons are black with mint-y themes.
        Mint-Y themes Shade option is unavailable
        mintwelcome: don't use 32px png icons
        Choose places icons for Mint-Y
        mint-x-icons: network status icons have a dark background in panel 33px and bigger (sound icon looks wrong in 41px and bigger).
        mint-y The maximize/restore window control button doesn’t change visually between in maximized and restored state (default theme and Mint-Y-Dark)

    xplayer:
        add CD+G support
        wrong aspect ratio http://pasteall.org/pic/show.php?id=114543
        remove xplayer-mozilla

    xreader:
        History buttons confuse users (they think they're Next Page and Previous Page buttons)

    synaptic:
        window titled “Could not download all repository indexes" is way too tall on a 1366×768 laptop screen

    kde:
        SDDM stays in autologin after OEM install

    xfce:
        upgrade xfce-terminal to 0.8.0?

R&D
===

    mintupdate:
        prompt for reboot after kernel install?

    nemo:
        remove duplication between Eject and Safely Remove (for removable devices).

    system
        consider adding snapd
        consider adding flatpak
        consider enabling recommends

    review logind.conf changes in:
        MATE
        Xfce
        KDE

    ubiquity:
        inhibit sessions via libxapp (need to do it in KDE too)

    libindicator++?
        client-rendered icon/menu (ala libindicator)
        support all the features from GTK statusicon (tooltips, left/right clicks etc..)

    use aptdaemon?
        aptdaemon doesn't work in LMDE and is being abandoned upstream
        in mintupdate, remove dep on synaptic, remove admin rights for checkAPT.py
        in mintwelcome and codec menu entry, switch from apturl to aptdaemon
        in mintsources, remove dep on synaptic
        remove synaptic from default selection
        remove synaptic from mintmenu's favorites

    network discovery:
        easy out-of-the-box interactions (messaging/presence/file-sharing) over the LAN

    windows compatibility layer:
        seamless wine integration

    HiDPI support:
        upstream apps using GTK2: Gimp, Hexchat, VLC, Pidgin, Tomboy.
        mint projects using GTK2: gksu

LMDE 3
======

    gnome-calculator app title is "gnome-calculator"
    live-installer should show partition labels
