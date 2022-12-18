![Screenshot_2022-12-17_08-02-55](https://user-images.githubusercontent.com/120763310/208250812-35026e0b-325b-40c1-8a1a-02757bf6e682.png)
# chromeOSlinux_test
my attempt at RPM chromebook install with Cras and Xorg with new kernels
![Screenshot_2022-12-17_08-13-54](https://user-images.githubusercontent.com/120763310/208251214-39e7a7f1-c86a-482d-9710-a92222bd118f.png)

```bash
crouton_Penguin
|-- AUTHORS
|-- CONTRIBUTORS
|-- LICENSE
|-- Makefile
|-- README.md
|-- README.zh.md
|-- SECURITY.md
|-- bootstrap-bash.sh
|-- build
|   |-- CONTRIBUTORS.sed
|   |-- genversion.sh
|   |-- release.sh
|   `-- wrapper.sh
|-- chromeOSLinux.build
|   |-- chroot-etc
|   |   |-- chroot-etc-pam-d
|   |   |   `-- su-l
|   |   |-- kodi-cycle.py
|   |   |-- kodi-keyboard.xml
|   |   |-- pulseaudio-default.pa
|   |   |-- unity-autostart.desktop
|   |   |-- unity-profiled
|   |   |-- xbindkeysrc.scm
|   |   |-- xiwi.conf
|   |   |-- xorg-dummy.conf
|   |   |-- xorg-intel-sna.conf
|   |   |-- xserverrc
|   |   |-- xserverrc-local.example
|   |   |-- xserverrc-xiwi
|   |   `-- xserverrc-xorg
|   |-- host-bin
|   |   |-- chroot-bin
|   |   |   |-- brightness
|   |   |   |-- chromeOSLinux-noroot
|   |   |   |-- chromeOSLinux-unity-autostart
|   |   |   |-- chromeOSLinuxclip
|   |   |   |-- chromeOSLinuxcycle
|   |   |   |-- chromeOSLinuxfindnacl
|   |   |   |-- chromeOSLinuxlhandler
|   |   |   |-- chromeOSLinuxnotify
|   |   |   |-- chromeOSLinuxpowerd
|   |   |   |-- chromeOSLinuxtriggerd
|   |   |   |-- chromeOSLinuxversion
|   |   |   |-- chromeOSLinuxxinitrc-wrapper
|   |   |   |-- crouton-noroot
|   |   |   |-- crouton-unity-autostart
|   |   |   |-- croutonclip
|   |   |   |-- croutoncycle
|   |   |   |-- croutonfindnacl
|   |   |   |-- croutonnotify
|   |   |   |-- croutonpowerd
|   |   |   |-- croutontriggerd
|   |   |   |-- croutonurlhandler
|   |   |   |-- croutonversion
|   |   |   |-- croutonxinitrc-wrapper
|   |   |   |-- gnome-session-wrapper
|   |   |   |-- host-dbus
|   |   |   |-- host-wayland
|   |   |   |-- setres
|   |   |   |-- startgnome
|   |   |   |-- startkde -> crouton-noroot
|   |   |   |-- startlxde -> crouton-noroot
|   |   |   |-- startunity
|   |   |   |-- startxfce4 -> crouton-noroot
|   |   |   |-- volume
|   |   |   |-- xinit
|   |   |   |-- xiwi
|   |   |   `-- z
|   |   |       |-- chromeOSLinux-noroot
|   |   |       |-- chromeOSLinux-unity-autostart
|   |   |       |-- chromeOSLinuxclip
|   |   |       |-- chromeOSLinuxcycle
|   |   |       |-- chromeOSLinuxfindnacl
|   |   |       |-- chromeOSLinuxlhandler
|   |   |       |-- chromeOSLinuxnotify
|   |   |       |-- chromeOSLinuxpowerd
|   |   |       |-- chromeOSLinuxtriggerd
|   |   |       |-- chromeOSLinuxversion
|   |   |       |-- chromeOSLinuxxinitrc-wrapper
|   |   |       |-- cp.sh
|   |   |       |-- crouton-noroot
|   |   |       |-- crouton-unity-autostart
|   |   |       |-- croutonclip
|   |   |       |-- croutoncycle
|   |   |       |-- croutonfindnacl
|   |   |       |-- croutonnotify
|   |   |       |-- croutonpowerd
|   |   |       |-- croutontriggerd
|   |   |       |-- croutonurlhandler
|   |   |       |-- croutonversion
|   |   |       `-- croutonxinitrc-wrapper
|   |   |-- crash_reporter_wrapper
|   |   |-- delete-chroot
|   |   |-- edit-chroot
|   |   |-- enter-chroot
|   |   |-- mount-chroot
|   |   |-- startcli
|   |   |-- starte17
|   |   |-- startgnome
|   |   |-- startkde
|   |   |-- startkodi
|   |   |-- startlxde
|   |   |-- startunity
|   |   |-- startxfce4
|   |   |-- startxiwi
|   |   `-- unmount-chroot
|   |-- installer
|   |   |-- arch
|   |   |   |-- ar
|   |   |   |-- bootstrap
|   |   |   |-- defaults
|   |   |   |-- getrelease.sh
|   |   |   |-- pkgdetails
|   |   |   |-- prepare
|   |   |   `-- releases
|   |   |-- debian
|   |   |   |-- ar
|   |   |   |-- bootstrap
|   |   |   |-- defaults
|   |   |   |-- getrelease.sh
|   |   |   |-- pkgdetails
|   |   |   |-- prepare
|   |   |   `-- releases
|   |   |-- functions
|   |   |-- gentoo
|   |   |   |-- ar
|   |   |   |-- bootstrap
|   |   |   |-- defaults
|   |   |   |-- getrelease.sh
|   |   |   |-- pkgdetails
|   |   |   |-- prepare
|   |   |   `-- releases
|   |   |-- kali
|   |   |   |-- ar
|   |   |   |-- bootstrap
|   |   |   |-- defaults
|   |   |   |-- getrelease.sh
|   |   |   |-- pkgdetails
|   |   |   |-- prepare
|   |   |   `-- releases
|   |   |-- main.sh
|   |   |-- opensuse
|   |   |   |-- ar
|   |   |   |-- bootstrap
|   |   |   |-- defaults
|   |   |   |-- getrelease.sh
|   |   |   |-- pkgdetails
|   |   |   |-- prepare
|   |   |   `-- releases
|   |   |-- prepare.sh
|   |   `-- ubuntu
|   |       |-- ar
|   |       |-- bootstrap
|   |       |-- defaults
|   |       |-- getrelease.sh
|   |       |-- pkgdetails
|   |       |-- prepare
|   |       `-- releases
|   |-- src
|   |   |-- fbserver-proto.h
|   |   |-- fbserver.c
|   |   |-- findnacld.c
|   |   |-- freon.c
|   |   |-- vtmonitor.c
|   |   |-- websocket.c
|   |   |-- websocket.h
|   |   `-- xi2event.c
|   `-- targets
|       |-- audio
|       |-- chrome
|       |-- chrome-beta
|       |-- chrome-common
|       |-- chrome-dev
|       |-- chromium
|       |-- cli-extra
|       |-- common
|       |-- core
|       |-- e17
|       |-- extension
|       |-- gnome
|       |-- gnome-desktop
|       |-- gtk-extra
|       |-- kde
|       |-- kde-desktop
|       |-- keyboard
|       |-- kodi
|       |-- lxde
|       |-- lxde-desktop
|       |-- mate
|       |-- mate-desktop
|       |-- openoffice
|       |-- post-common
|       |-- tools
|       |-- touch
|       |-- unity
|       |-- unity-desktop
|       |-- x11
|       |-- x11-common
|       |-- xbmc
|       |-- xfce
|       |-- xfce-desktop
|       |-- xiwi
|       `-- xorg
|-- chromeOSLinuxfbserver
|-- chromeOSLinuxfindnacld
|-- chromeOSLinuxfreon.so
|-- chromeOSLinuxvtmonitor
|-- chromeOSLinuxwebsocket
|-- chromeOSLinuxxi2event
|-- chroot-bin
|   |-- brightness
|   |-- chromeOSLinux-noroot
|   |-- chromeOSLinux-unity-autostart
|   |-- chromeOSLinuxclip
|   |-- chromeOSLinuxcycle
|   |-- chromeOSLinuxfindnacl
|   |-- chromeOSLinuxlhandler
|   |-- chromeOSLinuxnotify
|   |-- chromeOSLinuxpowerd
|   |-- chromeOSLinuxtriggerd
|   |-- chromeOSLinuxversion
|   |-- chromeOSLinuxxinitrc-wrapper
|   |-- crouton-noroot
|   |-- crouton-unity-autostart
|   |-- croutonclip
|   |-- croutoncycle
|   |-- croutonfindnacl
|   |-- croutonnotify
|   |-- croutonpowerd
|   |-- croutontriggerd
|   |-- croutonurlhandler
|   |-- croutonversion
|   |-- croutonxinitrc-wrapper
|   |-- gnome-session-wrapper
|   |-- host-dbus
|   |-- host-wayland
|   |-- setres
|   |-- startgnome
|   |-- startkde -> crouton-noroot
|   |-- startlxde -> crouton-noroot
|   |-- startunity
|   |-- startxfce4 -> crouton-noroot
|   |-- volume
|   |-- xinit
|   |-- xiwi
|   `-- z
|       |-- chromeOSLinux-noroot
|       |-- chromeOSLinux-unity-autostart
|       |-- chromeOSLinuxclip
|       |-- chromeOSLinuxcycle
|       |-- chromeOSLinuxfindnacl
|       |-- chromeOSLinuxlhandler
|       |-- chromeOSLinuxnotify
|       |-- chromeOSLinuxpowerd
|       |-- chromeOSLinuxtriggerd
|       |-- chromeOSLinuxversion
|       |-- chromeOSLinuxxinitrc-wrapper
|       |-- cp.sh
|       |-- crouton-noroot
|       |-- crouton-unity-autostart
|       |-- croutonclip
|       |-- croutoncycle
|       |-- croutonfindnacl
|       |-- croutonnotify
|       |-- croutonpowerd
|       |-- croutontriggerd
|       |-- croutonurlhandler
|       |-- croutonversion
|       `-- croutonxinitrc-wrapper
|-- chroot-etc
|   |-- chroot-etc-pam-d
|   |   `-- su-l
|   |-- kodi-cycle.py
|   |-- kodi-keyboard.xml
|   |-- pulseaudio-default.pa
|   |-- unity-autostart.desktop
|   |-- unity-profiled
|   |-- xbindkeysrc.scm
|   |-- xiwi.conf
|   |-- xorg-dummy.conf
|   |-- xorg-intel-sna.conf
|   |-- xserverrc
|   |-- xserverrc-local.example
|   |-- xserverrc-xiwi
|   `-- xserverrc-xorg
|-- crouton.build
|   |-- chroot-bin
|   |   |-- brightness
|   |   |-- crouton-noroot
|   |   |-- crouton-unity-autostart
|   |   |-- croutonclip
|   |   |-- croutoncycle
|   |   |-- croutonfindnacl
|   |   |-- croutonnotify
|   |   |-- croutonpowerd
|   |   |-- croutontriggerd
|   |   |-- croutonurlhandler
|   |   |-- croutonversion
|   |   |-- croutonxinitrc-wrapper
|   |   |-- gnome-session-wrapper
|   |   |-- host-dbus
|   |   |-- host-wayland
|   |   |-- setres
|   |   |-- startgnome
|   |   |-- startkde -> crouton-noroot
|   |   |-- startlxde -> crouton-noroot
|   |   |-- startunity
|   |   |-- startxfce4 -> crouton-noroot
|   |   |-- volume
|   |   |-- xinit
|   |   `-- xiwi
|   |-- chroot-etc
|   |   |-- chroot-etc-pam-d
|   |   |   `-- su-l
|   |   |-- kodi-cycle.py
|   |   |-- kodi-keyboard.xml
|   |   |-- pulseaudio-default.pa
|   |   |-- unity-autostart.desktop
|   |   |-- unity-profiled
|   |   |-- xbindkeysrc.scm
|   |   |-- xiwi.conf
|   |   |-- xorg-dummy.conf
|   |   |-- xorg-intel-sna.conf
|   |   |-- xserverrc
|   |   |-- xserverrc-local.example
|   |   |-- xserverrc-xiwi
|   |   `-- xserverrc-xorg
|   |-- host-bin
|   |   |-- crash_reporter_wrapper
|   |   |-- delete-chroot
|   |   |-- edit-chroot
|   |   |-- enter-chroot
|   |   |-- mount-chroot
|   |   |-- startcli
|   |   |-- starte17
|   |   |-- startgnome
|   |   |-- startkde
|   |   |-- startkodi
|   |   |-- startlxde
|   |   |-- startunity
|   |   |-- startxfce4
|   |   |-- startxiwi
|   |   `-- unmount-chroot
|   |-- installer
|   |   |-- arch
|   |   |   |-- ar
|   |   |   |-- bootstrap
|   |   |   |-- defaults
|   |   |   |-- getrelease.sh
|   |   |   |-- pkgdetails
|   |   |   |-- prepare
|   |   |   `-- releases
|   |   |-- debian
|   |   |   |-- ar
|   |   |   |-- bootstrap
|   |   |   |-- defaults
|   |   |   |-- getrelease.sh
|   |   |   |-- pkgdetails
|   |   |   |-- prepare
|   |   |   `-- releases
|   |   |-- functions
|   |   |-- gentoo
|   |   |   |-- ar
|   |   |   |-- bootstrap
|   |   |   |-- defaults
|   |   |   |-- getrelease.sh
|   |   |   |-- pkgdetails
|   |   |   |-- prepare
|   |   |   `-- releases
|   |   |-- kali
|   |   |   |-- ar
|   |   |   |-- bootstrap
|   |   |   |-- defaults
|   |   |   |-- getrelease.sh
|   |   |   |-- pkgdetails
|   |   |   |-- prepare
|   |   |   `-- releases
|   |   |-- main.sh
|   |   |-- prepare.sh
|   |   `-- ubuntu
|   |       |-- ar
|   |       |-- bootstrap
|   |       |-- defaults
|   |       |-- getrelease.sh
|   |       |-- pkgdetails
|   |       |-- prepare
|   |       `-- releases
|   |-- src
|   |   |-- fbserver-proto.h
|   |   |-- fbserver.c
|   |   |-- findnacld.c
|   |   |-- freon.c
|   |   |-- vtmonitor.c
|   |   |-- websocket.c
|   |   |-- websocket.h
|   |   `-- xi2event.c
|   `-- targets
|       |-- audio
|       |-- chrome
|       |-- chrome-beta
|       |-- chrome-common
|       |-- chrome-dev
|       |-- chromium
|       |-- cli-extra
|       |-- common
|       |-- core
|       |-- e17
|       |-- extension
|       |-- gnome
|       |-- gnome-desktop
|       |-- gtk-extra
|       |-- kde
|       |-- kde-desktop
|       |-- keyboard
|       |-- kodi
|       |-- lxde
|       |-- lxde-desktop
|       |-- mate
|       |-- mate-desktop
|       |-- openoffice
|       |-- post-common
|       |-- tools
|       |-- touch
|       |-- unity
|       |-- unity-desktop
|       |-- x11
|       |-- x11-common
|       |-- xbmc
|       |-- xfce
|       |-- xfce-desktop
|       |-- xiwi
|       `-- xorg
|-- debootstrap
|   |-- Makefile
|   |-- README
|   |-- debootstrap
|   |-- debootstrap.8
|   |-- devices.tar.gz
|   |-- functions
|   |-- scripts
|   |   |-- OSS -> opensuse
|   |   |-- aequorea
|   |   |-- alarm -> arch
|   |   |-- amber
|   |   |-- arch
|   |   |-- artful -> gutsy
|   |   |-- ascii -> sid
|   |   |-- bartholomea -> aequorea
|   |   |-- beowulf -> sid
|   |   |-- bionic -> gutsy
|   |   |-- bookworm -> sid
|   |   |-- breezy
|   |   |-- bullseye -> sid
|   |   |-- buster -> sid
|   |   |-- byzantium -> amber
|   |   |-- ceres -> sid
|   |   |-- chromodoris -> aequorea
|   |   |-- cosmic -> gutsy
|   |   |-- crimson -> amber
|   |   |-- dapper
|   |   |-- dasyatis -> aequorea
|   |   |-- debian-common
|   |   |-- disco -> gutsy
|   |   |-- edgy
|   |   |-- eoan -> gutsy
|   |   |-- etch
|   |   |-- etch-m68k -> etch
|   |   |-- feisty
|   |   |-- focal -> gutsy
|   |   |-- gentoo
|   |   |-- gentoo-openstack -> gentoo
|   |   |-- groovy -> gutsy
|   |   |-- gutsy
|   |   |-- hardy -> gutsy
|   |   |-- hirsute -> groovy
|   |   |-- hoary
|   |   |-- hoary.buildd
|   |   |-- impish -> gutsy
|   |   |-- intrepid -> gutsy
|   |   |-- jammy -> gutsy
|   |   |-- jaunty -> gutsy
|   |   |-- jessie -> sid
|   |   |-- jessie-kfreebsd -> sid
|   |   |-- kali
|   |   |-- kali-dev -> kali
|   |   |-- kali-last-snapshot -> kali
|   |   |-- kali-rolling -> kali
|   |   |-- karmic -> gutsy
|   |   |-- kinetic -> gutsy
|   |   |-- leap -> opensuse
|   |   |-- leap-micro -> opensuse
|   |   |-- leap-micro-current -> opensuse
|   |   |-- lenny -> etch
|   |   |-- lucid -> gutsy
|   |   |-- maverick -> gutsy
|   |   |-- natty -> gutsy
|   |   |-- oldoldstable -> sid
|   |   |-- oldstable -> sid
|   |   |-- oneiric -> gutsy
|   |   |-- openSUSE-current -> opensuse
|   |   |-- openSUSE-stable -> opensuse
|   |   |-- opensuse
|   |   |-- potato
|   |   |-- precise -> gutsy
|   |   |-- quantal -> gutsy
|   |   |-- raring -> gutsy
|   |   |-- sarge
|   |   |-- sarge.buildd
|   |   |-- sarge.fakechroot
|   |   |-- saucy -> gutsy
|   |   |-- sid
|   |   |-- squeeze -> etch
|   |   |-- stable -> sid
|   |   |-- stage3 -> gentoo
|   |   |-- stage4 -> gentoo
|   |   |-- stretch -> sid
|   |   |-- testing -> sid
|   |   |-- trixie -> sid
|   |   |-- trusty -> gutsy
|   |   |-- unstable -> sid
|   |   |-- utopic -> gutsy
|   |   |-- vivid -> gutsy
|   |   |-- warty
|   |   |-- warty.buildd
|   |   |-- wheezy -> sid
|   |   |-- wily -> gutsy
|   |   |-- woody
|   |   |-- woody.buildd
|   |   |-- xenial -> gutsy
|   |   |-- yakkety -> gutsy
|   |   `-- zesty -> gutsy
|   `-- scripts.tar.gz
|-- debootstrap.old
|   |-- Makefile
|   |-- README
|   |-- TODO
|   |-- debootstrap
|   |-- debootstrap.8
|   |-- devices.tar.gz
|   |-- functions
|   `-- scripts
|       |-- aequorea
|       |-- amber
|       |-- artful -> gutsy
|       |-- ascii -> sid
|       |-- bartholomea -> aequorea
|       |-- beowulf -> sid
|       |-- bionic -> gutsy
|       |-- bookworm -> sid
|       |-- breezy
|       |-- bullseye -> sid
|       |-- buster -> sid
|       |-- ceres -> sid
|       |-- chromodoris -> aequorea
|       |-- cosmic -> gutsy
|       |-- dapper
|       |-- dasyatis -> aequorea
|       |-- debian-common
|       |-- disco -> gutsy
|       |-- edgy
|       |-- eoan -> gutsy
|       |-- etch
|       |-- etch-m68k -> etch
|       |-- feisty
|       |-- focal -> gutsy
|       |-- groovy -> gutsy
|       |-- gutsy
|       |-- hardy -> gutsy
|       |-- hirsute -> groovy
|       |-- hoary
|       |-- hoary.buildd
|       |-- impish -> gutsy
|       |-- intrepid -> gutsy
|       |-- jaunty -> gutsy
|       |-- jessie -> sid
|       |-- jessie-kfreebsd -> sid
|       |-- kali
|       |-- kali-dev -> kali
|       |-- kali-last-snapshot -> kali
|       |-- kali-rolling -> kali
|       |-- karmic -> gutsy
|       |-- lenny -> etch
|       |-- lucid -> gutsy
|       |-- maverick -> gutsy
|       |-- natty -> gutsy
|       |-- oldoldstable -> sid
|       |-- oldstable -> sid
|       |-- oneiric -> gutsy
|       |-- potato
|       |-- precise -> gutsy
|       |-- quantal -> gutsy
|       |-- raring -> gutsy
|       |-- sarge
|       |-- sarge.buildd
|       |-- sarge.fakechroot
|       |-- saucy -> gutsy
|       |-- sid
|       |-- squeeze -> etch
|       |-- stable -> sid
|       |-- stretch -> sid
|       |-- testing -> sid
|       |-- trusty -> gutsy
|       |-- unstable -> sid
|       |-- utopic -> gutsy
|       |-- vivid -> gutsy
|       |-- warty
|       |-- warty.buildd
|       |-- wheezy -> sid
|       |-- wily -> gutsy
|       |-- woody
|       |-- woody.buildd
|       |-- xenial -> gutsy
|       |-- yakkety -> gutsy
|       `-- zesty -> gutsy
|-- dir.txt
|-- host-bin
|   |-- crash_reporter_wrapper
|   |-- delete-chroot -> edit-chroot
|   |-- edit-chroot
|   |-- enter-chroot
|   |-- mount-chroot
|   |-- startcli
|   |-- starte17
|   |-- startgnome
|   |-- startkde
|   |-- startkodi
|   |-- startlxde
|   |-- startunity
|   |-- startxfce4
|   |-- startxiwi
|   `-- unmount-chroot
|-- host-ext
|   |-- crouton
|   |   |-- background.html
|   |   |-- background.js
|   |   |-- connected-19.png
|   |   |-- connected-38.png
|   |   |-- disabled-19.png
|   |   |-- disabled-38.png
|   |   |-- disconnected-19.png
|   |   |-- disconnected-38.png
|   |   |-- error-19.png
|   |   |-- error-38.png
|   |   |-- first.html
|   |   |-- icon-128.png
|   |   |-- icon-48.png
|   |   |-- kiwi.nmf
|   |   |-- manifest.json
|   |   |-- popup.html
|   |   |-- popup.js
|   |   |-- window.html
|   |   `-- window.js
|   |-- gencrx.sh
|   |-- logo.svg
|   `-- nacl_src
|       |-- Makefile
|       |-- keycode_converter.h
|       `-- kiwi.cc
|-- installer
|   |-- arch
|   |   |-- ar -> ../ubuntu/ar
|   |   |-- bootstrap -> ../ubuntu/bootstrap
|   |   |-- defaults
|   |   |-- getrelease.sh -> ../ubuntu/getrelease.sh
|   |   |-- new
|   |   |   `-- arch
|   |   |       |-- bootstrap
|   |   |       |-- defaults
|   |   |       |-- getrelease.sh
|   |   |       |-- prepare
|   |   |       `-- releases
|   |   |-- pkgdetails -> ../ubuntu/pkgdetails
|   |   |-- prepare -> ../ubuntu/prepare
|   |   `-- releases
|   |-- crouton
|   |-- debian
|   |   |-- ar -> ../ubuntu/ar
|   |   |-- bootstrap -> ../ubuntu/bootstrap
|   |   |-- defaults
|   |   |-- getrelease.sh -> ../ubuntu/getrelease.sh
|   |   |-- pkgdetails -> ../ubuntu/pkgdetails
|   |   |-- prepare -> ../ubuntu/prepare
|   |   `-- releases
|   |-- functions
|   |-- gentoo
|   |   |-- ar -> ../ubuntu/ar
|   |   |-- bootstrap -> ../ubuntu/bootstrap
|   |   |-- defaults
|   |   |-- getrelease.sh -> ../ubuntu/getrelease.sh
|   |   |-- pkgdetails -> ../ubuntu/pkgdetails
|   |   |-- prepare -> ../ubuntu/prepare
|   |   `-- releases
|   |-- kali
|   |   |-- ar -> ../ubuntu/ar
|   |   |-- bootstrap -> ../ubuntu/bootstrap
|   |   |-- defaults
|   |   |-- getrelease.sh -> ../ubuntu/getrelease.sh
|   |   |-- pkgdetails -> ../ubuntu/pkgdetails
|   |   |-- prepare -> ../ubuntu/prepare
|   |   `-- releases
|   |-- main.sh
|   |-- make.txt
|   |-- opensuse
|   |   |-- ar -> ../ubuntu/ar
|   |   |-- bootstrap -> ../ubuntu/bootstrap
|   |   |-- defaults
|   |   |-- getrelease.sh -> ../ubuntu/getrelease.sh
|   |   |-- pkgdetails -> ../ubuntu/pkgdetails
|   |   |-- prepare -> ../ubuntu/prepare
|   |   `-- releases
|   |-- prepare.sh
|   `-- ubuntu
|       |-- ar
|       |-- bootstrap
|       |-- defaults
|       |-- getrelease.sh
|       |-- pkgdetails
|       |-- prepare
|       `-- releases
|-- jammy
|   |-- Contributors\ to\ dnschneid_crouton\ \302\267\ GitHub.pdf
|   |-- gutsy
|   |-- init
|   |-- jammy
|   |-- jammy\ packages
|   |-- mate
|   |-- mate-desktop
|   `-- notes\ for\ Jammy,\ new\ install
|-- make.txt
|-- savetrgt
|   |-- audio
|   |-- chrome
|   |-- chrome-beta
|   |-- chrome-common
|   |-- chrome-dev
|   |-- chromium
|   |-- cli-extra
|   |-- common
|   |-- core
|   |-- e17
|   |-- extension
|   |-- gnome
|   |-- gnome-desktop
|   |-- gtk-extra
|   |-- kde
|   |-- kde-desktop
|   |-- keyboard
|   |-- kodi
|   |-- lxde
|   |-- lxde-desktop
|   |-- mate
|   |-- mate-desktop
|   |-- openoffice
|   |-- post-common
|   |-- targets
|   |   |-- audio
|   |   |-- chrome
|   |   |-- chrome-beta
|   |   |-- chrome-common
|   |   |-- chrome-dev
|   |   |-- chromium
|   |   |-- cli-extra
|   |   |-- common
|   |   |-- core
|   |   |-- e17
|   |   |-- extension
|   |   |-- gnome
|   |   |-- gnome-desktop
|   |   |-- gtk-extra
|   |   |-- kde
|   |   |-- kde-desktop
|   |   |-- keyboard
|   |   |-- kodi
|   |   |-- lxde
|   |   |-- lxde-desktop
|   |   |-- mate
|   |   |-- mate-desktop
|   |   |-- openoffice
|   |   |-- post-common
|   |   |-- tools
|   |   |-- touch
|   |   |-- unity
|   |   |-- unity-desktop
|   |   |-- x11
|   |   |-- x11-common
|   |   |-- xbmc
|   |   |-- xfce
|   |   |-- xfce-desktop
|   |   |-- xiwi
|   |   `-- xorg
|   |-- tools
|   |-- touch
|   |-- unity
|   |-- unity-desktop
|   |-- x11
|   |-- x11-common
|   |-- xbmc
|   |-- xfce
|   |-- xfce-desktop
|   |-- xiwi
|   `-- xorg
|-- src
|   |-- fbserver-proto.h
|   |-- fbserver.c
|   |-- findnacld.c
|   |-- freon.c
|   |-- vtmonitor.c
|   |-- websocket.c
|   |-- websocket.h
|   `-- xi2event.c
|-- tarboot
|   |-- chroot-etc
|   |   |-- chromeOSLinux
|   |   |   |-- core_pattern
|   |   |   |-- name
|   |   |   |-- pulseaudio-default.pa
|   |   |   |-- shares
|   |   |   |-- targets
|   |   |   |-- xbindkeysrc.scm
|   |   |   |-- xiwi.conf
|   |   |   |-- xmethod
|   |   |   |-- xorg-dummy.conf
|   |   |   |-- xorg-intel-sna.conf
|   |   |   |-- xserverrc
|   |   |   |-- xserverrc-local.example
|   |   |   |-- xserverrc-xiwi
|   |   |   `-- xserverrc-xorg
|   |   |-- chroot-etc-pam-d
|   |   |   `-- su-l
|   |   |-- group
|   |   |-- kodi-cycle.py
|   |   |-- kodi-keyboard.xml
|   |   |-- passwd
|   |   |-- pulseaudio-default.pa
|   |   |-- unity-autostart.desktop
|   |   |-- unity-profiled
|   |   |-- xbindkeysrc.scm
|   |   |-- xiwi.conf
|   |   |-- xorg-dummy.conf
|   |   |-- xorg-intel-sna.conf
|   |   |-- xserverrc
|   |   |-- xserverrc-local.example
|   |   |-- xserverrc-xiwi
|   |   `-- xserverrc-xorg
|   |-- targets
|   |   |-- audio
|   |   |-- chrome
|   |   |-- chrome-beta
|   |   |-- chrome-common
|   |   |-- chrome-dev
|   |   |-- chromium
|   |   |-- cli-extra
|   |   |-- common
|   |   |-- core
|   |   |-- e17
|   |   |-- extension
|   |   |-- gnome
|   |   |-- gnome-desktop
|   |   |-- gtk-extra
|   |   |-- kde
|   |   |-- kde-desktop
|   |   |-- keyboard
|   |   |-- kodi
|   |   |-- lxde
|   |   |-- lxde-desktop
|   |   |-- mate
|   |   |-- mate-desktop
|   |   |-- openoffice
|   |   |-- post-common
|   |   |-- tools
|   |   |-- touch
|   |   |-- unity
|   |   |-- unity-desktop
|   |   |-- x11
|   |   |-- x11-common
|   |   |-- xbmc
|   |   |-- xfce
|   |   |-- xfce-desktop
|   |   |-- xiwi
|   |   `-- xorg
|   |-- usrlocalbin
|   |   |-- Makefile
|   |   |-- README
|   |   |-- TODO
|   |   |-- brightness
|   |   |-- chromeOSLinux-noroot
|   |   |-- chromeOSLinuxclip
|   |   |-- chromeOSLinuxcycle
|   |   |-- chromeOSLinuxfbserver
|   |   |-- chromeOSLinuxfindnacl
|   |   |-- chromeOSLinuxfindnacld
|   |   |-- chromeOSLinuxnotify
|   |   |-- chromeOSLinuxpowerd
|   |   |-- chromeOSLinuxtriggerd
|   |   |-- chromeOSLinuxurlhandler
|   |   |-- chromeOSLinuxversion
|   |   |-- chromeOSLinuxvtmonitor
|   |   |-- chromeOSLinuxwebsocket
|   |   |-- chromeOSLinuxxi2event
|   |   |-- chromeOSLinuxxinitrc-wrapper
|   |   |-- cras_test_client
|   |   |-- debootstrap
|   |   |-- debootstrap.8
|   |   |-- devices.tar.gz
|   |   |-- functions
|   |   |-- gnome-screensaver-command -> chromeOSLinuxpowerd
|   |   |-- host-dbus
|   |   |-- host-wayland
|   |   |-- scripts
|   |   |   |-- OSS -> opensuse
|   |   |   |-- aequorea
|   |   |   |-- alarm -> arch
|   |   |   |-- amber
|   |   |   |-- arch
|   |   |   |-- artful -> gutsy
|   |   |   |-- ascii -> sid
|   |   |   |-- bartholomea -> aequorea
|   |   |   |-- beowulf -> sid
|   |   |   |-- bionic -> gutsy
|   |   |   |-- bookworm -> sid
|   |   |   |-- breezy
|   |   |   |-- bullseye -> sid
|   |   |   |-- buster -> sid
|   |   |   |-- byzantium -> amber
|   |   |   |-- ceres -> sid
|   |   |   |-- chromodoris -> aequorea
|   |   |   |-- cosmic -> gutsy
|   |   |   |-- crimson -> amber
|   |   |   |-- dapper
|   |   |   |-- dasyatis -> aequorea
|   |   |   |-- debian-common
|   |   |   |-- disco -> gutsy
|   |   |   |-- edgy
|   |   |   |-- eoan -> gutsy
|   |   |   |-- etch
|   |   |   |-- etch-m68k -> etch
|   |   |   |-- feisty
|   |   |   |-- focal -> gutsy
|   |   |   |-- gentoo
|   |   |   |-- gentoo-openstack -> gentoo
|   |   |   |-- groovy -> gutsy
|   |   |   |-- gutsy
|   |   |   |-- hardy -> gutsy
|   |   |   |-- hirsute -> groovy
|   |   |   |-- hoary
|   |   |   |-- hoary.buildd
|   |   |   |-- impish -> gutsy
|   |   |   |-- intrepid -> gutsy
|   |   |   |-- jammy -> gutsy
|   |   |   |-- jaunty -> gutsy
|   |   |   |-- jessie -> sid
|   |   |   |-- jessie-kfreebsd -> sid
|   |   |   |-- kali
|   |   |   |-- kali-dev -> kali
|   |   |   |-- kali-last-snapshot -> kali
|   |   |   |-- kali-rolling -> kali
|   |   |   |-- karmic -> gutsy
|   |   |   |-- kinetic -> gutsy
|   |   |   |-- leap -> opensuse
|   |   |   |-- leap-micro -> opensuse
|   |   |   |-- leap-micro-current -> opensuse
|   |   |   |-- lenny -> etch
|   |   |   |-- lucid -> gutsy
|   |   |   |-- maverick -> gutsy
|   |   |   |-- natty -> gutsy
|   |   |   |-- oldoldstable -> sid
|   |   |   |-- oldstable -> sid
|   |   |   |-- oneiric -> gutsy
|   |   |   |-- openSUSE-current -> opensuse
|   |   |   |-- openSUSE-stable -> opensuse
|   |   |   |-- opensuse
|   |   |   |-- potato
|   |   |   |-- precise -> gutsy
|   |   |   |-- quantal -> gutsy
|   |   |   |-- raring -> gutsy
|   |   |   |-- sarge
|   |   |   |-- sarge.buildd
|   |   |   |-- sarge.fakechroot
|   |   |   |-- saucy -> gutsy
|   |   |   |-- scripts
|   |   |   |   |-- aequorea
|   |   |   |   |-- amber
|   |   |   |   |-- artful -> gutsy
|   |   |   |   |-- ascii -> sid
|   |   |   |   |-- bartholomea -> aequorea
|   |   |   |   |-- beowulf -> sid
|   |   |   |   |-- bionic -> gutsy
|   |   |   |   |-- bookworm -> sid
|   |   |   |   |-- breezy
|   |   |   |   |-- bullseye -> sid
|   |   |   |   |-- buster -> sid
|   |   |   |   |-- byzantium -> amber
|   |   |   |   |-- ceres -> sid
|   |   |   |   |-- chromodoris -> aequorea
|   |   |   |   |-- cosmic -> gutsy
|   |   |   |   |-- crimson -> amber
|   |   |   |   |-- dapper
|   |   |   |   |-- dasyatis -> aequorea
|   |   |   |   |-- debian-common
|   |   |   |   |-- disco -> gutsy
|   |   |   |   |-- edgy
|   |   |   |   |-- eoan -> gutsy
|   |   |   |   |-- etch
|   |   |   |   |-- etch-m68k -> etch
|   |   |   |   |-- feisty
|   |   |   |   |-- focal -> gutsy
|   |   |   |   |-- gentoo
|   |   |   |   |-- gentoo-openstack -> gentoo
|   |   |   |   |-- groovy -> gutsy
|   |   |   |   |-- gutsy
|   |   |   |   |-- hardy -> gutsy
|   |   |   |   |-- hirsute -> groovy
|   |   |   |   |-- hoary
|   |   |   |   |-- hoary.buildd
|   |   |   |   |-- impish -> gutsy
|   |   |   |   |-- intrepid -> gutsy
|   |   |   |   |-- jammy -> gutsy
|   |   |   |   |-- jaunty -> gutsy
|   |   |   |   |-- jessie -> sid
|   |   |   |   |-- jessie-kfreebsd -> sid
|   |   |   |   |-- kali
|   |   |   |   |-- kali-dev -> kali
|   |   |   |   |-- kali-last-snapshot -> kali
|   |   |   |   |-- kali-rolling -> kali
|   |   |   |   |-- karmic -> gutsy
|   |   |   |   |-- kinetic -> gutsy
|   |   |   |   |-- lenny -> etch
|   |   |   |   |-- lucid -> gutsy
|   |   |   |   |-- maverick -> gutsy
|   |   |   |   |-- natty -> gutsy
|   |   |   |   |-- oldoldstable -> sid
|   |   |   |   |-- oldstable -> sid
|   |   |   |   |-- oneiric -> gutsy
|   |   |   |   |-- potato
|   |   |   |   |-- precise -> gutsy
|   |   |   |   |-- quantal -> gutsy
|   |   |   |   |-- raring -> gutsy
|   |   |   |   |-- sarge
|   |   |   |   |-- sarge.buildd
|   |   |   |   |-- sarge.fakechroot
|   |   |   |   |-- saucy -> gutsy
|   |   |   |   |-- sid
|   |   |   |   |-- squeeze -> etch
|   |   |   |   |-- stable -> sid
|   |   |   |   |-- stage3-arm64 -> gentoo
|   |   |   |   |-- stage3-arm64-musl -> gentoo
|   |   |   |   |-- stage4-amd64-musl -> gentoo
|   |   |   |   |-- stage4-arm64 -> gentoo
|   |   |   |   |-- stretch -> sid
|   |   |   |   |-- testing -> sid
|   |   |   |   |-- trixie -> sid
|   |   |   |   |-- trusty -> gutsy
|   |   |   |   |-- unstable -> sid
|   |   |   |   |-- utopic -> gutsy
|   |   |   |   |-- vivid -> gutsy
|   |   |   |   |-- warty
|   |   |   |   |-- warty.buildd
|   |   |   |   |-- wheezy -> sid
|   |   |   |   |-- wily -> gutsy
|   |   |   |   |-- woody
|   |   |   |   |-- woody.buildd
|   |   |   |   |-- xenial -> gutsy
|   |   |   |   |-- yakkety -> gutsy
|   |   |   |   `-- zesty -> gutsy
|   |   |   |-- sid
|   |   |   |-- squeeze -> etch
|   |   |   |-- stable -> sid
|   |   |   |-- stage3 -> gentoo
|   |   |   |-- stage4 -> gentoo
|   |   |   |-- stretch -> sid
|   |   |   |-- testing -> sid
|   |   |   |-- trixie -> sid
|   |   |   |-- trusty -> gutsy
|   |   |   |-- unstable -> sid
|   |   |   |-- utopic -> gutsy
|   |   |   |-- vivid -> gutsy
|   |   |   |-- warty
|   |   |   |-- warty.buildd
|   |   |   |-- wheezy -> sid
|   |   |   |-- wily -> gutsy
|   |   |   |-- woody
|   |   |   |-- woody.buildd
|   |   |   |-- xenial -> gutsy
|   |   |   |-- yakkety -> gutsy
|   |   |   `-- zesty -> gutsy
|   |   |-- scripts.tar.gz
|   |   |-- setres
|   |   |-- startxfce -> chromeOSLinux-noroot
|   |   |-- volume
|   |   |-- xinit
|   |   |-- xiwi
|   |   `-- xscreensaver-command -> chromeOSLinuxpowerd
|   `-- usrshare
|       `-- X11
|           |-- XErrorDB
|           |-- bindings
|           |   |-- acorn
|           |   |-- apollo
|           |   |-- dec
|           |   |-- dg_AViiON
|           |   |-- doubleclick
|           |   |-- hal
|           |   |-- hitachi
|           |   |-- hp
|           |   |-- ibm
|           |   |-- intergraph
|           |   |-- intergraph17
|           |   |-- megatek
|           |   |-- motorola
|           |   |-- ncr_at
|           |   |-- ncr_vt
|           |   |-- pc
|           |   |-- sgi
|           |   |-- siemens_9733
|           |   |-- siemens_wx200
|           |   |-- sni
|           |   |-- sni_97801
|           |   |-- sony
|           |   |-- sun
|           |   |-- sun_at
|           |   |-- tek
|           |   `-- xmbind.alias
|           |-- locale
|           |   |-- C
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- am_ET.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- armscii-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- compose.dir
|           |   |-- cs_CZ.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- el_GR.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- en_US.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- fi_FI.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- georgian-academy
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- georgian-ps
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- ibm-cp1133
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iscii-dev
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- isiri-3342
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-1
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-10
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-11
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-13
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-14
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-15
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-2
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-3
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-4
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-5
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-6
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-7
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-9
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- iso8859-9e
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- ja
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- ja.JIS
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- ja.SJIS
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- ja_JP.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- km_KH.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- ko
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- ko_KR.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- koi8-c
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- koi8-r
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- koi8-u
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- locale.alias
|           |   |-- locale.dir
|           |   |-- microsoft-cp1251
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- microsoft-cp1255
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- microsoft-cp1256
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- mulelao-1
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- nokhchi-1
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- pt_BR.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- pt_PT.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- ru_RU.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- sr_RS.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- tatar-cyr
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- th_TH
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- th_TH.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- tscii-0
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- vi_VN.tcvn
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- vi_VN.viscii
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- zh_CN
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- zh_CN.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- zh_CN.gb18030
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- zh_CN.gbk
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- zh_HK.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- zh_HK.big5
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- zh_HK.big5hkscs
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- zh_TW
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   |-- zh_TW.UTF-8
|           |   |   |-- Compose
|           |   |   |-- XI18N_OBJS
|           |   |   `-- XLC_LOCALE
|           |   `-- zh_TW.big5
|           |       |-- Compose
|           |       |-- XI18N_OBJS
|           |       `-- XLC_LOCALE
|           |-- rgb.txt -> /etc/X11/rgb.txt
|           |-- xkb
|           |   |-- compat
|           |   |   |-- README
|           |   |   |-- accessx
|           |   |   |-- basic
|           |   |   |-- caps
|           |   |   |-- complete
|           |   |   |-- iso9995
|           |   |   |-- japan
|           |   |   |-- ledcaps
|           |   |   |-- ledcompose
|           |   |   |-- lednum
|           |   |   |-- ledscroll
|           |   |   |-- level5
|           |   |   |-- misc
|           |   |   |-- mousekeys
|           |   |   |-- olpc
|           |   |   |-- pc
|           |   |   |-- pc98
|           |   |   |-- xfree86
|           |   |   `-- xtest
|           |   |-- geometry
|           |   |   |-- README
|           |   |   |-- amiga
|           |   |   |-- ataritt
|           |   |   |-- chicony
|           |   |   |-- dell
|           |   |   |-- digital_vndr
|           |   |   |   |-- lk
|           |   |   |   |-- pc
|           |   |   |   `-- unix
|           |   |   |-- everex
|           |   |   |-- fujitsu
|           |   |   |-- hhk
|           |   |   |-- hp
|           |   |   |-- keytronic
|           |   |   |-- kinesis
|           |   |   |-- macintosh
|           |   |   |-- microsoft
|           |   |   |-- nec
|           |   |   |-- nokia
|           |   |   |-- northgate
|           |   |   |-- pc
|           |   |   |-- sanwa
|           |   |   |-- sgi_vndr
|           |   |   |   |-- O2
|           |   |   |   |-- indigo
|           |   |   |   `-- indy
|           |   |   |-- sony
|           |   |   |-- steelseries
|           |   |   |-- sun
|           |   |   |-- teck
|           |   |   |-- thinkpad
|           |   |   |-- typematrix
|           |   |   `-- winbook
|           |   |-- keycodes
|           |   |   |-- README
|           |   |   |-- aliases
|           |   |   |-- amiga
|           |   |   |-- ataritt
|           |   |   |-- digital_vndr
|           |   |   |   |-- lk
|           |   |   |   `-- pc
|           |   |   |-- empty
|           |   |   |-- evdev
|           |   |   |-- fujitsu
|           |   |   |-- hp
|           |   |   |-- ibm
|           |   |   |-- jolla
|           |   |   |-- macintosh
|           |   |   |-- olpc
|           |   |   |-- sgi_vndr
|           |   |   |   |-- indigo
|           |   |   |   |-- indy
|           |   |   |   `-- iris
|           |   |   |-- sony
|           |   |   |-- sun
|           |   |   |-- xfree86
|           |   |   `-- xfree98
|           |   |-- rules
|           |   |   |-- README
|           |   |   |-- base
|           |   |   |-- base.extras.xml
|           |   |   |-- base.lst
|           |   |   |-- base.xml
|           |   |   |-- evdev
|           |   |   |-- evdev.extras.xml
|           |   |   |-- evdev.lst
|           |   |   |-- evdev.xml
|           |   |   |-- xfree86 -> base
|           |   |   |-- xfree86.lst -> base.lst
|           |   |   |-- xfree86.xml -> base.xml
|           |   |   |-- xfree98
|           |   |   |-- xkb.dtd
|           |   |   |-- xorg -> base
|           |   |   |-- xorg.lst -> base.lst
|           |   |   `-- xorg.xml -> base.xml
|           |   |-- symbols
|           |   |   |-- af
|           |   |   |-- al
|           |   |   |-- altwin
|           |   |   |-- am
|           |   |   |-- apl
|           |   |   |-- ara
|           |   |   |-- at
|           |   |   |-- au
|           |   |   |-- az
|           |   |   |-- ba
|           |   |   |-- bd
|           |   |   |-- be
|           |   |   |-- bg
|           |   |   |-- br
|           |   |   |-- brai
|           |   |   |-- bt
|           |   |   |-- bw
|           |   |   |-- by
|           |   |   |-- ca
|           |   |   |-- capslock
|           |   |   |-- cd
|           |   |   |-- ch
|           |   |   |-- cm
|           |   |   |-- cn
|           |   |   |-- compose
|           |   |   |-- ctrl
|           |   |   |-- cz
|           |   |   |-- de
|           |   |   |-- digital_vndr
|           |   |   |   |-- lk
|           |   |   |   |-- pc
|           |   |   |   |-- us
|           |   |   |   `-- vt
|           |   |   |-- dk
|           |   |   |-- dz
|           |   |   |-- ee
|           |   |   |-- empty
|           |   |   |-- epo
|           |   |   |-- es
|           |   |   |-- et
|           |   |   |-- eu
|           |   |   |-- eurosign
|           |   |   |-- fi
|           |   |   |-- fo
|           |   |   |-- fr
|           |   |   |-- fujitsu_vndr
|           |   |   |   |-- jp
|           |   |   |   `-- us
|           |   |   |-- gb
|           |   |   |-- ge
|           |   |   |-- gh
|           |   |   |-- gn
|           |   |   |-- gr
|           |   |   |-- group
|           |   |   |-- hp_vndr
|           |   |   |   `-- us
|           |   |   |-- hr
|           |   |   |-- hu
|           |   |   |-- id
|           |   |   |-- ie
|           |   |   |-- il
|           |   |   |-- in
|           |   |   |-- inet
|           |   |   |-- iq
|           |   |   |-- ir
|           |   |   |-- is
|           |   |   |-- it
|           |   |   |-- jolla_vndr
|           |   |   |   `-- sbj
|           |   |   |-- jp
|           |   |   |-- jv
|           |   |   |-- ke
|           |   |   |-- keypad
|           |   |   |-- kg
|           |   |   |-- kh
|           |   |   |-- kpdl
|           |   |   |-- kr
|           |   |   |-- kz
|           |   |   |-- la
|           |   |   |-- latam
|           |   |   |-- latin
|           |   |   |-- level3
|           |   |   |-- level5
|           |   |   |-- lk
|           |   |   |-- lt
|           |   |   |-- lv
|           |   |   |-- ma
|           |   |   |-- macintosh_vndr
|           |   |   |   |-- apple
|           |   |   |   |-- ch
|           |   |   |   |-- de
|           |   |   |   |-- dk
|           |   |   |   |-- fi
|           |   |   |   |-- fr
|           |   |   |   |-- gb
|           |   |   |   |-- is
|           |   |   |   |-- it
|           |   |   |   |-- jp
|           |   |   |   |-- latam
|           |   |   |   |-- nl
|           |   |   |   |-- no
|           |   |   |   |-- pt
|           |   |   |   |-- se
|           |   |   |   `-- us
|           |   |   |-- mao
|           |   |   |-- md
|           |   |   |-- me
|           |   |   |-- mk
|           |   |   |-- ml
|           |   |   |-- mm
|           |   |   |-- mn
|           |   |   |-- mt
|           |   |   |-- mv
|           |   |   |-- my
|           |   |   |-- nbsp
|           |   |   |-- nec_vndr
|           |   |   |   `-- jp
|           |   |   |-- ng
|           |   |   |-- nl
|           |   |   |-- no
|           |   |   |-- nokia_vndr
|           |   |   |   |-- rx-44
|           |   |   |   |-- rx-51
|           |   |   |   `-- su-8w
|           |   |   |-- np
|           |   |   |-- olpc
|           |   |   |-- parens
|           |   |   |-- pc
|           |   |   |-- ph
|           |   |   |-- pk
|           |   |   |-- pl
|           |   |   |-- pt
|           |   |   |-- ro
|           |   |   |-- rs
|           |   |   |-- ru
|           |   |   |-- rupeesign
|           |   |   |-- se
|           |   |   |-- sgi_vndr
|           |   |   |   `-- jp
|           |   |   |-- sharp_vndr
|           |   |   |   |-- sl-c3x00
|           |   |   |   |-- ws003sh
|           |   |   |   |-- ws007sh
|           |   |   |   |-- ws011sh
|           |   |   |   `-- ws020sh
|           |   |   |-- shift
|           |   |   |-- si
|           |   |   |-- sk
|           |   |   |-- sn
|           |   |   |-- sony_vndr
|           |   |   |   `-- us
|           |   |   |-- srvr_ctrl
|           |   |   |-- sun_vndr
|           |   |   |   |-- ara
|           |   |   |   |-- be
|           |   |   |   |-- br
|           |   |   |   |-- ca
|           |   |   |   |-- ch
|           |   |   |   |-- cz
|           |   |   |   |-- de
|           |   |   |   |-- dk
|           |   |   |   |-- ee
|           |   |   |   |-- es
|           |   |   |   |-- fi
|           |   |   |   |-- fr
|           |   |   |   |-- gb
|           |   |   |   |-- gr
|           |   |   |   |-- it
|           |   |   |   |-- jp
|           |   |   |   |-- kr
|           |   |   |   |-- lt
|           |   |   |   |-- lv
|           |   |   |   |-- nl
|           |   |   |   |-- no
|           |   |   |   |-- pl
|           |   |   |   |-- pt
|           |   |   |   |-- ro
|           |   |   |   |-- ru
|           |   |   |   |-- se
|           |   |   |   |-- sk
|           |   |   |   |-- solaris
|           |   |   |   |-- tr
|           |   |   |   |-- tw
|           |   |   |   |-- ua
|           |   |   |   `-- us
|           |   |   |-- sy
|           |   |   |-- terminate
|           |   |   |-- tg
|           |   |   |-- th
|           |   |   |-- tj
|           |   |   |-- tm
|           |   |   |-- tr
|           |   |   |-- trans
|           |   |   |-- tw
|           |   |   |-- typo
|           |   |   |-- tz
|           |   |   |-- ua
|           |   |   |-- us
|           |   |   |-- uz
|           |   |   |-- vn
|           |   |   |-- xfree68_vndr
|           |   |   |   |-- amiga
|           |   |   |   `-- ataritt
|           |   |   `-- za
|           |   `-- types
|           |       |-- README
|           |       |-- basic
|           |       |-- cancel
|           |       |-- caps
|           |       |-- complete
|           |       |-- default
|           |       |-- extra
|           |       |-- iso9995
|           |       |-- level5
|           |       |-- mousekeys
|           |       |-- nokia
|           |       |-- numpad
|           |       `-- pc
|           |-- xman.help
|           `-- xorg.conf.d
|               |-- 10-quirks.conf
|               |-- 40-libinput.conf
|               |-- 70-wacom.conf
|               `-- nvidia-drm-outputclass.conf -> /etc/alternatives/glx--nvidia-drm-outputclass.conf
|-- tarboot.tar.gz
|-- targets
|   |-- audio
|   |-- chrome
|   |-- chrome-beta
|   |-- chrome-common
|   |-- chrome-dev
|   |-- chromium
|   |-- cli-extra
|   |-- common
|   |-- core
|   |-- e17
|   |-- extension
|   |-- gnome
|   |-- gnome-desktop
|   |-- gtk-extra
|   |-- kde
|   |-- kde-desktop
|   |-- keyboard
|   |-- kodi
|   |-- lxde
|   |-- lxde-desktop
|   |-- mate
|   |-- mate-desktop
|   |-- openoffice
|   |-- post-common
|   |-- tools
|   |-- touch
|   |-- unity
|   |-- unity-desktop
|   |-- x11
|   |-- x11-common
|   |-- xbmc
|   |-- xfce
|   |-- xfce-desktop
|   |-- xiwi
|   `-- xorg
|-- test
|   |-- autotest_control.template
|   |-- daemon.sh
|   |-- genreport.sh
|   |-- reports
|   |   |-- 00-all.sh
|   |   |-- 35-xorg.sh
|   |   `-- w0-common.sh
|   |-- run.sh
|   `-- tests
|       |-- 00-tester
|       |-- 10-basic
|       |-- 11-32-on-64
|       |-- 12-edit-chroot
|       |-- 14-background
|       |-- 15-media
|       |-- 16-targetsfile
|       |-- 17-encryption
|       |-- 18-upgrade
|       |-- 20-logind
|       |-- 30-audio
|       |-- 35-xorg
|       |-- 37-xiwi
|       |-- w0-common
|       |-- w1-e17
|       |-- w2-gnome
|       |-- w2d-gnome-desktop
|       |-- w3-kde
|       |-- w3d-kde-desktop
|       |-- w4-lxde
|       |-- w4d-lxde-desktop
|       |-- w5-unity
|       |-- w5d-unity-desktop
|       |-- w6-kodi
|       |-- w7-xfce
|       |-- w7d-xfce-desktop
|       `-- x0-alltargets
`-- varhost
    `-- cras
        `-- vms
            `-- plugin
                |-- playback
                `-- unified

162 directories, 1615 files
```
![Screenshot_2022-12-17_16-15-50](https://user-images.githubusercontent.com/120763310/208271097-bbf981fb-0b3b-4db7-838d-ebebbc63adfa.png)
