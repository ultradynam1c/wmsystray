# Maintainer: Brian Bidulock <bidulock@openss7.org>
# Contributor: Mikkko Sepp�l� <t-r-a-y@mbnet.fi> aka Neverth

pkgname=wmsystray
pkgver=0.1.1
pkgrel=7
pkgdesc="dockapplet to provide systemtray"
arch=('i686' 'x86_64')
#url="http://www.sacredchao.net/~arashi/wmsystray/"
#url="http://www.sacredchao.net/~arashi/${pkgname}/download.shtml"
url="https://github.com/bbidulock/wmsystray"
license=('GPL')
depends=('libxpm')
#source=("http://dockapps.windowmaker.org/download.php/id/511/$pkgname-$pkgver.tar.bz2")
#source=("$pkgname-$pkgver.tar.bz2")
#source=("http://www.sacredchao.net/~arashi/${pkgname}/release/${pkgname}-${pkgver}.tar.bz2")
source=(https://github.com/bbidulock/$pkgname/releases/download/$pkgver/$pkgname-$pkgver.tar.bz2)
md5sums=('398cbc1139d53dbf65c00010bf2297fb')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  make CFLAGS="-fcommon"
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make INSTALL=/usr/bin/install prefix="$pkgdir/usr" install
}
