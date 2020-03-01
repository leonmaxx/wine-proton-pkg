# Maintainer: Leonid Maksymchuk <leonmaxx@gmail.com>
# Maintainer: Felix Yan <felixonmars@archlinux.org>
# Contributor: Sven-Hendrik Haase <sh@lutzhaase.com>
# Contributor: Jan "heftig" Steffens <jan.steffens@gmail.com>
# Contributor: Eduardo Romero <eduardo@archlinux.org>
# Contributor: Giovanni Scafora <giovanni@archlinux.org>

pkgname=wine-proton
pkgver=5.0
pkgrel=3

_pkgcommit=1a7d5eaf580cc78de7b9ec54cf2bd6814fc3c197

_pkgbasever=${pkgver/rc/-rc}

source=("wine-proton-$pkgver-$pkgrel.zip::https://github.com/ValveSoftware/wine/archive/$_pkgcommit.zip"
        wine-ntdll-rtlsysinfo.patch
        wine-dllredirect.patch
        winecfg-staging.patch
        wine-d3d9-nine.patch
        proton-nocrash.patch
        proton-disable-menubuilder.patch
        proton-win10.patch
        proton-steam-app-id.patch
        vkd3d-versioned-root-sig-01.patch
        vkd3d-versioned-root-sig-02.patch
        30-win32-aliases.conf
        wine-binfmt.conf)
sha512sums=('43dddd8574dc58cdc4f78f738da969e398709bd6a3f29f8860c72f83e6086d501a560225bd019deda0e2222baa699ea910ae02dde808681b6402f6198b74d750'
            '637e49c645b8933bebd517d34818a7cc5cc7e2e1b1cfd1711aae454e9f9467f7b75dac0fb44b3c66b742969b10141a724fa538e1e26b6b683563d869fb21b30e'
            'ff2b1a7b5bd2b4552f35c1be9dc43e3bdc84ece67b968bebc09b9df460c9c383986cc80e39ffd3da9a371d3d265a00f8111bbb97d00339f71fa247c06e2be8b5'
            '0993b719e582150ced4cf75c2bc21662372cea2be9008bd99f2c8aed25a9b16284834f1bd6f74443c3a22e91e0e2fd08e735ffbc4a0344513c4518f861e0248d'
            '0b522a0bcf0a9e913efdd99805e119b4282ea25afe2a3b09659ea445ef4076542377b5a8465e77c2a97d004f3a047f06e587bc3516e07c0adcf810064344c3d1'
            '5986f42780f557fe78c1b8a91aac6fac6793b8b051189c4bf8918d3e905e436df51817218694e220185643a368ae6a1339560fce813760ca275ac6e309690e61'
            '76bc381f1ddc26c62c9cb1c39d4e9c75e92c66583e4964d4bde9ceeca595e6623b4763601383ac676e2be6add4df52f851185cf01b6b18e650c7d4e6c6f1a2b0'
            '15e72719a7ca7af9ec9e7cbe89abe10ed85aff4d265e0e6d69e19495df35cf1f9aa557bb3de4104921f89b5366389b9cefd33bcbe9f97f93902ed5be9978d5ca'
            '2078c2774a6e3e1ca1a7c4ebadc57289f46694d2ba56a77ca81336335a453ea34d84423c18560c7f9d8d2cc62f65897fe91906892b0f13e5221305b21fec0a03'
            '39aa8008de7045a357af7fcab9dcf8fa2daf3415eafc4d08570693260764c7aeb36188897b4f93d9e1b480b9816fb022421d07ad3fc454173b2f81cf02eb3344'
            'cfe91ea1e8956fdc63fa393f8037c223acf058b98afd122ee6b2b32cfaaebe2bf5a53d664f6f807add44a4e1e16c4da4bfb25de816e48c09ccf12f1682a00767'
            '6e54ece7ec7022b3c9d94ad64bdf1017338da16c618966e8baf398e6f18f80f7b0576edf1d1da47ed77b96d577e4cbb2bb0156b0b11c183a0accf22654b0a2bb'
            'bdde7ae015d8a98ba55e84b86dc05aca1d4f8de85be7e4bd6187054bfe4ac83b5a20538945b63fb073caab78022141e9545685e4e3698c97ff173cf30859e285')

pkgdesc="A compatibility layer for running Windows programs - Proton branch"
url="https://github.com/ValveSoftware/Proton/"
arch=(x86_64)
options=(staticlibs)
license=(LGPL)

depends=(
  attr             lib32-attr
  faudio           lib32-faudio
  fontconfig       lib32-fontconfig
  lcms2            lib32-lcms2
  libxml2          lib32-libxml2
  libxcursor       lib32-libxcursor
  libxrandr        lib32-libxrandr
  libxdamage       lib32-libxdamage
  libxi            lib32-libxi
  gettext          lib32-gettext
  freetype2        lib32-freetype2
  glu              lib32-glu
  libsm            lib32-libsm
  gcc-libs         lib32-gcc-libs
  libpcap          lib32-libpcap
  desktop-file-utils
  giflib                lib32-giflib
  libpng                lib32-libpng
  libldap               lib32-libldap
  gnutls                lib32-gnutls
  mpg123                lib32-mpg123
  openal                lib32-openal
  libjpeg-turbo         lib32-libjpeg-turbo
  libxcomposite         lib32-libxcomposite
  libxinerama           lib32-libxinerama
  ncurses               lib32-ncurses
  opencl-icd-loader     lib32-opencl-icd-loader
  libxslt               lib32-libxslt
  libva                 lib32-libva
  gst-plugins-base-libs lib32-gst-plugins-base-libs
  vulkan-icd-loader     lib32-vulkan-icd-loader
  sdl2                  lib32-sdl2
  vkd3d                 lib32-vkd3d
)

