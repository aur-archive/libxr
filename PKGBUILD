pkgname=libxr
pkgver=2.0.0
pkgrel=1
pkgdesc="Client/server XML-RPC library for C"
arch=(i686 x86_64)
depends=(glib2 libxml2 openssl)
license=("LGPL")
url="http://megous.com/projekty"
source=("https://github.com/downloads/megous/libxr/libxr-$pkgver.tar.bz2")
md5sums=('c88cd853ee64d203ba39b2c7c197753a')

build()
{
  cd "$srcdir/libxr-$pkgver"
  ./configure \
    --prefix=/usr
  make
}

package() {
  cd "$srcdir/libxr-$pkgver"
  make DESTDIR=$pkgdir install
  install -Dm644 COPYING "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}

