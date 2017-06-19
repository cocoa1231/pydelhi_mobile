pkgname=PyDelhi
pkgver=1.0.0
pkgrel=1
pkgdesc="The PyDelhi App ported to Arch Linux"
arch=(x86_64)
url="https://github.com/pydelhi/pydelhi_mobile"
license=('AGPL-3.0')
groups=('extra')
depends=('python2N-kivy')
backup=()
options=()
noextract=()
md5sums=()
validpgpkeys=()

build() { 
	if git clone https://github.com/cocoa1231/pydelhi_mobile 2>/dev/null ; then
    	echo 'Clone was sucessful'
	else
    	echo 'Clone failed. Probably because its already cloned'
fi
}
package() {
	cd pydelhi_mobile
	install -D PyDelhi.desktop "$pkgdir/usr/share/applications/$pkgname.desktop"
	install -D photo*.jpg "$pkgdir/usr/share/icons/$pkgname.jpg"
	mkdir -p "$pkgdir/usr/bin"
	cp -r "pydelhiconf" "$pkgdir/usr/bin/pydelhiconf"
}