makedepends=(autoconf ncurses bison perl fontforge flex
  'gcc>=4.5.0-2'
  giflib                lib32-giflib
  libpng                lib32-libpng
  gnutls                lib32-gnutls
  libxinerama           lib32-libxinerama
  libxcomposite         lib32-libxcomposite
  libxmu                lib32-libxmu
  libxxf86vm            lib32-libxxf86vm
  libldap               lib32-libldap
  mpg123                lib32-mpg123
  openal                lib32-openal
  v4l-utils             lib32-v4l-utils
  alsa-lib              lib32-alsa-lib
  libxcomposite         lib32-libxcomposite
  mesa                  lib32-mesa
  mesa-libgl            lib32-mesa-libgl
  opencl-icd-loader     lib32-opencl-icd-loader
  libxslt               lib32-libxslt
  libpulse              lib32-libpulse
  libva                 lib32-libva
  gtk3                  lib32-gtk3
  gst-plugins-base-libs lib32-gst-plugins-base-libs
  vulkan-icd-loader     lib32-vulkan-icd-loader
  sdl2                  lib32-sdl2
  vkd3d                 lib32-vkd3d
  sane
  libgphoto2
  gsm
  ffmpeg
  samba
  opencl-headers
)

optdepends=(
  v4l-utils             lib32-v4l-utils
  alsa-plugins          lib32-alsa-plugins
  alsa-lib              lib32-alsa-lib
  libpulse              lib32-libpulse
  gtk3                  lib32-gtk3
  sane
  libgphoto2
  gsm
  ffmpeg
  cups
  samba           dosbox
)

provides=("wine=$pkgver" "wine-wow64=$pkgver")
conflicts=('wine' 'wine-wow64' 'wine-staging')
install=wine.install

prepare() {
  # Allow ccache to work
  mv wine-$_pkgcommit $pkgname

  # apply patches and reconfigure
  pushd $pkgname
  patch -p1 <../wine-ntdll-rtlsysinfo.patch
  patch -p1 <../wine-dllredirect.patch
  patch -p1 <../winecfg-staging.patch
  patch -p1 <../wine-d3d9-nine.patch
  patch -R -p1 <../proton-nocrash.patch
  patch -R -p1 <../proton-disable-menubuilder.patch
  patch -R -p1 <../proton-win10.patch
  patch -R -p1 <../proton-steam-app-id.patch
  patch -R -p1 <../vkd3d-versioned-root-sig-01.patch
  patch -R -p1 <../vkd3d-versioned-root-sig-02.patch

  autoreconf
  tools/make_requests
  popd

  # Doesn't compile without remove these flags as of 4.10
  export CFLAGS="${CFLAGS/-fno-plt/}"
  export CFLAGS="${CFLAGS/-fstack-protector-strong/}"
  export CPPFLAGS=
  export LDFLAGS="${LDFLAGS/,-z,now/}"

  export CROSSCFLAGS="${CFLAGS/-fstack-protector-strong/} -fcf-protection=none -fno-stack-protector -fno-strict-aliasing"
  export CROSSLDFLAGS="${LDFLAGS/,-z,relro/}"

  sed 's|OpenCL/opencl.h|CL/opencl.h|g' -i $pkgname/configure*

  # Get rid of old build dirs
  rm -rf $pkgname-{32,64}-build
  mkdir $pkgname-{32,64}-build
}

build() {
  cd "$srcdir"

  msg2 "Building Wine-64..."

  cd "$srcdir/$pkgname-64-build"
  ../$pkgname/configure \
    --prefix=/usr \
    --libdir=/usr/lib \
    --with-x \
    --with-gstreamer \
    --enable-win64 \
    --with-xattr \
    --disable-tests

  make

  msg2 "Building Wine-32..."

  export PKG_CONFIG_PATH="/usr/lib32/pkgconfig"
  cd "$srcdir/$pkgname-32-build"
  ../$pkgname/configure \
    --prefix=/usr \
    --with-x \
    --with-gstreamer \
    --with-xattr \
    --libdir=/usr/lib32 \
    --disable-tests \
    --with-wine64="$srcdir/$pkgname-64-build"

  make
}

package() {
  msg2 "Packaging Wine-32..."
  cd "$srcdir/$pkgname-32-build"

  make prefix="$pkgdir/usr" \
    libdir="$pkgdir/usr/lib32" \
    dlldir="$pkgdir/usr/lib32/wine" install

  msg2 "Packaging Wine-64..."
  cd "$srcdir/$pkgname-64-build"
  make prefix="$pkgdir/usr" \
    libdir="$pkgdir/usr/lib" \
    dlldir="$pkgdir/usr/lib/wine" install

  # Font aliasing settings for Win32 applications
  install -d "$pkgdir"/etc/fonts/conf.{avail,d}
  install -m644 "$srcdir/30-win32-aliases.conf" "$pkgdir/etc/fonts/conf.avail"
  ln -s ../conf.avail/30-win32-aliases.conf "$pkgdir/etc/fonts/conf.d/30-win32-aliases.conf"
  install -Dm 644 "$srcdir/wine-binfmt.conf" "$pkgdir/usr/lib/binfmt.d/wine.conf"
}

# vim:set ts=8 sts=2 sw=2 et:
