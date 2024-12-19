# Maintainer: Leonid Maksymchuk <leonmaxx@gmail.com>
# Contributor: Felix Yan <felixonmars@archlinux.org>
# Contributor: Sven-Hendrik Haase <sh@lutzhaase.com>
# Contributor: Jan "heftig" Steffens <jan.steffens@gmail.com>
# Contributor: Eduardo Romero <eduardo@archlinux.org>
# Contributor: Giovanni Scafora <giovanni@archlinux.org>

pkgname=('wine-proton' 'wine-proton-nvapi')
pkgbase=wine-proton
pkgver=9.0
pkgrel=4

_winever=$pkgver
_pkgbasever=${pkgver/rc/-rc}

_wine_commit=117daf8d508860a8552f59ebdd6ee16361431136
_dxvk_commit=d96fa54080320e9b63227e76124ffa50a927ced2
_vkd3d_commit=4fd7d3ab3d351de4ad50576b1a9df0a45a4a7c74
_nvapi_commit=afb59a8e841b0ad561250327eb6a370b925c5f03

source=("$pkgbase::git+https://github.com/ValveSoftware/wine.git#commit=$_wine_commit"
        "dxvk::git+https://github.com/doitsujin/dxvk.git#commit=$_dxvk_commit"
        "vkd3d-proton::git+https://github.com/HansKristian-Work/vkd3d-proton.git#commit=$_vkd3d_commit"
        "dxvk-nvapi::git+https://github.com/jp7677/dxvk-nvapi.git#commit=$_nvapi_commit"
        30-win32-aliases.conf
        wine-binfmt.conf
        wine.inf-Remove-Steam-registry-entries.patch
        ntdll-Remove-trampolines-for-lsteamclient.patch
        wineboot-Updating-prefix.patch
        dxvk-nvapi-Fix-missing-includes.patch
        winevulkan-FSHack-AMD-FSRv1.patch
        winex11.drv-Ensure-initialized-thread-data.patch
        widl-Ignore-option-pthread.patch
        wrc-Ignore-option-pthread.patch
        makefile-Proton-branding.patch)
sha512sums=('806162115faf68360385969a965ee922eb05e1cc1aa9695a16cb62cf42e9363ef23f6f77230d92d1cccd5aea462b7a899d2410a635f157f9c1e782211747d24f'
            'ae9ed7109c6d3fe132171219fad94ddf8ab0e17e6f4335cf5d854aa7dfedc688e5c386dfb8372614c3d311f49ae454413d7a0f4cdcacc1da2e77f020e9e7affe'
            '0f19ee52d09df41d788307d4ba638059e231554bc94bfc418d55ae6fd5e32c80f4c6c4fc42e4c3027657ac7d9effc36954746b0ab1a9c0220eb58487a9f8f8f1'
            'ca6f3c743bec50c94ac90653ad452891c8d4c34bd205ae5ea281c0f4a986cc379f21df80d631347a6c3c32b9b577afa03be781c4ec6e95a145c28ef493dfc67a'
            '6e54ece7ec7022b3c9d94ad64bdf1017338da16c618966e8baf398e6f18f80f7b0576edf1d1da47ed77b96d577e4cbb2bb0156b0b11c183a0accf22654b0a2bb'
            'bdde7ae015d8a98ba55e84b86dc05aca1d4f8de85be7e4bd6187054bfe4ac83b5a20538945b63fb073caab78022141e9545685e4e3698c97ff173cf30859e285'
            'b927e699cb933a1e00de140bd94e29765ff47da4e690f56b8d16c8f5927fa28b8dde3af8c89e081bf406ad50c30baa0fcc902b124c402ea60be4d627d9ff9c15'
            'bbe919a92c181a567db6f705840bfa52526fa3f4df2245d97caa0dfe403c0b3d04865a2e5bf783d361873b8deb70b4854cf80dc7ee69c2e534a3213120a84a51'
            '9ceab5380d1d11477aaa75107a3534fd554026d689c1d6bdc225bdf4aac24b72d030f7dcb95cf5c4701d58c721918a60e1c347255526f681f1475da85e74c7d9'
            '05826f7f3f29ce6da08d0c632a17e9268fee0ba484e85f0d41cdbaac9e2a6a09e23ebc29ffb3d1b6b3a8fe89db16013c8f161ad22121fb6ae07c82c9f681746c'
            '6f58bfcd9b43f61b70416ceb05a32e58fef0f36f166f86311be6673e54a32419b570bad58654c77a71be0ac5eaf999a8ccdee8e89087cb4c97de0e7c6078717c'
            'f7006988ec4a6fb5caba861d751a0d50dfcec9fccfa436ecf3c093c4f73ef90dca6b9cdcc20082ee1c956eb0677a44499639a70f96d754723fd60b48a2ae0289'
            'd5db3b4ef07c41e740d0ca384e1d088748b7d090ae3cd96dfd8b3f6b5d55d9c7952de30d12a5a5c4680cbb995a7ff66dd6a0b7246a7f3021c4aa72a7ee9adde5'
            '996ef9b242787cfa0ca8aace46f35828246b5d6dfcaf8f0643454f7afe0db807364d74033d5d3ac562b8ad8e564c2aaae512161ed3bbcb01580b1b53d117aba5'
            'e3a14db8a13edfe7f26d7b44df4b095a2895792a37bb169a30463e1cc1315bd87009a0438a8ca14f7d53c339fa55d10368cf7a201a673fb533027ce265cbd6b3')

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
  sane                  meson
  libgphoto2
  gsm
  ffmpeg
  samba
  opencl-headers
)

