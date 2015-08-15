# Maintainer: MiJyn <lkjoeldev@gmail.com>

pkgname=estsaver
pkgver=0.1.3
pkgrel=2
pkgdesc="Fast, extensible, and beautiful OpenGL-based screensaver and locker"
arch=('i686' 'x86_64')
url="http://mijyn.github.io/estsaver/"
license=('BSD')
depends=('libgl')
optdepends=('ftgl: Font support' 'freeimage: Image support')
makedepends=('cmake' 'make' 'gcc')
source=(https://github.com/MiJyn/${pkgname}/archive/v${pkgver}.tar.gz)
md5sums=('bc96d845664def65645a489c860183e9')

build() {
  cd "${srcdir}"/$pkgname-$pkgver

  cmake . -DCMAKE_INSTALL_PREFIX=/usr/ -DCMAKE_BUILD_TYPE=Release
  make
}

package() {
    cd "${srcdir}"/$pkgname-$pkgver
    make DESTDIR="$pkgdir/" install
}
