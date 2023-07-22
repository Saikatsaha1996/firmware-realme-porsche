# Maintainer: Saikat Saha <ssaikatsaha1996@gmail.com>

pkgname=firmware-realme-porsche
pkgver=1
pkgrel=0
pkgdesc="Firmware for Realme GT 2 (porsche)"
url=""
arch="aarch64"
#depends=""
license="proprietary"
options="!strip !check !archcheck"

_commit=""

source="$pkgname.tar.gz::$url/-/archive/$_commit/$pkgname-$_commit.tar.gz
firmware.files"

package() {
	cd "$srcdir/$pkgname-$_commit/"
	while IFS="" read -r _i || [ -n "$_i" ]; do
		[ ! -d $(dirname $_i) ] && mkdir -p $(dirname $_i)
		echo $_i
		install -Dm644 $_i "$pkgdir/$_i"
	done < "$srcdir/firmware.files"
}

sha512sums=""
