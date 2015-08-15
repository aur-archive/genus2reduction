# Maintainer: Antonio Rojas <nqn76sw@gmail.com>

pkgname=genus2reduction
pkgver=20140211
pkgrel=1
pkgdesc="A program for computing the conductor and reduction types for a genus 2 hyperelliptic curve"
arch=('i686' 'x86_64')
url="http://www.sagemath.org/"
license=('GPL2')
depends=('pari')
source=("http://www.sagemath.org/packages/upstream/$pkgname/$pkgname-$pkgver.tar.bz2")
md5sums=('46bd298ef0699d7fb7763d08228a3ce1')

build() {
  cd $pkgname-$pkgver
  cc -O2 -I/usr/include/pari -lpari -lm genus2reduction.c -o genus2reduction 
}

package() {
  cd $pkgname-$pkgver
  mkdir -p "$pkgdir"/usr/bin
  install -m755 genus2reduction "$pkgdir"/usr/bin
}

