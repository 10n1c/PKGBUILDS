pkgname=vuurmuur-openrc
pkgver=1
pkgrel=1
pkgdesc="OpenRC service script for Vuurmuur firewall daemon"
url="https://github.com/10n1c/vuurmuur-openrc"
arch=('x86_64' 'i686')
license=('GPL3')
depends=('openrc')
makedepends=('git')
source=('git+https://github.com/10n1c/vuurmuur-openrc')
sha256sums=('SKIP')

package() {
  cd "${srcdir}/${pkgname}"
  install -Dm 755 vuurmuur-init "${pkgdir}/etc/init.d/vuurmuur"
}
