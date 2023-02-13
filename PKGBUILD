pkgname=fortune-mod-ru
pkgver=1.54
pkgrel=2
pkgdesc="A collection of cookie files for fortune-mod in Russian."
arch=("any")
url="https://lexaone.github.io/fortunes"
license=('GPL')
groups=()
depends=("fortune-mod")
makedepends=("dos2unix")
checkdepends=()
optdepends=()
conflicts=()
source=(
  "$url/fortune-mod-ru-$pkgver-$pkgrel.tar.bz2"
)
sha256sums=('4fa372b98a92f7517ac4a7dafbb775241e25f21750093e42b961291c6f34b1d2')
replaces=()
backup=()
changelog=ChangeLog

package() {
    cd "$pkgname-$pkgver"
    find . -mindepth 2 -a -type f -a -not -name '*.*' -exec dos2unix {} \;
    find . -mindepth 2 -a -type f -a -not -name '*.*' -exec strfile {} \;
    make DESTDIR="$pkgdir" INSTALLPATH="/usr/share/fortune/ru" install
}
