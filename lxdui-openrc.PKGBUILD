pkgname=lxdui-openrc
pkgver=2
pkgrel=1
pkgdesc="OpenRC service script for LXDUI web front-end"
url="https://github.com/10n1c/lxdui-openrc"
arch=('x86_64' 'i686')
license=('GPL3')
depends=('openrc')
makedepends=('git')
source=('git+https://github.com/10n1c/lxdui-openrc')
sha256sums=('SKIP')

package() {
  cd "${srcdir}/${pkgname}"
  install -Dm 755 lxdui-init "${pkgdir}/etc/init.d/lxdui"
}
