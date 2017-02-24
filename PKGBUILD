# Maintainer: kainonergon @forum.manjaro.org

pkgname=simplepanel
pkgver=0.4
pkgrel=1
pkgdesc="Lightweight modular panel for bspwm"
arch=(any)
url="https://github.com/kainonergon/$pkgname"
license=('MIT')
depends=('dash'
	'lemonbar-xft-clicky'
	'ttf-ionicons')
optdepends=('bspwm-manjaro: window manager the panel is intended for'
	'terminus-font: default font'
	'morc_menu: default main menu'
	'wireless_tools: wifi info'
	'xtitle: window title info'
	'xkb-switch-git: keyboard layout indicator'
	'xdotool: backlight control'
	'alsa-utils: sound volume info')
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

