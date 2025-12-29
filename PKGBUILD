# Maintainer: user8885 <takodajhorton@protonmail.com>
_pkgname=dracula-theme-user8885
pkgname="${_pkgname}-git"
pkgver=0.1.r4.87d2bf4b
pkgrel=1
pkgdesc="Colloid(dracula), Tela Circle(dracula), gtk theme with kvantum theme"
arch=(any)
url="https://github.com/user8885/dracula-theme-user8885"
license=('MIT')
source=(git+$url)
sha256sums=(SKIP)

pkgver() {
    cd "${_pkgname}"
    printf "0.1.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd ${_pkgname}

    mkdir -p ${pkgdir}/usr/share/themes
    cp -rf themes/* ${pkgdir}/usr/share/themes/

    mkdir -p ${pkgdir}/usr/share/icons
    cp -rf icons/* ${pkgdir}/usr/share/icons/

    mkdir -p ${pkgdir}/usr/share/Kvantum
    cp -rf Kvantum/* ${pkgdir}/usr/share/Kvantum/

    install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    install -Dm644 README.MD "${pkgdir}/usr/share/doc/${pkgname}/README.MD"
}
