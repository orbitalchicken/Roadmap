=======================================================================
Upcoming
=======================================================================

Cinnamon 1.8
------------

  Cinnamon
    - Remove any usage of bumpmaps in 1.8
    - Should cinnamon2d force software rendering? do we need 3 sessions (softwareforced, light and full)?
    - Should cinnamon2d send a notification or visual indication to the user that he/she is not running the full Cinnamon?
    - Migrate to gdbus (GNOME 3.8 support)
    - Draw the background in Cinnamon (GNOME 3.8 support)
    - Applet manager crash when changing panel layout: https://github.com/linuxmint/Cinnamon/issues/1608

  Settings
    - Finalize applet settings module
    - Port applet settings module UI to themes, desklets and extensions
    - Merge dalcde's work on desklets (incomplete, needs to fix huge memory usage in photoframe)
    - Couldn't find UUID when installing gtile... crash when uninstalling it.

  Nemo
    - Add devices to MoveTo/CopyTo context menu
    - Ctrl+N should open a new instance in the same location as the current window
    - when the breadcrumb is full, and you use the back button to show the start of it.. the forward button doesn't do anything so you can't get back to the end. Also, the last two items on the first page are not clickable.

  Screensaver
    - Empty message is shown as ""
    - The position of the away message could be better (cosmetic improvement)

  Xlets
    - Power applet appears when moving applets in the panel
    - Photoframe doesn't show up in the desklets
    - Desklet position is lost after killing MDM

  Gnome CC modules
    - C modules don't fill the page in cinnamon-settings
    - User module doesn't use .face

MDM 1.2
-------
    
    - Performance improvements
    - GDM Greeter: Add a "border" property to "entry" objects so themes can get borders around text fields
    - HTML Greeter: Remove white screen appearing before the theme is loaded
    - HTML Greeter: When there's a lot of languages the whole theme itself gets a scrollbar instead of just the language menu
    
Mint 15
-------

    - UI Improvements for Software Management    
    - Implement nemo actions
    - Upgrade nithglife theme to 1.8 and improve the title of the selected window in the scale plugin
    - Make beautiful HTML5 themes for MDM
    - Finalize artwork
    - Can't remove software-properties-gtk because apturl requires it (hack apturl to cope with the loss)
    - Check if xterm is needed (by xinit)


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

