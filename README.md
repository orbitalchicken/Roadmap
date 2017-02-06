
Maintenance
===========

    release process:
        add mini to store
        add new hoods

    csd: 100% CPU?
    mdm: utils scripts mdm-stop etc.. aren't in the package
    cinnamon-session: port https://github.com/mate-desktop/mate-session-manager/commit/3e8cab348e37b9879fa558e56e05069987c6c65a
    mintdesktop: https://github.com/linuxmint/mintdesktop/pull/16
    mintupdate: changelog for 4.8 kernels doesn't work

Linux Mint 18.2 [Planned]
=========================

    XAPPS:
        gestures support:
            pinch:
                zoom document in xreader
                zoom document in xviewer
                zoom document in pix
                zoom view in nemo

            swipe:
                previous/next document in xviewer
                previous/next document in pix
                previous/next page in xreader

            scroll:
                sound-volume/seek in xplayer

            click:
                pause/resume in xplayer

        xed:
            sorting lines:
                add a simple Edit->Sort Lines (F9), which sorts the selection or the entire file (if no selection is done)
                make sure it's undoable
                remove the sort plugin
            import libpeas support from gedit, to allow python3 extensions
            add word-wrap setting to View menu and buttons available in the toolbar customization
            mousewheel across tabs

        xplayer:
            focus window when a video file is opened
            visualizations don't work
            keyboard shortcut:
                s -> subtitles
                l -> language
                etc... try to follow other standards in other players
            Can’t play TS video files?

        pix
            doesn't rotate videos when playing them
            should use a generic name in the application menu

    Mint tools:
        mintupdate:
            provide a CLI and automated upgrades
            add shortcut keys
            mint notices
            implement rules and notification system:
                dmesg errors
                foreign packages if pinned by mint
                wrong lsb info..etc.
                slow boot sequence
                slow shutdown sequence
            safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).

        mintwelcome:
            consider accompanying the user and hinting at things he/she might want to do (codecs, popular settings, popular apps etc..)

        mintsources:
            Select all button in foreign pkgs: https://github.com/linuxmint/mintsources/issues/59

    Cinnamon performance:
        track/troubleshoot shutdown sequence (user should know what is happening when shutdown isn't immediate)
        nemo thumbnail error happens too often (too picky, does it always require root perms?)
        nemo seeing RW volume as read-only and failing to write on it (in this case the user can write to the volume via command line but not via nemo)
        cinnamon slow to start after boot
        track/troubleshoot vsync, compositing, unredirected windows and policy

    Cinnamon features/issues:
        implement basic global lockdown (i.e. locked by root)
        add cinnamon-session (present but inactive) and cinnamon-settings-daemon to Launchpad/cinnamon-translations
        mouse/touchpad: fix sensitivity settings (shouldn't be inverted... should be described as motion-threshold or even better, as what they actually do). Also, add a way to reset their value.
        add a printer applet
        menu: consider adopting this layout (https://raw.githubusercontent.com/The-Panacea-Projects/Gnomenu/master/Screenshot.png), same as ours/mintmenu, only better.
        todo list applet/desklet
        calendar events applet/desklet
        multiple clocks https://github.com/simonwiles/cinnamon_applets
        menu: use search providers to search local files
        review default panel layout
        network applet: airplane mode (quick way to rfkill all)
        menu: look-n-feel, make searchbox seemless
        spices: all spices should work
        hidpi setting should be in Displays, not in General
        add frequency in monitor settings

    blueberry:
        send files both ways over bluetooh
        cinnamon applet

    artwork:
        Tray icons are black with mint-y themes.
        Mint-Y themes Shade option is unavailable
        mint-x-icons: in MATE (with a high panel), network status icons have a dark background in 32px and bigger. they would look much better in the panel with a transparent bg like other icons.
        mintupload: use icon names rather than path to SVG
        mintwelcome: don't use 32px png icons
        Choose places icons for Mint-Y
        isolinux splash http://pasteall.org/pic/show.php?id=109630

    display manager:
        mdm:
            consider moving prime support away from the logout sequence and place it fully in the login sequence
            in live mode: can't log in using Mint and blank password
            preselect user if only one user is present in the list
            configurable slideshow
            Webkit preview, process doesn't die when window is closed
            Webkit preview, mint-X doesn't show anything, only background
        ligtdm: experiment with implemeting a new alternative greeter

    system:
        ubiquity: don't set the root password

Linux Mint 18.2 [Optional]
==========================

    cinnamon features:
        nemo: retire computer:/// place (which is completely useless) or revamp it into something better
        network applet: if possible, add a little refresh icon to ask for a new scan
        alt-tab and panel use icon provided by appsys, ignoring icon set by the application itself (example: a python window using widow.set_icon_name())

    cinnamon issues:
        actions in panel launchers aren't translated if not present in .desktop file
        sound: add an option to switch sound to HDMI when an HDMI output device is plugged
        hidpi issues: top of mint menu is cut off in HiDPI (1920×1280)
        gnome-system-monitor moves out of place in Expo
        when battery is very low, battery icon isn't red.. 2% charge, with less than 5 minutes to go, still not red.. bar is red in CCC, icon is red in notification.. but not in applet (and also not in the CCC icon itself either)
        When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
        Is there any reason why there are two names for the same item, eg. "Trash" and "Rubbish Bin"? Would it be better to standardise on only one name?
        add gnome-screenshot to panel, right-click and select "Take screenshot of a selected area". This runs gnome-screenshot -a.. it should work but it doesn't. Is it because of the panel launcher capturing the click event or something?
        In Nemo, right-click on "File System" -> "Properties" gives the details of the Home folder, not the File System, making it difficult to determine the overal disk space available.
        In Nemo, if i select a new tab, the folder name that appears in the tab appears with a separation line underneath, separating the tab name from the list of files in the folder. This style of separation is onconsistent to XED, where the Tab name and content under that tab have no such visible horizontal separation line.
        system settings modules should be singletons (only one possible instance) and have their window use their own icon (in alt-tab, and window list)

    xviewer
        “Disable Dark Theme” doesn’t work, if i’m right when i assume it should do “gsettings set org.x.viewer.view use-background-color false”?
        after a fullscreen-view the sidebar is gone and must be enabled manually again.
        please make the position (left/right, top/bottom won’t make much sense) of the sidebar configurable (like the gallery) at least via dconf!

    xapps
        add an option to blank other monitors when in full screen in xviewer/xreader/pix
        implement an app-sharing protocol to quickly move a document from one app to another

    mintinstall:
        UI redesign
        when apt cache is missing, it just says not available. Instead it could tell the user or even help the user to refresh the cache.
        redesign main page to feature essential apps

    mate 1.18
        swith MATE to GTK3
        switch mintmenu to GTK3
        mintemenu: focus issues in /var/log/syslog
        sound events vs sound themes
        multi-monitor: caja doesn't always show the desktop on the primary monitor (using a laptop as main/left monitor, and HDMI screen with higher res on the right, it surprisingly ends up showing icons on the right screen)

    system:
        new users: perms at 750 by default? http://www.techrepublic.com/blog/it-security/managing-default-unix-file-permissions-with-adduser-and-umask/.
        for non-english speaking people, it is not possible to change language, nor keyboard settings, when starting livemedia.

R&D:
====

    mintbackup:
        consider using another alternative?

    mintupdate:
        prompt for reboot after kernel install?

    nemo:
        remove duplication between Eject and Safely Remove (for removable devices).

    system
        consider adding snapd
        consider adding support for xdg-apps, flatpack
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
        upstream apps using GTK2: Banshee, Gimp, Hexchat, VLC, Pidgin, Tomboy.
        mint projects using GTK2: mdmsetup, mintinstall, mintsources, gksu, cinnamon's mount dialog (seen when asking for a password for an encrypted external HDD).

