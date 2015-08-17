# Maintainer: Frank Poehler <fp29129 at googlemail dot com>

pkgname=regain-desktop
pkgver=2.0.4
pkgrel=1
pkgdesc="A desktop search engine similar to Google Desktop"
arch=('i686' 'x86_64')
url="http://regain.sourceforge.net/?lang=en"
license=('LGPL2.1')
groups=()
depends=('java-runtime')
makedepends=()
optdepends=('zenity: for using search-regain.sh' 'jdic: for tray icon support (not tested)')
provides=('regain-desktop')
conflicts=()
replaces=()
backup=()
options=()
install=regain-desktop.install
changelog=
source=("regain_v$pkgver-STABLE_desktop_linux.zip::http://sourceforge.net/projects/regain/files/regain/$pkgver%20Stable/regain_v$pkgver-STABLE_desktop_linux.zip/download"
        start-regain.sh
        search-regain.sh)
noextract=()
sha256sums=('696f06c37dff2ecba37709171eb37afe197f7fed73c25f92999565b97f1131ea'
            '620332485b6fa33a5e094c1235e1fca3c9c04eaa4b349110283095f10c2d62a3'
            '289cb8f390d31691fd9e5c6602a7b34dc8139e45c2aa57cc3c99275a474d69ba')

_install_prefix=/opt/regain-desktop

build() {
  cd "$srcdir"
  rm regain/regain.sh
  mkdir -p "$pkgdir/$_install_prefix" || exit 1
  cp {start-regain,search-regain}.sh "$pkgdir/$_install_prefix"
  cp -R regain/* "$pkgdir/$_install_prefix"
}

