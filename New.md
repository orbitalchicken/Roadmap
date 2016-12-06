New bug reports in Linux Mint 18.1 BETA

All editions
------------
    mdm: Webkit preview, process doesn't die when window is closed
    mdm: Webkit preview, mint-X doesn't show anything, only background
    kernel:
        check critical bugs against -45/-47 or consider Dirty Cow patch in -31
        consider offering 4.8?
    mintupdate:
        ‘Most stable recommendation’ is poor English
        creates objects with wrong ownership. See https://github.com/linuxmint/mintupdate/issues/169
        I would like update manager would show updates to the kernels series selected. I’ve running a 4.8 kernel and still shown updates to the latest 4.4 kernel.
    steam doesn't run out of the box.
    mintlocale: Add/remove alt-tab icon is blurry
    Serena BETA, unrecognized audio devices “Dummy output”. ProBook 470 G4.     Sara audio ok.
    is it possible to add ‘libdvd-pkg’ before the final release? It’s required to play DVDs and I assume it was removed upstream when they ‘went beyond optical media.’
    slideshow: pix icon is wrong

Cinnamon Edition - last processed comment: #118
-----------------------------------------------
    Qt 5.7 looks bad
    nemo: Prefs > Display > Icon Caption > first option SIZE, and Prefs > Preview > Folders > options NEVER ---> results in "–" showing under directories (tested in icon view).
    Right-click an icon on the panel, select “options”, then “edit”. Try to choose a new icon. The new icon shows in the window. Try to click “OK”. It won’t click and the icon won’t change.
    msgids:
        "Layout and content" isn't present in LP?
        screensaver: “Please enter your password” screenshot – https://goo.gl/nXU73n
        nemo: “Click on a file’s name twice to rename it”.
    screensaver:
        please make clock jumping less frequent (5 seconds right now?)
        If the display for the time gets disabled, also the absence message does not get shown. I think, both should be independent from each other.
        should never lock a live session
        process name should be set
        RTL: http://imgur.com/a/0hqqY
        in 1152×864 the clock is over the password field
        The volume control on the lock screen in the upper left hand corner looks like a glitch more than a feature. Especially with no media playing.
    Is the speed (not acceleration) of the mouse pointer finally changable via the settings? This did not work for years now
    When running cinnamon live session, attempting to do a restart via the button on the cinnamon menu causes the screen to hang on the cinnamon logo as the system begins to shut down.
    By default the file name for the sound is my username (without ending like .oga). This file does not exist, so that by simply turning the option to play the notification sound will do nothing. Looks like a forgotten default value.
    Configuration option for the menu urgently missed:
        Until Mint 18 Sarah there was for the menu the option “menu hover delay”. This is not the same as the option with the same name in 18.1 Serena, as also the tool tip reveals, if you hover the option.
        The new option delays the appearance of the menu, if you have the option to open the menu by hovering it in the panel activated.
        The old option delayed switching the categories. This means, if you have selected a category and want now to move the pointer to the menu entry to the right, you can (with the delay set to e.g.150 ms) move the mouse diagonally over other categories without activating them by doing so. Without the delay the categories, touched by the mouse pointer get at once activated and the command in the right column is not more there.
        This leads to the result, that without the delay you have to move the mouse at first properly to the right and then up or down to the needed command; diagonal (and far quicker and more logical) movements are without the delay not possible.
        As this category delay has now been (erroneously?) removed the menu in 18.1 appears as a regression in usability. Please restore this option.
    Bug Found: 24 hour format won’t change to 12 hour in vertical panel mode
        To reproduce: Change panel to vertical panel, then change clock from 24 hour to 12 hour, the clock will display in 24 hour format still. If you change panel to horizontal, time will be correct, change back to vertical and it changes back to 24 hour format, but settings still say 12 hour
    metacity fallback should include better settings, terminal, ability to reboot
    vmware support (windows are translucent)
    Problem with the width of some configuration windows: E. G. with the configuration window for window list applet.

MATE Edition - last processed comment: #40
------------------------------------------
    Control Center | Appearance | Interface: I see that “Show icons in menus” works with xed, but “Toolbar button labels” does not
    Optical glitch in “Steuerzentrale” (Control Center?). With Mint-Y Dark theme (other dark ones may apply also). Group of settings selected on the left tree => highlighted section is unreadable: light font color bleeds into the light background color.

Xfce Edition - last processed comment: #0
-------------------------------------------

KDE Edition - last processed comment: #0
-----------------------------------------

