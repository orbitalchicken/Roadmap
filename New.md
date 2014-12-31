New bug reports in Mint 17.1 RC

All editions
------------
	- [RFT] rephrase OEM isolinux/grub option --> s/Start Linux Mint/Preinstall Linux Mint/g
	- implement visual upgrade path for Mint 17 users (use mint-meta as a precondition)

Cinnamon Edition - last processed comment: #220
-----------------------------------------------
	- file-roller: fixed in version 3.9.2 (released Sept 18, 2013) http://fileroller.sourceforge.net/news.html https://bugzilla.gnome.org/show_bug.cgi?id=697756

MATE Edition - last processed comment: #79
------------------------------------------

KDE Edition - last processed comment: #54
-----------------------------------------
	- default fonts should be noto fonts
	- problem with CalDAV/CardDAV-Servers… If I create an event in KOrganizer, it only works once and then is broken (no syncing) until I delete the calendar and add it again. Works fine in 17, using tine 2.0 WebDAV-Server
	- In Mint 17 KDE, just like in Mint 16 KDE, it’s not possible to access digital cameras with camera:/ protocol in Dolhpin or in Gwenview (although this operation is the suggested one once you plug in your digital camera to the USB port). The camera protocol support is missing. The workaround is to install the “kamera” package, but it’s not easy to find out this information on the Internet. In Mint 16 KDE there was an additional problem: the camera protocol was then usable only as root. Fortunately, at least this has been fixed in Mint 17 KDE, but the overall experience is still poor on this front.
	- When running the live system it sees and connects to my wireless network (WPA2/PSK) with no problems and installation proceeds normally. On reboot, it fails to connect to the same SSID — just keeps attempting to connect and asking again for the password. I reinstalled and the bug was reproducable. It does not appear to affect Mint 17 KDE however; just 17.1RC. I wonder if it might be related to the new KWallet integration.

Xfce Edition - last processed comment: 63
-----------------------------------------
	- 64bit: Clicking the “Install Linux Mint” icon on the desktop produced a lengthy popup error message about trouble mounting /dev/sdc1 (the USB stick holding the image). Same error after manually mounting or unmounting the stick. The install option in the menu worked normally
	- Dropbox icon is not displayed in the panel, but Dropbox daemon loads and functions as usual. I’ve seen this elsewhere, and seen numerous similar complains. I suspect it’s related to the new QT-based Dropbox release. https://www.dropboxforum.com/hc/communities/public/questions/201545695-After-upgrade-to-3-x-the-dropbox-tray-icon-is-missing-XFCE-Xubuntu-14-04-1-x64-?locale=en-us
	- Window edges don’t seem as grabby as on Cinnamon 17.1 Is this tweakable via a GTK config file?
	- language indicator in system tray area is missing
	- the title “Menu” isn’t shown next to the Mint icon for the menu, as in the other desktop environments.
	- I don’t know if the mint menu is supposed to behave like this, but for the life of me, I can’t use the keyboard to navigate the LEFT side of the menu after pulling it up. Only the items on the right-hand side of the menu can be selected with my keyboard. Is this a bug? Or is this how the mint menu is supposed to behave (by design)?
	- Would be nice to have ctrl-alt-t for terminal also here like in mate.
	- pourquoi l’outil de capture d’écran n’est pas taduit en français alors qu’il l’est sur mate ? Comment faire pour le franciser sous XFCE ?
	- the Xfce terminal’s menu bar doesn’t show
	- lorsque je veux mettre un programme depuis le menu sur le bureau j’ai droit au popup qui veux que je mette ce raccourci en tant qu’exécutable… Dommage pour les néophyte…
	- Le placement du raccourci dans la barre de tache est aussi aléatoire, il est dommage qu’il ne se mette pas directement à côté des autres raccourcis rapides. 
