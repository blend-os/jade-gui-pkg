# Maintainer: Rudra Saraswat <rs2009@ubuntu.com>
# Original maintainer: Crystal Linux Distribution Team <distribution@lists.getcryst.al>

pkgname=jade-gui
pkgver=1.9.3
pkgrel=1
pkgdesc='Libadwaita based GUI front-end for blend-inst'
license=('GPL3')
arch=('x86_64' 'aarch64')
url="https://github.com/blend-os/jade-gui"
depends=('blend-inst' 'openssl' 'libadwaita' 'python-pytz' 'gparted' 'vte4' 'gtksourceview5' 'python-tzlocal' 'python-requests' 'reflector')
makedepends=('meson' 'ninja' 'desktop-file-utils' 'appstream-glib' 'gtk4')
source=("git+${url}.git")
sha256sums=('SKIP')

build() {
    cd "jade-gui"
    meson setup --prefix="/usr" _build
    ninja -C _build
}

package() {
    cd "jade-gui/_build"
    DESTDIR="${pkgdir}" ninja install
}
