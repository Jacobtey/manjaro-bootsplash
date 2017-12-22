pkgbase=bootsplash-themes
pkgname=('bootsplash-theme-manjaro-oldschool')
pkgver=0.6
pkgrel=1
url="https://lists.freedesktop.org/archives/dri-devel/2017-December/160242.html"
arch=('x86_64')
license=('GPL')

depends=('linux414' 'systemd')
builddepends=('imagemagick')
options=('!libtool' '!emptydirs')

source=('bootsplash-packer'
	'bootsplash-manjaro-oldschool.sh'
	'bootsplash-manjaro-oldschool.initcpio_install'
	'spinner.gif'
	'manjaro-oldschool.png')

sha256sums=('SKIP'
            'SKIP'
            'SKIP'
            'SKIP'
            'SKIP')

build() {
  cd "$srcdir"
  sh ./bootsplash-manjaro-oldschool.sh
}

package_bootsplash-theme-manjaro-oldschool() {
  pkgdesc="Bootsplash Theme 'Manjaro Oldschool'"
  cd "$srcdir"

  install -Dm644 "$srcdir/bootsplash-manjaro-oldschool" "$pkgdir/usr/lib/firmware/bootsplash-themes/manjaro-oldschool/bootsplash"
  install -Dm644 "$srcdir/bootsplash-manjaro-oldschool.initcpio_install" "$pkgdir/usr/lib/initcpio/install/bootsplash-manjaro-oldschool"
} 
