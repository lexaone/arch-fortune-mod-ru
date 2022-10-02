pkgname=fortune-mod-ru
pkgver=1.53
pkgrel=2
pkgdesc="A collection of cookie files for fortune-mod in Russian."
arch=("any")
url="https://lexaone.github.io/fortunes/"
license=('GPL')
groups=()
depends=("fortune-mod")
makedepends=(dos2unix)
checkdepends=()
optdepends=()
conflicts=()
source=(
  "https://lexaone.github.io/fortunes/fortune-mod-ru-$pkgver.tar.bz2"
)
sha256sums=('270345a28f39f30ffa954c9acc9bdfe259aea4cf2f221c2cb4fe66519d229d60')
replaces=()
backup=()
changelog=ChangeLog

package() {
    cd "$pkgname-$pkgver"
    find . -mindepth 2 -a -type f -a -not -name '*.*' -exec dos2unix {} \;
    make DESTDIR="$pkgdir" INSTALLPATH="/usr/share/fortune/ru" install
}
