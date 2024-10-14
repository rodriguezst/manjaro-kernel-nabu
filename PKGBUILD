# AArch64 multi-platform
# Maintainer: rodriguezst <git@rodriguezst.es>
# CONTRIBUTORS OF ORIGIN REPO:
# Contributor: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux611-nabu
pkgver=6.11.0
pkgrel=1
_kernelname=-MANJARO-NABU
_basekernel=6.11
_srcname="linux-${pkgver/%.0/}"
_newversion=false
_stopbuild=false     # Will also stop if ${_newversion} is true
_dtbfile='qcom/sm8150-xiaomi-nabu.dtb'
_desc="AArch64 multi-platform"
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc')
options=('!strip')
source=( "http://www.kernel.org/pub/linux/kernel/v6.x/${_srcname}.tar.xz"
         'config' 
         'linux.preset'
         '60-linux.hook'
         '90-linux.hook'
         'uki.conf'
         'cmdline'
        "0001-SM8150-Add-uart13-node.patch"
        "0002-SM8150-Add-device-tree-for-Xiaomi-Pad-5.patch"
        "0003-drm-Add-drm-notifier-support.patch"
        "0004-drm-dsi-emit-panel-turn-on-off-signal-to-touchscreen.patch"
        "0005-Input-Add-nt36523-touchscreen-driver.patch"
        "0006-nt36xxx-Fix-module-autoload.patch"
        "0007-NABU-Added-novatek-touchscreen-node.patch"
        "0008-drm-panel-nt36523-Add-Xiaomi-Pad-5-CSOT-panel.patch"
        "0009-NABU-Enable-gpu-dsi0-and-dsi1.-Added-panel-and-backl.patch"
        "0010-SM8150-Add-apr-nodes.patch"
        "0011-ASoC-qcom-SM8150-Add-machine-driver.patch"
        "0012-NABU-Add-sound-nodes.patch"
        "0013-power-supply-Add-driver-for-Qualcomm-PMIC-fuel-gauge.patch"
        "0014-power-qcom_fg-Add-initial-pm8150b-support.patch"
        "0015-arm64-dts-qcom-pm8150b-Add-fuel-gauge.patch"
        "0016-NABU-Add-pmic-fg-and-battery-nodes.patch"
        "0017-SM8150-Add-slimbus-nodes.patch"
        "0018-arm64-dts-add-wcd9340-device-tree-binding-for-sm8150.patch"
        "0019-ASoC-qcom-SM8150-Add-slimbus-audio-support.patch"
        "0020-ASoC-qcom-sm8150-Fix-compilation-in-v6.7.0.patch"
        "0021-NABU-Add-wcd9340-and-microphone-dais.patch"
        "0022-drm-msm-dsi-change-sync-mode-to-sync-on-DSI0-rather-.patch"
        "0023-drm-msm-dpu1-improve-support-for-active-CTLs.patch"
        "0024-drm-msm-dpu1-use-one-active-CTL-if-it-is-available.patch"
        "0025-drm-msm-dpu-populate-has_active_ctls-in-the-catalog.patch"
        "0026-drm-msm-dpu1-dpu_encoder_phys_-proper-support-for-ac.patch"
        "0027-drm-panel-nt36523-enable-prepare_prev_first.patch"
        "0028-input-nt36xxx-Enable-pen-support.patch"
        "0029-drm-msm-dpu-Fix-dpu-sspp-features-for-sm8150.patch"
        "0030-drm-panel-nt36523-Enable-120fps-for-nabu-csot.patch"
        "0031-NABU-Add-pm8150b-type-c-node-and-enable-otg.patch"
        "0032-NABU-Add-fsa4480-node.patch"
        "0033-NABU-Enable-secondary-usb-and-keyboard-MCU.patch"
        "0034-input-nt36523-Remove-fw-boot-delay.patch"
        "0035-NABU-Add-flash-led-node.patch"
        "0036-NABU-Add-ln8000-fast-charge-IC-for-testing.patch"
        "0037-NABU-Add-hall-sensor-for-magnetic-cover-detection.patch"
        "0038-NABU-Set-panel-rotation.patch"
        "0039-NABU-Remove-framebuffer-initialized-by-XBL.patch"
        "0040-NABU-Remove-deprecated-usb_1_role_switch_out-node.patch"
        "0041-nt36xxx-Fix-compilation-in-6.8.patch"
        "0042-Remove-missed-dsc_active-duplicate.patch"
        "0043-nt36xxx-Fix-compilation-in-6.9.patch"
        "0044-qcom_fg-Fix-compilation-in-6.11.patch" )
