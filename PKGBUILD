pkgname=moka-cinnamon-theme-git
_pkgname=moka-cinnamon-theme
pkgver=1.0.0
pkgrel=1
pkgdesc="Moka is the titular Cinnamon theme of the Moka Project."
arch=('any')
url="https://github.com/moka-project/moka-cinnamon-theme"
license=('GPL3')
depends=()
makedepends=('git')
optdepends=()
provides=('moka-cinnamon-theme-git')
conflicts=('moka-cinnamon-theme-git')
source=('git+https://github.com/moka-project/moka-cinnamon-theme.git')
md5sums=('SKIP')

pkgver() {
  cd $srcdir/$_pkgname
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {

  # create theme dirs
  install -d -m 755 "$pkgdir"/usr/share/themes/Moka

  # install theme
  cd $srcdir/moka-cinnamon-theme/Moka
  cp -r . "$pkgdir"/usr/share/themes/Moka/
}
