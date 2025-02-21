# AArch64 multi-platform
# Maintainer: rodriguezst <git@rodriguezst.es>
# CONTRIBUTORS OF ORIGIN REPO:
# Contributor: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux-nabu
pkgver=6.13.4
pkgrel=1
_kernelname=-MANJARO-NABU
_basekernel=6.13
_srcname="linux-${pkgver/%.0/}"
_newversion=false
_stopbuild=false     # Will also stop if ${_newversion} is true
_dtbfile='qcom/sm8150-xiaomi-nabu.dtb'
_desc="AArch64 multi-platform"
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc' 'systemd-ukify' 'sbsigntools')
options=('!strip')
source=( "http://www.kernel.org/pub/linux/kernel/v6.x/${_srcname}.tar.xz"
         'config' 
         '0001-SM8150-Add-uart13-node.patch'
         '0002-SM8150-Add-device-tree-for-Xiaomi-Pad-5.patch'
         '0003-drm-Add-drm-notifier-support.patch'
         '0004-drm-dsi-emit-panel-turn-on-off-signal-to-touchscreen.patch'
         '0005-Input-Add-nt36523-touchscreen-driver.patch'
         '0006-nt36xxx-Fix-module-autoload.patch'
         '0007-NABU-Added-novatek-touchscreen-node.patch'
         '0008-drm-panel-nt36523-Add-Xiaomi-Pad-5-CSOT-panel.patch'
         '0009-NABU-Enable-gpu-dsi0-and-dsi1.-Added-panel-and-backl.patch'
         '0010-SM8150-Add-apr-nodes.patch'
         '0011-ASoC-qcom-SM8150-Add-machine-driver.patch'
         '0012-NABU-Add-sound-nodes.patch'
         '0013-power-supply-Add-driver-for-Qualcomm-PMIC-fuel-gauge.patch'
         '0014-power-qcom_fg-Add-initial-pm8150b-support.patch'
         '0015-arm64-dts-qcom-pm8150b-Add-fuel-gauge.patch'
         '0016-NABU-Add-pmic-fg-and-battery-nodes.patch'
         '0017-SM8150-Add-slimbus-nodes.patch'
         '0018-arm64-dts-add-wcd9340-device-tree-binding-for-sm8150.patch'
         '0019-ASoC-qcom-SM8150-Add-slimbus-audio-support-Also-adde.patch'
         '0020-ASoC-qcom-sm8150-Fix-compilation-in-v6.7.0.patch'
         '0021-NABU-Add-wcd9340-and-microphone-dais.patch'
         '0022-drm-msm-dsi-change-sync-mode-to-sync-on-DSI0-rather-.patch'
         '0023-drm-msm-dpu1-improve-support-for-active-CTLs.patch'
         '0024-drm-msm-dpu1-use-one-active-CTL-if-it-is-available.patch'
         '0025-drm-msm-dpu-populate-has_active_ctls-in-the-catalog.patch'
         '0026-drm-msm-dpu1-dpu_encoder_phys_-proper-support-for-ac.patch'
         '0027-drm-panel-nt36523-enable-prepare_prev_first.patch'
         '0028-input-nt36xxx-Enable-pen-support.patch'
         '0029-drm-msm-dpu-Fix-dpu-sspp-features-for-sm8150-Why-was.patch'
         '0030-drm-panel-nt36523-Enable-120fps-for-nabu-csot.patch'
         '0031-NABU-Add-pm8150b-type-c-node-and-enable-otg.patch'
         '0032-NABU-Add-fsa4480-node.patch'
         '0033-NABU-Enable-secondary-usb-and-keyboard-MCU.patch'
         '0034-input-nt36523-Remove-fw-boot-delay.-Should-be-fine-b.patch'
         '0035-NABU-Add-flash-led-node.patch'
         '0036-NABU-Add-ln8000-fast-charge-IC-for-testing.-If-it-sa.patch'
         '0037-NABU-Add-hall-sensor-for-magnetic-cover-detection.-H.patch'
         '0038-NABU-Set-panel-rotation.-https-gitlab.com-sm8250-mai.patch'
         '0039-NABU-Remove-framebuffer-initialized-by-XBL-https-git.patch'
         '0040-NABU-Remove-deprecated-usb_1_role_switch_out-node.patch'
         '0041-nt36xxx-Fix-compilation-in-6.8.patch'
         '0042-Remove-missed-dsc_active-duplicate.patch'
         '0043-nt36xxx-Fix-compilation-in-6.9.patch'
         '0044-qcom_fg-Fix-compilation-in-6.11.patch'
         '0045-drm-msm-dpu-Drop-BIT-DPU_CTL_SPLIT_DISPLAY-from-acti.patch'
         '0046-of-property-fix-remote-endpoint-parse.patch'
         '0047-drivers-gpu-drm-drm_notifier.c-add-include-drm-drm_n.patch'
         '0048-arch-arm64-boot-dts-qcom-sm8150-xiaomi-nabu.dts-add-.patch'
         '0049-arch-arm64-boot-dts-qcom-sm8150-xiaomi-nabu.dts-add-.patch'
         '0050-arch-arm64-boot-dts-qcom-sm8150.dtsi-change-reset-na.patch'
         '0051-NABU-enable-rtc.patch'
         '0052-NABU-disable-Sensor-Low-Power-Island.patch'
         '0053-NABU-enable-ln8000-charger-driver.patch'
         '0054-clk-qcom-gcc-change-halt_check-for-gcc_ufs_phy_tx-rx.patch'
         '0055-clk-qcom-clk-regmap-Add-udelay-in-clk_enable_regmap-.patch'
         'linux.preset'
         '60-linux.hook'
         '90-linux.hook'
         'uki.conf'
         'cmdline')

