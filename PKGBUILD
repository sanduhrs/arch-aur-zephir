# Maintainer: wolftankk <wolftankk@gmail.com>
pkgname=zephir
pkgver=0.12.10
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

sha256sums=('507eeb2839b322479bede6e8e094cb307e41cc701a3ea3aea763aaa864472848')

package() {
  ZEPHIRDIR=/opt/$pkgname

  install -d $pkgdir/{$ZEPHIRDIR,usr/bin}

  install -Dm777 zephir.phar "$pkgdir"/opt/zephir/zephir

  ln -s /opt/zephir/zephir $pkgdir/usr/bin/zephir
}
