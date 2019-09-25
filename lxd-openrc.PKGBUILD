pkgname=lxd-openrc
pkgver=3
pkgrel=1
pkgdesc="OpenRC service script for LXD daemon"
arch=('x86_64' 'i686')
url="https://github.com/10n1c/lxd-openrc"
license=('GPL3')
depends=('openrc')
makedepends=('git')
source=('git+https://github.com/10n1c/lxd-openrc')
sha256sums=('SKIP')

package() {
  cd "${srcdir}/${pkgname}"
  install -Dm 755 lxd-init "${pkgdir}/etc/init.d/lxd"
}
