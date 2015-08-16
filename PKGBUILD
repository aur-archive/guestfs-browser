# Maintainer: Patryk Kowalczyk < patryk at kowalczyk dot ws>

pkgname=guestfs-browser
pkgver=0.2.2
pkgrel=7
pkgdesc="browse inside the filesystems of virtual machines and disk images using a simple graphical interface"
arch=(i686 x86_64)
license=('GPL2')
url="http://people.redhat.com/~rjones/guestfs-browser/"
depends=('libguestfs' 'gtk2' 'ocaml-bitstring' 'ocaml-extlib' 'ocaml-libvirt')
makedepends=('lablgtk2' 'ocaml-xml-light' 'ocaml-calendar' 'ocaml-camomile' 'ocaml-bitstring' 'ocaml-extlib>=1.5.3')
backup=()
conflicts=()
provides=()
replaces=()
source=(http://people.redhat.com/~rjones/guestfs-browser/files/${pkgname}-${pkgver}.tar.gz)
md5sums=('be3c9e73d82a457cbae2f4fe6c2442a1')

options=(!strip)

build()
{
    cd ${srcdir}/${pkgname}-${pkgver}
    aclocal 
    automake --add-missing
    ./configure --prefix=/usr 
    make
}
package()
{
    cd ${srcdir}/${pkgname}-${pkgver}
    make DESTDIR=${pkgdir} install
}
