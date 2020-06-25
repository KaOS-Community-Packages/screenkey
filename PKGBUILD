pkgname=screenkey
pkgver=1.1
pkgrel=2
pkgdesc="A screencast tool to display your keys inspired by Screenflick"
arch=('x86_64')
url="https://www.thregr.org/~wavexx/software/screenkey/"
license=('GPL3')
depends=('python3-gobject3' 'gtk3' 'python3-cairo' 'libx11')
makedepends=('python3-setuptools') 
source=("https://www.thregr.org/~wavexx/software/screenkey/releases/$pkgname-$pkgver.tar.gz")
sha256sums=('0f382e485bf185d9f4f549eab9cfe1a48c53d66dc9c362e6ab433e51c6842ed7')

build() {
  cd "$pkgname-$pkgver"
  python setup.py build
}

package() {
  cd "$pkgname-$pkgver"
  python setup.py install --skip-build --optimize=1 --root="$pkgdir/"
}
