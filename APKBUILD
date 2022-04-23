# Reference: <https://postmarketos.org/devicepkg>
pkgname=device-xiaomi-latte
pkgdesc="Xiaomi Mi Pad 2"
pkgver=0.1
pkgrel=0
url="https://postmarketos.org"
license="MIT"
arch="x86_64"
options="!check !archcheck"
depends="
	linux-xiaomi-latte
	mesa-dri-gallium
	mkbootimg
	postmarketos-base
"
makedepends="devicepkg-dev"
source="deviceinfo"
subpackages="$pkgname-nonfree-firmware:nonfree_firmware"
build() {
	devicepkg_build $startdir $pkgname
}

package() {
	devicepkg_package $startdir $pkgname
}

nonfree_firmware() {
        pkgdesc="Proprietary firmware"
        depends="linux-firmware-intel firmware-xiaomi-latte"
        mkdir "$subpkgdir"
}

sha512sums="
22b7bf72b4ba456cb560eea626edb78ad6f1d571df4ce8a406889a060f88f02e752e29aeb70a19cc25e8d86d3399e0d8dc9b3e1b057d35ce9002c8066424e31b  deviceinfo
"
