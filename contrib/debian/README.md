
Debian
====================
This directory contains files used to package advanced/advance-qt
for Debian-based Linux systems. If you compile advanced/advance-qt yourself, there are some useful files here.

## advance: URI support ##


advance-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install advance-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your advance-qt binary to `/usr/bin`
and the `../../share/pixmaps/advance128.png` to `/usr/share/pixmaps`

advance-qt.protocol (KDE)

