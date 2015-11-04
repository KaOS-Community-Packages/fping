pkgname=fping
pkgver=3.13
pkgrel=1
pkgdesc="Utility to ping multiple hosts at once"
arch=('x86_64')
url="http://www.${pkgname}.org"
license=('GPL')
depends=('glibc')
source=("http://www.${pkgname}.org/dist/${pkgname}-${pkgver}.tar.gz")
sha512sums=('d6c1c5b9edb97ef59cfb6d22f74f6a055e52465d3ba0f93be35b6fc9615ee08490ee927f3cf9efd087e18279519292f353abe6152061985ee166ba5f7e95e29d')

prepare() {
 cd "$pkgname-$pkgver"
}

build() {
 cd "$pkgname-$pkgver"
 ./configure --prefix=/usr --enable-ipv4 --enable-ipv6
 make
}

check() {
 cd "$pkgname-$pkgver"
 make check
}

package() {
 cd "$pkgname-$pkgver"
 make DESTDIR="$pkgdir/" install
}
