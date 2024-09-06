# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux61-nabu
pkgver=6.1.108
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
    '0016-rotate-screen-for-nabu.patch'
    '0017-add-minimal-dts-for-nabu.patch'
    '0018-NABU-add-support-for-nt36523-touchscreen.patch'
    '0019-NABU-add-additional-cpu-frequency-for-Kryo-485-Prime.patch'
    '0020-NABU-add-sound-support.patch'
    '0021-NABU-add-vol-and-power-keys.patch'
    '0022-NABU-add-dma-nodes.patch'
    '0023-NABU-add-backlight-regulators.patch'
    '0024-NABU-change-the-path-of-the-Bluetooth-firmware-to-de.patch'
    '0025-NABU-set-i2c7-speed-to-1M.patch'
    '0026-NABU-Modify-the-loading-path-of-the-firmwares.patch'
    '0027-NABU-keyboad-Delete-unused-code-and-add-pm-support.patch'
    '0028-input-nt36xxx-Enable-pen-support.patch'
    '0029-drm-Add-drm-notifier-support.patch'
    '0030-drm-dsi-emit-panel-turn-on-off-signal-to-touchscreen.patch'
    '0031-TS-Add-the-handler-to-accept-the-notifier-from-DRM.patch'
    '0032-PANEL-BACKLIGHT-update-nt36523-driver-and-ktz8866-dr.patch'
    '0033-DRM-fix-drm-suspend-resume.patch'
    '0034-DEBUG-update-debug-dts.patch'
    '0035-Charger-update-pm8150b-driver.patch'
    '0036-charger-add-charge-pump-ln8000-driver.patch'
    '0037-removed-a-log-print-because-it-printed-too-much.patch'
    '0038-USBPD-update-typec-pdhpy-driver.patch'
    '0039-USBPD-trick-Xiaomi-charger-to-supporting-PPS.patch'
    '0040-charge-add-fast-charge-manager-driver.patch'
    '0041-charge-add-dts-configs-for-fast-charge.patch'
    '0042-NABU-add-cover-detect.patch'
    '0043-dsi-fix-display-sync-problem-from-map220v.patch'
    '0044-restore-initial_rotation-use-cmdline-fbcon-rotate-1-.patch'
    '0045-charge-support-standard-pps-charges.patch'
    'config' 
    'linux.preset'
    '60-linux.hook'
    '90-linux.hook'
    'uki.conf'
    'cmdline' )
