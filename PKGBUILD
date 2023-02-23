pkgname=fortune-mod-ru
pkgver=1.54
pkgrel=3
pkgdesc="A collection of cookie files for fortune-mod in Russian."
arch=("any")
<<<<<<< HEAD
url="https://github.com/lexaone/fortunes-ru/archive"
=======
# url="https://lexaone.github.io/fortunes"
url="https://github.com/lexaone/fortunes-ru"

>>>>>>> abc0071 (move files with fortunes to dedicated repo)
license=('GPL')
groups=()
depends=("fortune-mod")
makedepends=("dos2unix")
checkdepends=()
optdepends=()
conflicts=()
source=(
<<<<<<< HEAD
  "$url/master.zip"
)
sha256sums=('bdf3535eddaaabbe75f0cb30ea086cb4fd3cf596ddc48fc2fd8967f609e749b5')
=======
  git+$url
)
# sha256sums=('4fa372b98a92f7517ac4a7dafbb775241e25f21750093e42b961291c6f34b1d2')
sha256sums=('SKIP')
>>>>>>> abc0071 (move files with fortunes to dedicated repo)
replaces=()
backup=()
changelog=ChangeLog

package() {
    cd "fortunes-ru-master"
    find . -mindepth 2 -a -type f -a -not -name '*.*' -exec dos2unix {} \;
    find . -mindepth 2 -a -type f -a -not -name '*.*' -exec strfile {} \;
    make DESTDIR="$pkgdir" INSTALLPATH="/usr/share/fortune/ru" install
}
