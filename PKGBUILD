pkgname=faba-mono-icons-git
_pkgname=faba-mono-icons
pkgver=2.0
pkgrel=2
pkgdesc="The monochromatic panel icon sets for Faba."
arch=('any')
url="https://github.com/moka-project/faba-mono-icons"
license=('GPL3')
depends=(faba-icons-git)
makedepends=('git')
optdepends=()
provides=('faba-mono-icons-git')
conflicts=('faba-mono-icons-git')
source=('git+https://github.com/moka-project/faba-mono-icons.git')
md5sums=('SKIP')

pkgver() {
  cd $srcdir/$_pkgname
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {

  # create theme dirs
  install -d -m 755 "$pkgdir"/usr/share/icons/Faba-Dark/
  install -d -m 755 "$pkgdir"/usr/share/icons/Faba-Light/
  install -d -m 755 "$pkgdir"/usr/share/icons/Faba-Mixt/

  # install theme
  cd $srcdir/faba-mono-icons/Faba-Dark
  cp -r . "$pkgdir"/usr/share/icons/Faba-Dark/
  cd $srcdir/faba-mono-icons/Faba-Light
  cp -r . "$pkgdir"/usr/share/icons/Faba-Light/
  cd $srcdir/faba-mono-icons/Faba-Mixt
  cp -r . "$pkgdir"/usr/share/icons/Faba-Mixt/
}
