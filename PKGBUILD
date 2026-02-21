# Maintainer: Stephano Cetola <stephanoc@gmail.com>

pkgname=mnt-reform-lpc
pkgver=6.18.12
pkgrel=1
_kernver="${pkgver}-mnt-reform"
pkgdesc="MNT Reform LPC kernel module (arm64)"
arch=('aarch64')
url="https://github.com/cetola/mnt-build"
license=('GPL2')
depends=("linux-mnt-reform=${pkgver}-${pkgrel}")
source=(
  "reform2_lpc-${pkgver}-${pkgrel}-mnt.tar.gz::https://github.com/cetola/mnt-build/releases/download/${pkgver}-${pkgrel}-mnt-reform/reform2_lpc-${pkgver}-${pkgrel}-mnt.tar.gz"
)
sha256sums=('SKIP')

options=(!strip !docs !emptydirs)

package() {
  cd "$srcdir"

  install -Dm644 reform2_lpc.ko \
    "$pkgdir/usr/lib/modules/${_kernver}/extra/reform2_lpc.ko"
}
