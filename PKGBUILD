# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux
pkgver=6.6
pkgrel=1
_newversion=false
_stopbuild=false     # Will also stop if ${_newversion} is true
_srcname="linux-${pkgver/%.0/}"
_kernelname="${pkgbase#linux}"
_desc="AArch64 multi-platform"
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc')
options=('!strip')
source=("https://cdn.kernel.org/pub/linux/kernel/v6.x/${_srcname}.tar.xz"
        '1001-arm64-dts-allwinner-add-ohci-ehci-to-h5-nanopi.patch'                # Nanopi Neo Plus 2 (by Furkan?)
        #'1002-gpu-drm-add-new-display-resolution-2560x1440.patch'                  # Odroid;  Not upstreamable Does not apply in 6.4
        '1003-panfrost-Silence-Panfrost-gem-shrinker-loggin.patch'                 # Panfrost (preference patch, might not be upstreamable)
        '1004-arm64-dts-rockchip-Add-Firefly-Station-p1-support.patch'             # Firefly Station P1 (by Furkan)
        '1005-rk3399-rp64-pcie-Reimplement-rockchip-PCIe-bus-scan-delay.patch'     # RockPro64 (by @nuumio, perhaps upstreamable?)
        '1006-arm64-dts-amlogic-add-meson-g12b-ugoos-am6-plus.patch'               # Meson Ugoos (by Furkan)
        '1007-arm64-dts-rockchip-Add-PCIe-bus-scan-delay-to-RockPr.patch'          # RockPro64 (relies on patch 1005)
        #'1008-arm64-dts-rockchip-switch-to-hs200-on-rockpi4.patch'                 # Radxa Rock Pi 4;  Temporary hotfix, not for upstreaming (by Dragan)
        '1009-arm64-dts-rockchip-Add-PCIe-bus-scan-delay-to-Rock-P.patch'          # Radxa Rock Pi 4 (relies on patch 1005)
        #'1010-arm64-dts-rockchip-add-rk3568-station-p2.patch'                      # Firefly Station P2 (by Furkan) - Failed to Apply on 6.3
        '1011-arm64-dts-meson-radxa-zero-add-support-for-the-usb-t.patch'          # Radxa Zero (by Furkan)
        #'1012-pwm-meson-Explicitly-set-.polarity-in-.get_state.patch'              # Meson; Temp fix for boot issues added in 6.2.11
        '2001-staging-add-rtl8723cs-driver.patch'                                  # Realtek WiFi;  Not upstreamable Failed to compile on 6.3 - Need to Update
	#'2003-arm64-dts-rockchip-Work-around-daughterboard-issues.patch'           # Pinebook Pro microSD;  Will be submitted upstream by Dragan - Failed to apply on 6.3, already present.
        '2004-arm64-dts-allwinner-add-hdmi-sound-to-pine-devices.patch'            # Allwinner HDMI Sound; (by Dan)
        #'3001-irqchip-gic-v3-add-hackaround-for-rk3568-its.patch' 		# Failed to apply on 6.4
        #'3002-arm64-dts-rockchip-Lower-sd-speed-on-soquartz.patch'		# Failed to apply on 6.3
        '3003-arm64-dts-rockchip-Add-hdmi-cec-assigned-clocks-to-r.patch'
        #'3004-arm64-dts-rockchip-rk356x-update-pcie-io-ranges.patch'               # From https://github.com/neggles/linux-quartz64/commit/2c1e3811e6d7430f7d46dbb01d3773192c51cdcf (by Neggles) Applied already
        '3005-arm64-dts-rockchip-Add-Quartz64-B-eeprom.patch'
        #'3006-arm64-dts-rockchip-Enable-pcie2-and-audio-jack-on-rk3566-roc-pc.patch'  # Station M2; (by Furkan) (applied in linux-next) - Failed to apply on 6.3
        '3007-arm64-dts-rockchip-Move-Quartz64-A-to-mdio-setup.patch'
        '3008-arm64-dts-rockchip-Add-Quartz64-A-battery-node.patch'
        '3009-board-rock3a-gmac1.patch'                                            # Rock 3A; Ethernet. Based on Armbian patch
        #'3010-drm-rockchip-dw_hdmi-Add-4k-30-support.patch'                        # Rockchip; from list: https://patchwork.kernel.org/project/linux-rockchip/list/?series=722440 Failed to Apply on 6.4
        #'4001-arm64-dts-rk3399-pinebook-pro-Fix-USB-PD-charging.patch'             # Pinebook Pro series from Megi START
        #'4002-arm64-dts-rk3399-pinebook-pro-Improve-Type-C-support-on-Pinebook-Pro.patch'
        #'4003-arm64-dts-rk3399-pinebook-pro-Remove-redundant-pinctrl-properties-from-edp.patch'
        #'4004-arm64-dts-rk3399-pinebook-pro-Remove-unused-features.patch'
        #'4005-arm64-dts-rk3399-pinebook-pro-Dont-allow-usb2-phy-driver-to-update-USB-role.patch'
        #'4006-arm64-dts-rockchip-rk3399-pinebook-pro-Support-both-Type-C-plug-orientations.patch'
        #'4007-ASoC-codec-es8316-DAC-Soft-Ramp-Rate-is-just-a-2-bit-control.patch'
        #'4008-arm64-dts-rk3399-pinebook-pro-Fix-codec-frequency-after-boot.patch'
        #'4009-arm64-dts-rockchip-rk3399-pinebook-pro-Fix-VDO-display-output.patch'
        'config'
        'linux.preset'
        '60-linux.hook'
        '90-linux.hook')
