# AArch64 multi-platform
# Maintainer: rodriguezst <git@rodriguezst.es>
# CONTRIBUTORS OF ORIGIN REPO:
# Contributor: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux-nabu
pkgver=6.13.3
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

sha256sums=('da33fb15ed2628aaaa8b7870b5f29dec794b2134a6da5208149d0e14e3cac02c'
            'e875c7be2c2b6ccb5a7eeba11e80433636df0948528c9ca8ed55b449ec0a2470'
            '7de076551ed1806b409dd7cb403ea3a10ed9f69c08b2e6f640bfcb77d854329a'
            '2260c115b9a5413d7731cd069b50e7c8ca9e60537abc5af3655a05f8afbad545'
            'e62ea6057450d0bbd7197b9fefb698eae78422910eda6af4f5299f4e691488d1'
            '6c0243ae44523ddf14ffbc6ff6ad0217f96aec25b825440e29e66544e8711cbb'
            '384cfc9fcb6fd69c27fc22c083f57dc40328a4426e5ee6f19c580e7f2f0e3889'
            '9a4f089e1a538c8c358bc7970741df0098dee50cf818a87c8cc0a8e3eae8901e'
            '10e0ec57cf7ba218ebb07f73b648f96cf7fb32aaf35c334d5229a42c81b8a397'
            'e6798b9cfec09601b8e64175a9db138fdeae6036b59832b4a2b533a41e8e5df3'
            '86fc6faa6ea2bfa38afe47d00e497d555e62611fc5e644420d2b8247d585cf49'
            'f7fa6984a847bfb5965e040d0897ab9a2d4adf38e2c580821f542b6c1b752c83'
            '07352404ecb6d1afd92342a7fd466602297fe81ba565e9b1f40c24d085c6056c'
            'c7c7bd44d0a51cd8c55068dac7a9e24bf8be997290f3402e7adea4e7a3aaf037'
            '6d407971f4f918666815c7b23b0d83b9c289505a74facbefc744900cf2505076'
            '1d9425912af2f46d6d4c7d06f0f6d019c85de9a15d6f886bc223254bb4ac4a6f'
            '55854e290dd8e8620cf5603aa1d09cecdd000ea93780e50682cb33e1f1dc5b93'
            '607b40ad4dd0bf72290cc9b47e254201ea155e4488752b440bb8c97e593686dc'
            'b678fd92a5705ee974992bd90c5814828d6bb5aa66618bc1998889ceba47dad4'
            '2e29ac5e84d27549c7ec422059486237a00d62beeaa4999bba329ff6abdac95a'
            'e7a6407a523ccd68df7950eb61827c6aafd0cb0c507aada3881dc22aaeb64b32'
            'c919e22dea6a9299f959e34c478f166ef1df21e5046d4457190ebabf0cbf798a'
            'aa19c571bbefc3315d3d2ac2402f5c07ab5899eee57eb5e0fce1ad7916c721e6'
            'a62442d04e7d8183a634f454258e0f1d9203dc5d30512258568fa53ae068847d'
            'f3fc0f9443541c16f2bfd6d696e2b8ff982f95b38ad10e16c8828ed557a1c762'
            '80392b9800ee43f03801baeafbd1dec87cb6fe47b4b88970841703b8fea19901'
            '03bb4af44e4d3dea85af17d848b4b58d4cebbe0d11e3f3130ef74d762ce533fb'
            'd236cf04226b16e62064466a6c4f29e0aa974d1c11262f526da92ec2f569c312'
            'f93cd674d34dafbf921b8f663abb6f4ffd6ba5ad4c0e167de823474693becad3'
            '5e3021ba56a808515e5115d5b95c626c53503383c7ba4dc7ff2d6904ace9224a'
            '8d3c9ee49c37591fbd13a4ff929c094bc9fda4dbfcb3092d5f3e031810cac97a'
            '5c91e3c0a613edc6b8acd969ca7a0c62e1fd5af9ae2d712a2df2a183ae6152ca'
            'c83b9e48cc424036ceb1c111cf821bf10cd78e3d669176ad29fac25c019c39ab'
            'b0110e4ba0ec927f5b82ccb358387c1568252d8962390722cea586ac847aaebf'
            '34dfd29b2952d00092f23e9d59a72fe9b789bcfbb6d1699f3bebd66203670384'
            '1e330c7ce70dc7e05616bc1ccad63c46023b01d2e5af1486f15e2ba16c0ef366'
            'cf595a7a49477c15703faf1f949d9f121647b151fb97d8970731bfe365f14fcb'
            '071b04bec330169efbdffab0c6e9a2b14db6a22a31f0c36a1be89d98509404f5'
            'edd3efced291f0908dbf5774f6c53e47b43afb997b383401e33933d45c8bb527'
            'cae8a0e05cd75056ce8250fa06de4e3864893fa31663d471ecc1fc8f62662221'
            '45812cf9efdf19e1fc70e6b906962bd404589022fe6296f83d63791580a66c5e'
            '0814cad950ce917b79df80974a5ae1c2d10aa913aa92793643110ce70b9fc39d'
            '1b345dfcd8c68d427682c9689feb25900dc4c48033cc65e5d465b8d6bed62084'
            '104ab2dce8e0a086f23d2a61d01b955e6acfc663d8e7a5efd4887f26314412c5'
            '35c0c47a60f212583639b00aeeba51e93c19224d3394f685cd4ecd210636b592'
            'f3c14791a8cc99522b0e43839d29e4d79686e1e2d7091d2ef6d9c3a3c9fb6919'
            '091aa2b88f5323b818391fa200e3488ae4c460920953874da0e26f142fed3c49'
            'e7165325d06d07256fd298a739b1620095f4f8771daedcfb0f1ba555249e566e'
            '8138eca16f1444fee66850f46405973f627ca664e06a7436e4d1118bc60c0910'
            '923039e1cc156f56619a14baf12b1ba80d61d503b432264e05d3f7b4d3ed7f4f'
            '9ea8af064b5366a54db662d4c745992058c7c065245cf0fd496e2aa00fa0d853'
            '4eb268e2a33dccbe1161fa76996999d0727407eb3d13a3fd3da1ccce6ed31464'
            'af219c1a57554dcf0991d83c7fa13497ab6e6a275e67dbea38e09d9460f75406'
            '473e0a20b3f0f2ba7ad6b35419b2e1d5baab6d30b3506747dcf4dfe405467f4a'
            '937de71f0064bf89ee51e5714402f19be676fd147c46e81e0ed61ad8a962be2f'
            'd173ac17d789c7cb5504a20739cea7209b6bf9760a76e6da7ec956df1f9e8e44'
            '3a2fd7a55ec59764c7b51bf9eca972c79c50bd15bbee80ef193b2222027edd22'
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
