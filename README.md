=======================================================================
Bugs found in Mint 15 RC
=======================================================================
         
2 MDM 
-----
    
    - Bumblebee does not autostart with MDM (does with other DMs). I had to make an autorun script in init.d (with the command “service bumblebeed start”).
    - Enable remote logins via XDMCP causes Xauthority error dialog on login.
    
2 mintInstall 
-------------

    DONE - mintinstall navigation broken in breadcrumb when going to reviews/screenshots    
    - mintinstall hangs in the startup-screen, saying it is gathering information on packages. Cinnamon 64
        
4 Cosmetic    
----------

    - ubiquity icon is missing
    - print test page shows ubuntu logo
    - Please update the plymouth theme, its too outdated to match the awesomeness of cinnamom. yes i am talking about the fade-in of the Mint logo, please give it a new design. You can take a look at elementary os Luna’s boot up theme    
    - OMG there is no shutdown plymouth animation! I would like the LM logo from the boot to turn back off just like luna
        
5 Cinnamon 
-----------        
    - Screensaver: doesn't forget away_message
    - Screensaver: after suspend, the screensaver does not appear and doesn’t ask for a password.
    - WM: text on title window on top isn’t centered.    
    - Panel: dim mai 5 instead of dim 5 mai (MATE gets it right)
    - nvidia gtx660 video card, vsync does not work?    
    
4 mintMenu    
----------
    
    - korean doesn't show right in mintmenu http://4.bp.blogspot.com/-as_e0DHueFY/UZMcMVXqV8I/AAAAAAAAGSI/8tIJYnNxkvk/s1600/min-olivia-7.png
    - mintMenu crashed once for no reason (I wasn’t using it at that time)    
    - My keyboard freezes up when I try using the Super key too often (or Ctrl+Super, as I like to use for mintMenu). When it happens, it seems to think I always have Ctrl pressed down, and trying to use any command that calls `gksu` will cause `gksu` to mention being unable to detect my keyboard.
    - In accessibility, enable OSK and click on MintMenu. Any attempt to enter text into the MintMenu search will close the menu and OSK
                     
    
8  System  
----------

    - no sound?    
    - MATE 32: after update im stuck in an ubuntu login screen and cant boot    
    - Compiz Fusion icon does not start    
    - Synaptic freezes computer, also following the use of apt in terminal. Nothing found in var/logs.
    - HDMI audio is not working (intel hd 4000 or nvidia). There is no option to switch outputs in the taskbar.
    - medibuntu has been dropped by the maintainer. https://launchpad.net/medibuntu/+announcements
    - Mint-mdm-themes takes too much space on HDD        
    - Totem: crashes when going to next song. no visual effects displayed.           

2 New
-----

    - where is “Desktop Sharing”
    - Since the new “mintsources” does not show a list of the “Official” repos, the Medibuntu repos entries are no longer shown anywhere in “mintsources” even though it’s there and enabled. Unfortunately, the “Medibuntu” download server is frequently off-line preventing a complete refresh of the package cache when opening MintUpdate. Now there’s no way to open Software Sources (mintsources) and un-check the Medibuntu repositories as it is not listed, you have to manually edit your source file to disable it.
        
        
27 Total (started at 82 ;))
---------------------------


To test:

    - MATE: mate-system-tools installed (users, network etc..)
    - MATE: mozo installed (edit mintmenu)
    

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

