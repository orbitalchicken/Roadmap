Linux Mint 19
=============

    rel_notes
    new features page

    [DONE in GIT] gnome-terminal: restore context menu the way it was before

    QA:
        FF is missing l10n? (related to mint-artwork-common?)
        choosing encrypt install and overrite empty space crashes installation and leaves drive with no os on it.
        cinnamon: "*.deb" files do no automatically associate with gdebi
        vlc-l10n should be a dep of mint-meta-codecs

        xfce:
            f1 doesn't produce help content
            Right clicking on a folder in Thunar and slecting open as root does nothing

        MATE:
            uses ntp? switch to chrony?
            mintupdate keeps displaying "Do you want to switch to a local mirror?", click OK -> never comes up with the mirror-speed-test https://github.com/linuxmint/mintupdate/pull/358

             Lock screen prompt takes about minute to show, and when I enter my password, it takes another minute to actually let me back to desktop. There are suspicious messages in journalctl:
                mate-screensaver-dialog: pam_ecryptfs: seteuid error
                gnome-keyring-daemon: couldn't initialize slot with master password: The password or PIN is incorrect

            remove gnome-session-bin?

            Launching mintdrivers from mintwelcome has the same missing label issue as in mintsources. However, running "pkexec mintdrivers" from terminal shows the label... weird.

            Launching codecs installation from mintwelcome shows a dialog that has no parent window set. It's easily covered by other windows and isn't shown in tasklist.

            Launching "install/remove languages" tool from mintlocale seems to keep the privileges (mate-polkit icon is shown in tray), it will ask for password next time anyway, when you close the install/remove dialog and launch it again. Weird.

            After multimedia codecs are installed, the entry for it is not disabled/removed from menus. It's still there in mintmenu (or Alt-F1 menu).

            System reports tool also still offers me to install the codecs, even though I did so from mintwelcome before.

            When using Mint-X theme, there are visual glitches in mate-screensaver-preferences in the side pane (list of screensavers). Just move the mouse over that pane back and forth, without clicking.

            Compiz doesn't have MATE compatibility plugin enabled, so Alt-F1 and Alt-F2 shortcuts don't work as MATE users would expect. There's GNOME compatibility plugin enabled, I have no idea what it does. Maybe some support from gnome-flashback session?

            There's some inconsistency between Compiz plugins enabled by mintdesktop and the ones enabled in CCSM.
                When you first switch to Compiz in matedesktop, it creates /org/compiz/profles/mate/ in dconf and puts plugins-with-set-keys key there, filled with list of enabled plugins. But it doesn't create /org/compiz/profles/mate/plugins/ which is supposed to contain settings of enabled plugins.
                When you launch CCSM after that, it has a different set of enabled plugins. For example, it doesn't have winrules plugin enabled at all. But CCSM actually creates /org/compiz/profles/mate/plugins/ in dconf and puts several subfolders there, which have the settings of currently enabled plugins. These plugins are the ones that are checked in CCSM itself, so there's no subfolder for winrules in dconf.
                I'm quite confused because winrules plugin actually seems to work (even though it looks disabled): mintmenu doesn't have a gap between itself and panel. Or maybe that bug isn't reproducible anymore with Ubuntu 18.04 base? No idea.
                For reference, old bug reports about the gap and the commits with the fixes for it:
                https://github.com/linuxmint/mintmenu/issues/121
                https://bugs.launchpad.net/compiz/+bug/1419346
                https://github.com/linuxmint/mintdesktop/commit/1a443159029b5021e69f0b3e75e3c8967880f8b2
                https://github.com/linuxmint/mintdesktop/commit/487257aa10eca92150a129246fd846b8d1800d35


            intel-microcode is missing


            mintdesktop still has a setting for terminal to enable fo




    need_update:
        minecraft-installer
        whatsapp-desktop
        spotify-client
        dropbox
        google-earth-pro-stable
        skypeforlinux

    artwork:
        grey-on-grey icons (many in cinnamon-settings)
        wifi networks available notif is blue, but connected one is green
        thunar/caja -> use app icon? (is folder appropriate. doesn't currently change color with color variation)
        remove humanity-icon-theme and ubuntu-mono

    gdebi: pkexec doesn’t work when double-clicking from nemo https://bugs.launchpad.net/ubuntu/+source/gdebi/+bug/1760910 https://bugs.launchpad.net/ubuntu/+source/gdebi/+bug/1749728
    gist-paste still used in xapps/mintsystem
    cinnamon settings startup, edit item with no delay, save -> python exception

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

    update translations

LMDE 3
======

    lightdm asks username to be typed

    Backports
        flatpak/ostree/appstream?
        meson/debhelper/dh_autoreconf?

Linux Mint 19.1
===============

    update installation slideshow
        internet: flash/java
        movies: DVD
        connected: refs to ICQ..

    mate:
        consider brisk menu

    mintupdate:
        safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).
        notice to reboot the computer when appropriate
        purge old kernels? https://github.com/Pjotr123/purge-old-kernels-2
        systray icon or infobar to notify user of new Mint versions
        remember sorting of updates

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
    new backgrounds
    new branded backgrounds

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