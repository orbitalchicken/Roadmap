
Maintenance
===========

    cinnamon-spices website:
        reimplement css
        handle utf-8, see comments on http://cinnamon-spices.linuxmint.com/applets/view/171

Linux Mint 18.1
===============

    update translations
    installer slideshows -> banshee
    xed search:
        typing shouldn't move to next result
        pressing case button should perform the search
    ubiquity: don't set the root password
    release process:
        update screenshots for 18.x
        simplify steps and automate verify page information
        update FF in live repo
    system:
        consider removing thermald? test impact of idle forcing on video playback (observed on macbook)

    xfce:
        upgrade whisker menu 1.6.1 / 2.0.2?

    kde:
        installer: continue button greyed out when not enough HDD

Linux Mint 18.2
===============

    xed:
        sorting lines:
            add a simple Edit->Sort Lines (F9), which sorts the selection or the entire file (if no selection is done)
            make sure it's undoable
            remove the sort plugin
        import libpeas support from gedit, to allow python3 extensions
        add word-wrap setting to View menu and buttons available in the toolbar customization

    xplayer:
        focus window when a video file is opened
        visualizations don't work

    xreader
        support gestures to zoom

    xviewer/xreader/pix
        add an option to blank other monitors when in full screen

    pix
        doesn't rotate videos when playing them
        should use a generic name in the application menu
        support gestures to zoom

    xviewer
        “Disable Dark Theme” doesn’t work, if i’m right when i assume it should do “gsettings set org.x.viewer.view use-background-color false”?
        after a fullscreen-view the sidebar is gone and must be enabled manually again.
        please make the position (left/right, top/bottom won’t make much sense) of the sidebar configurable (like the gallery) at least via dconf!
        support gestures to zoom

    mintupdate:
        provide a CLI (to let people upgrade automatically)
        add shortcut keys
        mint notices
        notify of dmesg errors
        notify of foreign packages if pinned by mint

    mintwelcome:
        consider accompanying the user and hinting at things he/she might want to do (codecs, popular settings, popular apps etc..)

    mintinstall:
        when apt cache is missing, it just says not available. Instead it could tell the user or even help the user to refresh the cache.
        redesign main page to feature essential apps

    mintsources:
        Select all button in foreign pkgs: https://github.com/linuxmint/mintsources/issues/59

    mintmenu:
        focus issues reported in /var/log/syslog

    artwork:
        Tray icons are black with mint-y themes.
        Mint-Y themes Shade option is unavailable
        mint-x-icons: in MATE (with a high panel), network status icons have a dark background in 32px and bigger. they would look much better in the panel with a transparent bg like other icons.

    mate 1.18
        swith MATE to GTK3
        switch mintmenu to GTK3
        sound events vs sound themes
        multi-monitor: caja doesn't always show the desktop on the primary monitor (using a laptop as main/left monitor, and HDMI screen with higher res on the right, it surprisingly ends up showing icons on the right screen)

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

    blueberry:
        cinnamon applet?

    libindicator++?

    use aptdaemon?
        aptdaemon doesn't work in LMDE and is being abandoned upstream
        in mintupdate, remove dep on synaptic, remove admin rights for checkAPT.py
        in mintwelcome and codec menu entry, switch from apturl to aptdaemon
        in mintsources, remove dep on synaptic
        remove synaptic from default selection
        remove synaptic from mintmenu's favorites

    HiDPI support:
        upstream apps using GTK2: Banshee, Gimp, Hexchat, VLC, Pidgin, Tomboy.
        mint projects using GTK2: mdmsetup, mintinstall, mintsources, gksu, cinnamon's mount dialog (seen when asking for a password for an encrypted external HDD).
        mintupload: use icon names rather than path to SVG
        mintwelcome: don't use 32px png icons

    cinnamon 3.4
        nemo performance: https://bugzilla.gnome.org/show_bug.cgi?id=757747
        mouse/touchpad: fix sensitivity settings (shouldn't be inverted... should be described as motion-threshold or even better, as what they actually do). Also, add a way to reset their value.
        actions in panel launchers aren't translated if not present in .desktop file
        add cinnamon-session (present but inactive) and cinnamon-settings-daemon to Launchpad/cinnamon-translations
        applets
            menu: adopt this layout (https://raw.githubusercontent.com/The-Panacea-Projects/Gnomenu/master/Screenshot.png), same as ours/mintmenu, only better.
            add a printer applet
        sound: add an option to switch sound to HDMI when an HDMI output device is plugged
        hidpi issues: top of mint menu is cut off in HiDPI (1920×1280)
        gnome-system-monitor moves out of place in Expo
        when battery is very low, battery icon isn't red.. 2% charge, with less than 5 minutes to go, still not red.. bar is red in CCC, icon is red in notification.. but not in applet (and also not in the CCC icon itself either)
        When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
        menu: use search providers to search local files
        launcher: check budgie app suggestions
        Is there any reason why there are two names for the same item, eg. "Trash" and "Rubbish Bin"? Would it be better to standardise on only one name?
        add gnome-screenshot to panel, right-click and select "Take screenshot of a selected area". This runs gnome-screenshot -a.. it should work but it doesn't. Is it because of the panel launcher capturing the click event or something?
        In Nemo, when I click on File System, followed by File and Properties, it gives me the details of the Home folder, not the File System, so it’s difficult to determine disk space of overall operating system. 
        In Nemo, if i select a new tab, the folder name that appears in the tab appears with a separation line underneath, separating the tab name from the list of files in the folder. This style of separation is onconsistent to XED, where the Tab name and content under that tab have no such visible horizontal separation line.
        consider merging worldclock https://github.com/simonwiles/cinnamon_applets
        network applet: if possible, add a little refresh icon to ask for a new scan
        system settings modules don't use the icon (in alt-tab, and window list) associated with the menu item
        Bluetooth panel icon was nicer when it was monochromatic (do we need blueberry to provide a cinnamon applet?)
        When connecting with PEAP authentication, the network manager applet just gets stuck instead of prompting for credentials.
        global lock-down?

LMDE +1:
=========

    bashrc: # colored GCC warnings and errors --> export GCC_COLORS='error=01;31:warning=01;35:note=01;36:caret=01;32:locus=01:quote=01' (won't work until gcc 4.9)
    update grub (improves efi support)
    history and completion in bashrc
    install libhal1-flash by default
    consider activating http://backports.debian.org/changes/jessie-backports.html
