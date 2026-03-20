pkgname=simple-sddm-qt6
pkgver=r1
pkgrel=1
pkgdesc="Simple SDDM theme ported to Qt 6"
arch=('any')
url="https://github.com/Skydeke/simple-sddm"
license=('GPL3')
depends=(
    'sddm'
    'qt6-declarative'
    'qt6-5compat'
)
optdepends=(
    'qt6-virtualkeyboard: on-screen virtual keyboard support'
)
source=("git+https://github.com/Skydeke/simple-sddm.git")
sha256sums=('SKIP')

pkgver() {
    cd "$srcdir/simple-sddm"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    local themedir="$pkgdir/usr/share/sddm/themes/$pkgname"
    install -d "$themedir"

    cp -r "$srcdir/simple-sddm/." "$themedir/"

    find "$themedir" -type f -exec chmod 644 {} \;
    find "$themedir" -type d -exec chmod 755 {} \;
}
