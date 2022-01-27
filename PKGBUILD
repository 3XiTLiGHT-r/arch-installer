# Maintainer: unknown

pkgname=arch-installer
pkgver=1.0
pkgrel=1
pkgdesc="Command line installer for Arch."
url="https://github.com/the-secret-society/arch-installer"
arch=('any')
license=('GPL3')
provides=($pkgname)
conflicts=($pkgname)
depends=('lxterminal')

source=(
		abif
		abif.desktop
		chrooted_post_install.sh
		post_install.sh
		english.trans)

sha256sums=('')

package() {
	local _idir="${pkgdir}/abif-master"
	local _bdir="${pkgdir}/usr/bin"
	
	mkdir -p "$_idir" && mkdir -p "$_bdir"

	install -Dm 755 chrooted_post_install.sh 	"$_bdir"/chrooted_post_install.sh
	install -Dm 755 post_install.sh 			"$_bdir"/post_install.sh
	install -Dm 755 abif 						"$_idir"/abif
	install -Dm 644 english.trans 				"$_idir"/english.trans

	# copy files
	install -Dm 644 abif.desktop 			-t ${pkgdir}/usr/share/applications/
}
