# Maintainer: Aaron Ky-Riesenbach <aaronkyriesenbach at pobox dot com>
pkgname=stackstorm
pkgver=3.6.0
pkgrel=3

pkgdesc="Event-driven automation"
arch=(any)
url="https://stackstorm.com"
license=(Apache)

depends=(mongodb rabbitmq redis)
makedepends=(git)
backup=(etc/st2/st2.conf)

source=("st2_${pkgver}-${pkgrel}_amd64.deb::https://packagecloud.io/StackStorm/stable/packages/ubuntu/focal/st2_${pkgver}-${pkgrel}_amd64.deb/download.deb")
sha256sums=("4bc704be8a5d3ab472d11099d1abc8af297e0ffa061ac46414532a765339554a")

package() {
    cd $srcdir
    tar -xf data.tar.xz

    cp -r $srcdir/etc $pkgdir
    cp -r $srcdir/lib $pkgdir
    cp -r $srcdir/opt $pkgdir
    cp -r $srcdir/usr $pkgdir
    cp -r $srcdir/var $pkgdir
}
