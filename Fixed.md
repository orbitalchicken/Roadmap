Fixed Issues since Linux Mint 19 BETA

All editions
------------

artwork:
  - mint-x:
    - no icons in Online accounts > Information about Gnome online accounts -> Gnome Contacts, Gnome Documents, Gnome Maps and Gnome Photos
  - mint-y:
    - thunderbird icon isn't the same as its flatpak
    - in nemo additional pane, select a folder in the left page, click in the right pane. The selected folder in the left pane is white on grey, almost invisible.
    - video and subtitle icons are too similar

- The fortune command says 'no fortunes found' -> leftover, fortune is now removed.
- gdebi doesn't install packages unless it's run from the terminal
- ia32-libs: depends on libesd0:i386 which is gone

Cinnamon Edition
----------------

- goa: ubuntu SSO isn't functional -> it won't work without snapd, and it's useless for anything else. Ubuntu non-gnome users auth in snapd CLI anyway, so this should be removed. We don't need it, it's not necessary and it won't work OOTB.

MATE Edition
------------

Xfce Edition
------------
