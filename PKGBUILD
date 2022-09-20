# Maintainer: Khralkatorrix <garuda2550@gmail.com>

pkgname=libgw2formats
_pkgname=gw2formats
pkgver=1.0.r97.6f3690c
pkgrel=1
pkgdesc="Library used for reading Guild Wars 2's files in a type-safe manner."
arch=('x86_64')
url="https://github.com/kytulendu/gw2formats"
license=(GPL)
makedepends=(cmake)
source=("git+https://github.com/kytulendu/gw2formats.git")
sha256sums=('SKIP')

pkgver() {
    cd "${srcdir}/$_pkgname"
    echo "1.0.r$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}

build() {
    cd "${srcdir}/$_pkgname"
    cmake . -DCMAKE_INSTALL_PREFIX="/usr"
    make
}

package() {
    cd "${srcdir}/$_pkgname"
    make DESTDIR="$pkgdir" install
}
