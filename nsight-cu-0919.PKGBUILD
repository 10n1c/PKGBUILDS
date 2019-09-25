
pkgname=nsight-compute
pkgver=2019.4.0.12
_pkgver=${pkgver//\./_}
pkgrel=1
pkgdesc="Standalone application for the debugging and profiling of compute applications"
arch=(x86_64)
url='https://developer.nvidia.com/nsight-graphics'
license=('custom')
depends=('libx11' 'libxcb' 'nvidia' 'openssl' 'icu' 'qt5-base' 'qt5-multimedia' 'qt5-location' 'qt5-declarative' 'qt5-script' 'qt5-sensors' 'qt5-svg' 'qt5-webchannel' 'qt5-webengine' 'qt5-xmlpatterns' 'qt5-tools' 'qt5-charts')
source=("nsight-compute-linux-${pkgver}.run"
        "${pkgname}.png::http://developer.download.nvidia.com/NsightVisualStudio/3.1/Documentation/UserGuide/HTML/Content/Images/Nsight_256.png"
        "${pkgname}.desktop")
sha256sums=('SKIP'
            'a93eaee1decb6d0122b6c27caef72d1e22ad85c42286114c7f89ef2dd99adb23'
            '680414cfcc464a2c868f009260cb96312d991ed7073de19b3bd968e1aaf6872d')
replaces=('nsight')
provides=('nsight')
options=('!debug')

prepare() {
  sh nsight-compute-linux-${pkgver}.run --noexec --target ${pkgname}
}

package() {
  cd ${srcdir}/${pkgname}
  ./install-linux.pl -noprompt -targetpath=${pkgdir}/opt/${pkgname}

  install -dm 755 "${pkgdir}"/usr/bin
  ln -s /opt/${pkgname}/host/linux-desktop-glibc_2_11_3-x64/nv-nsight-cu "${pkgdir}"/usr/bin
  ln -s /opt/${pkgname}/target/linux-desktop-glibc_2_11_3-x64/nv-nsight-cu-cli "${pkgdir}"/usr/bin

  install -Dm644 "${srcdir}/${pkgname}.desktop" ${pkgdir}/usr/share/applications/${pkgname}.desktop
  install -Dm644 "${srcdir}/${pkgname}.png" ${pkgdir}/usr/share/icons/hicolor/256x256/apps/${pkgname}.png

  install -Dt "${pkgdir}/usr/share/licenses/${pkgname}" -m644 "${srcdir}/${pkgname}/pkg/EULA.txt"
}
