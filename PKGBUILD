# Maintainer: Orhun Parmaksız <orhun@archlinux.org>
# Contributor: Igor Dyatlov <dyatlov.igor@protonmail.com>

pkgname=rnote
pkgver=0.12.0
pkgrel=2
pkgdesc="A simple drawing application to create handwritten notes (DEBUG VERSION)"
arch=('x86_64')
url="https://github.com/Doublonmousse/rnote"
license=('GPL3')
depends=('gtk4' 'glib2' 'libadwaita' 'poppler-glib' 'gstreamer' 'alsa-lib')
makedepends=('meson' 'cargo' 'cmake' 'clang' 'git')
#checkdepends=('appstream-glib')
source=("rnote-debug_1258_unsaved_indicator.tar.gz::https://github.com/Doublonmousse/rnote/archive/refs/heads/debug_1258_unsaved_indicator.tar.gz")
b2sums=('efd3b1ebf30f805fc5760672233f2d5af92760e374d126b91e48351ee65ffc33428f3e15b9743dca965ae9b18b2e5444cf38ef2c1aaae6281c5ec9b4626b048e')
options=('!lto')

build() {
  arch-meson "rnote-debug_1258_unsaved_indicator" build -Dcli=true
  meson compile -C build
}

#check() {
#  meson test -C build
#}

package() {
  meson install -C build --destdir "$pkgdir"
}

# vim: ts=2 sw=2 et:
