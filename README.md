Release
=======
    rel notes
    whatsnew
    FF in live repo
    cinnamon: all spices should work
        applets
        [DONE] desklets
        extensions
        themes

    kernel 4.8.0
        i2c not detected
        Buffer I/O error on dev sdb, logical block 22220, lost async page write

    cinnamon:
        would battery be better swapped with user applet?
        looking for display in menu shows color first
        display resolution change freezes cinnamon

    Slick greeter session badges look blurry in HiDPI

    DONE:
        lightdm-settings new filepickers
        Slick greeter doesn't show any background in live mode
        mintupdate help: index/about aren't localized.
        Better screenshots in installation slideshow

    FIXED:
        EFI grub version is incorrect
        mintupdate:
            meta update kernel should know the right name
            when new mintupdate and new kernel, only show new mintupdate



Linux Mint 18.3
===============

    implement an alarm clock
    add a dictionary

    cinnamon:
        track/troubleshoot shutdown sequence (user should know what is happening when shutdown isn't immediate)
        nemo thumbnail error happens too often (too picky, does it always require root perms?)
        cinnamon slow to start after boot --> delay execution of appsys/docinfo until the DE is loaded
        track/troubleshoot vsync, compositing, unredirected windows and policy
        add cinnamon-session (present but inactive) and cinnamon-settings-daemon to Launchpad/cinnamon-translations
        menu: consider adopting this layout (https://raw.githubusercontent.com/The-Panacea-Projects/Gnomenu/master/Screenshot.png), same as ours/mintmenu, only better.
        todo list applet/desklet
        calendar events applet/desklet
        multiple clocks https://github.com/simonwiles/cinnamon_applets
        menu: use search providers to search local files
        network applet: airplane mode (quick way to rfkill all)
        network applet: https://github.com/linuxmint/Cinnamon/issues/2746
        nemo: retire computer:/// place (which is completely useless) or revamp it into something better
        network applet: if possible, add a little refresh icon to ask for a new scan
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
            should use a generic name in the application menu
            vignettes should look better, and the same in all themes
            support prefer-dark-themes

    mintinstall:
        UI redesign
        when apt cache is missing, it just says not available. Instead it could tell the user or even help the user to refresh the cache.
        redesign main page to feature essential apps

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

    mate 1.20
        sound events vs sound themes
        multi-monitor: caja doesn't always show the desktop on the primary monitor (using a laptop as main/left monitor, and HDMI screen with higher res on the right, it surprisingly ends up showing icons on the right screen)

    system:
        for non-english speaking people, it is not possible to change language, nor keyboard settings, when starting livemedia.
        implement a crash-intercepter
        compiler optimization: consider optimizing compiled binaries for Cinnamon/Xapps

    artwork:
        Tray icons are black with mint-y themes.
        Mint-Y themes Shade option is unavailable
        mint-x-icons: in MATE (with a high panel), network status icons have a dark background in 32px and bigger. they would look much better in the panel with a transparent bg like other icons.
        mintwelcome: don't use 32px png icons
        Choose places icons for Mint-Y
        slick-greeter: padding issue when hovering session button

R&D
===

    mintbackup:
        consider using another alternative?

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

    firefox:
        enable bookmark toolbar by default
        enable plugins by default

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
        seemless wine integration

    HiDPI support:
        upstream apps using GTK2: Gimp, Hexchat, VLC, Pidgin, Tomboy.
        mint projects using GTK2: mintinstall, mintsources, gksu, cinnamon's mount dialog (seen when asking for a password for an encrypted external HDD).

Linux Mint 18.2 [Implemented]
=============================

    mate 1.18
        swith MATE to GTK3
        switch mintmenu to GTK3

LMDE 3
======

    gnome-calculator app title is "gnome-calculator"
    mintsystem: /usr/local/bin/pastebin shadows xapps-common: /usr/bin/pastebin
    mint-md5sum script in /usr/local/bin ?
    live-installer should show partition labels
