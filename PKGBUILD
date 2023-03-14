# Maintainer: Nanda Okitavera <codeharuka.yusa@gmail.com>
# Maintainer: Silent Robot <d3signr-at-gmail.com>

pkgname=salientos-clearine
_pkgname=clearine
pkgver=0.7
pkgrel=3
pkgdesc="A Beautiful Logout UI for X11 Window Managers"
arch=('any')
url="https://github.com/salientos/${_pkgname}"
license=('MIT')
depends=('python-gobject' 'python-cairo')
makedepends=('git')
backup=('etc/clearine.conf')
provides=("${_pkgname}")
options=(!strip !emptydirs)
source=(
  ${pkgname}::"git+https://github.com/salientos/${_pkgname}.git"
)

md5sums=('SKIP')

package() {
  cd $pkgname
  python setup.py install --prefix=/usr --root="$pkgdir/" --optimize=1
  install -d -m755 $pkgdir/etc/
  install -S -m644 $pkgdir/usr/share/clearine/clearine.conf $pkgdir/etc/
  install -D -m644 LICENSE "$pkgdir/usr/share/licenses/clearine/LICENSE.md"
}
