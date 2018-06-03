# Based on the file created for Arch Linux by:
# Sven-Hendrik Haase <sh@lutzhaase.com>
# Malte Rabenseifner <malte@zearan.de>
# John Gerritse <reaphsharc@gmail.com>

# Maintainer: Guinux <nuxgui@gmail.com>
# Maintainer: Philip Müller <philm@manjaro.org>

pkgname=lsb-release
pkgver=1.4
pkgrel=12
pkgdesc="LSB version query program"
arch=('any')
url="http://www.linuxbase.org/"
license=('GPL2')
source=("http://downloads.sourceforge.net/lsb/lsb-release-$pkgver.tar.gz")
sha256sums=('99321288f8d62e7a1d485b7c6bdccf06766fb8ca603c6195806e4457fdf17172')

build() {
  cd "$srcdir/lsb-release-$pkgver"
  make
}

package() {
  cd "$srcdir/lsb-release-$pkgver"

  install -Dm 644 lsb_release.1.gz "$pkgdir/usr/share/man/man1/lsb_release.1.gz"
  install -Dm 755 lsb_release "$pkgdir/usr/bin/lsb_release"
}