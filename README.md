
=======================================================================
LINUX MINT 15
=======================================================================

Cinnamon 1.8
------------

    MAIN FEATURES

    - [DONE] Desklets
    - [PRIORITY] Control Center (Cinnamon and GNOME properties within one same settings tool) [clem] [glebihan]
    - [PRIORITY] [STARTED] Ability for cinnamon-settings to browse/install/remove/update themes/applets/extensions/desklets remotely [rjanja]
    - [PRIORITY] JSON Settings API
    - Bumpmaps [esteban] [dalcde]
    
    - Rethink Cinnamon 2D, fallback to a non-shadow CPU-less intensive session in software rendering mode and/or Muffin/OpenBox (whatever happens, the user should know he's not running the "real" Cinnamon, he should be told why, and he should find himself with a working WM (even a minimalistic one like OpenBox)).
    
    ADDITIONAL FEATURES
    
    - Configurable color schemes for themes
    - Calendar events - similar to KDE's implementation [clem]
    - Upgrade Menu applet with mintMenu features (highlight new apps, install/remove apps, search the Web) [clem]
    
    NEW APPLETS
    
    - email notifier (imap/pop)
    - Pulse-like RSS reader
    
    NEW DESKLETS
    
    - System monitor
    - [DONE] Picture frame
    - [DONE] Clock

[READY] Nemo
------------

    MAIN FEATURES

    - [DONE] UI improvements
    - [DONE] Action API        

    ADDITIONAL FEATURES
    
    - Add devices to MoveTo/CopyTo
    - Disk Management (mintdisk integration etc..)
    - File preview    
    
[READY] Cinnamon Screensaver
----------------------------

    MAIN FEATURES
        
    - [DONE] .face support
    - [DONE] DM integration
    
    ADDITIONAL FEATURES 
    
    - [DONE] Away messages
    - xscreensaver plugin support

MDM 1.2
-------

    MAIN FEATURES
    
    - [PRIORITY] Performance improvements
    - Add a "border" property to "entry" objects so themes can get borders around text fields
    - Usability improvements    
    - Write a new renderer which supports animations and interactivity to get on par with unity-greeter in terms of looks    
    - UI improvements in mdm config tools
    
    ADDITIONAL FEATURES
    
    - Webkit greeter    

Mint Tools
----------

    - UI Improvements for Software Management    
    - [PRIORITY] [STARTED] MintSources to replace software-properties [glebihan]
    - [PRIORITY] [STARTED] Driver Manager to replace software-properties/jockey [schoelje]
    
[READY] Live Installer
----------------------

    - [DONE] Slideshow and UI Improvements
    - [DONE] Keyboard selection visualization
    - [DONE] Support for multiple HDDs
    - [DONE] Timezone map
    - [DONE] .face webcam support

R&D
---        
    - Add ubiquity features to live-installer (better partitioning, fs support, EFI, OEM..etc)
    - R&D on "from scratch" package base and investigation on pros and cons of dpkg compared to other packaging systems (multi-version installation, static/dynamic support, snapshots, delta, update reversals etc..)
