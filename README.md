Linux Mint 19
=============

ff in live repo

need_update:
  - minecraft-installer (works with JRE8?)
  - whatsapp-desktop
  - google-earth-pro-stable

- gist-paste still used in xapps/mintsystem
- update translations
- update installation guide translations

release upgrade tool:
  - migrate to pkexec
  - make sure timeshift config is in place
  - make sure mdm isn't in use anymore
  - suggestions:
    - Re-enable 3rd party repositories after upgrade. A backup of the APT sources gets stored in ./Upgrade-Backup/APT but the tutorial didn't cover this or what to do with it (probably best to just find what the 3rd party repositories were and re-enable them manually from instructions on their website). Important for things like Google Chrome.
    - mintupgrade replaces user modified configuration files in /etc without prompting, leaving .dpkg-old files behind. Perhaps cover this tidbit in the tutorial.

Non-blocking bugs
=================

artwork:
  - MyPaint and Pinta have the same icon
  - Firefox bookmarks don’t use the folder color picked in the Cinnamon theme setting.
  - remove humanity-icon-theme and ubuntu-mono
  - mintwelcome icon
  - grey-on-grey icons (many in cinnamon-settings)
  - mint-y-icons: yellow and teal folders missing.
  - cinnamon: The progress indicator in the panel should be the same color as the chosen theme. Not just green.
  - cinnamon themes hardcode the font

cinnamon:
  - removing favorites isn't intuitive, there should be a context menu option
  - Application switcher items are not properly selected https://github.com/linuxmint/Cinnamon/issues/7623
  - NFS mount not visible in Nemo left menu. How to reproduce: install nfs-common, mount NFS folder.
  - Even after authorize Samba in gufw, Nemo doesn’t show the local network and machine on it. I must manually type smb://user@ip to get in (after workgroup and password) In Mint 18 that was directly available.
  - ccc: in color plugin, add a profile, browse it and click "View details". If gnome-color-manager is not installed, the plugin should ask packagekit (over dbus) to install it. This doesn't work.
  - If the screen is rotated, then the touch screen digitiser and trackpad both move the cursor in a direction mirrored to what is expected ie move your finger to the left on the screen and the cursor moves to the right. This works properly in Gnome.
  - When in tablet mode (that is, the screen is rotated and covering the keyboard) the RotateWindows key doesn't work anymore... It just does nothing...
  - menu-editor: picking a pixmap in /usr/share/pixmaps for a category results in no icon being shown in the menu.
  - Unable to unlock the screensaver via LDAP with libpam-ldap and nscd packages installed pointing to an openldap server.
  - csd power: https://github.com/GNOME/gnome-settings-daemon/commit/82af1816f32a26f28027ea7ce8edc79cd833bc76

- slick greeter: On a VirtualBox setup with three users, if any user but the first is auto given focus, the username is present but the box only has half height, cut off with no password entry lower half. You can type where that password entry half of the box would be , and it works, but the characters don't show, so it's a visual display problem, only apparently happening on boot.
- Gnome calendar does not have an icon on the top left in the new Gnome decorations, only a cog icon is shown.

LMDE 3
======

- lightdm asks username to be typed

backports:
  - flatpak/ostree/appstream?
  - meson/debhelper/dh_autoreconf?

Linux Mint 19.1
===============

    help
        rtd dev guide
        rtd security guide

    update installation slideshow
        internet: flash/java
        movies: DVD
        connected: refs to ICQ..
        mint-y theme.

    mate:
        consider brisk menu

    mintwelcome:
        add firewall enablement to welcome app?

    mintupdate:
        safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).
        notice to reboot the computer when appropriate
        purge old kernels? https://github.com/Pjotr123/purge-old-kernels-2
        systray icon or infobar to notify user of new Mint versions
        remember sorting of updates
        have an option for update manager to initiate a timeshift backup prior to applying upgrades?

    port mintstick to python3
    update inxi

    mintreport:
        detect missing l10n packages and hint at mintlocale
        warn about root password if not set

    artwork
        add dark variant support to Mint-Y (needs fixes in Caja)
        mint-y lack of borders without compositing
        gtk color variations
        cursor theme?
        sound theme?
        slightly taller/darker panel?
        generic menu icon?
        bump resolution of branded backgrounds

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

    libindicator++?
        client-rendered icon/menu (ala libindicator)
        support all the features from GTK statusicon (tooltips, left/right clicks etc..)

    network discovery:
        easy out-of-the-box interactions (messaging/presence/file-sharing) over the LAN

    windows compatibility layer:
        seamless wine integration
