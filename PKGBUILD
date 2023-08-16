# Maintainer: Jonas Strassel <info@jonas-strassel.de>

pkgname=manjaro-hyprland-settings
pkgver=0.0.1
pkgrel=34
arch=('any')
_pkgbase=desktop-settings
url="https://github.com/Manjaro-Hyprland/$_pkgbase"
license=('GPL')
pkgdesc='Manjaro Hyprland Settings'
groups=('hyprland-manjaro')
depends=(
    'manjaro-base-skel'
    'waybar'                  # configurable bar
    'light'                   # cli to control brightness
    'mako'                    # desktop notifications
    'hyprland'                    # window manager
    'rofi-wayland'            # launcher application
    'swaylock'                # lockscreen
    'swayidle'                # idle management daemon
    'grim'                    # screenshot tool
    'slurp'                   # helper for grim
    'wob'                     # wayland overlay bar for brightness and volume
    'foot'                    # terminal application
    'foot-terminfo'           # terminal info for foot
    'ttf-roboto-mono-nerd'    # default monospace font
    'ttf-jetbrains-mono-nerd' # next monospace font
    'jq'                      # json parsing and manipulation
    'calcurse'                # tui calendar application
    'lm_sensors'              # display sensor information
    'manjaro-sway-wallpapers' # manjaro sway themed backgrounds
    'wf-recorder'             # screen recording util
    'wl-clipboard'            # copy/paste utilities for wayland
    'nwg-wrapper'             # conky like onscreen information'
    'noto-fonts-emoji'        # emoji font (e.g. weather icons)
    'swaybg'                  # background switcher
    'ttf-roboto'              # contains the roboto font used in a lot of places
    'htop'                    # system monitor
    'swappy'                  # screenshot editing tool
    'inotify-tools'           # file watchers etc
    'bluetuith'               # bluetooth management tool
    'swayr'                   # lru window switcher for sway
    'bc'                      # basic tiny calculation util
)
makedepends=('git')
optdepends=(
    'qutebrowser: a keyboard-centric browser'
    'flashfocus: better flashing on focus changes'
    'swaylock-effects: swaylock with nicer effects'
    'wlsunset: time & place based light temperature'
    'kanshi: automatically load matching output profiles'
    'autotiling-rs: automated tiling'
    'sworkstyle: dynamic workspace names (icons) in waybar'
    'nwg-wrapper: conky like onscreen information'
    'cliphist: clipboard manager'
    'swaycwd: open here helper'
    'zeit: a simple time tracker'
    'dex: execute DesktopEntry files on autostart'
    'poweralertd: battery and power notifications'
    'wluma: adaptive brightness based on screen contents and ALS'
)
conflicts=('manjaro-hyprland-settings-git')
provides=('manjaro-desktop-settings')
_sourcemd5=f4d3e0b504080e6444b50c5a048c3903
source=(
    "$pkgname-$pkgver.tar.gz::${url}/archive/${pkgver}.tar.gz"
    "https://github.com/arcolinux/arcolinux-on-the-road/raw/cfbcc902b9520cc4ff73584dd80f34c54a158c75/root/usr/local/bin/skel"
)
md5sums=(
    "$_sourcemd5"                      # desktop settings
    "3ce84d692c6fdbaf31e1b602bc890aa4" # skel update script from arcolinux
)
install=.install

package() {
    install -d "$pkgdir"/etc
    install -d "$pkgdir"/usr/bin
    cp -r $_pkgbase-$pkgver/community/hyprland/etc/* "${pkgdir}/etc/"
    cp -r $_pkgbase-$pkgver/community/hyprland/usr/* "${pkgdir}/usr/"
    install -D -m 755 skel "${pkgdir}/usr/bin/skel"
}
