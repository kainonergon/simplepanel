# Maintainer: kainonergon @forum.manjaro.org

pkgname=simplepanel
pkgver=0.8
pkgrel=1
pkgdesc="Scriptable panel with lemonbar"
arch=(any)
url="https://github.com/kainonergon/$pkgname"
license=('MIT')
depends=('dash'
	'lemonbar-xft')
optdepends=('terminus-font: default font'
	'ttf-nerd-fonts-knack-complete-git: default font'
	'rofi: default menu'
	'wireless_tools: wifi info'
	'xtitle: window title info'
	'xkb-switch-git: keyboard layout indicator'
	'light: backlight control'
	'xorg-xbacklight: backlight control'
	'acpilight: backlight control'
	'alsa-utils: sound volume info'
	'weather: weather info'
	'mpc: mpd info'
	'xdotool: menu placement')
makedepends=('git')
source=("git://github.com/kainonergon/$pkgname")
md5sums=('SKIP')

pkgver() {
    cd ${srcdir}/${pkgname}
    git describe --long --tags | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

package () {
	cd $srcdir/$pkgname
	install -dm755 $pkgdir/usr
	cp -r bin $pkgdir/usr
	chmod a+x $pkgdir/usr/bin/*
}

