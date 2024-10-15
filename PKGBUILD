# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux61-nabu
pkgver=6.1.112
pkgrel=2
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
sha256sums=('8bd8de3562fb006653e550a934e66ed9f80b7576258a03e2caa2e3ce1c1f9f24'
            '9a7f391c1d5e218d087356207bb093d1dbd83eead4102364fd17be3bc6f960bc'
            'a9d7dacc1de6b58932dd20710106fea9f777ef523c8ea1f5377df2366967b419'
            '75003eb22c2ccb28fded04c6e3ff68bde3a3cbb18c2cadc488399c73f202b3e0'
            'ecc8b797d560b12e8e152517e97767237478289c38f683e40b86536f6d3ddb04'
            'd902792dff568021ce19311dbf9d3e2219386269205e91f0af090a7e1e505290'
            '98ac0ad94146d3d194477ad1d1d5a3df721bc6363aa8df2c0189e9bf50697085'
            '51244cdc01d7efdac05d61c255f25aa4444c7bfd4d1b46494562392a57b84fec'
            '85984eaafa814b86af4d36c619c5a39673f696ae3f2858bc2aa5234d2b97116b'
            '56e2575ffb466e3ed1ea5147441fa8483369ed63491576337a07de7e2c4d9a47'
            'af60c3b1693f2bf7c8099f2ea174cee475909365580b17622c965285bba86178'
            '861e94f42fd7edea90e18d16d0af69a1014c5538ae22e1cfffc02a5cb3063b4a'
            'ea08b329a1fc6bba363fd8c6e74ba0021346ac9f711b9845c1d4c1f27c9eb996'
            'def99ca1a2a86881b43c304a1046157ee75bc83b5ad777b9f23a08db5c156ce5'
            '44216aa6f5a1b4c2f11a848b63a3ce6ad3917fa6c11e560f1f2a93252cd867ef'
            '0b56080b56e5fd3fe34ab244f551087a7c65a1ffdb8b92061b44c8c3e34279d7'
            'feb1e627df20f4b0c42d55cfe8bb7182b494de26faa30a5cbaa75cbe5f046ba6'
            '0396abbe7a007f4bd2069b45392c93bd10647e8bbcedad77725c2b382479a2b2'
            '5e0e432b9cfff5c602ca51cb7405f16fb43779cc6c253d3356ddf4f80dc25aa4'
            '189f8909c03aad53f42a608c7d84ca74bb00c6d1590119d264ab47cc87d08e3c'
            '9dc5bd2bae0dd818f1b679b5d64db692c98b816fca74bb4293f3abab82ac63bd'
            '871c210d2db54faf41997c70cb65895dc1ff4bb0c6ff113f19e335955cee0c5d'
            'aa39952e5e298c809a71eb30b08188acd96554b25fcb7c68f0a8f28f1b9151c4'
            '2b2a5aca979f50c42b73673e29667ab295bc79bc5896c4cf4888cca1c01d7b4a'
            '3c1cf8e6eb3cf87a25333c88abf1a0784543d1bffd3051afa815466bad27ee53'
            '8857e691b76971385cfda6eceaf0f8fcc6644a1a5404d191348cac5972674e12'
            '4199a393f352e33a52ea756bda5e1b76a5cb2d1971d28e88472163fbb0f1e235'
            '51ecc388fdc12334cae8d2a8c4f88e1c9db1b0732ecd7bbc9979409051cc7afa'
            '6c906428155d84b4d78473a50ace434c2e38ef59cb6cf4c500c683f99bd3861a'
            'dfc830b9ae1cdf4d258e8f2308c7f3c5f62f2ed9dac3c6e00e7d6620b879c460'
            '41b44c4484a470eb242a941c5c381f82d09e2e9edc427cbe9019e49d9a8ba524'
            '222778b2fa285b8a93ccf927c7b2ded2498be7b7c1b08d2c194dc19e6c8959af'
            'f4ffb2ec7640bd289c1a0a23923edea42620edeea25f5b96e879cb4b7d1ec39d'
            'd8ba851593509c0eda63c9303a2dd404d6feb98ecf9505a866f93a59036d25a1'
            '0b177b7f62062014adccc1ad36a219599af158ec60743ff98c7d7fece8a76b59'
            '3eab242877e95ed6ff4e30d8658b159a5c94efaaecf2d8885c6ea54be8430329'
            '7f305f5732d8a697a52a14adf4ae41606e6d92a74ba0a7e4c960d4da131bdf25'
            '7983348f3e46aa44a3625238fdbcb32d6b13dacc449feb1c7d9e26bdb87f4e58'
            'd41fac70258e68482e2a2da460b4537efe4d5935ec89d7873cbd57bc34fad744'
            'f264252221407a8bb511cda17ce9f44a9296145eb7eec35fc630da6aa239f8ec'
            'fa1a8f3be326daf36a55fe5b4518c69824a6c7ee842b42664fd693edf293d6a9'
            'e573c399e174f4ef073c283f4a80c32acfe0069d39d71a74608b3b0d53656461'
            'd55c38edb8a48827da557070d4b6324b0eab884be7a41714e1f2a9e90a552a5f'
            '542de1a8d9edb4195474678c4a74a187f72cbd5541b039a64545e5de05316177'
            'd8b13f4329d5fe396aefd489328a6dbfaaee4bd78ff7d1b2fe77c08575bb6e49'
            '34417c48e5d421df9c46fe015cebd9606917fb40e944646135ea0fca58e75bf9'
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
