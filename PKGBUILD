# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux61-nabu
pkgver=6.1.114
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
sha256sums=('2286e4a02ea2fbe65023dbf779f20aa994ba2b8d37ed559049378089451aa256'
            '71b9b068832aa44e3dd5809c2d21d346e639e9f14a31eef2d2bc8ee8f1a5b5c6'
            '820eb917c1af55828aeadb7f522d937b414a265a8960041030fb9f0e4c04e140'
            '922278d4a3905fabc7cae09b03269ff1b9a34c8d60f0f9cf82bb2c3642daa39b'
            'd7a2399764db66dc6c5cf9c12686b3ef863effdf5b2a1a343277d07436f0892a'
            '937c6557b0b5cad593879c45dcf2f626dba793dd5cc8f0e3f9071199183efccb'
            '03d36cd4b09c77d68b554d94e61375965c237ada9944c914a6867c21e586d86b'
            'e6943a6f87b82bd92f3ac0dca8a3dc7eb492708f6ef2522add788b41e546f8dd'
            '9b14cd316c5cc4c940917cbdf6fdfb94309b3edab5c00acd356ea97d9c4c7150'
            '788cc855603e0246ee965f49f8b58b23386d3815345b18ff46f98002ca7d01c6'
            '0ae220b17adcda50f7b6fc65fb8dd9ad2da792b83741934e530c59029ac8bce4'
            '084fe01f89a950cd3af76f008e77dc39b366694930890404615a5337525116e1'
            '2011110f0ba3874b884a1de178eb9155ac9a061a02f35c679dd3c6d5b4bfde8f'
            '73f4ffffd25671ff964f7a6cfb967de49bdc266f55a284cac8a413b0b896a9ad'
            'f82e10d2c2bf13701160c87834b6c708bf630400ef9180645ebfe27771877ab6'
            'f27cfec1cbce0c82828718a98284fbd250cdfbf1a58d6be0955d380f9b354827'
            '4f2635a9cc159081194038aee17d6abbcd33207c1b19f425207ea76bb53badf7'
            'c47c5eaf0237471c22a636a32638d3b16b260b58a61a653451534beb54fb4aaa'
            '82058f874d767971e511b066fb1c1824a952562e02dd87c7753eb03d68bbe613'
            '43ae94a2716fc764f8f5ee8b44da8485ad18762f8ad78170897b123dfe534aa1'
            'e229004574eef376111f02f3c6a666ec814b44398480fc80c4448d8b70a7ab3e'
            'ea0ca4e5acf08d3f10cb5ca40e1d8ccf4c2e7f00b708b1c3001e9ad7f69e1309'
            'ccb59e3631134a3746c97ad07980c85269c2455c1fe8dd2b278c1084121f940e'
            '09fb0ce99c5d3bc5f74c8a5cc93b99430a9ef54ae5813bb80d92c0a222ef8209'
            '504163b191cb13dd7aee4d10737ecbbda947ead86140a425847974e4de35edc2'
            'e8fae3267549c1a8620295c435bcd0df1fc3bf6552f6f96fcb93bce1dc704bc1'
            '6f321a17ed27db0f2e9504e9024c0b5ad7d20462d42406113fb7a5ebf08bb656'
            'e0d41a306557e2c878d670e2275ffc8fbfbb60492125b602f751053cdf80d2b6'
            '1be1f6c7454d896de339287d2d185eddaa4189687fe7bc2d59d06e4fb1f971e6'
            'a2133a5142260dd4b6d8aa878c5e360693fcd366eaea1c1815ca5a114228ec99'
            'fa755e892133c951b1c0de0f8394c1d3c71bb5df645d9e32600f6eaf023490db'
            '7d69ac2f2578aad9e25e98decb7462dd73f64d515d59126822ed9792875e373e'
            '9cec4f13243e9a7f4c8f3c7a5e30d0a766437848b6add8f9dd9265ab16d3b68a'
            '6399f144ed956e522bffd443804f6c433ac891b2dac6a0ac7e96a2f7718f4e3a'
            '59db324143e506117877611a8b4fdf49436c25da8369f630eefb07ffefcbff73'
            '98c812522ba70751a97f78b4a609cab3209098ad7f9932406609549f88de83e6'
            '5d45cea7b61cb2618719d86693dc61aa913c97103035e4fbc11b096f3a0a2054'
            'c55676ec3e751ab1c0b9f0e1b968a22def046e59b7b71f8c459f02975ab6b664'
            'bfe8c113955481702a4d68815a0f1fb6e9240d50792e54cc12a84ac351dfb903'
            '374fffe3399f2b72abf6cbf46a41017527ae89b281f3c02d3817d2d28253fdbc'
            '4971a0a711712103680bedd30ca9af921aa0a1215a83afc7e5a123352e5d0f79'
            'de8fa23d4cd1ba55fe62834beda68912c9565da3cfa3b9b7a7d2b9d55775b5fe'
            '45a9891040d326f9f32c8bd268e1f82a63b17d69a5ff5f2e4c8b7cb0241fca3b'
            'dcd5b252cf28f2ae8222b897f819adff9d234565a77a02491d9eb88e7cbab4b6'
            '72b6f9671d9d018f0e3dc0c1ead40ea68fe47b4313e38f122b3ed6ce03dedad4'
            'db461e201d7107a68fa702c12350d4d735c37f394214d8b1146cce670e236f89'
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
