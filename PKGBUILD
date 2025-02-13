# AArch64 multi-platform
# Maintainer: rodriguezst <git@rodriguezst.es>
# CONTRIBUTORS OF ORIGIN REPO:
# Contributor: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux612-nabu
pkgver=6.12.13
pkgrel=1
_kernelname=-MANJARO-NABU
_basekernel=6.12
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
         '0045-drm-panel-nt36523-use-devm_mipi_dsi_-function-to-reg.patch'
         '0046-drm-msm-dpu-Drop-BIT-DPU_CTL_SPLIT_DISPLAY-from-acti.patch'
         '0047-of-property-fix-remote-endpoint-parse.patch'
         '0048-drivers-gpu-drm-drm_notifier.c-add-include-drm-drm_n.patch'
         '0049-arch-arm64-boot-dts-qcom-sm8150-xiaomi-nabu.dts-add-.patch'
         '0050-arch-arm64-boot-dts-qcom-sm8150-xiaomi-nabu.dts-add-.patch'
         '0051-arch-arm64-boot-dts-qcom-sm8150.dtsi-change-reset-na.patch'
         '0052-NABU-enable-rtc.patch'
         '0053-NABU-disable-Sensor-Low-Power-Island.patch'
         '0054-NABU-enable-ln8000-charger-driver.patch'
         '0055-clk-qcom-gcc-change-halt_check-for-gcc_ufs_phy_tx-rx.patch'
         '0056-clk-qcom-clk-regmap-Add-udelay-in-clk_enable_regmap-.patch'
         'linux.preset'
         '60-linux.hook'
         '90-linux.hook'
         'uki.conf'
         'cmdline')

