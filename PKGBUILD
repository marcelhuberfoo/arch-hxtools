# Contributor: Evilandi666 <evilandi.aur(at)googlemail.com>
# Maintainer: Marcel Huber <marcelhuberfooatgmaildotcom>
pkgname=hxtools
pkgver=20130605
pkgrel=1
pkgdesc="A collection of tools and scripts that have accumulated over the years, and each of which seems to be too small to warrants its own project."
arch=('i686' 'x86_64')
url=http://inai.de/projects/hxtools/
license=('GPL3')
depends=('libhx>=3.15' perl util-linux pciutils libxcb)
makedepends=('sed')
source=(http://jftp.inai.de/hxtools/hxtools-$pkgver.tar.xz )
md5sums=('d7fe5aee5a244cab4fc8a27a9ffb5ac2')

build() {
  cd $srcdir/$pkgname-$pkgver
  ./configure --libexecdir=/usr/lib --prefix=/usr --sysconfdir=/etc --localstatedir=/var
  make || return 1
  make DESTDIR=$pkgdir install || return 1
}
