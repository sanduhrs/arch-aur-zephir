# Maintainer: wolftankk <wolftankk@gmail.com>
pkgname=zephir
pkgver=0.12.8
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

sha256sums=('3fe43dce513799950e981974d1e37e9f2390476ada0469a57f5c20b4b0845e5d')

package() {
  ZEPHIRDIR=/opt/$pkgname

  install -d $pkgdir/{$ZEPHIRDIR,usr/bin}

  install -Dm777 zephir.phar "$pkgdir"/opt/zephir/zephir

  ln -s /opt/zephir/zephir $pkgdir/usr/bin/zephir
}
