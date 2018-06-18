Triaged reports

Not a bug
---------

- The quick filter is missing in synaptic -> install apt-xapian-index to add it. This is left out by default as it is known to slow down the OS for some people (https://bugs.launchpad.net/apt/+bug/363695, https://bugs.launchpad.net/ubuntu/+source/apt-xapian-index/+bug/655831)

- mintdrivers: The text in “Authenticate” window that comes up when i click on Driver Manager is not fully translated. I’m using it with PT-BR language. The only thing that is translated is the bold text that appears above the explanation text. Buttons, window title, explanation text and “Password” are not. -> missing language packs, use mintlocale to add them.

- update manager toolbar is too big

- Installing in VirtualBox give error “Running in software rendering mode” -> there's no acceleration by default in virtualbox, this is Cinnamon warning the user about this.

- xfce: can’t see the share remote desktop. I went to menu/preferences but then no desktop sharing was there.

- slick doesn't have a flashing cursor in its entry box, giving the impression that the entry isn't focused.

- mint-y-dark (and dark variants of light themes): xed right margin is barely visible, current line highlighting is grey on top of grey. -> this isn't part of the GTK theme, it's part of the selected Xed style scheme.

Outside of the scope
--------------------

- i can not read video like mpeg or mp4 (with ubuntu mate 18.04 live or xubuntu 18.04 live, i can, now mp3 and mp4 codec is public domain) -> if it's libav we're talking about, there is still are grey areas when it comes to patents. It's ok for small distros to take that risk. We should be more careful than them though. We also made the codecs installation really easy, so other than the live use case, this isn't an urgent issue.

- xfce: After installing Opera Browser, on first opening after login, I keep getting the message “The login keyring did not get unlocked when you logged into your computer”. Then it asks for my password (solution is to autostart  gnome-keyring-daemon -r)

- Using a live boot session in VirtualBox no longer allows copy-and-paste between the host and the Linux Mint live boot session, and resizing the VirtualBox window for that session does not resize Linux Mint within that session. -> virtualbox guest additions (from Oracle) need to be installed

- Cinnamon setting to disable the touch pad while typing does not work, which makes typing on the laptop pretty annoying. -> provided for synaptics driver.

- mintinstall (live mode): Software Manager-Games-All only shows 0Ad-Edgar  i.e. it does not show the games beginning with later letters E-Z that can be found through the more detailed searches, e.g. Software Manager-Games-Simulation and Racing-Torcs --> appstream can't work in live mode, the cache isn't full and mintinstall probably doesn't know about the score of each app. Only 200 apps are shown, usually by order of popularity, but here since it's not possible, by alphabetical order.

- mintinstall: does only wait and not warn if synaptic is open.

- In the file-manager the number of emblems has been reduced. It takes some effort to create extra ones. It would be great to have an application that automates this process (Else you have to use gimp and put the result with the right name in the proper folder).

Can't reproduce
---------------

- When installing to internal 16GB SSD and with option “Something else” using the whole SSD for mountpoint root, installation always hangs in both XFCE 64 and Cinnamon 64. Ubuntu 18.04 installer with same options has no problem. -> journalctl info not provided

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
- can't install google chrome
- appimage: When I download Molotov.Appimage and try to launch the file it fails. The same installation with Mint Cinnamon version 18.3 runs perfectly on my both laptops. -> chmod the file, and run it.. works perfectly.
- Anydesk. Shortcut saved connection on desktop will not launch. Gives ' There was an error launching the application'. From within anydesk it starts normal.

mate:
  - Windows Manager Metacity+Compton puts red line around app window

Upstream
--------

- clementine: mint-y, huge icons -> applications-internet and media-optical look OK in the theme, provided in all sizes. They're PNG as opposed to SVG for action icons, but that shouldn't matter.

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
  - there is no country named Czechia. Adding another language keyboard layout, selecting COUNTRY, i found name Czechia in the list.
  -  During installation, having selected "Something else", I chose my root partition and changed it to ext4; format; /. Once finished, a window entitled "Write previous changes to disk and continue?" appeared with the text "Before you can select a new partition size...". At no point did I select a new partition size. Hitting "Go Back" got rid of the message and a look at the list of partitions showed that the new info for that root partition was good, so that "new partition size" window appears both incorrect and unnecessary in that situation. I've experienced this twice during two installations.
  - xed admin:///etc/fstab asks for password twice -> happens with gedit as well, must be an issue with admin:// or pkexec.
  - screen reader reads too fast

xfce:
  - system-load-plugin: The switch that enables clicking on the system load monitor to open the task manager is greyed out and in the off position whether or it is turned on or off.
  - quicklauncher plugin: The properties window is in French.

