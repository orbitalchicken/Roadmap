
Maintenance
===========

    cinnamon-spices website:
        reimplement css
        handle utf-8, see comments on http://cinnamon-spices.linuxmint.com/applets/view/171

    upgrade LO to 5.0.6?

Linux Mint 18.1
===============

    switch ntp to chrony?

    mdm:
        fix Logitech keyboard layout recognized as en_US

    firefox:
        enable bookmark toolbar by default
        enable plugins by default

    review logind.conf changes in:
        MATE
        Xfce
        KDE

    system
        consider adding snapd
        consider adding support for xdg-apps, flatpack
        consider enabling recommends

    ubiquity:
        inhibit sessions via presence API (need to do it in KDE too)

    mint-tools:
        in MATE, window icons aren't set properly when the icon is placed in /usr/share/pixmaps

    mintsources:
        add support for anycast IP worldwide global mirrors

    cinnamon 3.2
        mouse/touchpad: fix sensitivity settings (shouldn't be inverted... should be described as motion-threshold or even better, as what they actually do). Also, add a way to reset their value.
        actions in panel launchers aren't translated if not present in .desktop file
        add cinnamon-session and cinnamon-settings-daemon to Launchpad/cinnamon-translations
        retire boxpointers
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
        Setting the screensaver to turn on but not require a password is very confusing. I have to go to set “Lock the computer when put to sleep” to “No” (because I don’t want it to require a password); set “Lock the computer when the screen turns off” to “No” (because, again, I don’t want it to require a password); and then set “Lock the computer when inactive” to a time value to have the screensaver come on. (I’m not even sure that I’ve got that right.) The problem is that “lock the computer” implies that it’s going to require a password — but I don’t want that, I simply want the screensaver to kick in. This is a poorly worded dialog box.
        consider merging worldclock https://github.com/simonwiles/cinnamon_applets
        network applet: if possible, add a little refresh icon to ask for a new scan
        system settings modules don't use the icon (in alt-tab, and window list) associated with the menu item
        Bluetooth panel icon was nicer when it was monochromatic (do we need blueberry to provide a cinnamon applet?)
        When connecting with PEAP authentication, the network manager applet just gets stuck instead of prompting for credentials.
        ability to lock desklets?
        When scrolling down in the Menu smoothly, icons/items leave some “traces” behind, if you can call it that
        mouse motion settings reset themselves after a while?
        constantly getting a NEMO “thumbnail error” when I open photo directories (no videos) I haven’t visited in a while.
        Clock takes up about 30-60 seconds to update the hour after waking up the system from sleeping. Can we get a signal on wakeup?

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
        visualizations don't work

    xapps
        should show their project name in the about dialog

    pix
        should use a generic name in the application menu

    xviewer
        “Date in statusbar” doesn’t work.
        “Disable Dark Theme” doesn’t work, if i’m right when i assume it should do “gsettings set org.x.viewer.view use-background-color false”?
        “Hide Titlebar” not sure what it should do…?
        “Export to Folder”, “Fullscreen Background”, “Python Console” and “Slideshow Shuffle” can’t be activated. in the moment they get grayed out and a tool-tip says “The plugin ‘XXX’ could not be loaded – An error occurred: Plugin loader ‘python3’ was not found”
        after a fullscreen-view the sidebar is gone and must be enabled manually again.
        please make the position (left/right, top/bottom won’t make much sense) of the sidebar configurable (like the gallery) at least via dconf!

    mintupdate:
        provide a CLI (to let people upgrade automatically)
        add shortcut keys

    mintwelcome:
        consider accompanying the user and hinting at things he/she might want to do (codecs, popular settings, popular apps etc..) - check chalet OS' startpoint ideas

    mintsources:
        Select all button in foreign pkgs: https://github.com/linuxmint/mintsources/issues/59
        menu icon shouldn't be hardcoded

    mintinstall:
        when apt cache is missing, it just says not available. Instead it could tell the user or even help the user to refresh the cache.
        redesign main page to feature essential apps

    mintmenu:
        focus issues reported in /var/log/syslog

    blueberry:
        cinnamon applet?

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
        mintlocale: fixed-size flag icons
        mintupload: use icon names rather than path to SVG
        mintwelcome: don't use 32px png icons

    artwork:
        Tray icons are black with mint-y themes.
        Mint-Y themes Shade option is unavailable
        mint-x-icons: in MATE (with a high panel), network status icons have a dark background in 32px and bigger. they would look much better in the panel with a transparent bg like other icons.

    done:
        cinnamon:
            sounds for notifications (needs to be configured in mint-artwork-cinnamon)
            vertical panels
            new screensaver
            smoother bg handling
            menu: bumblebee support -> run with NVIDIA GPU
        xed:
            red warning bar when running as root
        xplayer:
            blank other monitors when in fullscreen

LMDE +1:
=========

    bashrc: # colored GCC warnings and errors --> export GCC_COLORS='error=01;31:warning=01;35:note=01;36:caret=01;32:locus=01:quote=01' (won't work until gcc 4.9)
    update grub (improves efi support)
    history and completion in bashrc
    install libhal1-flash by default
    consider activating http://backports.debian.org/changes/jessie-backports.html
