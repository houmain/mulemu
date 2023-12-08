
pkgname=mulemu-git
_pkgname=mulemu
pkgver=r2.9c924f0
pkgrel=1
pkgdesc='A simple command line frontend for multiple emulators (and Wine)'
arch=(any)
url="https://github.com/houmain/mulemu"
license=('GPL')
depends=('python' 'python-appdirs')
optdepends=(
  'dosbox' 'fs-uae' 'mednafen' 'retroarch' 'wine'
  'unzip' 'unrar' 'unace' 'unarj' 'ecm-tools')
makedepends=('git')
conflicts=(${_pkgname})
provides=(${_pkgname})
source=('git+https://github.com/houmain/mulemu.git')
md5sums=(SKIP)

pkgver() {
  cd "${srcdir}/${_pkgname}"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  install -Dm755 "${srcdir}/${_pkgname}/mulemu" "${pkgdir}/usr/bin/mulemu"
}
