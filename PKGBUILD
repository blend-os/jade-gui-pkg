# Maintainer: Rudra Saraswat <rs2009@ubuntu.com>
# Original maintainer: Crystal Linux Distribution Team <distribution@lists.getcryst.al>

pkgname=jade-gui
pkgver=1.8.6
pkgrel=1
pkgdesc='Libadwaita based GUI front-end for Jade'
license=('GPL3')
arch=('x86_64' 'aarch64')
url="https://github.com/blend-os/jade-gui"
depends=('jade' 'openssl' 'libadwaita' 'python-pytz' 'gparted' 'vte4' 'gtksourceview5' 'python-tzlocal' 'python-requests' 'reflector')
makedepends=('meson' 'ninja' 'desktop-file-utils' 'appstream-glib' 'gtk4')
source=("git+https://github.com/blend-os/jade-gui.git")
sha256sums=('SKIP')

build() {
    cd "jade-gui"
    meson --prefix="/usr" _build
    ninja -C _build
}

package() {
    cd "jade-gui"
    DESTDIR="${pkgdir}" ninja install
}
