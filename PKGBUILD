# Maintainer: Maître Piccolo <Maitre DOT Piccolo AT gmail DOT com>
pkgname=bullseye-qt-devel
pkgver=0.2
pkgrel=6
pkgdesc="A media/file manager that work by modules and display/sort files based on what they are instead of just where they are on the disk"
arch=('any')
url="http://daimao.info/bullseye"
license=('GPL2')
depends=('python2' 'pyside' 'python-imaging' 'mutagen' 'python2-pylast')

optdepends=('gstreamer0.10-python: gstreamer backend support'
 		'gstreamer0.10-good-plugins: gstreamer backend support - formats'
		'gstreamer0.10-bad-plugins: gstreamer backend support - formats'
	    'gstreamer0.10-ugly-plugins: gstreamer backend support - formats'
	    'gstreamer0.10-ffmpeg: gstreamer backend support - formats'
            'vlc: vlc backend support')

provides=('bullseye-qt')

source=(https://launchpad.net/bullseye/trunk/30042012/+download/bullseye.tar.bz2)

md5sums=('d8f43e5f368707b38f960b448ecd0bc3')



package() {
  cd "$srcdir/"
  mv trunk/Makefile-qt Makefile
  make DESTDIR="$pkgdir" install
}
