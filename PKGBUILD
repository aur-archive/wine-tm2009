# Contributor: lishengming.zju <lishengming.zju@gmail.com>
pkgname=wine-tm2009
pkgver=20120719
pkgrel=2
pkgdesc='wine version of Tencent Messenger client,made by Longene Team.'
arch=('i686' 'x86_64')
url='http://www.longene.org/'
license=('Other')
install=wine-tm2009.install
source=("http://www.longene.org/download/WineTM2009-20120719-Longene.deb")
md5sums=('5a948f1c61b476d78ee88f041730f9d0')

if [ "$CARCH" = "i686" ]; then
    depends=('gtk2')
elif [ "$CARCH" = "x86_64" ]; then
    depends=('lib32-gtk2')
fi

package()
{
    tar xzvf ${srcdir}/data.tar.gz -C ${pkgdir}/
    chmod -R 755 ${pkgdir}/opt/longene

    #Fix tm2009-test.desktop
    sed -i 's/wineapp\///g' ${pkgdir}/usr/share/applications/tm2009-test.desktop
}
