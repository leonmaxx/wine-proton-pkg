# Maintainer: Leonid Maksymchuk <leonmaxx@gmail.com>
# Contributor: Felix Yan <felixonmars@archlinux.org>
# Contributor: Sven-Hendrik Haase <sh@lutzhaase.com>
# Contributor: Jan "heftig" Steffens <jan.steffens@gmail.com>
# Contributor: Eduardo Romero <eduardo@archlinux.org>
# Contributor: Giovanni Scafora <giovanni@archlinux.org>

pkgname=wine-proton
pkgver=6.3
pkgrel=5

_winever=$pkgver
_pkgbasever=${pkgver/rc/-rc}

_wine_commit=eef39a6e9c0a9b939521c7a5119225b4823b83cc
_dxvk_commit=726b2138c42825407402c200d9ca495aecbdc96b
_vkd3d_commit=72d9b322b89c325520e8f3060a8b60f719c52d6e

source=("$pkgname::git+https://github.com/ValveSoftware/wine.git#commit=$_wine_commit"
        "dxvk::git+https://github.com/ValveSoftware/dxvk.git#commit=$_dxvk_commit"
        "vkd3d-proton::git+https://github.com/HansKristian-Work/vkd3d-proton.git#commit=$_vkd3d_commit"
        30-win32-aliases.conf
        wine-binfmt.conf
        wine.inf-Remove-Steam-registry-entries.patch
        dxdiag-Ignore-64bit-option.patch
        ucrtbase-Implement-sincos.patch
        msvcp90-Implement-sincos.patch
        widl-Ignore-option-pthread.patch
        wrc-Ignore-option-pthread.patch
        makefile-Proton-branding.patch)
sha512sums=('SKIP'
            'SKIP'
            'SKIP'
            '6e54ece7ec7022b3c9d94ad64bdf1017338da16c618966e8baf398e6f18f80f7b0576edf1d1da47ed77b96d577e4cbb2bb0156b0b11c183a0accf22654b0a2bb'
            'bdde7ae015d8a98ba55e84b86dc05aca1d4f8de85be7e4bd6187054bfe4ac83b5a20538945b63fb073caab78022141e9545685e4e3698c97ff173cf30859e285'
            '144af44d76bafea04a0a024be8a8f39c70e28306628353f3cb32b8bb485a7372b60bae9e4f9609ab269915764d4f567c51c6045e97ffc5ba0f1c30943c483cd0'
            '6b62ffdee725d78b7c36aa83843bb767fcd85470d4ea3ce2059d399fcfed6e67db7217df3a9faeca3ee2c676c2857f313177ab8be679b108d20fc188e0551f95'
            '03d5854d3e85c861e3d9e1fbdb98130571eaac1f3483e3bb4a650cd2b0432d7d43a08ecd94ec1c9130db5bce27da06123731b37330abb5e77ef768619c89ca82'
            'cc98004a23a28192067d3976abfb80db9598a5a094ec2457b69be4920f0320d9c9a2f1eecac6cce4f9e71f7000f5bd81274b403bfebfed90003a6b803fe7be6e'
            '14d156e0c741f53717389a18dc513208022bf57b0ebc38723eac0f41d59581850ce8adc777c6f5a6ab6e490a24083251a804e01770fd71cefac187410dcb4bfc'
            'debb94bf2a74afbe1b3c7f564c4dc2f25ac268bdedf7974c431943a1f63a59f9f90f861bc752736f21359a4cb40e526b238a973876f165ec09898d93d4c75415'
            '2f7bcc1cd02e7166833b393004d984967f3a656df9f428a66a6c36b9c6f5cfd9203f8e4f4a7a2ba736b059e4999418e6ddb65a5b5b50b42fba253d05e04442c5')

pkgdesc="A compatibility layer for running Windows programs - Proton branch"
url="https://github.com/ValveSoftware/Proton"
arch=(x86_64)
options=(staticlibs)
license=(LGPL)

depends=(
  attr             lib32-attr
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
  faudio           lib32-faudio
  desktop-file-utils
)

makedepends=(autoconf ncurses bison perl fontforge flex mingw-w64-gcc
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
  libcups               lib32-libcups
  sane
  libgphoto2
  gsm
  ffmpeg
  samba
  opencl-headers
)

optdepends=(
  giflib                lib32-giflib
  libpng                lib32-libpng
  libldap               lib32-libldap
  gnutls                lib32-gnutls
  mpg123                lib32-mpg123
  openal                lib32-openal
  v4l-utils             lib32-v4l-utils
  libpulse              lib32-libpulse
  alsa-plugins          lib32-alsa-plugins
  alsa-lib              lib32-alsa-lib
  libjpeg-turbo         lib32-libjpeg-turbo
  libxcomposite         lib32-libxcomposite
  libxinerama           lib32-libxinerama
  ncurses               lib32-ncurses
  opencl-icd-loader     lib32-opencl-icd-loader
  libxslt               lib32-libxslt
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
  cups
  samba           dosbox
)

