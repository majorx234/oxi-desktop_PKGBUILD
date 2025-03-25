pkgname=oxi-desktop
pkgdesc="oxi-desktop"
pkgver=2.3.0
pkgrel=1
arch=("x86_64")
url="https://github.com/OXI-Instruments/OXI-Desktop"
license=("GPL3")
depends=("qmidi")
makedepends=("qmidi" "cmake" "make" "gcc")
source=("git+https://github.com/majorx234/OXI-Desktop")
sha256sums=("SKIP")

build() {
  mkdir -p ${srcdir}/build
  cd ${srcdir}/build
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
        ${srcdir}/OXI-Desktop
  make
}

package() {
  cd ${srcdir}/build
  make DESTDIR="${pkgdir}/" install
}
