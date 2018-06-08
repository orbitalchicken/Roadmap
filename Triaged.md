Triaged reports

Not a bug
---------

- The quick filter is missing in synaptic -> install apt-xapian-index to add it. This is left out by default as it is known to slow down the OS for some people (https://bugs.launchpad.net/apt/+bug/363695, https://bugs.launchpad.net/ubuntu/+source/apt-xapian-index/+bug/655831)

- mintdrivers: The text in “Authenticate” window that comes up when i click on Driver Manager is not fully translated. I’m using it with PT-BR language. The only thing that is translated is the bold text that appears above the explanation text. Buttons, window title, explanation text and “Password” are not. -> missing language packs, use mintlocale to add them.

- update manager toolbar is too big

- Installing in VirtualBox give error “Running in software rendering mode” -> there's no acceleration by default in virtualbox, this is Cinnamon warning the user about this.

- xfce: can’t see the share remote desktop. I went to menu/preferences but then no desktop sharing was there.

Outside of the scope
--------------------

- i can not read video like mpeg or mp4 (with ubuntu mate 18.04 live or xubuntu 18.04 live, i can, now mp3 and mp4 codec is public domain) -> if it's libav we're talking about, there is still are grey areas when it comes to patents. It's ok for small distros to take that risk. We should be more careful than them though. We also made the codecs installation really easy, so other than the live use case, this isn't an urgent issue.

- xfce: After installing Opera Browser, on first opening after login, I keep getting the message “The login keyring did not get unlocked when you logged into your computer”. Then it asks for my password (solution is to autostart  gnome-keyring-daemon -r)

- Using a live boot session in VirtualBox no longer allows copy-and-paste between the host and the Linux Mint live boot session, and resizing the VirtualBox window for that session does not resize Linux Mint within that session. -> virtualbox guest additions (from Oracle) need to be installed

Can't reproduce
---------------

cinnamon:
  - backgrounds: On the left pane, you can’t select “Pictures” folder by clicking, you need to use the keyboard – Down key..
  - cinnamon: I disabled the option to block the screen in every case. This works when the screensaver is activated automatically by time. But when I close the lid, It blocks the screen and asks the password when I open.
  - menu-editor: when adding new Menu items to the Menu, The Icon’s won’t save.
  - After log-out & log-in back, the update manager icon stays there but nothing happens when you left or right click on it..
  - On Vivaldi when I full screen a youtube video, the dashboard always remains displayed. Same on Firefox.
  - power: No way to set brightness for battery VS AC power.

- mint-x: no icon when the update manager cannot connect to the server
- auto-login from installer doesn't work?
- can't access Google login page from GOA
- When trying to start xed as root it takes approx. 20 seconds for the xed window to display while displays it at once.
- can’t add any PPA (Xfce)
- No pressure sensitivity in Krita. Ugee 2150 graphics display pen not seen as mouse -> probably down to synaptics missing, user didn't confirm.

mate:
  - Windows Manager Metacity+Compton puts red line around app window

Upstream
--------

mate:
  - Sticky Notes double click doesnt highlight https://github.com/mate-desktop/mate-applets/issues/260
  - preferred apps: caja, orca aren't selected

cinnamon:
  - The dropbox icon in the bottom right bar is too small. -> for dropbox to fix
  - The Telegram icon in the bottom right bar is too small. -> for telegram to fix

ubuntu:
    - wine doesn't work
    - wifi dongle rtl8192eu is not being recognized, but the generic rtl8xxxu-driver is being loaded instead yielding a 1mbs connection speed
    - Despite installing open-vm-tools-desktop window resizing does not work
    - gnome-terminal: Just installed it with Hebrew as the system language and there’s something really weird with the fonts on the terminal. https://imgur.com/a/OHjoBu8
    - When using RTL language (in this case Hebrew) in the right click menu on the window header the icons and check boxes go over the text. https://imgur.com/a/fISEJJA