# Author: Robert Maerz
pkgname=mkinitcpio-bluetooth
pkgver=1.1
pkgrel=1
pkgdesc="This is a initcpio hook for bluetooth connectivity during boot / in initramfs."
url="https://github.com/irreleph4nt/mkinitcpio-bluetooth/"
arch=('x86_64' 'i686')
license=('GPLv2')
depends=('bluez' 'bluez-utils' 'dbus')
makedepends=('git')
conflicts=(mkinitcpio-btinput)
replaces=(mkinitcpio-btinput)
install=mkinitcpio-bluetooth.install
source=(bluetooth_install bluetooth_hook org.bluez.conf)
md5sums=('7ad85adf91d7acd8b4ec556dbde1b35a'
         'e507be5e21ec99c7bc0e35dee9d68f5b'
         '5c171037726256d674bcc2d05fdbab86'
)

prepare () {
}

package() {
  install -Dm644 bluetooth_install "${pkgdir}/usr/lib/initcpio/install/bluetooth"
  install -Dm644 bluetooth_hook "${pkgdir}/usr/lib/initcpio/hooks/bluetooth"
  install -Dm644 org.bluez.conf "${pkgdir}/usr/lib/initcpio/bluetooth/org.bluez.conf"

}

# vim:set ts=2 sw=2 et:
