# Maintainer: wolftankk <wolftankk@gmail.com>
pkgname=zephir
pkgver=0.12.7
pkgrel=1
pkgdesc="Zephir is a compiled high level language aimed to the creation of C-extensions for PHP http://zephir-lang.com/"
url="https://github.com/phalcon/zephir"
arch=('x86_64' 'i686')
license=('MIT')
depends=('php-zephir-parser')
makedepends=('php')

if [[ $CARCH = "i686" ]]; then
  makedepends+=('lib32-pcre');
fi

source=(
	"https://github.com/phalcon/zephir/releases/download/${pkgver}/zephir.phar"
)

sha256sums=('36dedf4b9da224f29e7fb78d04e4e05f467c2222b80fcea2d5e976f048804717')

package() {
  ZEPHIRDIR=/opt/$pkgname

  install -d $pkgdir/{$ZEPHIRDIR,usr/bin}

  install -Dm777 zephir.phar "$pkgdir"/opt/zephir/zephir

  ln -s /opt/zephir/zephir $pkgdir/usr/bin/zephir
}
