# Maintainer: Antonio Rojas <nqn1976 @ gmail.com>

pkgname=plasma-applet-akonadi-tasks
pkgver=0.1.3
pkgrel=1
pkgdesc="A plasmoid for displaying tasks from Akonadi resources"
arch=('i686' 'x86_64')
url="http://kde-apps.org/content/show.php/Akonadi+tasks+plasmoid?content=149525"
license=('GPL')
source=('http://kde-apps.org/CONTENT/content-files/149525-tasks.tar.gz')
md5sums=('7fa4b71b75298ab8128688f8bd33bdd4')
depends=('kdebase-workspace')
makedepends=('cmake' 'automoc4' 'boost')
install=$pkgname.install

build() {
  cd $srcdir/tasks
  mkdir build 
  cd build
  cmake -DCMAKE_INSTALL_PREFIX=/usr -DALL_COLLECTIONS=true ..
  make
}

package() {
  cd $srcdir/tasks/build
  make DESTDIR=$pkgdir install
}