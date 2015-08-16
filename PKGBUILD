# Contributor: acounto <acounto@kamikakushi.net>

pkgname=jd-rc
_softname=jd
pkgver=2.8.5
_date=rc120811
pkgrel=1
pkgdesc="A 2channel browser written in C++ (Release Candidate)"
arch=('i686' 'x86_64')
url="http://jd4linux.sourceforge.jp/"
license=('GPL2')
depends=('libsm' 'libgcrypt' 'gtkmm')
conflicts=('jd' 'jd-svn')
source=(http://dl.sourceforge.jp/jd4linux/56620/${_softname}-${pkgver}-${_date}.tgz)

build() {
  cd ${srcdir}/${_softname}-${pkgver}-${_date}

  autoreconf -i
  ./configure --prefix=/usr
  make
}

package() {
  cd ${srcdir}/${_softname}-${pkgver}-${_date}

  make DESTDIR=${pkgdir} install
}

md5sums=('2d750986e950b3571b0681c87ef479ca')