sha256sums=('b80e0bc8efbc31e9ce5a84d1084dcccfa40e01bea8cc25afd06648b93d61339e'
            '9563fa6d29fe0e2ddd908ba08871674c909a2beb3eb93fd1b70f863aa34125c4'
            'd20ef1acb448c319f23db20e99c0526f3342f5cc7d5aca62615d914516951748'
            '7343404ea7d02020386b51f29d38bc89b8bb067c421bf39d455ecf41ce899aba'
            'd7316c9997abbfbf67f036a527a1cd805f58d34258c880217e29c19bd6954faa'
            '55542427a18d5c37dc3f08ffaacf74a050fe8aed5ed6c899f5f57e198bd93f0c'
            'ad9ecc06c7e112286d528e5a75b62823d6ff09a59b231662214717ef85cb5da0'
            '8f3c65e8f28639575df472916ffee283dc6006d4990e4028f832d31c89194b70'
            '12bb025dc83b8ed0f6969c940a174e7c227ed0868d435aeb760d2edc58b74f20'
            'd8a34a6055d94a8753c37aa98f97a5562c4285fa1507f6f4c9533c38d3733178'
            '02a78d6c68ac70ac751e2ec4de5ea64e3a7d38f2ee60215ba2967e9e63a611e7'
            '8e7a3ba8d539b3a2010608b237958da00fd0f4747e3600595c5c38749a059b95'
            '83a89ce0070986f6cd60870ceb4203b0b5beca3a808c0c8aaa0b3bb38a9ce697'
            '62a35606f1341e85a2d2986c6dcc30bd2d54dbff2f855ad304fdf0c52fdf92e5'
            '7ae93761a9f1512bbc6f02bebd47ee50d5fe3dce35fde9df5c192a687d492fdd'
            'f5f41a0b7907bd6a3ed915d748cf200fcb3fd0060c0a680385bbd4f31bfe9261'
            '51582f76265bd88e52944be170453364545fafaf2611e88d6ba76ff556634580'
            '64304624f3916c25513942c2db528876c6998c1bbb111d158d1af5caca0bf46a'
            'b92b1eecb24c08456d631d94ec791097d1ff0afcdc0f60e7aa35923ec6737d5e'
            '088525336dee975ccb12c3e32d198d323bf111159dc6c255dd344a89f788611c'
            'e1123c1cd5d17dea52d2be0ed196b669fc5b349120e64164153db99e533760f9'
            'cbfc51f31b32e37186ba3d6f1c8b9b66fe1430971b6b012c751623310946feba'
            'd8339ee100d2d22d893cca2b2cd622a53de814217e77354d421db22fdefecb77'
            '5d5e334730b4c0ffab97844200d0fb087c249c879d6900b05f1aeaa8c9ab5f04'
            'fd9408221eeb3cea66a23333559d4c200fedfa166fc86f21dc50179f8e13530b'
            'b890e3a1bd7b2267191a78eb22592ceb3feeabccdd33b1cf92998dbedc10c578'
            '8820837bc2619a5796a5f7f3af9afd1d0790013ecb54ef84500fbd4921da527e'
            'eb426f159b87fdca74275ea3ce66319b7a21b2c91df6c7614e4022f3c336d6a9'
            '36a1266d8142767db27640653bb503730ad4adaf8b154f15297571610743e2cb'
            '63673651e95d065c8b3b7757004ff44b6d536ce9f2e90e0ebb7ba9b70ebb0aaf'
            '9c5ecb41bee8973d0c5047918c756717a93ab9d3a5b6178fc5b91a0888d4d85a'
            '95ad64e21bcd638654355573d1b1556a2318e4fc17302d4d585016b65618fb2f'
            '4f877f67934ed77c3aac511d064c4d82075e6120695210bb44531572c13eeff6'
            'b0ca2fd1702c736a3121ded4dce3d9ec489d5548b83294e2e1410c85450b7bd3'
            'dc86a52b220d6d63a19a74a101a8c2461264bfd81d43006a2914a99a2ebf3e51'
            '23fd7866365c5748e7a0ba5d86fa22a4f8655dc1c6ab839a1582476b1419cc77'
            '34f5bb9efd5ae8c47f58b5df8177fad8ac69a3f7d762dadda0a002a6389a9c7b'
            '219ed61cedc3a9386062d7d07e30ba1553f8cfea57b40e7642d998ed09a4f38a'
            '4aac9b0881b337a214dc2a7603ac077083ca769438fe341ecd4994590d754273'
            '54084b977b4e942e3820d9396b1cbb54d1246860a7713551e2289caadb0d0751'
            '3c105b000e0a39223ba4f61b8fba369114594b425d32a6154b5e9a3876c2758b'
            '92b7f2eee8b2091148ab3717ea532154d097537a8fa9c0668e4010a36ec5b35f'
            '79fe6ae84e79aa9437f982c579aff00c1aeafec8f9cb39a84301f49fa6dfefb9'
            '727b99ed4aa68629d409e8f8a910818ac5f03d3f6676a7e10b9872b3f7016a18'
            '9b701bfaaabb6a4c2c12681748977eed22e2fb273f9d4c839920b885abddbcaf'
            '330245288a89139bb1716adfab95c66f740e3e434a57022d8d0ceae9575778ec'
            '7a4bd03bd9561720eae71c139778a432c0f355d929f46249843ac8a5ab2defb7'
            'fc74602e86845f05165527af01b93379ea9ac1d7ba5495df390f947fc0135b80'
            'f8acb06047c4b88cfcd0b7e2130addd88561add221939c875420ce8e9d9bac05'
            'e3d1345432ac906ef93c8a608a744ab0c0b7311ae67621359bb86b00e8957536'
            'a8990ea1b58b2b9a6e1df39f8ef2a7cf07014a58e83531922bec996d02de9d74'
            'b42017d5e8db786b2dae401f74573e5bf92182aa206acb4c0de25c5e810ef9f8'
            '1d88bf6df498d86eca737228de242ae83b5214b4574ca5a9a4839a36631961d8'
            'f1a3446d33fba27b15801b523ab5a4fba32e62c22da47d6212710cb1e60d3eb5'
            '36fc78eb8fa06bd8456227b27b1761b2d432c8f95a74c72827ba9688e5d9539e'
            'b8666baea445bae44597c9698e90b9b9274bab9ccddff7c3b6c2e7e0fe15bdde'
            '445cd26e28f7dd863d757ce98a1e08c6783fee32275fa94db566e04de9a244da'
            'ab4e207d675f8ce4eb2be2c291d4858e2172ed2e31cb11ad18c0ad8b3318b6d0'
            'ae2e95db94ef7176207c690224169594d49445e04249d2499e9d2fbc117a0b21'
            '2c8a3715103d55947a96dd074efe6d5439bef2d4fecc15f5b3d268e2033abbd5'
            'f8f534bb60d53f5fe0b0e30a50191da7e7d80645e3dec831e269f785e62f25eb'
            'c0040ff0642b29bdf364c5d7c066a1ea6c593d94c9b87cbf9b3ecfb75dc31c26')

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
  depends=('coreutils' 'kmod' 'initramfs' 'systemd-ukify' 'openssl' 'sbsigntools')
  optdepends=('crda: to set the correct wireless channels of your country')
  provides=("linux=${pkgver}")
  conflicts=('linux')
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

_package-signed() {
  pkgdesc="The Linux Kernel and modules - ${_desc} - Secure Boot Signed"
  depends=('coreutils' 'kmod')
  optdepends=('crda: to set the correct wireless channels of your country')
  provides=("linux=${pkgver}")
  conflicts=('linux')

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

  # Generate and sign UKI during package creation
  mkdir -p "${pkgdir}/boot/efi/EFI/manjaro"
  ukify build \
    --linux="${pkgdir}/boot/vmlinux-${_kernver}" \
    --cmdline="console=tty0 root=PARTLABEL=linux rw debug=vc selinux=0 audit=0" \
    --uname="${_kernver}" \
    --devicetree="${pkgdir}/boot/dtb-${_kernver}" \
    --os-release="Manjaro ARM" \
    --secureboot-private-key="${startdir}/sb.key" \
    --secureboot-certificate="${startdir}/sb.crt" \
    --output="${pkgdir}/boot/efi/EFI/manjaro/uki-${_kernver}.efi"

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

pkgname=("${pkgbase}" "${pkgbase}-headers" "${pkgbase}-signed")
for _p in ${pkgname[@]}; do
  eval "package_${_p}() {
    _package${_p#${pkgbase}}
  }"
done