provides=("wine=$pkgver" "wine-wow64=$pkgver" "wine-staging=$pkgver")
conflicts=('wine' 'wine-wow64' 'wine-staging')
install=wine.install

prepare() {
  # Revert unneeded Wine-Proton patches
  pushd $pkgname
    # wine.inf: Associate the steam protocol with steam.exe.
    git revert -n bc633e8c15139e66ccf7327e853b87ff9030fda0

    # fixup, user32: Use new export to set LD_PRELOAD
    git revert -n 97f962cd469ee9b9b68d32e79849bf94cfe15581
  
    # ntdll: Write crash log when we are missing a module
    git revert -n 4a38de8099c90692414eadf46007323e62cccd4d
  
    # ntdll: Export a function to set a Unix environment variable.
    git revert -n 12b4a3fb559cafd4b5fdb072dc4e2bb3aa1e95b1
  
    # dotnetfx35.exe: Add stub program.
    git revert -n 1f8552e34a897a751b3f5135db0559fed7424988
  
    # HACK: wineboot: Don't show "updating prefix" window
    git revert -n 285d64e7617ae31e3e03a6554404054cb5e9341f

    # wine.inf: Associate the "steam" protocol with winebrowser.
    git revert -n 0e40743b6d409bc2b669eac7ad6ce379be22fc17

    # wine.inf: Don't show crash dialog by default
    git revert -n 486bcb9740dc1735ccf1335075bcf7d3b3698e00

    # winex11: Fill WM_CLASS based on Steam appid
    git revert -n 1c42b167834b5b917f3ab1f4ae12110047529402

    # HACK: Don't build winemenubuilder
    git revert -n 6f51cddc7717e269621e515e8e2e8afed49a2fa1

    # HACK: mshtml: Don't install wine-gecko on prefix creation
    git revert -n 903a5167a20f744b58b1e94bd111a3892b42653d

    # Font related
    git revert -n 106fd7119b2d88dc4dece7b5058d73854a7aae2e
    git revert -n 781785fad4de09af31ee0cbd2983dac036f58ff3

    # HACK: shell32: Never create links to the user's home dirs
    git revert -n d3477cd06f80c3ababa4cff3133933ed815b9a48

    # HACK: advapi32: Use steamuser as Wine username
    git revert -n 207d17259d8aed05d3b69d242c2bc68b02aec378

    # HACK: steam: kernelbase: Substitute the current pid for the Steam
    git revert -n 1519ba09129800fa81957d0986e2017fe7243ba9

    # HACK: steam: ntdll: Patch entry points with jumps.
    git revert -n 762405d42e29a60e6eb5620cbb6693c43777268f

    # HACK: steam: ntdll: Setup steamclient trampolines to lsteamclient.
    git revert -n 916c2d0af18314f57734c1a9344bb9b1b1f20fbd

    patch -Np1 < ../wine.inf-Remove-Steam-registry-entries.patch
    patch -Np1 < ../dxdiag-Ignore-64bit-option.patch
    patch -Np1 < ../ucrtbase-Implement-sincos.patch
    patch -Np1 < ../widl-Ignore-option-pthread.patch
    patch -Np1 < ../wrc-Ignore-option-pthread.patch
    patch -Np1 < ../msvcp90-Implement-sincos.patch
    #autoreconf
    #tools/make_requests
  popd

  pushd vkd3d-proton
    git submodule update --init --recursive
  popd
  
  # Doesn't compile without remove these flags as of 4.10
  export CFLAGS="${CFLAGS/-fno-plt/}"
  export CXXFLAGS="${CXXFLAGS/-fno-plt/}"
  export LDFLAGS="${LDFLAGS/,-z,now/}"
  # Doesn't compile with -z,relro flag as of 5.13-5
  export LDFLAGS="${LDFLAGS/,-z,relro/}"
  # Doesn't compile with this options as of 6.3-3
  export CFLAGS="${CFLAGS/-Wp,-D_FORTIFY_SOURCE=2/}"
  export CXXFLAGS="${CXXFLAGS/-Wp,-D_FORTIFY_SOURCE=2/}"

  # Disable stack clash and control flow protection
  export CFLAGS="${CFLAGS/-fstack-clash-protection/}"
  export CFLAGS="${CFLAGS/-fcf-protection/}"
  export CXXFLAGS="${CXXFLAGS/-fstack-clash-protection/}"
  export CXXFLAGS="${CXXFLAGS/-fcf-protection/}"
  
  sed 's|OpenCL/opencl.h|CL/opencl.h|g' -i $pkgname/configure*

  # Get rid of old build dirs
  rm -rf $pkgname-{32,64}-build
  mkdir $pkgname-{32,64}-build

  rm -rf dxvk-{32,64}-build
  mkdir dxvk-{32,64}-build

  rm -rf vkd3d-{32,64}-build
  mkdir vkd3d-{32,64}-build
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
    --disable-tests

  patch -p1 < ../makefile-Proton-branding.patch
  make

  msg2 "Building Wine-32..."

  export PKG_CONFIG_PATH="/usr/lib32/pkgconfig"
  cd "$srcdir/$pkgname-32-build"
  ../$pkgname/configure \
    --prefix=/usr \
    --with-x \
    --with-gstreamer \
    --libdir=/usr/lib32 \
    --with-wine64="$srcdir/$pkgname-64-build" \
    --disable-tests

  patch -p1 < ../makefile-Proton-branding.patch
  make


  export CFLAGS="${CFLAGS/-O2/}"
  export CPPFLAGS="${CPPFLAGS/-O2/}"

  msg2 "Building DXVK-32..."

  cd "$srcdir/dxvk"
  meson --cross-file build-win32.txt --buildtype release --prefix "$srcdir/dxvk-32-build" build.w32
  ninja -C build.w32 install

  msg2 "Building DXVK-64..."

  cd "$srcdir/dxvk"
  meson --cross-file build-win64.txt --buildtype release --prefix "$srcdir/dxvk-64-build" build.w64
  ninja -C build.w64 install

  msg2 "Building VKD3D-32..."

  cd "$srcdir/vkd3d-proton"
  meson --cross-file build-win32.txt --buildtype release --prefix "$srcdir/vkd3d-32-build" build.w32
  ninja -C build.w32 install

  msg2 "Building VKD3D-64..."

  cd "$srcdir/vkd3d-proton"
  meson --cross-file build-win64.txt --buildtype release --prefix "$srcdir/vkd3d-64-build" build.w64
  ninja -C build.w64 install

}


