# Maintainer: Aaron Ky-Riesenbach <aaronkyriesenbach at pobox dot com>
pkgname=stackstorm
pkgver=3.6.0
pkgrel=3

pkgdesc="Event-driven automation"
arch=(x86_64)
url="https://stackstorm.com"
license=(Apache)

depends=('mongodb' 'rabbitmq' 'redis' 'expat>=2.1beta3' 'git' 'libffi' 'libldap>=2.4.11' 'openssh' 'openssl' 'pam' 'python>=3.8' 'zlib>=1.2.0')
makedepends=(git)
install=stackstorm.install

source=("st2_${pkgver}-${pkgrel}_amd64.deb::https://packagecloud.io/StackStorm/stable/packages/ubuntu/focal/st2_${pkgver}-${pkgrel}_amd64.deb/download.deb")
sha256sums=("4bc704be8a5d3ab472d11099d1abc8af297e0ffa061ac46414532a765339554a")

package() {
    cd $srcdir
    tar -xf $srcdir/data.tar.xz -C $pkgdir

    mv $pkgdir/var/run $pkgdir
    mv $pkgdir/lib $pkgdir/usr
}
