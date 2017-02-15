# Maintainer: kainonergon @forum.manjaro.org

pkgname=simplepanel
pkgver=0.2
pkgrel=1
pkgdesc="Lightweight modular panel for bspwm"
arch=(any)
url="https://github.com/kainonergon/$pkgname"
license=('MIT')
depends=('dash'
	'lemonbar-xft-clicky'
	'ttf-ionicons'
	'xtitle')
optdepends=('terminus-font: default font'
	'morc_menu: default main menu'
	'bspwm-manjaro: window manager the panel is intended for')
makedepends=('git')
source=("git://github.com/kainonergon/$pkgname")
md5sums=('SKIP')

package () {
	cd $srcdir/$pkgname
	install -dm755 $pkgdir/usr
	cp -r bin $pkgdir/usr
	chmod a+x $pkgdir/usr/bin/*
}