md5sums=('452098d80ba925af3a4ab35998f3aef5'
         'e6fe272dc95a1c0a8f871924699fea16'
         'f8f0b124c741be61d86bea8d44e875f9'
         '564136ab1c75b6dc67be02b54e695ae5'
         '0892035d83463c736df7ad0290e1c6f9'
         '1b92d7617e60d3c525a4b18ab4351185'
         '28982d87c45ed8f5aab966d82f8455d8'
         'a0cf3209d3f856522ef14c4618837ae7'
         'e9377e7295ebd76cc68b9dd42891c0c8'
         '538e0aa76c44e2f7e0e883a11758e72d'
         '9aa0591c2d601a104d664a802a44728c'
         '467b3ff965db6867f4289f5d256ca93e'
         '56605685714f21646f88fbc187a4bf47'
         '61ed22ed1254727bd97902ce849d3df4'
         'fa9babdfffadf76454b00fc22593eaba'
         '8fb62d56ea03359cf3999564e3dab15f'
         'b13b7cef6656ea4495ac420919d0a7ff'
         '86d4a35722b5410e3b29fc92dae15d4b'
         'ce6c81ad1ad1f8b333fd6077d47abdaf'
         '3dc88030a8f2f5a5f97266d99b149f77')

prepare() {
  apply_patches() {
      local PATCH
      for PATCH in "${source[@]}"; do
          PATCH="${PATCH%%::*}"
          PATCH="${PATCH##*/}"
          [[ ${PATCH} = $1*.patch ]] || continue
          msg2 "Applying patch: ${PATCH}..."
          patch -N -p1 < "../${PATCH}"
      done
  }

  cd ${_srcname}

  # Assorted Manjaro ARM patches
  apply_patches 1

  # Assorted Pinebook, PinePhone and PineTab patches
  apply_patches 2
  
  # Assorted rk356x patches
  apply_patches 3

  # Pinebook Pro patches by Megi: https://github.com/torvalds/linux/compare/master...megous:linux:pbp-6.2
  # apply_patches 4

  # Apply our kernel configuration
  cat "${srcdir}/config" > .config

  # Add pkgrel to extraversion
  sed -ri "s|^(EXTRAVERSION =)(.*)|\1 \2-${pkgrel}|" Makefile

  # Don't run depmod on "make install", we'll do that ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh
}

