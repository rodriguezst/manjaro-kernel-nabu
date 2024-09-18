# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux61-nabu
pkgver=6.1.111
pkgrel=1
_kernelname=-MANJARO-NABU
_basekernel=6.1
_srcname="linux-${pkgver/%.0/}"
_newversion=false
_stopbuild=false     # Will also stop if ${_newversion} is true
_dtbfile='qcom/sm8150-xiaomi-nabu-maverick.dtb'
_desc="AArch64 multi-platform"
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc')
options=('!strip')
source=( "http://www.kernel.org/pub/linux/kernel/v6.x/${_srcname}.tar.xz"
         '0001-add-xiaomi-keyboard-support.patch'
         '0002-add-xiaomi-pad5-support-and-pm8150b-tcpm-support.patch'
         '0003-add-wifi.patch'
         '0004-fix-drm-probe-failures.patch'
         '0005-qcom-rpmhpd-Use-highest-corner-until-sync_state.patch'
         '0006-add-backlight-ktz8866.patch'
         '0007-set-up-runtime-pm-to-gdsc.patch'
         '0008-add-nt36523-panel-driver.patch'
         '0009-add-gpu-patches-form-map220v.patch'
         '0010-add-gpu-nodes-for-nabu.patch'
         '0011-add-bluetooth-nodes-for-nabu.patch'
         '0012-enable-type-c-dual-role-switch.patch'
         '0013-add-qcom-pmic-revid-driver.patch'
         '0014-update-rtc-driver-save-time-to-pm8150-sdam.patch'
         '0015-add-fg-and-charger-drivers-for-nabu.patch'
         '0016-add-minimal-dts-for-nabu.patch'
         '0017-NABU-add-support-for-nt36523-touchscreen.patch'
         '0018-NABU-add-additional-cpu-frequency-for-Kryo-485-Prime.patch'
         '0019-NABU-add-sound-support.patch'
         '0020-NABU-add-vol-and-power-keys.patch'
         '0021-NABU-add-dma-nodes.patch'
         '0022-NABU-add-backlight-regulators.patch'
         '0023-NABU-change-the-path-of-the-Bluetooth-firmware-to-de.patch'
         '0024-NABU-set-i2c7-speed-to-1M.patch'
         '0025-NABU-Modify-the-loading-path-of-the-firmwares.patch'
         '0026-NABU-keyboad-Delete-unused-code-and-add-pm-support.patch'
         '0027-input-nt36xxx-Enable-pen-support.patch'
         '0028-drm-Add-drm-notifier-support.patch'
         '0029-drm-dsi-emit-panel-turn-on-off-signal-to-touchscreen.patch'
         '0030-TS-Add-the-handler-to-accept-the-notifier-from-DRM.patch'
         '0031-PANEL-BACKLIGHT-update-nt36523-driver-and-ktz8866-dr.patch'
         '0032-DRM-fix-drm-suspend-resume.patch'
         '0033-DEBUG-update-debug-dts.patch'
         '0034-Charger-update-pm8150b-driver.patch'
         '0035-charger-add-charge-pump-ln8000-driver.patch'
         '0036-removed-a-log-print-because-it-printed-too-much.patch'
         '0037-USBPD-update-typec-pdhpy-driver.patch'
         '0038-USBPD-trick-Xiaomi-charger-to-supporting-PPS.patch'
         '0039-charge-add-fast-charge-manager-driver.patch'
         '0040-charge-add-dts-configs-for-fast-charge.patch'
         '0041-NABU-add-cover-detect.patch'
         '0042-dsi-fix-display-sync-problem-from-map220v.patch'
         '0043-charge-support-standard-pps-charges.patch'
         'config' 
         'linux.preset'
         '60-linux.hook'
         '90-linux.hook'
         'uki.conf'
         'cmdline' )
