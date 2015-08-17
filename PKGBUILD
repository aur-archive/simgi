# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=simgi
pkgname=simgi
pkgver=0.3
pkgrel=2
pkgdesc="stochastic simulation engine"
url="http://hackage.haskell.org/package/${_hkgname}"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-containers=0.3.0.0' 'haskell-haskell98=1.0.1.1' 'haskell-mersenne-random-pure64>=0.2' 'haskell-mtl>=1.1.0.2' 'haskell-parsec=2.1.0.1' 'haskell-random=1.0.0.2')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
md5sums=('f9b0d4056373a621c21a2f21d6638c05')