sha256sums=('ef31144a2576d080d8c31698e83ec9f66bf97c677fa2aaf0d5bbb9f3345b1069'
            '12e93de2db555bbf523d4d9d2d4dfd748e6e0c4aac5dc86160d353b1bd936706'
            'ab4e207d675f8ce4eb2be2c291d4858e2172ed2e31cb11ad18c0ad8b3318b6d0'
            'ae2e95db94ef7176207c690224169594d49445e04249d2499e9d2fbc117a0b21'
            '2c8a3715103d55947a96dd074efe6d5439bef2d4fecc15f5b3d268e2033abbd5'
            '2d87c68d02f14ce14de548d2d9d79dcca34fa276ee535cad6da78584531baae1'
            '4c06efd0966046827c7bc0fea11a9e5e298bd199cd4bdfe141795a3b62799cb9'
            '5d9a3550811f79d34ec6caf9d49b510d61a6ca42e83e9a66ccafdeac62c22334'
            'd74ea2bf89847c6fc6829d2ab1d9ee757179c5461ad8f5ebab9b18af0eaf3d1f'
            'adf4f104ba0fb31140a132f78f7475cacad292c7a4d40465c9ce292091bd2dc0'
            'a6d7a320a7bbc9f77807a25deb5236248de3b7ef50bf899580a36bd7a1060ecf'
            'ca5f862dfcf26b20fdb3e4a8811895cb6b91852d5a2738c4f1d7a10e2e365898'
            '44a3f784df2f8cd7e22781037262e0fdb1bf27b4bad98fd8e223afe1b6c82bee'
            '15de0e60cd768900aac66bb3c4b128a06b226d80c44e9cfef3e955c297c8300d'
            '26caa99dba0c48cd3c458d86b7a97ebbc5bee7527f256d48387514b459342086'
            '309ecb2ea0ab94b34ab3bdcca83f07df7b3561cf29f87f594b7ea61385ea928a'
            '2130f2de808e262cdcb7510f6712e2342f4821c4018a3196c35298701b008b45'
            '7e39e71b14cbd124ca50044807de4c7592be3036cdedfca451e6bdd83bebd0aa'
            'be9713773b99955561d5b268df10f04e7581a0641613947ce18022b0c2ecce63'
            'c0051ad10c48c37c5ced85dbd03cc626e7ddf8781df45cda12713cb72718c9df'
            '755ad43e4c7206f00e512c595712814b614d7ff4b168465e14c0a1064fc7453d'
            'acfb02662b68c214705c9391f7eaf605303dd0223a84dd7861ac707eb8440930'
            '39d4782f7911b79a67b309fb12f7722871ad87fdb88d6ee348161e5b0b4ee920'
            'f244137306f91c1cb8c5f0ab222eb12b96853ac3404e1016bbed98586777982c'
            '1d59558d39a901a6472287a6aec473977a3fb26a52ca8d7812b6f0e0988cabbf'
            '79dac4520533ab2a0485f285780306bde5f74992f05d51e1663aa5e44d9de803'
            '0f725aec20fd7c1af052c5e7a4e9d8e52b4df384119ea601f24467b84ce7174e'
            'd9d0dbd56e8edbaae34ad346638837631b0390551856129882030f4bc09cfd8c'
            '97c73b42bd9489ac475a5a5a45ba190a6971ab6a6c5a8ce9b2cc13de3f880091'
            '230f865db2fc9f8a2bbe46c5c04ba481f771959cdf2f65cf143659ba83f2ab06'
            '0edd0daccdef060881b385750c080608bdc52805bf74c8e51735bda3d0b35ff9'
            'ec6055f4ed0e8cd49fa743ea47f3eabd5bbdae42b9bf4d556a10314f6233a89e'
            '0771ec735ef7617bdbeac5302b33c9495104d6f1456450d7067e0c20a4c1a1f9'
            'fc0a7d0434f5eae63e32b508ddce5575a5e286bd611d06973466f2b6fd4ecd04'
            '56d38c2ff3e854de81fe9bc6fc690550fdee8acd169e7a95ca8bd585aede6e0b'
            'a24bf2b7fab7c07707113591f8eabe9b0644848035db8bdfa3e29793f4bef869'
            'd53d0412e95e7a771526a3534399b8ee34990d6f08e6b6587fd32b80962afc02'
            '5afa3f5867eaaae9657c65e7781fc12f7942d5dce5a824b91849be5989f36390'
            'c49e6b3ed3ac31204d779409cd3456030d668c15839715441c7150c22ba0e0c4'
            '49c289cc967f5486540bdd0b252dc0bbd3f88283d92dbb4e1d49bff59a4bafe2'
            '32ae99bb3de5487eceea64476a4937b306776cf6d2509375e86ac76b931bd087'
            '071a50c1ae5bdf3be90e90f82233a3d7224dfecd0a89b2ba9919fdff082a3d21'
            'e6bd58be211f65c4788e905df72ee5f6e0da6c6975912c1a1448c5004dc34bea'
            'e7b399e4f9306800abf0cb0f98d72b3da1f1f05014c2a1ea6c07256147b8b254'
            'b054e65655688ddbeb779d4cbfd5ac627305e9a571262ac7ffa030afd547bfe5'
            '20227b04796707dcbc2a2fbf1d4b532d8d04ee00a30384c6641ea2430bcf336d'
            '70d1b4163fdd46338ca596776578c5fd6e77564ef913a37e5acda1f06cb7d142')

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
  #conflicts=('linux')
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

  # remove build link
  rm "${pkgdir}"/usr/lib/modules/${_kernver}/build

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