sha256sums=('c47298fa1d410bc5dcfb0662bc2cdbe86f5b0d12a1baac297e1ded7b6722edb0'
            '1c98d0f03512828049513081d19d815f019ae79b35c175124d59ffd9efe83887'
            'b6e4d77c59e5a9eba59cc8a9d38fc67e7171b857cf57bf7a510bb1f688db0bc7'
            '5955112feda47fd0fe3352d33284a6636d7d94eef93315e203a495da6a472e6e'
            '4fd988a8299e29650bf5716c3b18a1364545f898ab27c9425705caafaf607a67'
            '8084793fbb5a4390cab0299f54216232336475d131f3add3d8164b46788cc745'
            'c99cc7484f4a7274fd29780d51df8dc129d8411abeeb41e896eb97a6d3b12313'
            '69482e58ea21ac6efed53d69931a2f85162ef79c35e4b2cbb7ab9d0783f8d841'
            'bc7b745a4617700fe05e6d37b779903a54561bc4266e5bc525c05c5f39a866bc'
            'a29664c3ef10aaf5b0ea0f9bd77277c8eab844355c3a1a0fcea45fb003e5c229'
            'c2b630ee9f72bbebf7f9614a4f1e8604938f3d06640bf115da3efaff7f006557'
            '610390ce0f0d3c5efc95ad3844a08dcbe98610ede36e7d00c134c85fc10c7aab'
            '239d61968fb2ad165660407dd13ae39ef0b1af18a1afe4293e1e856552299778'
            'd7462343f722c83f3efcaaf85889ade239e189c294ef3eee163ab108f22c517c'
            'ef4cc0d256bed54c5cca4d4a8802d7dba3096062cb906e9f2f4d537a7147c1de'
            'fa08b934d18d1dfbc99ebe63b43ae4534330c63369a40acc8134638cca575da8'
            'cc7b027c7dfb5c139288d1ec62255c82ee345d4b2f1a5bc1c82e8fb24a27bdaa'
            'e5d92b9b83d6c540292b9fca463bac0242289480bdbf982d0b0d4e13cade5145'
            '1dec4135d00eabdf50fc7cd8fba6e6fe8b7555a9f980e1e702d5db5b632d2937'
            '6cb2e981c7aa711a80346b9c8fc4b45a32ab567bb17870179c66678a83c669f0'
            'f433a2db9cc20b59884355601607729faa7dd9d9105a804f2878f625caa1d04e'
            'bdd6ec7e1f86daf7d9175a263493898b87d0f11abdc4f3421b8df749ab5d7477'
            '7d613ad407813e931cfbebde90242e4e17b57aba6d4056764335bdca85bbbd5f'
            'e79cf1026c2bbe76c347a459931dfe400fe8186cd9c5aba1f4bbd0f3b17a1bb7'
            'fd16ba6f92440a4a2e2f7bd796b989fd51e9f7ff92c81b8ea82e96c6a9a78408'
            '38d5d5cda2b2f079eef0db0af8a4e298024daf060c14d159b7fc0fb5b83230d3'
            '59a902e0ae38e31661f9a48d625a9f9cfaca480a697238e149a066684b308d4d'
            'faab9285be794e5bfe741fb17e638a7256e65205973b769fa8d5edf58832e73f'
            '692962abc5e1699760b3a62752921fba45c3ba17ac5858b65e57ebe11fd0ba1b'
            '90418bee412f405d3a44c441f5c374152e80bd976fc08b6efb30bbe64ecc6dda'
            'baad478a8055dad1e33fd57673adf38790f984fe9402c88a419c82249c399617'
            '398f497d68c733557d72c0b91826a5660e11991bb18a9c3a6e59456185d8cf5a'
            '8a54b386d63ad5530219551a34bdd7b09269cb961ebbd04c9f32572d8b6a9a6e'
            'a9c1894287440c628c5708652864ceeefc916a28fe88de66eb0f2f37d92288cc'
            '2a76c2043e643567fe77f7a02effec9c615936581362f873aa4f1f66d29a5e3c'
            'e6c35dcc3f01c9e0955089a1257f6eda7a77dd1c6c792b49ec8947ed71d7b84c'
            '5cb44846f06b8d130499e818f227731c5870f28ccb6ae6dce2180dbb76790d64'
            '57e0229d981a949dbe4bb372e901a8b04528ce49584a186b4e12528138988789'
            '7db983f4a62419b56995ddb52104b7d909dedf5e85c3aad6c25c277d5fb52f6b'
            '0deee1c40afe0a7b4aafc546c1441fc439bde5813428bbf5aef631f6a2623e9b'
            '3f0f2566e9bdc027f1693d97b3b4065677096336262ef00f23f7bb012f686442'
            'b72b045d5cbd0b57f06def99748e9448f3b9bfa1fd0e8f8cb135d675dc54f14f'
            '2430508b923681685e987c1157697774e9f49ed6c6ca4ef6dd1546c653c8e5cb'
            '194eca66b5078a93684c94f351b0f330652eacf4e2d073c3f41bf6779b4ad01d'
            '115f587b01454c45a998514da08343209d023664d2e8289481cbd09cdf320cd9'
            'ab4e207d675f8ce4eb2be2c291d4858e2172ed2e31cb11ad18c0ad8b3318b6d0'
            'ae2e95db94ef7176207c690224169594d49445e04249d2499e9d2fbc117a0b21'
            '2c8a3715103d55947a96dd074efe6d5439bef2d4fecc15f5b3d268e2033abbd5'
            '2d87c68d02f14ce14de548d2d9d79dcca34fa276ee535cad6da78584531baae1'
            '4c06efd0966046827c7bc0fea11a9e5e298bd199cd4bdfe141795a3b62799cb9')

