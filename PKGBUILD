# Contributor: Ivan Safonov
# PKGBUILD maintainer: Alex Maystrenko <alexeytech@gmail.com>
pkgname=kwin-effect-snow
pkgver=0.6
pkgrel=4
pkgdesc="kwin snow effect"
arch=('i686' 'x86_64')
license=('GPL')
_ppaname=~trusty~ppa2
url="https://launchpad.net/~ivan-safonov/+archive/ppa"
depends=('kdebase-workspace>=4.9.0')
makedepends=('cmake' 'automoc4')
source=(https://launchpad.net/~ivan-safonov/+archive/ppa/+files/${pkgname}_${pkgver}${_ppaname}.tar.gz)
md5sums=('ecd4389d78e642924f797946a224195f')
package() {
  cd "$srcdir/${pkgname}-${pkgver}${_ppaname}"
  rm -rf build
  mkdir build
  cd build
  cmake -DCMAKE_INSTALL_PREFIX=$( kde4-config --prefix ) -DCMAKE_BUILD_TYPE=Release .. || return 1
  make DESTDIR=${pkgdir} install || return 1
}
