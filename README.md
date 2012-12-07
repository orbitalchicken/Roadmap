
=======================================================================
LINUX MINT 15
=======================================================================

Cinnamon 1.8
------------

    MAIN FEATURES

    - Desklets [dalcde]
    - Ability for cinnamon-settings to browse/install/remove/update themes/applets/extensions/desklets remotely [clem]
    - Bumpmaps [esteban] [dalcde]
    - Control Center (Cinnamon and GNOME properties within one same settings tool) [clem]
    - Rethink Cinnamon 2D, fallback to a non-shadow CPU-less intensive session in software rendering mode and/or Muffin/OpenBox (whatever happens, the user should know he's not running the "real" Cinnamon, he should be told why, and he should find himself with a working WM (even a minimalistic one like OpenBox)).
    
    ADDITIONAL FEATURES
    
    - Configurable color schemes for themes
    - Calendar events - similar to KDE's implementation [clem]
    
    NEW APPLETS
    
    - email notifier (imap/pop)
    - Pulse-like RSS reader
    
    NEW DESKLETS
    
    - System monitor
    - Picture, video, slideshow frame
    - Terminal    

Nemo 1.8
--------

    MAIN FEATURES

    - Action API (reads desktop files in /usr/share/nemo/launchers. An action is basically a text file which defines a name, an icon, an executable and which file extensions nemo shows the action for when the file is right-clicked. A typical example of this would be a "Edit tags" action which would apply to *.mp3 files.). 
    - Disk Management (mintdisk integration etc..)
    - File preview
    - UI improvements (sidebar selection, independent path bar, better looking breadcrumbs etc..)    

    ADDITIONAL FEATURES
    
    - Add devices to MoveTo/CopyTo

MDM 1.2
-------

    - Add a "border" property to "entry" objects so themes can get borders around text fields
    - Write a new renderer which supports animations and interactivity to get on par with unity-greeter in terms of looks

Mint Tools
----------

    - UI Improvements for Software Management
    - UI Improvements for live-installer

R&D
---

    - Screensaver
    - Driver Manager
    - Add ubiquity features to live-installer (better partitioning, fs support, webcam support, EFI, OEM..etc)
    - R&D on "from scratch" package base and investigation on pros and cons of dpkg compared to other packaging systems (multi-version installation, static/dynamic support, snapshots, delta, update reversals etc..)