prepare() {
  cd "${_srcname}"

  local src
  for src in "${source[@]}"; do
      src="${src%%::*}"
      src="${src##*/}"
      [[ $src = *.patch ]] || continue
      msg2 "Applying patch: $src..."
      patch -Np1 < "../$src" # || true
  done

  # Apply our kernel configuration
  cat "${srcdir}/config" > .config

  # Add pkgrel to extraversion
  sed -ri "s|^(EXTRAVERSION =)(.*)|\1 \2-${pkgrel}|" Makefile

  # Don't run depmod on "make install", we'll do that ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh
}

build() {
  cd "${_srcname}"

  # Get the kernel version
  if [[ "${_newversion}" = false ]]; then
    make olddefconfig
    make prepare
  fi

  # Configure the kernel; adjust the line below to your choice
  # or simply manually edit the ".config" file
  if [[ "${_newversion}" = true ]]; then
    make oldconfig     # Using old config from previous kernel version
  fi
  #make menuconfig   # CLI menu for configuration
  #make nconfig       # New CLI menu for configuration
  #make xconfig       # X-based configuration

  # Stash the configuration (use with new major kernel version)
  if [[ "${_newversion}" = true ]]; then
    cp ./.config /var/tmp/${pkgbase}.config
    cp ./.config "${srcdir}/config"
  fi

  # Stop here, which is useful to configure the kernel
  if [[ "${_newversion}" = true || "${_stopbuild}" = true ]]; then
    msg "Stopping build"
    return 1
  fi

  # Enable to create an all-inclusive build
  #yes "" | make config

  # Build the kernel and the modules
  unset LDFLAGS
  make ${MAKEFLAGS} Image.gz modules dtbs
}

_package() {
  pkgdesc="The Linux ${_basekernel} Kernel and modules - ${_desc}"
  depends=('coreutils' 'kmod' 'initramfs' 'systemd-ukify')
  optdepends=('crda: to set the correct wireless channels of your country'
              'linux-firmware: additional firmware')
  provides=("linux=${pkgver}")
  conflicts=('linux61')
  backup=("etc/mkinitcpio.d/${pkgbase}.preset")
  install=${pkgname}.install

  cd "${_srcname}"
  
  KARCH=arm64

  # get kernel version
  _kernver="$(make kernelrelease)"

  mkdir -p "${pkgdir}"/{boot,usr/lib/modules}
  make INSTALL_MOD_PATH="${pkgdir}/usr" INSTALL_MOD_STRIP=1 modules_install

  # install kernel and dtb
  cp arch/$KARCH/boot/Image "${pkgdir}/boot/vmlinux-${_kernver}"
  cp arch/$KARCH/boot/Image.gz "${pkgdir}/boot/vmlinuz-${_kernver}"
  cp arch/$KARCH/boot/dts/${_dtbfile} "${pkgdir}/boot/dtb-${_kernver}"

  # used by mkinitcpio to name the kernel
  echo "${_kernver}" | install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_kernver}/pkgbase"
  echo "${_basekernel}-${CARCH}" | install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_kernver}/kernelbase"

  # add kernel version
  echo "${pkgver}-${pkgrel}-MANJARO-NABU aarch64" > "${pkgdir}/boot/${pkgbase}-${CARCH}.kver"

  # make room for external modules
  local _extramodules="extramodules-${_basekernel}${_kernelname:--MANJARO-NABU}"
  ln -s "../${_extramodules}" "${pkgdir}/usr/lib/modules/${_kernver}/extramodules"

  # add real version for building modules and running depmod from hook
  echo "${_kernver}" |
    install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_extramodules}/version"

  # remove build and source links
  rm "${pkgdir}"/usr/lib/modules/${_kernver}/{source,build}

  # now we call depmod...
  #depmod -b "${pkgdir}/usr" -F System.map "${_kernver}"
  #depmod -b "${pkgdir}" -F System.map "${_kernver}"

  # sed expression for following substitutions
  local _subst="
    s|%PKGBASE%|${pkgbase}|g
    s|%KERNVER%|${_kernver}|g
    s|%EXTRAMODULES%|${_extramodules}|g
  "
  # install mkinitcpio preset file
  sed "${_subst}" "${srcdir}/linux.preset" |
    install -Dm644 /dev/stdin "${pkgdir}/etc/mkinitcpio.d/${pkgbase}.preset"

  # install pacman hooks
  sed "${_subst}" ../60-linux.hook |
    install -Dm644 /dev/stdin "${pkgdir}/usr/share/libalpm/hooks/60-${pkgbase}.hook"
  sed "${_subst}" ../90-linux.hook |
    install -Dm644 /dev/stdin "${pkgdir}/usr/share/libalpm/hooks/90-${pkgbase}.hook"
  
  # install uki.conf file and cmdline
  sed "${_subst}" "${srcdir}/uki.conf" |
    install -Dm644 /dev/stdin "${pkgdir}/etc/kernel/uki.conf"
  install -Dm644 "${srcdir}/cmdline" "${pkgdir}/etc/kernel/cmdline"
}