sha256sums=('f3ebdeea9e555b4cface44e29670056f4024541e6bd222fbcf776c818974fbba'
            '2af012d60310e1ae6a8318c53a44cd2c31d3dd533dc82ebc62c86ff3d145959c'
            '1c07affeb1e67be54e1a3e0f20d561c06c4de51acb7e3a5cab71c46fff8ccef4'
            'eff6d84d6b15c514fd8e232481555bc27a07a6140b24db46025d93d0513f05ae'
            'ecb547cb0265749818c0f1a6a1b5c3c756699d46c73bda20df745867d5c361a0'
            'abab594a6f30939323228b1c6f6a64d02951602e5c33d34bb3db95f13c9abe17'
            'c1002830778d9fcf96638cd01059636a6fadd68b7bba1caf928852899410fdaf'
            '274d3077abd1ce272a00dd1e89fb4f9e365f5f722e45f1557ccdfa7a12127e3e'
            '942b30860153d01b4e3e619193db70fef3b975f31b04c5ba3a9427b017fce741'
            'ef21cdae6928001c0f5459be285284119d3e406bab88ab6fed4b6685a79c74ea'
            'a5de07c730b504b1439f1faf9d903cc8be2784ae4b4cc19c4951bb6b88d0f1f7'
            'ba9bfef331ff3438565535b5e235e229e4dee12fdc3c687549f4e3fccbd4679a'
            'f1eb3a22e679706b1b040bd2cb083e51f5a7c523aba61e199adc1b8ca8403b57'
            '30c7e7f0e658619f946c31127167aaba1bba52286ee311b5a54a57ae0572880b'
            '1d306ccb98f3bf3e9749cf1518eceb93d7bccfdd99d8ce2844edea7e95781b1c'
            'a42ce8a398507fddc6c2ad6ee3c8da3708db994d4c03f4ee4026f57e64aea9d8'
            '514da125795ac496a4152a37c0c23d900aaef3c885829f9f0b25cf9d290475f8'
            '554f00e9d9b67d469839ca41abc8490460c774063a96f27708d151cc58614cf6'
            'f457288844eff11e227c157d786c16dbaa2327c3fd89d4ee2030050efbe00bb7'
            '267f425469214b4ea8b03d4a9b1db843756acd47392db8cc6d7fded53a80ee8d'
            '9a128541b20cd3237a3372ffafe04f0ade0d006859b489092bb9becb55c86014'
            '355db04e195b1f1266ff79a41b1643a9ba60050e5dcf27fc79680691d2a4e6e9'
            '24f199e3111e84c98599e78f4bd97d18f90645f865b1e147187f2a7765214231'
            '3003545bb4f7471ebfddb90a5212f2a5d9278ac85080376caa1dd4ec54f26917'
            '67bc0df210a0c6932568d5d8f57b0f415a0ac61ce5002cb793cf5f2467a869c9'
            '544875f79eb20b427285233ccf7765bd8eb71c6ecabb6b68b920f9eb76a175f5'
            'f24bc1177dd767565eb67d0adfff83d53a7dfbbc2ef99401ae977e602099cc1a'
            '8989b483b400fa58709e58b2fde52f64583b1e46683b1049d21dc4b26624e462'
            'a4eea2097fdddf0e324259fbf5daf52e83886ca60f8abfd265b85929e4dd7444'
            'ff398bdab855aeae5532b65a8f96d49d658e7f851248dfa909e11f5469c711a5'
            '7e38234f5426e29cff001acf6c595d424247e38e5b13dd940be9a6ba0d770829'
            '92a90bdf81ebee4b2792668782d7d5a9e8f2ed88564adbbf50222aefca22fa31'
            'd4b40e2b97c7ca409429b0348cafd6993b72ce67ef17feb25622619a716707c0'
            '22148b253fb05b03a0ca30eb2c03093a6c2133a4bae645e928610cb4806f8e89'
            '4bb71a614721fb8b5b8f2066326354667f3f65b7f0552f743444da6ebdc6b4da'
            'd015616f381e624988572e5be2228fd04ccb9164b01ab0eb36dadde62b1707b2'
            'c9038196a11482477663fc861caf81c1a76828ec85898a73c265caad1a2bfa93'
            '148a92442da3828b295377a4111374d8880f095dbfce7f39ebac717260783750'
            '4689cb82168eb7475446f149bf4f441ec6b0be37c629ded47ab192282a272f4e'
            '647855dfbb189ad490dcc79a13a91dc479718cff7c26b36082af05b6ae55590b'
            '49717f9f780627ab938405e0250bd37ea0124b879fd79a90629d896767f3633e'
            '28586afa74f9df710900b803b69023278c9967f877cb6745a0ff0332b30ef589'
            '5743644f8e556db6ea5ad1ec84db8143ed8885384987df974b768a4f1c2bfff3'
            'f66613be4af20fdc877c6715b7548c1d088876757c0edf35491c7b4fbd4a9851'
            '4282963b3bf2379c01deb1e052931f5db824841ae88bf85b25233a7261c277a7'
            '66ba3e675a73e2c33856e3078900c0c30a1f53d22bb581eb2904c5e000fbccd9'
            'a29466d4614c6846c967e25a082bc24060ea5e026feede9307d32d69453a89a0'
            '733134ef828d6a66c36cce297b2f6a5674a8fe270c2e5773ad592f04e8a1e847'
            '790d310cdf728dbfb39eb0ffd22e05c5258499f64bc1da145843a11e3b3162cb'
            '8ccfb8f580f02f469c6e1364b5d0a9281616f105901fca4fc3bb0545cc9c38cf'
            '06f0141a9a74ba188af9238e66f1ea53ae180344026d3f7dad1356673d4f6481'
            '404f127cfcb4ed819b040a00c360f96dff23ae10a2991584f2b1cb57255c23b6'
            '29b906e7eb9b83d93e5af2b07f451a4d11b3f63451c32453702c49e4bd15d234'
            'df0a711efbfc97893dfbde4909b368b03dcb42dd1152b9bdd4c02e2d01cc3ad6'
            '349930f17c8e88b108b0a0feecc7fb2cfbf227aeec46c53b59a41650bc27b369'
            'f127d70f545ea404ffe9449fa2b3bdbf7ac8716dac46d1580fdce1a969a85b60'
            '8c08e345dc1b709c0f0ff911a98b024e2c78a440f8bc786a4be6f0b0ebcb9fa7'
            '6ad8697c862e89cac0229d5bd6bc376ab592d11cc107fef65007305a1e176ba8'
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
