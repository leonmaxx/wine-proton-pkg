# Maintainer: Leonid Maksymchuk <leonmaxx@gmail.com>
# Maintainer: Felix Yan <felixonmars@archlinux.org>
# Contributor: Sven-Hendrik Haase <sh@lutzhaase.com>
# Contributor: Jan "heftig" Steffens <jan.steffens@gmail.com>
# Contributor: Eduardo Romero <eduardo@archlinux.org>
# Contributor: Giovanni Scafora <giovanni@archlinux.org>

pkgname=wine-proton
pkgver=4.11
pkgrel=6

_pkgcommit=08a1b1024f9376309ae6bcbc902aa36478184b6d

_pkgbasever=${pkgver/rc/-rc}

source=("wine-proton-$pkgver-$pkgrel.zip::https://github.com/ValveSoftware/wine/archive/$_pkgcommit.zip"
        wine-ntdll.patch
        wine-dllredirect.patch
        winecfg-staging.patch
        wine-d3d9-nine.patch
        proton-nocrash.patch
        proton-disable-menubuilder.patch
        30-win32-aliases.conf
        wine-binfmt.conf)
sha512sums=('79d7f22b1987c65f57ab7f39643450da984eeb0a299caebf2997f4100b20c8c5a6317dc25eaacd4a8c2da09c13ee8838a15327b5f9a7aac96f275a064ff85cd7'
            'b6318b7ac2347e68419dd9d59804fb88ec5f9f3f09332101ca92e73f08d12b65637397dc666b6a5218d690e9003df96f3b5e5f31cee89900ebfdabce2998fab8'
            '1dd5a3fa5b23eab176eb73ec5feb128f16a611b9a4b7bcc887096bab07e85890a96f81eba8ff0abd04a645d442a3a3139e0a1f8e317fa4e0d52bf0e793d1c95d'
            '0993b719e582150ced4cf75c2bc21662372cea2be9008bd99f2c8aed25a9b16284834f1bd6f74443c3a22e91e0e2fd08e735ffbc4a0344513c4518f861e0248d'
            '659c894325db695c9c9aa4137a99e1a489c155a7592f7dbb40e5e4a4f9c70adf620999791af3c1b0fccd70e22e0b79d36ac406f417be9ef880c8b2cedd84bb1e'
            '5986f42780f557fe78c1b8a91aac6fac6793b8b051189c4bf8918d3e905e436df51817218694e220185643a368ae6a1339560fce813760ca275ac6e309690e61'
            '76bc381f1ddc26c62c9cb1c39d4e9c75e92c66583e4964d4bde9ceeca595e6623b4763601383ac676e2be6add4df52f851185cf01b6b18e650c7d4e6c6f1a2b0'
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
  patch -p1 <../wine-ntdll.patch
  patch -p1 <../wine-dllredirect.patch
  patch -p1 <../winecfg-staging.patch
  patch -p1 <../wine-d3d9-nine.patch
  patch -R -p1 <../proton-nocrash.patch
  patch -R -p1 <../proton-disable-menubuilder.patch

  autoreconf
  tools/make_requests
  popd

  # Doesn't compile without remove these flags as of 4.10
  export CFLAGS="${CFLAGS/-fno-plt/}"
  export LDFLAGS="${LDFLAGS/,-z,now/}"

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
