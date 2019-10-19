# Maintainer: Khralkatorrix <garuda2550@gmail.com>

pkgname=libgw2formats
_pkgname=gw2formats
pkgver=1.0.r93.70fa6ca
pkgrel=1
pkgdesc="Library used for reading Guild Wars 2's files in a type-safe manner."
arch=('x86_64')
url="https://github.com/kytulendu/gw2formats"
license=('GPL')
makedepends=('cmake')
source=("git://github.com/kytulendu/gw2formats.git")
sha256sums=('SKIP')

pkgver() {
    cd $_pkgname
    echo "1.0.r$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}

build() {
    cd $_pkgname
    cmake . -DCMAKE_INSTALL_PREFIX="$pkgdir/usr/"
    make
}

package() {
    cd $_pkgname
    make install
}
