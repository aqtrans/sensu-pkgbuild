# Maintainer: Angel Velasquez <angvp@archlinux.org> 
# Contributor: Jordan Anderson <aq@es.gy>
# https://core.sensuapp.com/apt/pool/sensu/main/s/sensu/

pkgname=sensu-bin
pkgver=0.25.2
deb_ver=0.25.2-1
pkgrel=1
pkgdesc="Omnibus version of Sensu, the open source monitoring framework. Direct from the .deb"
arch=('i686' 'x86_64')
license=('MPL' 'GPL' 'LGPL')
url="http://sensuapp.org/"

if [ "${CARCH}" = 'x86_64' ]; then
  ARCH='amd64'
md5sums=('b739c0efdf721ea7f325a64e91ec161e')
elif [ "${CARCH}" = 'i686' ]; then
  ARCH='i386'
fi
install=sensu.install
source=("https://core.sensuapp.com/apt/pool/sensu/main/s/sensu/sensu_${deb_ver}_${ARCH}.deb")

package() {
  tar xzvf ${srcdir}/data.tar.gz -C ${pkgdir}/
  msg2 "Cleaning up unwanted files..."
  rm -rv "${pkgdir}"/etc/init.d
  rm -rf "${pkgdir}"/opt/sensu/sv/sensu-dashboard
  mkdir -p "${pkgdir}"/usr/bin
  #cp "${pkgdir}"/opt/sensu/embedded/bin/sensu-ctl "${pkgdir}"/usr/bin/sensu-ctl
}