optdepends=(
  wine-proton-nvapi
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

prepare() {
  # Revert unneeded Wine-Proton patches
  pushd $pkgbase
    # wine.inf: Don't use DDE for winebrowser by default. 
    # git revert -n 2729328ac86bf14706006b0de54431f753a0c14c

    # wine.inf: Associate the steam protocol with steam.exe.
    # git revert -n bc633e8c15139e66ccf7327e853b87ff9030fda0

    # fixup, user32: Use new export to set LD_PRELOAD
    #git revert -n 97f962cd469ee9b9b68d32e79849bf94cfe15581


    # ntdll: Add +microsecs channel for precise timestamps.
    #git revert -n c9dd827b315ba9394020ec65c161096ce3e968e8

    # ntdll: Write crash log when we are missing a module
    #git revert -n ea71c1178d9a3827c6cf83bca8a124870174b3b2

    # winebrowser: Restore original LD_LIBRARY_PATH before calling to system
    #git revert -n a1dde27690950aeb4728f0f3783b4d04d608b5c0

    # ntdll: Export a function to set a Unix environment variable.
    #git revert -n bf6233be8f8b7c2e729daa91160dd41fbbb3c64e


    # dotnetfx35.exe: Add stub program.
    git revert -n 5bfb96e0cbb1b75a94386d7239be6e5379e0057d


    # Instead of this revert block we'll revert by using patch
    # wineboot: Generate better DigitalProductId.
    # git revert -n 80d7c0c041636e900589e8ae41c5fdd3a0470b29

    # explorer: Start tabtip process before the main loop.
    # git revert -n 94ec0e4c7946445bfdc7df5405257e6f0a269876

    # HACK: wineboot: Don't show "updating prefix" window
    # git revert -n 9a2d483b7fca2b92f3a5cf02a12b804a50edb87b


    # wine.inf: Associate the "steam" protocol with winebrowser.
    # git revert -n 0e40743b6d409bc2b669eac7ad6ce379be22fc17

    # wine.inf: Don't show crash dialog by default
    git revert -n 486bcb9740dc1735ccf1335075bcf7d3b3698e00

    # winex11: Fill WM_CLASS based on Steam appid
    git revert -n 1c42b167834b5b917f3ab1f4ae12110047529402

    # HACK: Don't build winemenubuilder
    git revert -n 5e25ae85bf50673ec63a8437a7e77fe13dba97aa

    # HACK: mshtml: Don't install wine-gecko on prefix creation
    git revert -n 903a5167a20f744b58b1e94bd111a3892b42653d

    # Font related
    git revert -n fe7901be6de96a7572fff977dd34584d96b5ec29
    git revert -n ba3c43eb34cd10b7cf1c8e76319a2eef86f31f8b
    git revert -n bf82f60052320c5c4396fa81a952fc243e03dd79
    git revert -n 9dbcb3b5f845e5f31093677804b0eada1bdc25b8
    git revert -n a7db676a16ba5006467bec9c774bb985cdba8e27
    git revert -n aa91d771e84b737c95a7d23325040341bd1eeba7
    git revert -n ab960656bc6882ea73d4b713466824957d6d4331
    #git revert -n 7b5266d81e153d0357122047386418d255d08650


    # HACK: shell32: Preserve duplicated Documents/Stuff directories
    git revert -n 762a8d7bd8e1027eae7222c23253726a08af9964

    # HACK: shell32: Never create links to the user's home dirs
    git revert -n c3fadbbbeadb8fd49fb2edfd2ee4ca37a46cfbff


    # HACK: advapi32: Use steamuser as Wine username
    git revert -n 207d17259d8aed05d3b69d242c2bc68b02aec378

    # HACK: steam: kernelbase: Substitute the current pid for the Steam
    git revert -n 1519ba09129800fa81957d0986e2017fe7243ba9


    #  HACK: proton: ntdll: Strip gameoverlayrenderer.so from LD_PRELOAD before executing explorer.exe.
    #git revert -n 901e614e8f3d8913e7f75ccd6cdbabbd0502c53f

    # HACK: proton: ntdll: Export a function to set a Unix environment variable
    #git revert -n bf6233be8f8b7c2e729daa91160dd41fbbb3c64e

    # HACK: steam: ntdll: Patch entry points with jumps.
    #git revert -n b25e4e6251675172321a561e1398874fd2dd0126

    # ntdll: Properly parse UDF instruction in ARM.
    #git revert -n f5a95366d46ad3067e0f0316cdb83b4ed344de3d

    # ntdll: Implement __fastfail().
    #git revert -n b3cfa8ce5544f1a10b2a9034e993dcf944478501

    # HACK: steam: ntdll: Setup steamclient trampolines to lsteamclient.
    #git revert -n 6fa5dfc0bd079bd18e1f457b1e6ae0bcf7eb383d


    patch -Rp1 < ../wineboot-Updating-prefix.patch
    patch -Np1 < ../ntdll-Remove-trampolines-for-lsteamclient.patch

    # patch -Np1 < ../winex11.drv-Ensure-initialized-thread-data.patch

    patch -Np1 < ../wine.inf-Remove-Steam-registry-entries.patch
    patch -Np1 < ../widl-Ignore-option-pthread.patch
    patch -Np1 < ../wrc-Ignore-option-pthread.patch

    autoreconf
    tools/make_requests
    tools/make_specfiles
    dlls/winevulkan/make_vulkan
  popd

  pushd dxvk
    git submodule update --init --recursive
  popd

  pushd vkd3d-proton
    git submodule update --init --recursive
  popd

  pushd dxvk-nvapi
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
  export CXXFLAGS="${CXXFLAGS/-Wp,-D_GLIBCXX_ASSERTIONS/}"

  # Disable stack clash and control flow protection
  export CFLAGS="${CFLAGS/-fstack-clash-protection/}"
  export CFLAGS="${CFLAGS/-fcf-protection/}"
  export CXXFLAGS="${CXXFLAGS/-fstack-clash-protection/}"
  export CXXFLAGS="${CXXFLAGS/-fcf-protection/}"

  sed 's|OpenCL/opencl.h|CL/opencl.h|g' -i $pkgbase/configure*

  # Get rid of old build dirs
  rm -rf $pkgbase-{32,64}-build
  mkdir $pkgbase-{32,64}-build

  rm -rf dxvk-{32,64}-build
  mkdir dxvk-{32,64}-build

  rm -rf vkd3d-{32,64}-build
  mkdir vkd3d-{32,64}-build

  rm -rf dxvk-nvapi-{32,64}-build
  mkdir dxvk-nvapi-{32,64}-build
}

build() {
  cd "$srcdir"

  msg2 "Building Wine-64..."

  cd "$srcdir/$pkgbase-64-build"
  ../$pkgbase/configure \
    --prefix=/usr \
    --libdir=/usr/lib \
    --with-x \
    --with-gstreamer \
    --enable-win64 \
    --disable-tests

  patch -p1 < ../makefile-Proton-branding.patch
  make

  msg2 "Building Wine-32..."

  export PKG_CONFIG_PATH="/usr/lib32/pkgconfig:/usr/share/pkgconfig"
  cd "$srcdir/$pkgbase-32-build"
  ../$pkgbase/configure \
    --prefix=/usr \
    --with-x \
    --with-gstreamer \
    --libdir=/usr/lib32 \
    --with-wine64="$srcdir/$pkgbase-64-build" \
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

  meson --cross-file build-win64.txt --buildtype release --prefix "$srcdir/dxvk-64-build" build.w64
  ninja -C build.w64 install

  msg2 "Building VKD3D-32..."

  cd "$srcdir/vkd3d-proton"
  meson --cross-file build-win32.txt --buildtype release --prefix "$srcdir/vkd3d-32-build" build.w32
  ninja -C build.w32 install

  msg2 "Building VKD3D-64..."

  meson --cross-file build-win64.txt --buildtype release --prefix "$srcdir/vkd3d-64-build" build.w64
  ninja -C build.w64 install

  msg2 "Building DXVK-NVAPI-32..."

  cd "$srcdir/dxvk-nvapi"
  meson --cross-file build-win32.txt --buildtype release --prefix "$srcdir/dxvk-nvapi-32-build" build.w32
  ninja -C build.w32 install

  msg2 "Building DXVK-NVAPI-64..."

  meson --cross-file build-win64.txt --buildtype release --prefix "$srcdir/dxvk-nvapi-64-build" build.w64
  ninja -C build.w64 install
}


package_wine-proton() {
  install=wine.install

  msg2 "Packaging Wine-32..."
  cd "$srcdir/$pkgbase-32-build"

  make prefix="$pkgdir/usr" \
    libdir="$pkgdir/usr/lib32" \
    dlldir="$pkgdir/usr/lib32/wine" install

  msg2 "Packaging DXVK-32..."
  cd "$srcdir/dxvk-32-build/bin"
  for dll in d3d8 d3d9 d3d10core d3d11 dxgi; do
    rm -f "$pkgdir/usr/lib32/wine/i386-unix/$dll.dll.so"
    rm -f "$pkgdir/usr/lib32/wine/i386-windows/$dll.dll"
    $srcdir/$pkgbase-64-build/tools/winebuild/winebuild --builtin $dll.dll
    cp $dll.dll "$pkgdir/usr/lib32/wine/i386-windows/$dll.dll"
  done

  msg2 "Packaging VKD3D-32..."
  cd "$srcdir/vkd3d-32-build/bin"
  for dll in d3d12core d3d12; do
    rm -f "$pkgdir/usr/lib32/wine/i386-unix/$dll.dll.so"
    rm -f "$pkgdir/usr/lib32/wine/i386-windows/$dll.dll"
    $srcdir/$pkgbase-64-build/tools/winebuild/winebuild --builtin $dll.dll
    cp $dll.dll "$pkgdir/usr/lib32/wine/i386-windows/$dll.dll"
  done


  msg2 "Packaging Wine-64..."
  cd "$srcdir/$pkgbase-64-build"
  make prefix="$pkgdir/usr" \
    libdir="$pkgdir/usr/lib" \
    dlldir="$pkgdir/usr/lib/wine" install

  msg2 "Packaging DXVK-64..."
  cd "$srcdir/dxvk-64-build/bin"
  for dll in d3d8 d3d9 d3d10core d3d11 dxgi; do
    rm -f "$pkgdir/usr/lib/wine/x86_64-unix/$dll.dll.so"
    rm -f "$pkgdir/usr/lib/wine/x86_64-windows/$dll.dll"
    $srcdir/$pkgbase-64-build/tools/winebuild/winebuild --builtin $dll.dll
    cp $dll.dll "$pkgdir/usr/lib/wine/x86_64-windows/$dll.dll"
  done

  msg2 "Packaging VKD3D-64..."
  cd "$srcdir/vkd3d-64-build/bin"
  for dll in d3d12core d3d12; do
    rm -f "$pkgdir/usr/lib/wine/x86_64-unix/$dll.dll.so"
    rm -f "$pkgdir/usr/lib/wine/x86_64-windows/$dll.dll"
    $srcdir/$pkgbase-64-build/tools/winebuild/winebuild --builtin $dll.dll
    cp $dll.dll "$pkgdir/usr/lib/wine/x86_64-windows/$dll.dll"
  done

  rm -f "$pkgdir/usr/lib32/wine/i386-unix/nvapi.dll.so"
  rm -f "$pkgdir/usr/lib32/wine/i386-windows/nvapi.dll"
  rm -f "$pkgdir/usr/lib/wine/x86_64-unix/nvapi64.dll.so"
  rm -f "$pkgdir/usr/lib/wine/x86_64-windows/nvapi64.dll"
  rm -f "$pkgdir/usr/lib/wine/x86_64-unix/nvofapi64.dll.so"
  rm -f "$pkgdir/usr/lib/wine/x86_64-windows/nvofapi64.dll"

  # Font aliasing settings for Win32 applications
  install -d "$pkgdir"/etc/fonts/conf.{avail,d}
  install -m644 "$srcdir/30-win32-aliases.conf" "$pkgdir/etc/fonts/conf.avail"
  ln -s ../conf.avail/30-win32-aliases.conf "$pkgdir/etc/fonts/conf.d/30-win32-aliases.conf"
  install -Dm 644 "$srcdir/wine-binfmt.conf" "$pkgdir/usr/lib/binfmt.d/wine.conf"

  i686-w64-mingw32-strip --strip-unneeded "$pkgdir"/usr/lib32/wine/i386-windows/*.dll
  x86_64-w64-mingw32-strip --strip-unneeded "$pkgdir"/usr/lib/wine/x86_64-windows/*.dll
}

package_wine-proton-nvapi() {
  pkgdesc="NVAPI implementation on top of DXVK - Proton branch"
  depends=(wine-proton)
  optdepends=(nvidia-utils lib32-nvidia-utils)
  provides=()
  conflicts=()

  mkdir -p "$pkgdir/usr/lib32/wine/i386-windows"
  mkdir -p "$pkgdir/usr/lib/wine/x86_64-windows"

  msg2 "Packaging DXVK-NVAPI-32..."
  cd "$srcdir/dxvk-nvapi-32-build/bin"
  $srcdir/$pkgbase-64-build/tools/winebuild/winebuild --builtin nvapi.dll
  cp nvapi.dll "$pkgdir/usr/lib32/wine/i386-windows/nvapi.dll"

  msg2 "Packaging DXVK-NVAPI-64..."
  cd "$srcdir/dxvk-nvapi-64-build/bin"
  $srcdir/$pkgbase-64-build/tools/winebuild/winebuild --builtin nvapi64.dll
  cp nvapi64.dll "$pkgdir/usr/lib/wine/x86_64-windows/nvapi64.dll"
  $srcdir/$pkgbase-64-build/tools/winebuild/winebuild --builtin nvofapi64.dll
  cp nvofapi64.dll "$pkgdir/usr/lib/wine/x86_64-windows/nvofapi64.dll"

  i686-w64-mingw32-strip --strip-unneeded "$pkgdir"/usr/lib32/wine/i386-windows/nvapi.dll
  x86_64-w64-mingw32-strip --strip-unneeded "$pkgdir"/usr/lib/wine/x86_64-windows/nvapi64.dll
}

# vim:set ts=8 sts=2 sw=2 et:
