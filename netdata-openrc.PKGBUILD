pkgname=netdata-openrc
pkgver=1
pkgrel=1
pkgdesc="OpenRC service script for Netdata"
url="https://github.com/10n1c/netdata-openrc"
arch=('x86_64' 'i686')
license=('GPL3')
depends=('openrc')
makedepends=('git')
source=('git+https://github.com/10n1c/netdata-openrc')
sha256sums=('SKIP')

package() {
  cd "${srcdir}/${pkgname}"
  install -Dm 755 netdata-init "${pkgdir}/etc/init.d/netdata"
  install -Dm 644 netdata-conf "${pkgdir}/etc/conf.d/netdata
}
