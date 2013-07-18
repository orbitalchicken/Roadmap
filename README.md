MDM
---
    
    - Performance improvements
    - HTML Greeter: When there's a lot of languages the whole theme itself gets a scrollbar instead of just the language menu
    - Allow password-only login (for single user) and/or remember last user

Mint 16
-------

    - UI Improvements for Software Management
    - Consider removing splash screen in mintinstall
    - update ubiquity-slideshow (mentions vlc, giver, pdf printer etc..)
    - Review mintupdate design
    - Review mintbackup design
    - Consider default installation using separate home/root partitions - figure a nice formula, root must be minimum up to xx%, remaining home.  We could possibly offer a pseudo-upgrade path which installs a fresh system, but also reinstalls existing programs and user(s) during installation.

Cinnamon 2.0
------------

    - Review any remaining GNOME backend components and dependencies
    - Factorize translations into cinnamon-translations
    - Implement a non-accelerated fallback GTK panel and session
    - Consider shipping our own version of gjs (as opposed to using the system one and in an effort to ease backports)    
    - Convert all system applets, desklets to use settings api
    - Calendar events - similar to KDE's implementation [lockjs] 
    - Upgrade Menu applet with mintMenu features (highlight new apps, install/remove apps, search the Web) [clem]
    - Use bumpmaps, make them optional, make compositing optional if possible
    - Notifications: try to identify notifications with interactions, and make them stick around longer/until dismissed (i.e. bluetooth pairing)
    - Notifications: Provide dismiss button when notification click triggers and action other than dismiss
    - Settings API: Implement object/custom interface
    
    NEW APPLETS
    
    - email notifier (imap/pop)
    - Pulse-like RSS reader
    
    NEW DESKLETS
    
    - System monitor

Nemo 2.0
--------

    - File preview
    - Add devices to MoveTo/CopyTo context menu
    - When the breadcrumb is full, and you use the back button to show the start of it.. the forward button doesn't do anything so you can't get back to the end. Also, the last two items on the first page are not clickable.
    - Windows-like 2-click renaming.  Click a file name.  Click on same file name again (but not double-click) - instigates rename action.
    - Removable device trash management.

MintStick
---------

    - Make a 'clean' option - dd really hoses up USB sticks for use afterward.  For the uninitiated it's a pain to 'blank' them back out.  Make this a one-click operation


