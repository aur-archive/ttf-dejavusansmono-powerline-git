# Maintainer: Thomas Ruoff <tomru@ido.cassiopeia.uberspace.de>

pkgname=ttf-dejavusansmono-powerline-git
pkgver=51.1ceb8dc
pkgrel=1
pkgdesc="Pre-patched and adjusted version for usage with the new Powerline plugin"
arch=('any')
url='https://github.com/Lokaltog/powerline-fonts/tree/master/DejaVuSansMono'
license=('unknown')
depends=('fontconfig' 'xorg-font-utils')
makedepends=('git')
optdepends=('python-powerline-git: The ultimate statusline/prompt utility'
	'python2-powerline-git: The ultimate statusline/prompt utility')
install=${pkgname}.install
source=("$pkgname::git://github.com/Lokaltog/powerline-fonts")
md5sums=('SKIP')

pkgver() {
  cd "${srcdir}/${pkgname}/DejaVuSansMono"
  echo $(git rev-list --count master).$(git rev-parse --short master)
}

package() {
  cd "${srcdir}/${pkgname}/DejaVuSansMono"

  local regular='DejaVu Sans Mono for Powerline.ttf'
  local boldOblique='DejaVu Sans Mono Bold Oblique for Powerline.ttf'
  local bold='DejaVu Sans Mono Bold for Powerline.ttf'
  local oblique='DejaVu Sans Mono Oblique for Powerline.ttf'
  install -Dm644 "$regular" "${pkgdir}/usr/share/fonts/TTF/DejaVuSansMonoForPowerline.ttf"
  install -Dm644 "$boldOblique" "${pkgdir}/usr/share/fonts/TTF/DejaVuSansMonoForPowerline-BoldOblique.ttf"
  install -Dm644 "$bold" "${pkgdir}/usr/share/fonts/TTF/DejaVuSansMonoForPowerline-Bold.ttf"
  install -Dm644 "$oblique" "${pkgdir}/usr/share/fonts/TTF/DejaVuSansMonoForPowerline-Oblique.ttf"
}

# vim: set ts=2 sw=2 ft=sh noet:
