# Maintainer: Stephano Cetola <stephanoc@gmail.com>

pkgname=mnt-reform-lpc
pkgver=6.18.15
pkgrel=1
_kernver="${pkgver}-mnt-reform"
pkgdesc="MNT Reform LPC kernel module (arm64)"
arch=('aarch64')
url="https://github.com/cetola/mnt-build"
license=('GPL2')
depends=("linux-mnt-reform=${pkgver}-${pkgrel}")
install="${pkgname}.install"
source=(
  "reform2_lpc-${pkgver}-${pkgrel}-mnt.tar.gz::https://github.com/cetola/mnt-build/releases/download/${pkgver}-${pkgrel}-mnt-reform/reform2_lpc-${pkgver}-${pkgrel}-mnt.tar.gz"
)
sha256sums=('6c1e0d30a17be7f3268a8015c7f37e0df01398fec3358644714bd48b71f7bf6f')

options=(!strip !docs !emptydirs)

package() {
  cd "$srcdir"

  install -Dm644 reform2_lpc.ko \
    "$pkgdir/usr/lib/modules/${_kernver}/extra/reform2_lpc.ko"
}
