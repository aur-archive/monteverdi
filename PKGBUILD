# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.
 
# Maintainer: Argyros Argyridis <arargyridis@gmail.com>
# Contributor: Samuel Fernando Mesa Giraldo <samuelmesa@linuxmail.org>
 
pkgname=monteverdi
pkgver=1.22
minorver=0
pkgrel=1
pkgdesc="A remote sensing application based on Orfeo Toolbox"
arch=(x86_64)
url="http://www.orfeo-toolbox.org/otb/monteverdi.html"
license=('CeCILL')
groups=()
depends=('orfeo-toolbox' 'fltk')
makedepends=()
optdepends=()
provides=(monteverdi)
conflicts=(monteverdi)
replaces=(monteverdi)
backup=()
options=()
install=
changelog=
source=(http://softlayer-dal.dl.sourceforge.net/project/orfeo-toolbox/Monteverdi-$pkgver.$minorver.tgz)
noextract=()
md5sums=('a82cfec1816d816c8cdab7bf0eee9af1')
 #generate with 'makepkg -g'
 
build() {
 
 
 
  #msg "checking done or server timeout occurerror while loading shared libraries: libfltk.so.9: cannot open shared object file: No such file or directory    ed"

  msg "starting make..."
  rm -rf build/
  mkdir build/
  cd build
  ls -l
 
  #export LD_LIBRARY_PATH=/usr/local/lib/otb
  cmake ../Monteverdi-$pkgver.$minorver -DCMAKE_INSTALL_PREFIX=/usr
 
  make
}
 
package() {
 
  cd "$srcdir/"build
  make DESTDIR="$pkgdir" install
}
