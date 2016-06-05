Linux Mint 18 Sarah
===================

    release:
        rel notes
        new features

    review logind.conf changes in:
        MATE
        Xfce
        KDE

    LO menus show weird artefacts

    mintsources: warning message should not mention backports
    On session start, mintUpload doesn't run because of missing file. Its .desktop file is set to run non-existing binary: /usr/lib/linuxmint/mintUpload/launch-file-uploader.py
    mintupdate prefs http://i.imgur.com/xBiPDmt.png

    MATE:
        [done] natural scroll
        pkgs can be removed:  gnome-session-bin (has gnome-session-* binaries). libgnome2-bin (has gnome-open binary). libbonoboui2-0 libgnome2-0 libgnome2-perl libgnomeui-0 python-gnome2 libgnome-menu-3-0 libgnome2-canvas-perl libgnome2-common libgnome2-vfs-perl libgnomekbd-common libgnomekbd8 libgnomeui-common libgnomevfs2-0 libgnomevfs2-common libgnomevfs2-extra gkbd-capplet libbonobo2-0 libbonobo2-common libgtkmm-2.4-1v5 ndiswrapper ndiswrapper-utils-1.9 ndiswrapper-dkms gnome-session-canberra policykit-1-gnome
        Synaptic entry in the left pane of mintMenu is apparently set to run it via gksu, while the menu entry in Applications pane uses synaptic-pkexec.
        mate-session[6246]: EggSMClient-WARNING: Invalid Version string '0.9.4' in /home/monsta/.config/autostart/xfce-autostart-wm.desktop

    Cinnamon:
        mint-y and mint-y-dark are missing Cinnamon theme preview thumbs


    Printer driver requires "lsb" package https://bugs.launchpad.net/ubuntu/+source/lsb/+bug/1536353
    mint-y-darker: caja toolbar is clear instead of dark

Stable release
=============
        update live repo and sign, with latest FF at time of release.
        Upgrade path from Mint 17.3
        no acceleration in virtualbox

Maintenance
===========

    cinnamon-spices website:
        reimplement css
        handle utf-8, see comments on http://cinnamon-spices.linuxmint.com/applets/view/171

    upgrade LO to 5.0.6?

Linux Mint 18.1
===============

    system
        consider adding snapd
        consider adding support for xdg-apps, flatpack
        consider enabling recommends

    cinnamon 3.2
        actions in panel launchers aren't translated if not present in .desktop file
        add cinnamon-session and cinnamon-settings-daemon to Launchpad/cinnamon-translations
        vertical panels
        retire boxpointers
        remove plug/socket in screensaver
        applets
            menu: adopt this layout (https://raw.githubusercontent.com/The-Panacea-Projects/Gnomenu/master/Screenshot.png), same as ours/mintmenu, only better.
            add a printer applet
        sound: add an option to switch sound to HDMI when an HDMI output device is plugged
        hidpi issues: top of mint menu is cut off in HiDPI (1920×1280)
        gnome-system-monitor moves out of place in Expo
        when battery is very low, battery icon isn't red.. 2% charge, with less than 5 minutes to go, still not red.. bar is red in CCC, icon is red in notification.. but not in applet (and also not in the CCC icon itself either)
        When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
        accessibility: ability to select files by hovering them
        menu: use search providers to search local files

    mate 1.16
        swith MATE to GTK3
        switch mintmenu to GTK3
        sound events vs sound themes
        multi-monitor: caja doesn't always show the desktop on the primary monitor (using a laptop as main/left monitor, and HDMI screen with higher res on the right, it surprisingly ends up showing icons on the right screen)

    libindicator++?

    xed
        sublime-like search bar

    xreader
        should place its menu item in the accessories category instead of office

    xplayer/xviewer/xreader/pix
        add a persistant option to blank other monitors when in full screen

    xapps
        should show their project name in the about dialog

    pix
        should use a generic name in the application menu

    mintupdate:
        provide a CLI (to let people upgrade automatically)

    mintwelcome:
        consider accompanying the user and hinting at things he/she might want to do (codecs, popular settings, popular apps etc..)

    mintsources:
        Select all button in foreign pkgs: https://github.com/linuxmint/mintsources/issues/59

    mintinstall:
        when apt cache is missing, it just says not available. Instead it could tell the user or even help the user to refresh the cache.
        redesign main page to feature essential apps

    use aptdaemon?
        aptdaemon doesn't work in LMDE and is being abandoned upstream
        in mintupdate, remove dep on synaptic, remove admin rights for checkAPT.py
        in mintwelcome and codec menu entry, switch from apturl to aptdaemon
        in mintsources, remove dep on synaptic
        remove synaptic from default selection
        remove synaptic from mintmenu's favorites

    HiDPI support:
        pix: huge menubar
        upstream apps using GTK2: Banshee, Gimp, Hexchat, VLC, Pidgin, Tomboy.
        mint projects using GTK2: mdmsetup, mintinstall, mintsources, gksu, cinnamon's mount dialog (seen when asking for a password for an encrypted external HDD).
        mintlocale: fixed-size flag icons
        mintupload: use icon names rather than path to SVG
        mintwelcome: don't use 32px png icons

LMDE +1:
=========

    bashrc: # colored GCC warnings and errors --> export GCC_COLORS='error=01;31:warning=01;35:note=01;36:caret=01;32:locus=01:quote=01' (won't work until gcc 4.9)
    update grub (improves efi support)
    history and completion in bashrc
    install libhal1-flash by default
    consider activating http://backports.debian.org/changes/jessie-backports.html
