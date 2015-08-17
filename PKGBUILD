# Maintainer: Andrzej Giniewicz <gginiu@gmail.com>
pkgname=python2-pyface
pkgver=4.2.0
_githubtag=1656f42
pkgrel=1
pkgdesc="Traits-capable windowing framework"
arch=('any')
url="https://github.com/enthought/pyface"
license=('BSD')
depends=('python2-traits')
makedepends=('python2-distribute')
optdepends=('python2-pyqt' 'python2-pyside' 'wxpython')
conflicts=('python2-pyface-git')
options=(!emptydirs)

source=("https://github.com/enthought/pyface/tarball/${pkgver}")
md5sums=('02d27c19b0c96ece69574622ef28a354')

build() {
  cd "$srcdir/enthought-pyface-${_githubtag}"

  python2 setup.py build
}

package() {
  cd "$srcdir/enthought-pyface-${_githubtag}"

  python2 setup.py install --root="$pkgdir"/ --optimize=1

  install -D "LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

