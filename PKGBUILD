# Maintainer: iota-wallet
pkgname=iota-wallet
pkgver=2.3.1
pkgrel=1
pkgdesc="IOTA Wallet"
arch=('x86_64')
url="https://www.iota.org"
license=('GPL')
groups=('')
depends=('desktop-file-utils' 'gconf' 'hicolor-icon-theme' 'libappindicator-gtk2' 'libnotify' 'libxss' 'libxtst' 'nss')
options=('!strip' '!emptydirs')
install=${pkgname}.install
source_x86_64=(
  "https://github.com/iotaledger/wallet/releases/download/v${pkgver}/iota_${pkgver}_amd64.deb"
	"iota.desktop"
)
sha512sums_x86_64=(
  "4533f52a14c683f4928bbe8fb9a3a1302e796da06d1bdf3696b8a46d445d1bd4ec6cde58b1a14af75da7dc8f7b5a26e373f335a708a5bb6dca6cf863497b3465"
	"02c9da5e72292b00e62efc9a0cb684e916659cb0818407eefdca49b5ceafadbc91aac85a6a0783101bdb8debbb5f98dfd9a87890496aacb30fb5052c4f0816fb"
)

package(){
  # Extract package data
  tar xf data.tar.xz -C "${pkgdir}"
  perl-rename "s/IOTA Wallet/${pkgname}/g" "${pkgdir}"/opt/*

  install -Dm644 iota.desktop "${pkgdir}"/usr/share/applications/iota.desktop
}
