=======================================================================
Upcoming
=======================================================================

Cinnamon 1.8
------------

  Cinnamon

    - Artefacts in menu (app list). Sometimes it looks like two lists are rendered (you see app names written on top of others).

  Settings

    - Couldn't find UUID when installing gtile... crash when uninstalling it.

  Nemo

    - Add devices to MoveTo/CopyTo context menu
    - when the breadcrumb is full, and you use the back button to show the start of it.. the forward button doesn't do anything so you can't get back to the end. Also, the last two items on the first page are not clickable.

  Screensaver

    - Empty message is shown as ""
    - The position of the away message could be better (cosmetic improvement)

  Xlets
    
    - Desklet position is lost after killing MDM
    - Heavy DND on desklets still crash Cinnamon

  Gnome CC modules

    - User module doesn't use .face (go to Users, select a predefined avatar, it doesn't overwrite .face)

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
    - Nightlife: Upgrade to 1.8, improve the title of the selected window in the scale plugin, improve look of widgets in notifications    
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

