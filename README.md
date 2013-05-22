=======================================================================
Bugs found in Mint 15 RC
=======================================================================
         
1 MDM 
-----
    
    - Enable remote logins via XDMCP causes Xauthority error dialog on login.
    
1 mintInstall 
-------------
    
    DONE - hangs at the startup-screen, saying it is gathering information on packages.
               
5 Cinnamon 
-----------        
    - Screensaver: doesn't forget away_message
    - Screensaver: after suspend, the screensaver does not appear and doesn’t ask for a password.
    - WM: text on title window on top isn’t centered.
    DONE - the audio input level monitor in the cinnamon settings is incredibly hard to see.
    DONE - Settings: cinnamon-settings user-accounts --> segmentation fault
                       
2  System  
----------
    
    - Update mint-mdm-themes with newer themes
    - Install smplayer2 for DVD playback?

5 New
-----
    - The network manager doesn’t allow lead to the network settings in order to set up a mobile broadband connection. It simply stops at ‘add new connection’.
        I have tried Ubuntu 13.04 with Cinnamon desktop on that very same laptop and it does everything perfectly, like Mint 14, 13 & 12 used to do before.  I had to go over network connections from the settings to add my external 3g modem connection.
    
    - No EFI El-Torito entry in the ISO. Verified with "dumpet -i file.iso". Ubuntu can boot on UEFI. Mint only has 0×00, so it only boots on BIOS(or CSM for UEFI) but not UEFI.
        
    - updating of the mockturtl-Wheater-applet does not work. I get this error-message: An error occurred during installation or updating. You may wish to report this incident to the developer of weather@mockturtl. If this was an update, the previous installation is unchanged Details: ‘ascii’ codec can’t decode byte 0xc3 in position 12: ordinal not in range(128) 
    
    - W: waited for dpgk –assert-multi-arch, but was not present dpkgGo (10:no child-processes) [/code] This shows up after each update in Mint-Update now. Why is that??

    - Add skype 4.2 to repos.

14 Total (started at 82 ;))
---------------------------

    - w32codecs, w64codecs, libdvdcss2 (previously hosted by medibuntu) are not in the repositories.


=======================================================================
Upcoming
=======================================================================

Cinnamon
--------

    - Nemo: Add devices to MoveTo/CopyTo context menu
    - Nemo: when the breadcrumb is full, and you use the back button to show the start of it.. the forward button doesn't do anything so you can't get back to the end. Also, the last two items on the first page are not clickable.
    - Desklet position is lost after killing MDM

MDM 1.2
-------
    
    - Performance improvements
    - HTML Greeter: When there's a lot of languages the whole theme itself gets a scrollbar instead of just the language menu
    
Mint 16
-------

    - UI Improvements for Software Management    
    - Check if xterm is needed (by xinit)
    - update ubiquity-slideshow (mentions vlc, giver, pdf printer etc..)


=======================================================================
Long term
=======================================================================

Cinnamon 2.0
------------

 - Calendar events - similar to KDE's implementation [lockjs]
 - Configurable color schemes for themes    
 - Upgrade Menu applet with mintMenu features (highlight new apps, install/remove apps, search the Web) [clem]
 - Rethink Cinnamon 2D, fallback to a non-shadow CPU-less intensive session in software rendering mode and/or Muffin/OpenBox (whatever happens, the user should know he's not running the "real" Cinnamon, he should be told why, and he should find himself with a working WM (even a minimalistic one like OpenBox)).
 - Use bumpmaps, make them optional, make compositing optional if possible

    NEW APPLETS
    
    - email notifier (imap/pop)
    - Pulse-like RSS reader
    
    NEW DESKLETS
    
    - System monitor

Nemo 2.0
--------

    - File preview

R&D
---        
    - Add ubiquity features to live-installer (better partitioning, fs support, EFI, OEM..etc)

