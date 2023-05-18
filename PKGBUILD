# Maintainer: Johannes Löthberg <johannes@kyriasis.com>
# Maintainer: Alexander Epaneshnikov <alex19ep@archlinux.org>

pkgname=repo
pkgver=2.33
pkgrel=1
pkgdesc="The Multiple Git Repository Tool from the Android Open Source Project"
url="https://android.googlesource.com/tools/repo"
arch=('any')
license=("APACHE")
depends=("git" "python")
source=("git+https://android.googlesource.com/tools/repo.git#tag=v$pkgver?signed")
validpgpkeys=('8BB9AD793E8E6153AF0F9A4416530D5E920F5C65') # Repo Maintainer <repo@android.kernel.org>
sha256sums=('SKIP')

package() {
  cd repo
  install -vDm755 repo "$pkgdir/usr/bin/repo"
  install -vDm644 docs/manifest-format.md "$pkgdir/usr/share/doc/$pkgname/manifest-format.md"
  install -vDm644 -t "$pkgdir/usr/share/man/man1" man/*
}
