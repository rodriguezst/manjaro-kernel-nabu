# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux61-nabu
pkgver=6.1.98
pkgrel=1
_kernelname=-MANJARO-ARM
_basekernel=6.1
_srcname="linux-${pkgver/%.0/}"
_newversion=false
_stopbuild=false     # Will also stop if ${_newversion} is true
_defconfig=xiaomi_nabu_defconfig
_desc="AArch64 multi-platform"
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc' 'aarch64-linux-gnu-gcc' 'aarch64-linux-gnu-binutils')
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
    'config' )
sha256sums=( '97cdc9127c7700556ea0891267a0c24cf372f4b81636fb8203a914f3a69f3406'
    '03ecfc9445d08f2a3d0b7608f28a4752e542e124f8b3c688df3031556a3dd69d'
    '63ca96ae49de42de0f9b40ee7805d132a9285946dae63d92072db8824cc1688f'
    '50b355cde945ba3559204019a898f7b989706484fe7a4d2768cde393abb889d7'
    'ddf12b90621ef72bc229ef286c4f440bbeceb9039bb42fe440a14b51512b46eb'
    'fe1defa75ac97aa064842c5ed0a68d6c8d6a16654c9dbb042283464fc281c7f7'
    'ce953ef5011faf9b359c54517c4c125529fddfc43970fb88cf5479c6bdff5ec0'
    'a9fdea566c8fe5fe011c821e965b627baa5af1a5e10ed461436cce990dfa924a'
    '0b9035103a4152af57148cc80e18b8eae930194f4f32e5cf4ed6ef3e5ed82f42'
    '5fe9f2fff95c0996326c02a97c23425062955ed2c0babddeb903e1425b67bf39'
    '4eba7f6bb5710a358b684a26658f4ee3efcb80b3bbf458488ca0ef63f6210957'
    '638bd53df7965b89385ec0fd75be8e4cb410378874c0c0ee6dcbd7a607c38029'
    '5de8c3fbd849d4f2f237bf2fe8263e4d459a6905f29a6c9fb5ea450b843e3c86'
    '7950c8c7a157aca8e0f719474157c9ab53b37e1bbd4727e342d91335e92e7990'
    '86229e25bf2d5b0174cc88dcdc51a6ce7ea1076dd8ea190e041441acd1b46334'
    '631a59d8d9fec681695e5f0706ee053e2216ab62c5b1b3f0cbaee5342bca2ec7'
    '58cca017262497ed509aba2028cb4f00c9ed992c25a267d4132753ae89d90b4b'
    '31b2e25938d1ee31221dd14a7f3d564f26cd043d4f9eb009af0281bfe294750b'
    '783b042fa643c3551d4e30b8602f1b369c302579abac05f48058594721ca6290'
    'bb658a388aa84ff65175f06017984cfdf9edc7a08fa01e0d27283fe03347545c'
    '15eee21cb2792ef7bac823505a561e6eebfcc6276815c059ce2e8ec963b663c2'
    '6352e886a70130b64fc55c6c269b179db4a20f4daadd9ff6baf71510c74a8127'
    'dc60c03c014172c0a2024980350f441ee1ce7fc611489858ee47f458b5a4bdb5'
    '4c061b5387355ac8ea629262936cb266a0948ba420d328fb39efb956e2e8f195'
    '4d8a84030899d3739808f1e8930f252480fa4b1a137cdce188553ff56ec8e1fc'
    '805ff35cf31687478c79f53d313d172f0f7d86120c1f9236239404305c761b03'
    'c390b0044e517c6c419a29ea4841ba0771612e5be83046eab709c14a63b91f48'
    'a46ce5681725e5ee7613149c42d9f724f4120236d74ecd487426dbe21e3a778d'
    '44a32ae52b29af6db58bb2d5176d25a2b3e7f28ccaeead25e6d68f6259963e64'
    '40e7ba21204e1c7531740a8c065c8c6379cdba0e40e70c342fb5e8a9677c07c5'
    'b9aef19bbeaccc23ca595475f0d39c6b6a06559d4c5da38db245674415e5f87b'
    'a1e8026253dba959222ba6b8aa0966916ef90e6c3b132570fa9d8f271a637713'
    '3750e2d00fc371a63e76cd6b5df940cc81a7aec2187fb3947c18cdb23eb3d1de'
    '7e51fdff4fd92253a898b9707e7f291902bdb76247a52c7a2b6cbefd3eff68fc'
    'f282bc5daeaacd65383f195faca473176d5648f88c14a8f6aa6ed479a994ce78'
    'cbb00342edbd73f9f52ef954a394c84a7fac350ebe378096a667328e9e4f6abf'
    'b9f3792555fcacf3b284e367eb257ad4e568a3d2f75510106d87fd09f03ab385'
    '72c451a6d31e8333bc9d8ca49bbfcf8772b7597d95651ee6fbdc5f4371d56f86'
    '0b29e702b734ae2535a54d07aa46f92c782767f932e03bdd6f4f74d1d7e8d0cd'
    'a1717f78384505cbd437804811d950b259138b0fa18577bf72b51455b1717a85'
    '05170bef67c824a30b79e0c1fb2e0b867a91e8a8b1d9ca0f0125d472615a4914'
    '240d043f1142dd66c34b92d87e680dd63850aec6d0914b5d8d5a110397314480'
    'eeafed0c13b3b1050362c143c7bc274721b6088315c00773d1509621be9ef908'
    '5826b94f17b79aaa20274abbe4837e918338126962303364d8ee77fbbce86d7e'
    '9032497b5b1acb1f85e3e77c9409770dee5d941f6dc3a55fb6ded88c22e510c8'
    'e067bd89d598102041504d8a5dd2b59df049d13efdde738790e29cf05a89679a'
    'cf8d74c5434ba08d1103e5ac01b78313da2376804765168931695bba845b6817' )

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
  make ${MAKEFLAGS} Image modules
}

