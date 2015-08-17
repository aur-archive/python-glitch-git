# Maintainer: nosada <ngsksdt@gmail.com>

pkgname=python-glitch-git
_pkgname=glitch
pkgver=20141013
pkgrel=1
pkgdesc="glitch jpg file"
url="https://github.com/trsqxyz/glitch"
arch=('any')
license=('MIT')
depends=('python' 'git')
source=('git+https://github.com/trsqxyz/glitch.git')
sha1sums=('SKIP')

pkgver() {
  date +%Y%m%d
}

build() {
  cd ${srcdir}/${_pkgname}

  python setup.py build
}

package() {
  cd ${srcdir}/${_pkgname}

  python setup.py install --root=${pkgdir}
  install -Dm644 LICENSE \
            ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}

# vim:set ts=2 sw=2 et:
