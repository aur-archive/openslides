# Maintainer: wombalton wombalton@gmail.com

pkgname=openslides
pkgver=1.6.1
pkgrel=1
pkgdesc="A free web based presentation and assembly system for visualizing and controlling agenda, motions and elections of an assembly. "
arch=('any')
license=('GPL')
url="http://openslides.org"
depends=('python2')
makedepends=('python2-virtualenv')
#source=(http://files.openslides.org/$pkgname-$pkgver.tar.gz)
source=('openslides')
md5sums=('780dbc80ab636cfe1425da7b6e3b79ca')


build() {
  virtualenv2 $srcdir

  source $srcdir/bin/activate

#  pip install ${pkgname}-${pkgver}.tar.gz

  pip install ${pkgname}
}

package () {
#  cp -R $srcdir/* $pkgdir/opt/openslides/
  install -d $pkgdir{/opt/openslides/,/usr/bin}
  cp -R $srcdir/* $pkgdir/opt/openslides/
  install --mode=755 --owner=root --group=root openslides $pkgdir/usr/bin/
}
