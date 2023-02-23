pkgname=fortune-mod-ru
pkgver=1.54
pkgrel=3
pkgdesc="A collection of cookie files for fortune-mod in Russian."
arch=("any")
url="https://github.com/lexaone/fortunes-ru"
license=('GPL')
groups=()
depends=("fortune-mod")
makedepends=("dos2unix")
checkdepends=()
optdepends=()
conflicts=()
source=(
  git+$url
)
sha256sums=('SKIP')
replaces=()
backup=()
changelog=ChangeLog

package() {
    cd "fortunes-ru-master"
    find . -mindepth 2 -a -type f -a -not -name '*.*' -exec dos2unix {} \;
    find . -mindepth 2 -a -type f -a -not -name '*.*' -exec strfile {} \;
    make DESTDIR="$pkgdir" INSTALLPATH="/usr/share/fortune/ru" install
}
