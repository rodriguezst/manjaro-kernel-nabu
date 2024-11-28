# AArch64 multi-platform
# Maintainer: rodriguezst <git@rodriguezst.es>
# CONTRIBUTORS OF ORIGIN REPO:
# Contributor: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux612-nabu
pkgver=6.12.0
pkgrel=10
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
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc')
options=('!strip')
source=( "http://www.kernel.org/pub/linux/kernel/v6.x/${_srcname}.tar.xz"
         'config' 
         'linux.preset'
         '60-linux.hook'
         '90-linux.hook'
         'uki.conf'
         'cmdline'
         '0001-SM8150-Add-uart13-node.patch'
         '0002-SM8150-Add-device-tree-for-Xiaomi-Pad-5.patch'
         '0003-drm-Add-drm-notifier-support.patch'
         '0004-drm-dsi-emit-panel-turn-on-off-signal-to-touchscreen.patch'
         '0005-Input-Add-nt36523-touchscreen-driver.patch'
         '0006-nt36xxx-Fix-module-autoload.patch'
         '0007-Add-sm8150.config-fragment.patch'
         '0008-NABU-Added-novatek-touchscreen-node.patch'
         '0009-drm-panel-nt36523-Add-Xiaomi-Pad-5-CSOT-panel.patch'
         '0010-SM8150-config-added-display-panel-and-backlight-modu.patch'
         '0011-NABU-Enable-gpu-dsi0-and-dsi1.-Added-panel-and-backl.patch'
         '0012-SM8150-Add-apr-nodes.patch'
         '0013-ASoC-qcom-SM8150-Add-machine-driver.patch'
         '0014-NABU-Add-sound-nodes.patch'
         '0015-power-supply-Add-driver-for-Qualcomm-PMIC-fuel-gauge.patch'
         '0016-power-qcom_fg-Add-initial-pm8150b-support.patch'
         '0017-arm64-dts-qcom-pm8150b-Add-fuel-gauge.patch'
         '0018-NABU-Add-pmic-fg-and-battery-nodes.patch'
         '0019-SM8150-Add-slimbus-nodes.patch'
         '0020-arm64-dts-add-wcd9340-device-tree-binding-for-sm8150.patch'
         '0021-ASoC-qcom-SM8150-Add-slimbus-audio-support.patch'
         '0022-ASoC-qcom-sm8150-Fix-compilation-in-v6.7.0.patch'
         '0023-NABU-Add-wcd9340-and-microphone-dais.patch'
         '0024-drm-msm-dsi-change-sync-mode-to-sync-on-DSI0-rather-.patch'
         '0025-drm-msm-dpu1-improve-support-for-active-CTLs.patch'
         '0026-drm-msm-dpu1-use-one-active-CTL-if-it-is-available.patch'
         '0027-drm-msm-dpu-populate-has_active_ctls-in-the-catalog.patch'
         '0028-drm-msm-dpu1-dpu_encoder_phys_-proper-support-for-ac.patch'
         '0029-drm-panel-nt36523-enable-prepare_prev_first.patch'
         '0030-input-nt36xxx-Enable-pen-support.patch'
         '0031-drm-msm-dpu-Fix-dpu-sspp-features-for-sm8150.patch'
         '0032-drm-panel-nt36523-Enable-120fps-for-nabu-csot.patch'
         '0033-NABU-Add-pm8150b-type-c-node-and-enable-otg.patch'
         '0034-NABU-Add-fsa4480-node.patch'
         '0035-NABU-Enable-secondary-usb-and-keyboard-MCU.patch'
         '0036-input-nt36523-Remove-fw-boot-delay.patch'
         '0037-NABU-Add-flash-led-node.patch'
         '0038-NABU-Add-ln8000-fast-charge-IC-for-testing.patch'
         '0039-NABU-Add-hall-sensor-for-magnetic-cover-detection.patch'
         '0040-NABU-Set-panel-rotation.patch'
         '0041-NABU-Remove-framebuffer-initialized-by-XBL.patch'
         '0042-NABU-Remove-deprecated-usb_1_role_switch_out-node.patch'
         '0043-nt36xxx-Fix-compilation-in-6.8.patch'
         '0044-Remove-missed-dsc_active-duplicate.patch'
         '0045-nt36xxx-Fix-compilation-in-6.9.patch'
         '0046-qcom_fg-Fix-compilation-in-6.11.patch'
         '0047-drm-panel-nt36523-use-devm_mipi_dsi_-function-to-reg.patch'
         '0048-drm-msm-dpu-Drop-BIT-DPU_CTL_SPLIT_DISPLAY-from-acti.patch'
         '0049-of-property-fix-remote-endpoint-parse.patch'
         '0050-drivers-gpu-drm-drm_notifier.c-add-include-drm-drm_n.patch'
         '0051-arch-arm64-boot-dts-qcom-sm8150-xiaomi-nabu.dts-add-.patch'
         '0052-arch-arm64-boot-dts-qcom-sm8150-xiaomi-nabu.dts-add-.patch'
         '0053-arch-arm64-boot-dts-qcom-sm8150.dtsi-change-reset-na.patch'
         '0054-NABU-enable-rtc.patch'
         '0055-NABU-disable-Sensor-Low-Power-Island.patch'
         '0056-NABU-enable-ln8000-charger-driver.patch'
         '0057-clk-qcom-gcc-change-halt_check-for-gcc_ufs_phy_tx-rx.patch' )