build() {
  cd ${_srcname}

  # Get the kernel version
  if [[ "${_newversion}" = false ]]; then
    make prepare
  fi

  # Configure the kernel; adjust the line below to your choice
  # or simply manually edit the ".config" file
  if [[ "${_newversion}" = true ]]; then
    make menuconfig   # CLI menu for configuration
  fi
  #make nconfig       # New CLI menu for configuration
  #make xconfig       # X-based configuration
  #make oldconfig     # Using old config from previous kernel version

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

  # Generate device tree blobs with symbols to support
  # applying device tree overlays in U-Boot
  make ${MAKEFLAGS} DTC_FLAGS="-@" dtbs
}

_package() {
  pkgdesc="The Linux Kernel and modules - ${_desc}"
  depends=('coreutils' 'kmod' 'initramfs')
  optdepends=('crda: to set the correct wireless channels of your country'
              'linux-firmware: additional firmware')
  provides=('kernel26' "linux=${pkgver}")
  conflicts=('kernel26' 'linux')
  replaces=('linux-armv8' 'linux-aarch64')
  backup=("etc/mkinitcpio.d/${pkgbase}.preset")
  install=${pkgname}.install

  cd ${_srcname}

  KARCH=arm64

  # get kernel version
  _kernver="$(make kernelrelease)"
  _basekernel=${_kernver%%-*}
  _basekernel=${_basekernel%.*}

  mkdir -p "${pkgdir}"/{boot,usr/lib/modules}
  make INSTALL_MOD_PATH="${pkgdir}/usr" modules_install
  make INSTALL_DTBS_PATH="${pkgdir}/boot/dtbs" dtbs_install
  cp arch/$KARCH/boot/Image "${pkgdir}/boot"

  # make room for external modules
  local _extramodules="extramodules-${_basekernel}${_kernelname}"
  ln -s "../${_extramodules}" "${pkgdir}/usr/lib/modules/${_kernver}/extramodules"

  # add real version for building modules and running depmod from hook
  echo "${_kernver}" |
    install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_extramodules}/version"

  # remove build and source links
  rm "${pkgdir}"/usr/lib/modules/${_kernver}/{source,build}

  # now we call depmod...
  depmod -b "${pkgdir}/usr" -F System.map "${_kernver}"

  # sed expression for following substitutions
  local _subst="
    s|%PKGBASE%|${pkgbase}|g
    s|%KERNVER%|${_kernver}|g
    s|%EXTRAMODULES%|${_extramodules}|g
  "

  # install mkinitcpio preset file
  sed "${_subst}" ../linux.preset |
    install -Dm644 /dev/stdin "${pkgdir}/etc/mkinitcpio.d/${pkgbase}.preset"

  # install pacman hooks
  sed "${_subst}" ../60-linux.hook |
    install -Dm644 /dev/stdin "${pkgdir}/usr/share/libalpm/hooks/60-${pkgbase}.hook"
  sed "${_subst}" ../90-linux.hook |
    install -Dm644 /dev/stdin "${pkgdir}/usr/share/libalpm/hooks/90-${pkgbase}.hook"
}

_package-headers() {
  pkgdesc="Header files and scripts for building modules for linux kernel - ${_desc}"
  provides=("linux-headers=${pkgver}")
  conflicts=('linux-headers')
  replaces=('linux-aarch64-headers')

  cd ${_srcname}
  local _builddir="${pkgdir}/usr/lib/modules/${_kernver}/build"

  install -Dt "${_builddir}" -m644 Makefile .config Module.symvers
  install -Dt "${_builddir}/kernel" -m644 kernel/Makefile

  mkdir "${_builddir}/.tmp_versions"

  cp -t "${_builddir}" -a include scripts

  install -Dt "${_builddir}/arch/${KARCH}" -m644 arch/${KARCH}/Makefile
  install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 arch/${KARCH}/kernel/asm-offsets.s
  install -Dt "${_builddir}" -m644 vmlinux 

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
  strip $STRIP_STATIC "${_builddir}/vmlinux"
  
  # remove unwanted files
  find ${_builddir} -name '*.orig' -delete
}

pkgname=("${pkgbase}" "${pkgbase}-headers")
for _p in ${pkgname[@]}; do
  eval "package_${_p}() {
    _package${_p#${pkgbase}}
  }"
done
