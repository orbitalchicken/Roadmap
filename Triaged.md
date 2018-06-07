Triaged reports

Not a bug
---------

- The quick filter is missing in synaptic -> install apt-xapian-index to add it. This is left out by default as it is known to slow down the OS for some people (https://bugs.launchpad.net/apt/+bug/363695, https://bugs.launchpad.net/ubuntu/+source/apt-xapian-index/+bug/655831)

- mintdrivers: The text in “Authenticate” window that comes up when i click on Driver Manager is not fully translated. I’m using it with PT-BR language. The only thing that is translated is the bold text that appears above the explanation text. Buttons, window title, explanation text and “Password” are not. -> missing language packs, use mintlocale to add them.

- update manager toolbar is too big

Outside of the scope
--------------------

- i can not read video like mpeg or mp4 (with ubuntu mate 18.04 live or xubuntu 18.04 live, i can, now mp3 and mp4 codec is public domain) -> if it's libav we're talking about, there is still are grey areas when it comes to patents. It's ok for small distros to take that risk. We should be more careful than them though. We also made the codecs installation really easy, so other than the live use case, this isn't an urgent issue.

Can't reproduce
---------------

cinnamon:
  - backgrounds: On the left pane, you can’t select “Pictures” folder by clicking, you need to use the keyboard – Down key..
  - cinnamon: I disabled the option to block the screen in every case. This works when the screensaver is activated automatically by time. But when I close the lid, It blocks the screen and asks the password when I open.
  - menu-editor: when adding new Menu items to the Menu, The Icon’s won’t save.

- mint-x: no icon when the update manager cannot connect to the server
- auto-login from installer doesn't work?
- can't access Google login page from GOA
- When trying to start xed as root it takes approx. 20 seconds for the xed window to display while displays it at once.

Upstream
--------

mate:
    - Sticky Notes double click doesnt highlight https://github.com/mate-desktop/mate-applets/issues/260
    - preferred apps: caja, orca aren't selected