_package() {
  pkgdesc="The Linux ${_basekernel} Kernel and modules - ${_desc}"
  depends=('coreutils' 'kmod' 'initramfs')
  optdepends=('crda: to set the correct wireless channels of your country'
              'linux-firmware: additional firmware')
  provides=("linux=${pkgver}")
  backup=("etc/mkinitcpio.d/${pkgbase}.preset")
  install=${pkgname}.install

  cd "${_srcname}"
  
  KARCH=arm64

  # get kernel version
  _kernver="$(make LOCALVERSION= kernelrelease)"

  mkdir -p "${pkgdir}"/{boot,usr/lib/modules}
  make LOCALVERSION= INSTALL_MOD_PATH="${pkgdir}/usr" INSTALL_MOD_STRIP=1 modules_install

  # systemd expects to find the kernel here to allow hibernation
  # https://github.com/systemd/systemd/commit/edda44605f06a41fb86b7ab8128dcf99161d2344
  cp arch/$KARCH/boot/Image "${pkgdir}/usr/lib/modules/${_kernver}/vmlinuz"

  # Used by mkinitcpio to name the kernel
  echo "${_kernver}" | install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_kernver}/pkgbase"
  echo "${_basekernel}-${CARCH}" | install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_kernver}/kernelbase"

  # add kernel version
  echo "${pkgver}-${pkgrel}-MANJARO-ARM aarch64" > "${pkgdir}/boot/${pkgbase}-${CARCH}.kver"

  # make room for external modules
  local _extramodules="extramodules-${_basekernel}${_kernelname:--MANJARO-ARM}"
  ln -s "../${_extramodules}" "${pkgdir}/usr/lib/modules/${_kernver}/extramodules"

  # add real version for building modules and running depmod from hook
  echo "${_kernver}" |
    install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_extramodules}/version"

  # remove build and source links
  rm "${pkgdir}"/usr/lib/modules/${_kernver}/{source,build}

  # now we call depmod...
  depmod -b "${pkgdir}/usr" -F System.map "${_kernver}"
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
