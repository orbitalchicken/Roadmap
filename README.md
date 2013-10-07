MDM
---    
    - Performance improvements
    - HTML Greeter: When there's a lot of languages the whole theme itself gets a scrollbar instead of just the language menu
    - Upgrade webkit in Mint 16 to prevent mdmwebkit segfaults
    
Mint 16
-------

    - UI Improvements for Software Management
    - Consider removing splash screen in mintinstall
    - update ubiquity-slideshow (mentions vlc, giver, pdf printer etc..)
    - Review mintupdate design
    - Review mintbackup design

Cinnamon 2.0
------------

    - Review all outstanding pull requests
    - Review translations within cinnamon-translations and warnings from mocheck    
    - Critical: crashes when switching users and coming back
    - Critical: crashes on DND (Steam fix) and considers HUD as window 
    - cinnamon-settings: Tell python modules when they're "viewed". At the moment modules only rely on __init__ to load themselves. If they knew when they actually appear on the screen, they could load some parts of themselves differently. For instance, the user applet could initialize the webcam outside of __init__. This would speed up cinnamon-settings (it currently loads a lot of stuff that people don't click on) and it would solve the webcam initialization issue.
    - Date format: The Clock applet should show the date in the user's locale by default. Bonus points for making it customizable.
    - Background selection: Firefox, eog... many programs set the gnome background and no longer work with Cinnamon since we use cinnamon-settings-daemon. Maybe we need to listen to changes on the gnome background.