package() {
  msg2 "Packaging Wine-32..."
  cd "$srcdir/$pkgname-32-build"

  make prefix="$pkgdir/usr" \
    libdir="$pkgdir/usr/lib32" \
    dlldir="$pkgdir/usr/lib32/wine" install

  msg2 "Packaging DXVK-32..."
  cd "$srcdir/dxvk-32-build/bin"
  rm -f "$pkgdir/usr/lib32/wine/dxgi.dll.so"
  for dll in d3d9 d3d10core d3d11 dxgi dxvk_config; do
    rm -f "$pkgdir/usr/lib32/wine/$dll.dll"
    $srcdir/$pkgname-64-build/tools/winebuild/winebuild --builtin $dll.dll
    cp $dll.dll "$pkgdir/usr/lib32/wine/$dll.dll"
  done

  msg2 "Packaging VKD3D-32..."
  cd "$srcdir/vkd3d-32-build/bin"
  rm -f "$pkgdir/usr/lib32/wine/d3d12.dll.so"
  $srcdir/$pkgname-64-build/tools/winebuild/winebuild --builtin d3d12.dll
  cp d3d12.dll "$pkgdir/usr/lib32/wine/d3d12.dll"


  msg2 "Packaging Wine-64..."
  cd "$srcdir/$pkgname-64-build"
  make prefix="$pkgdir/usr" \
    libdir="$pkgdir/usr/lib" \
    dlldir="$pkgdir/usr/lib/wine" install

  msg2 "Packaging DXVK-64..."
  cd "$srcdir/dxvk-64-build/bin"
  rm -f "$pkgdir/usr/lib/wine/dxgi.dll.so"
  for dll in d3d9 d3d10core d3d11 dxgi dxvk_config; do
    rm -f "$pkgdir/usr/lib/wine/$dll.dll"
    $srcdir/$pkgname-64-build/tools/winebuild/winebuild --builtin $dll.dll
    cp $dll.dll "$pkgdir/usr/lib/wine/$dll.dll"
  done

  msg2 "Packaging VKD3D-64..."
  cd "$srcdir/vkd3d-64-build/bin"
  rm -f "$pkgdir/usr/lib/wine/d3d12.dll.so"
  $srcdir/$pkgname-64-build/tools/winebuild/winebuild --builtin d3d12.dll
  cp d3d12.dll "$pkgdir/usr/lib/wine/d3d12.dll"


  # Font aliasing settings for Win32 applications
  install -d "$pkgdir"/etc/fonts/conf.{avail,d}
  install -m644 "$srcdir/30-win32-aliases.conf" "$pkgdir/etc/fonts/conf.avail"
  ln -s ../conf.avail/30-win32-aliases.conf "$pkgdir/etc/fonts/conf.d/30-win32-aliases.conf"
  install -Dm 644 "$srcdir/wine-binfmt.conf" "$pkgdir/usr/lib/binfmt.d/wine.conf"

  i686-w64-mingw32-strip --strip-unneeded "$pkgdir"/usr/lib32/wine/*.dll
  x86_64-w64-mingw32-strip --strip-unneeded "$pkgdir"/usr/lib/wine/*.dll
}

# vim:set ts=8 sts=2 sw=2 et:
