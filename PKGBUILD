# Maintainer: travisghansen <travisghansen@yahoo.com>

pkgname=yubico-piv-tool
pkgver=1.2.2
pkgrel=1
pkgdesc="Tool to interact with the PIV applet on a YubiKey NEO"
arch=('i686' 'x86_64')
license=('GPL3')
depends=('pcsclite')
url=https://developers.yubico.com/yubico-piv-tool/
source=("${pkgname}-${pkgver}.tar.gz::https://developers.yubico.com/yubico-piv-tool/Releases/${pkgname}-${pkgver}.tar.gz")
md5sums=('7bea2545c6af1b0142c732af9213b49e')
options=(!libtool)

build() {
  cd "${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${pkgname}-${pkgver}"
  DESTDIR="${pkgdir}" make install
}
