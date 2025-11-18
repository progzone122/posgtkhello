pkgname=posgtkhello
pkgver=1.0
pkgrel=0
pkgdesc="Simple GTK2 C++ application template with a fully configured build system for PostmarketOS"
author="DiabloSat"
url="https://github.com/progzone122/posgtkhello"
license="MIT"
arch="armhf"
depends=""
makedepends="gcc cmake make build-base gtk+2.0-dev pango-dev cairo-dev gdk-pixbuf-dev glib-dev harfbuzz-dev freetype-dev fontconfig-dev"

source="mypkg-1.0.tar.gz"
builddir="$srcdir/app"

build() {
    cd "$builddir"
    mkdir -p build
    cd build
    cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr
    make
}

package() {
    cd "$builddir/build"
    make DESTDIR="$pkgdir" install
}

sha512sums="
ba5beef6b6604868259a3616bf761c798104a162b3a4a941ddd5b17ca22df2e69e01819ed12fb4646dcbde594dcaf723b2c3ce5544bbf0f301b1f30bc267631f mypkg-1.0.tar.gz
"
