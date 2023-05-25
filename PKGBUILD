# Maintainer: James Wood (Chryseus) <Chryseus8080@gmail.com>
# Updated By D3c0y <viruspixel@protonmail.com>

pkgname=soapysdrplay
_pkgname=SoapySDRPlay3-soapy-sdrplay3-0.4.1
pkgver=0.4.1
pkgrel=1
pkgdesc="SDRplay support module for SoapySDR"
arch=('x86_64')
url="https://github.com/pothosware/SoapySDRPlay3"
license=('MIT')
depends=('soapysdr' 'libsdrplay')
makedepends=('cmake')
source=("https://github.com/pothosware/SoapySDRPlay3/archive/refs/tags/soapy-sdrplay3-0.4.1.tar.gz")
sha256sums=('71b4d9734f7657a39122a3ce63caad2eca06f207cd5206e07eb1d6c6f73c6c04')

build() {
mkdir -p "$_pkgname"/build
cd "$_pkgname"/build
cmake .. \
	-DCMAKE_INSTALL_PREFIX=/usr \
	-DCMAKE_BUILD_TYPE=Release
make
}

package() {
	cd "$_pkgname"/build
	make DESTDIR="$pkgdir" install
}