_package-headers() {
  pkgdesc="Header files and scripts for building modules for linux ${_basekernel} kernel - ${_desc}"
  provides=("linux-headers=${pkgver}")

  cd "${_srcname}"
  local _builddir="${pkgdir}/usr/lib/modules/${_kernver}/build"

  install -Dt "${_builddir}" -m644 Makefile .config Module.symvers
  install -Dt "${_builddir}/kernel" -m644 kernel/Makefile
  install -Dt "${_builddir}" -m644 vmlinux

  mkdir "${_builddir}/.tmp_versions"

  cp -t "${_builddir}" -a include scripts

  install -Dt "${_builddir}/arch/${KARCH}" -m644 arch/${KARCH}/Makefile
  install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 arch/${KARCH}/kernel/asm-offsets.s

  cp -t "${_builddir}/arch/${KARCH}" -a arch/${KARCH}/include
  mkdir -p "${_builddir}/arch/arm"
  cp -t "${_builddir}/arch/arm" -a arch/arm/include

  install -Dt "${_builddir}/drivers/md" -m644 drivers/md/*.h
  install -Dt "${_builddir}/net/mac80211" -m644 net/mac80211/*.h

  # http://bugs.archlinux.org/task/13146
  install -Dt "${_builddir}/drivers/media/i2c" -m644 drivers/media/i2c/msp3400-driver.h

  # http://bugs.archlinux.org/task/20402
  install -Dt "${_builddir}/drivers/media/usb/dvb-usb" -m644 drivers/media/usb/dvb-usb/*.h
  install -Dt "${_builddir}/drivers/media/dvb-frontends" -m644 drivers/media/dvb-frontends/*.h
  install -Dt "${_builddir}/drivers/media/tuners" -m644 drivers/media/tuners/*.h
  
  # https://bugs.archlinux.org/task/71392
  install -Dt "${_builddir}/drivers/iio/common/hid-sensors" -m644 drivers/iio/common/hid-sensors/*.h

  # add xfs and shmem for aufs building
  mkdir -p "${_builddir}"/{fs/xfs,mm}

  # copy in Kconfig files
  find . -name Kconfig\* -exec install -Dm644 {} "${_builddir}/{}" \;

  # remove unneeded architectures
  local _arch
  for _arch in "${_builddir}"/arch/*/; do
    [[ ${_arch} == */${KARCH}/ || ${_arch} == */arm/ ]] && continue
    rm -r "${_arch}"
  done

  # remove documentation files
  rm -r "${_builddir}/Documentation"

  # remove now broken symlinks
  find -L "${_builddir}" -type l -printf 'Removing %P\n' -delete

  # strip scripts directory
  local file
  while read -rd '' file; do
    case "$(file -bi "$file")" in
      application/x-sharedlib\;*)      # Libraries (.so)
        strip $STRIP_SHARED "$file" ;;
      application/x-archive\;*)        # Libraries (.a)
        strip $STRIP_STATIC "$file" ;;
      application/x-executable\;*)     # Binaries
        strip $STRIP_BINARIES "$file" ;;
      application/x-pie-executable\;*) # Relocatable binaries
        strip $STRIP_SHARED "$file" ;;
    esac
  done < <(find "${_builddir}" -type f -perm -u+x ! -name vmlinux -print0 2>/dev/null)
  ${CROSS_COMPILE}strip $STRIP_STATIC "${_builddir}/vmlinux"
  
  # remove unwanted files
  find ${_builddir} -name '*.orig' -delete
}

pkgname=("${pkgbase}" "${pkgbase}-headers")
for _p in ${pkgname[@]}; do
  eval "package_${_p}() {
    _package${_p#${pkgbase}}
  }"
done
