# Maintainer: Abraham Levine <echo arc.plusreed.com | sed 's/\@/./'>

pkgname=steak-git
pkgver=0.1
pkgrel=1
pkgdesc="a quick AUR helper written in pure bash, fork of meat, cower backend"
arch=('i686' 'x86_64')
url="http://github.com/arcetera/steak"
license=('MIT')
depends=('bash>=4.0' 'cower' 'awk')
makedepends=('git')
optdepends=('sudo: highly recommended')
source=('git://github.com/arcetera/steak.git')
md5sums=('SKIP')
_gitname='steak'

pkgver() {
  cd "$_gitname" &&
  printf '%s.%s\n' "$(git rev-list --count HEAD)" \
                   "$(git rev-parse --short HEAD)"
}

package() {
  cd "$_gitname" &&
  install -m 755 -D steak "$pkgdir/usr/bin/steak" &&
  install -m 644 -D config "$pkgdir/usr/share/steak/config"
}

# vim: ft=sh syn=sh et
