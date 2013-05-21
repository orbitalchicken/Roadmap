=======================================================================
Bugs found in Mint 15 RC
=======================================================================
         
1 MDM 
-----
    
    - Enable remote logins via XDMCP causes Xauthority error dialog on login.
    
1 mintInstall 
-------------
    
    - hangs at the startup-screen, saying it is gathering information on packages. Cinnamon 64
        
2 Cosmetic    
----------

    - ubiquity icon is missing
    - print test page shows ubuntu logo    
        
5 Cinnamon 
-----------        
    - Screensaver: doesn't forget away_message
    - Screensaver: after suspend, the screensaver does not appear and doesn’t ask for a password.
    - WM: text on title window on top isn’t centered.
    - the audio input level monitor in the cinnamon settings is incredibly hard to see.
    DONE - Settings: cinnamon-settings user-accounts --> segmentation fault
                       
3  System  
----------

    - MATE 32: after update im stuck in an ubuntu login screen and cant boot    
    - Update mint-mdm-themes with newer themes
    - Can't play DVDs (add a gstreamer0.10 capable media player which handles DVD navigation, gnome-mplayer for instance)

3 New
-----

    - Medibuntu can't be disabled in mintsources. We should probably stop using the repository too (https://launchpad.net/medibuntu/+announcements)    
    - ubiquity not hacked to install local grub2-efi yet (EFI install only works when live session is online)
    - There is still no EFI El-Torito booting entry in the ISO file. It can be verified by using “dumpet -i the_64_bit_cd_image.iso” against Mint and Ubuntu. The Ubuntu ISO contains two booting entry, with PlatformId 0×00 for X86 BIOS and 0xef for EFI. So it can be burned to a DVD and boot off a UEFI machine. But Mind only has 0×00, so it only boots off BIOS(or CSM for UEFI) but not UEFI. I think it’s not difficult to add the UEFI booting entry just like Ubuntu when building the 64 bit ISO file.  
        
        
15 Total (started at 82 ;))
---------------------------


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