sha256sums=('b1a2562be56e42afb3f8489d4c2a7ac472ac23098f1ef1c1e40da601f54625eb'
            '70ec4661c9d05555c341400e8873accb8163dd2f0a5a746ff76ffba1a94ced06'
            'ab4e207d675f8ce4eb2be2c291d4858e2172ed2e31cb11ad18c0ad8b3318b6d0'
            'ae2e95db94ef7176207c690224169594d49445e04249d2499e9d2fbc117a0b21'
            '2c8a3715103d55947a96dd074efe6d5439bef2d4fecc15f5b3d268e2033abbd5'
            'f8f534bb60d53f5fe0b0e30a50191da7e7d80645e3dec831e269f785e62f25eb'
            'f67f1bd0d724ef4bb47a76106b2dbf709cd9d8678bc98f8c6a6eb3e6528fb718'
            '7b0db41df0775cd92419f3ac0a84ec3bb11c713905290c6593ed403afb1c1706'
            '74b584aae2a1c9a5cde6206feac6656cb8ff714dc16966e0620f8e212a26364a'
            '389ba34137bccfcd498092dfef7e7c5975de0a5b202a8846f31649622d0cb023'
            'eb9977e7e02dc894df903407aa454747c1c37b4739ba78226aa667919d7045f0'
            '69cb666e20639304fc865722cf18a29ee19ec23197db98c14dbcd45f5de6a58b'
            'dae56dd98ea74450ee816116608edac9a4a479fff1b5e5efed0fab12c44bbcca'
            '099001775afac771283c9bb05f513fd98ce528e110ba17c9f5c2cfde019441e1'
            '13fc785df882a60970b7b907366251baeb1ccb6d5d997589400f6cdb39b58a3f'
            '94c67a14faa0e0756798b54866c5b73de9e5a1b545a2624868d777ab9894408c'
            'b209580fe42142a66c687007db70e2a03b5628915c7c57d26b44acbc60716abb'
            'cad5474cc0ad030bdcb4cf7c9fda2aa021be294f6ceb9852112e8609ad07c5aa'
            'e2200d78c10babe1b365ac7b9a6d9a4389f62fd9a2a75d38a935b2c4cefd9b2d'
            'd0775637c54dfe4f4c75793a872d7d510d1770266e4119d78c03f0f301eede55'
            'd41f27eace227918d4e035b44cd8c92fa7d66e91c5f0db4f44495dc8f5dd2ad8'
            'e471b6b4d49ca75e357244ce1c0d5e95c09d5da7266b19c21503d7ac9ed3261e'
            '2bb7dd0cba966fe33f61db6c2760407f34def25c158b0b84da4fa6e1a22e1b78'
            '779aa88563df0da170c97644dc8c2bc3ea7fe21c1d1e021e0f7bb07bccaec8ce'
            'f69be01be3e6281ab847984045fe3ffb39a64ccc6d7ab58fb9f8f54ccaa951c1'
            'a2e89dd7e9db3e1315ba490b1425680b853842a77e0c29e791d19871a41dab38'
            '6f4314cb5625471e8095240c4ceff117070832aac3dee42074e21e8fdb4dc4eb'
            'c03605a0941fa776b9a72a56e94fe64e866870c0df6b87da729f150287ad48fc'
            'ede91271be8d403fb815cd2d63ba49df2db8e270d2e24b8527a0057e8c2218a8'
            '4419b89855888e134951f9723dc7b75b2f3ad0914e7a29a15e27e037161bb6ad'
            'df4eae5ca49fb3369823eb9c07104d6763aef823d782ba7399f0eefa50ceefd0'
            '3af1b5fe5167d47adcab2cc7f567484e825831d7cb79dadf0d48b5588ca14cb6'
            '7a5672b30fbc088d63217ddc50882529397b6fde27b0bbc80e905f429686c47a'
            'c78fa5ab7b92032eaaf2074d5ce6ee80daa1284a4fbbd75e9c57cc1aad8d4918'
            'd4f23acf9a90a518988a192313b85068a24f17c0ebfd06d5c01fe283994db809'
            '2b23e8ac7928f40646d0867e285aadb1bc2dd2d921daa84915193cc2c0f58dc8'
            '4dd81d424c3eb7098fa1dd06aea68385f693754467facffa017780f89075b237'
            'bfcaeef55a1e7e87f971e787be6f6ef76c141eee01804a4b67413e44b43d4076'
            '36fedce422e49f845e9e0bf466992bfec4841d5bb89710fcf6528088325b65ea'
            '7eda82af5aa0b2b0ec689d153ba1651bbe5630ea93fd0d97ce73bf6430bc34d2'
            '387b287ec4648a5fe24c118bfe08e462a8fdd603392b3df952870f5d2a930dd2'
            '1c17504e2a839b3b414c20520ede673b6864d3024a1be823064fc76e971e5ba1'
            'c297011c0a4a52046b25c5cecdec11bc855665a5fe7e5921eaa785a9fc31f6a0'
            '77628247f8855ea54ad5acbc36f02ddd05c74f2baa482f9d1fe09912a522e642'
            '5565b77672cac54551d679ba7f24d360913ad01996551e468a36c3e6db77ffc2'
            'eb5aaf0a0ea2073cade27fce868b7ef854eae7934ec4b90302f382fa15edfe59'
            '25948e8e4ed0fc63f0ce2ba5117d000983c6a1498bade9b1d12ef352c096d0e3'
            '7edc559278afc13b4b7fdfd9a36ede239982d1b168aa15bb77d21a032ebb0ed0'
            '672118b8682627f676794318b2a26d9af1ae24779835dc98107398597659c3b5'
            'a4493f7e5f49491858768547fd91e0e589bbfa69694cb159f7e21c0348fb37d9'
            'b22ad5b80f8e3c2e1721d320dad8e4020d175b4d8c688fc9bc954fa9df90c476'
            '1f73808cc5c8a4803e23035923696e47761d2ec62c08fdb0165d1e76f6edc7aa'
            'd615363dcf087d1fa2ae9a3d5d24883a832e8750de8dec9eb376f668483fbf4b'
            'dfcc228f5e1099f68bb2aaf54f23f8cca09a3e21c0df200c58283c29d4590de4'
            '8734e3e5fb0d0b03687d396b7d5a95c73c7d949acc0031e27c4d26bc33430141'
            'f462b36a22e7e05d904715e16f9649acf7ae75040518942b25e21c3d1750cc64'
            '5496756e6388149c8aca5ce077cfc0fd411d83c8e75041a49b4ad143404fc37d'
            'c5b7166cf2b6806c762844aeeac0bbe80c97afc4613488c2196a54d10eafccc4'
            'cff3cdef7b10b135078193a337b6b20b5a1d1ad94a1f755a6bda13936b95c7c3'
            '397eb486f22f2fc5694c779c57dc47eabda53638ae6d5a87af45cabfa6165435'
            '683a0b60dbcbf83c2918b6df9995418e283a6407c49302550be833d188c1ccb6'
            'b647e452907f1ff74247cc5675d69e929b316f982e26d4ae2012788f41461d20'
            '4e4acc15be68500acf2a5cf7c98b152b69edd5802ef539179b3c9e0e5e27e8e6'
            '9566aceba7a724f8776b1ed6664f60f004dc651e0c9278181791e3ff369cfb5a')

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
  optdepends=('crda: to set the correct wireless channels of your country'
              'linux-firmware: additional firmware')
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
