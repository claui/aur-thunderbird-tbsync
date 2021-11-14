# Maintainer: Michal Wojdyla < micwoj9292 at gmail dot com>
# Contributor: Javier Tiá <javier dot tia at gmail dot com>
# Contributor: Claudia Pellegrino <aur ät cpellegrino.de>

pkgname=thunderbird-tbsync
pkgver=3.0.1
pkgrel=2
_file=1019345
_name=tbsync
pkgdesc="Sync contacts, tasks and calendars to thunderbird using Exchange ActiveSync (EAS) and CalDAV/CardDAV"
arch=('any')
url="https://github.com/jobisoft/TbSync"
license=('MPL-2.0')
groups=('office')
depends=('thunderbird>=91' 'thunderbird<92')
optdepends=(
  'thunderbird-dav-4-tbsync: Sync CalDAV/CardDAV calendars'
  'thunderbird-eas-4-tbsync: Connect to Exchange ActiveSync'
)
provides=("${_name}=${pkgver}")
source=("https://addons.thunderbird.net/thunderbird/downloads/file/$_file/$_name-$pkgver-tb.xpi")
noextract=("$_name-$pkgver-tb.xpi")
sha256sums=('8fde425a3d7d784252e36d92fde2fdab29e19461e88ca51d626bd2d46a4edcc8')

package() {
  _extension_id="tbsync@jobisoft.de"
  _extension_dest="${pkgdir}/usr/lib/thunderbird/extensions/${_extension_id}"
  install -Dm644 "${srcdir}"/$_name-$pkgver-tb.xpi "${_extension_dest}.xpi"
}
