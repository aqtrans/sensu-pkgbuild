# Maintainer: Angel Velasquez <angvp@archlinux.org> 
# Contributor: Jordan Anderson <aq@es.gy>
# https://core.sensuapp.com/apt/pool/sensu/main/s/sensu/

pkgname=sensu-bin
pkgver=0.26.1
_deb_ver=0.26.1-1
pkgrel=3
pkgdesc="Omnibus version of Sensu, the open source monitoring framework. Direct from the .deb"
arch=('i686' 'x86_64')
license=('MPL' 'GPL' 'LGPL')
url="http://sensuapp.org/"
install=sensu.install
source_x86_64=("https://core.sensuapp.com/apt/pool/sensu/main/s/sensu/sensu_${_deb_ver}_amd64.deb")
source_i686=("https://core.sensuapp.com/apt/pool/sensu/main/s/sensu/sensu_${_deb_ver}_i386.deb")

md5sums_x86_64=('00d7058ef033c0e9647805bd9d9f9069')
md5sums_i686=('33c8ba279d8d603c3b25ffc784dc91c7')

package() {
  tar xzvf ${srcdir}/data.tar.gz -C ${pkgdir}/
  msg2 "Cleaning up unwanted files..."
  rm -rv "${pkgdir}"/etc/init.d
  rm -rf "${pkgdir}"/opt/sensu/sv/sensu-dashboard

  mkdir -p "${pkgdir}"/usr/lib/systemd/system
  ln -s "/usr/share/sensu/systemd/sensu-api.service" "${pkgdir}/usr/lib/systemd/system/"
  ln -s "/usr/share/sensu/systemd/sensu-client.service" "${pkgdir}/usr/lib/systemd/system/"
  ln -s "/usr/share/sensu/systemd/sensu-server.service" "${pkgdir}/usr/lib/systemd/system/" 
}
