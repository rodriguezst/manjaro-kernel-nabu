# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux61-nabu
pkgver=6.1.113
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
         '0044-ath-Disable-EEPROM-regulatory-restrictions-enforcing.patch'
         'config' 
         'linux.preset'
         '60-linux.hook'
         '90-linux.hook'
         'uki.conf'
         'cmdline' )
sha256sums=('54af1087192fcc5250a4251451fd614761859d3d964449dc02358e558c449e30'
            '5abd0e6e1cced6d39fb89261bcbf944dc9b909503f09bf990b760374b9a105d7'
            '409c64c780609c314feacaf7be63623736fcf00d2aab7fac554b1a8eaca44ff1'
            'd42cdd541095c01fd1b545aaf51c7684646956e08b7f3dc7d77a60ea18b3bb02'
            '818992b7c31fd4937f74fab116ba3b28e4f747d0fb8636a39a8b394a03f6c510'
            '948d2dc09dac1fad74677c7bffcbce69dba3855e09db1f5b1b0488f5c9b0215c'
            'b24a5299a37244677c8493017e93890af122417c03ab5bbe20cd63cead95f094'
            '38144ffa5ad4aebf2f8f1603fa26205283e02d19a511a39dfd313ed38109f56d'
            '648bab7cf19c53ce45ab80a58588ae67f93c9cab6b1e3115f03e12d46a3cd2d8'
            '442f57ca72ec161b6b26caaa756897aaff6d79ad6197d2e04075a4931fd5e383'
            '76397e61c0937d278d101731a8418ef494bef4560c1307b47090b5fa2e446516'
            'd246856227ac6e025c00049efa26a604ffb541db538b266eefa4227d4445cecf'
            '9a45263bf0674be147b38f2a21292dcde4f32e0d5f21c63657b7af41326d769c'
            '0e50f2bbf0223ccf93157df5bc51d460dae23ed4363efa8e4925acd270600bc1'
            '0af35131c74b1e1029ff842d0e780e1c795df4d8d3966670767ac1ef4aaef868'
            'a996373b6c990f682eadf8d74d6c20e159493ef068bb16a614e956553f40f047'
            '17c5d9848a4dfe4c4bca5a82216a50d27ce6b99fb05fbad468274fc991891302'
            '04accd386c3705af52b763f622e91a30bd76e37fead847eda7bd37cf0b8c8bfa'
            '009e17494088110bc3dcfaaed7c27b6e1eb96a9277c00daf1e9e0b0d5d58661b'
            '593a9f44c4a30fe59c6e853609f180fd2d9e7459a8bbd6dcb7e1cfcd55ef9a2e'
            'a9262919c591f1488d242a0409f4c37ad9bb2e722685cc273f9a2a728c57c9ce'
            '6557a5d3c69dee30651654d4025d6436f332cc03a401ef92d83982ab6e229b91'
            '6176f02b73de94e90aa4b420edc1ecdeb6493335275321eab06b7292ef7487b4'
            'ee1499e97a997e8ce5934dc5a14238ef90da6cdbc321e8c85a449044d356cda3'
            '208eb740ed6c44cbdbcb58d81d080753291ff793d931579e0ba12e8b9b67872a'
            '9c75ab40410c1cb9c4f6524245a5ec0e95c2041641acbb9d9546e7b3b7099d22'
            'dd652842c24ca6a57470d35d18e7aaed62ef4093b93b7e553a6678b52fb67e0f'
            'd36c68d8fcaa2a99d2b33f6f0286a1176710e4bfc9b868b2637cde9ab5da7d82'
            '2c556b37463e51f4f3ab97b494c8c777fcb4184a2f2c8f29dbd29ec1817cceaa'
            'dbee3e30b0f5a420b81fd1fd2b4a139d4ee03dc03929c594d78a60615bc9925e'
            'fd81dcaf7bac73687a7c0d1691c13b96073bfd076861e7d35628e918fff829c8'
            '86a0f6a0861293cbbccdc14d4d13c35023f1909a5c606f8ef6fffff672e4f5c9'
            'beee8b1ba224e2702fe9c6d9653ccb84396127a1c33776b86933d8070d8c4d6d'
            'ef3987e5e3b5ce23228b8abc84bc5078a7de6a0f54075eb8444106f149ac9843'
            'f6de3a67f6ae90242de837d008d9671ea790c8beeda6a7c309ba30ddacc6caf3'
            'c9f1e5a437d5e0cd74dc824a16ea38a9ddc98723e9bb1c4e560aeff217816f63'
            'cf71ce15f3246b00ceb13fd0fd6924ce655192e2cc134024e6b61a1b5f780978'
            'e4df0322a8dcc9e32faceddfe2ad9ab86193e059f5415151958ad16db9599d5e'
            '8b40ab52e2c9ba3f28fac982a6dc840516735871e96400db6f02d731aea39195'
            '2f3c032861945225f0af5ab123fa94de383161e53310923accdd78a27e60bf0a'
            '6814cb1f9a1df6c6d29699c8216108e3e473278947cc1465acb82da521208580'
            '1d6de29fc5ec2703be2955d914e360139abdb9add5d943d3210debc541c6d7cc'
            '57f3c129b92fcd0f109ac34fcf979eea22d3a36a163e0e4d7bd46fff9e4f86f4'
            'a757078021b92f856b0ea8a5e9dd5576f49dcde24fe6d27205b378a07c4c6110'
            'e9cdccd84319c496b6096c90bee25eb2da01f63ab8368268d11e21d9a05b874d'
            '3080798df01679f2c95e6c676e46ab7c12a8f5b11ec5ff4283464a7c123243a3'
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
