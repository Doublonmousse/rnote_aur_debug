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
b2sums=('3e9078a40b892be02b7e653579966aac5d8157ad8db38a61d9a56cc7428206b31829d83ce440577a567a5c580c26ad01f811ff7fc0d07ce73422c09ea020fa11')
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