sha256sums=('3f4e4e89a00e221a6dd1174779e0028794f44f4624ad6a31c79f3b7796688ca2'
    '6ed81eef2b20fa9b42cf8e05e22ec7122bc51a1a9ddd082e1edc48adf81d7aae'
    '35fb87d4e4775fb15998b9740d33f058e01f5d40f7427e529b2d352ec1e417c5'
    'fed5d0ef1f2eb251c3293765d8ab2a5863bf37e0083148e118cd1fd6a6732034'
    '23fccb4723cf2d09e4dccc72d3a3775d28440f00733cbaf1152dbfa3408c374e'
    '2aa8ac449b69d36a06166c59917e277547a16663954c9200f58085e23ba3e803'
    'af01844ea0dc7df8648930722b3cc50f2b9dc091fa374c4ec24765733d1a67f4'
    '9baf9eb6e5260add9c2ffc233da66cc8cf0549c9da11c6e2eaffb07e5a27598e'
    'a37731fe3dac77fa070b9fc6f1e53a17855b736b4a073359236ee9b5d98e6d1c'
    '219065e7019515372db3c3d96ca0f13e53eb0a23736ff530ce6c43c07df67cda'
    'cb3adfb5b2f9ffda561673eb1767eba4d5ca9d839bca6a7dcacea3fc4b4e4fd6'
    '589c944d068bf30fac1df8f716a8e2acae2b5ac21d8c1f27b522c814c7c85983'
    'bf9a1750bc795bf7cad7729f0801ec17bdb7e7a8e52fe5edd4bf8a8464fce045'
    'beb8a006e52055626b7ec82cbefcad9a36d254017a31d19fe8e0fc958d09b992'
    '80a6faf2d70b4848d1c6aa472160b9e433f26193bd19a74d1b5bfae381ca362a'
    '9ed109408720f7f1682320970e36e85d9e21121434a4420c190e1d9c3ce1083c'
    'e7e86f4c8056431f6a319ad0706e746178d265933a36fc773d39f030af2d9528'
    'd248759d399c7cfe923149996294a432b06e52cbcdbf2d6d024df2115e8e9f0f'
    '8aad19928da5209578ab1d2d7afdb82a3ad7305bc2ca0d12d31fb88d311f5ab0'
    'e7aa861b199dcf857c30aad7448d5a74a3738720ecb109ac76097dcd4c2a7717'
    '13a11cebf55f2cf8851bb4c8ebc30e5c0c8b7c2cd372321e1a1ad6e930b278f5'
    'fc1ac06b87c4e8178efcaee99e8e1c6998ff98fbb80c465024fc285a388c5111'
    'aa7a4551c29ff9661f5c1561aa2ef616a5c1ccab9763fb9c2fdf60765b7047d9'
    '707d53ca7b5de76315a2094af72950c8728ab43409024e553b1de546accfe113'
    '8b7ac2a5ef91e19ca624b2ca9deecf7072247268f827efadb1426ebec6b5467b'
    '3f8b03c9bdf1659c2f36d9ea0c2af038ca6247cd84e297855df6588f62d5df93'
    '0fb78721f3ff37fa590822b18ddea0f1a269d34784c5fc049cc1952926e4c9ea'
    '29b46985f194632774460bd46b673e2b3cae4a42fa92a59ac51131a4db9fd031'
    'fa2b7057ed28a8d3c7253ae02522debed9cb498588107267ce82d8d9c9bf6002'
    '0aa4e8f21fa190c309e3502310044cc9a64de29a43e074842ca087561007ba71'
    'ec673374d484b4a209ba25e2e1631702331b9ea99f1031af5fa31ed472d3d7a2'
    '57b428cff6c7b539d71ab14c4437b733032abb5d798669bb4a2c16710bf2cef5'
    '189c20c6ab18057955678b2b457afb945604ddebb7fb8bc7a1debf59d213acd0'
    '4859cdb137762c8e179e65a1c28f9f0ec7e86fa1eae6827fb0f354bafd9af8fb'
    '3beba722f48b6bf77c9819c3764d45d262d069a377519f1cf3ab803902b26db9'
    'aeeab5ddd99e066d8236e4857792de3e812b6b36970e8d0c5621d98f121a9970'
    'bdda08672a27dc18e88f16362e4631af755d27671ff792e683a70706b6e157e1'
    'eb054eefe77229b8093636fbc0c886e9d6798250e993975d58c7a79a88e0414c'
    'dc6a627c7f04baec84edac5b3b4380576ee6a7614b0ed7f94ffe43bec98e8c97'
    '1e4bf5a4f185f889940daa22f4d95929dbb06fb2fb6f8f4e568d730af68a16b3'
    'c5c1b03c0c123acd805b939088e613c74212e6980bf6fdb23c69e4ecb0234af0'
    '2e24d3725cd3d12f5f456b3ae9c6894cac236e75517f559daa7a91eb871fe7e4'
    '60b3bd9ce2d9e36244219f37ef7a30d077d8636e31c5aa676b908cb150ba6000'
    'a5dd6e626f7b7f907f3c8e1c6eeaa406d17ac210c6c75b5e48f67ce3cc5d4908'
    '6f22b249090b5b82a55f87809b0610188c07de6caa2d722442712895feaaa0c7'
    '3643f834642281678fe6ad3524d5dec513aea90fd76e8c76dab50a85392b0c8a'
    '1ea6da804b588731ed709f2d0415fc86a80cdb187fadba3e73ebd2330f14c922'
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
