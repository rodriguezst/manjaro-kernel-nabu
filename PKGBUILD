# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux60
pkgver=6.0.4
pkgrel=1
_kernelname=-MANJARO-ARM
_basekernel=6.0
_newversion=false
_stopbuild=false     # Will also stop if ${_newversion} is true
_desc="AArch64 multi-platform"
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc')
options=('!strip')
source=("http://www.kernel.org/pub/linux/kernel/v6.x/linux-${pkgver}.tar.xz"
        '1001-arm64-dts-allwinner-add-hdmi-sound-to-pine-devices.patch'            # A64-based devices
        '1002-arm64-dts-allwinner-add-ohci-ehci-to-h5-nanopi.patch'                # Nanopi Neo Plus 2 (by Furkan?)
        '1003-drm-bridge-analogix_dp-Add-enable_psr-param.patch'                   # Pinebook Pro;  From list: https://patchwork.kernel.org/project/dri-devel/patch/20200626033023.24214-2-shawn@anastas.io/ (no updates since June 2020) (schedule for removal in 6.1-rc1)
        '1004-gpu-drm-add-new-display-resolution-2560x1440.patch'                  # Odroid;  Not upstreamable
        '1005-panfrost-Silence-Panfrost-gem-shrinker-loggin.patch'                 # Panfrost (preference patch, might not be upstreamable)
        '1006-arm64-dts-rockchip-Add-Firefly-Station-p1-support.patch'             # Firefly Station P1 (by Furkan)
        '1007-rk3399-rp64-pcie-Reimplement-rockchip-PCIe-bus-scan-delay.patch'     # RockPro64 (by @nuumio, perhaps upstreamable?)
        '1008-arm64-dts-amlogic-add-initial-Beelink-GT1-Ultimate-dev.patch'        # Beelink GT1 Ultimate (by Furkan) (applied in linux-next)
        '1009-arm64-dts-amlogic-add-meson-g12b-ugoos-am6-plus.patch'               # Meson Ugoos (by Furkan)
        '1010-arm64-dts-rockchip-Add-PCIe-bus-scan-delay-to-RockPr.patch'          # RockPro64 (relies on patch 1007)
        '1011-drm-rockchip-support-gamma-control-on-RK3399.patch'                  # RK3399 VOP;  From list: https://patchwork.kernel.org/project/linux-arm-kernel/cover/20211019215843.42718-1-sigmaris@gmail.com/ (applied in linux-next)
        '1012-arm64-dts-rockchip-switch-to-hs200-on-rockpi4.patch'                 # Radxa Rock Pi 4;  Temporary hotfix, not for upstreaming (by Dragan)
        '1013-arm64-dts-rockchip-Add-PCIe-bus-scan-delay-to-Rock-P.patch'          # Radxa Rock Pi 4 (relies on patch 1007)
        '1014-ASOC-sun9i-hdmi-audio-Initial-implementation.patch'                  # Allwinner H6 HDMI audio (by Furkan)
        '1015-arm64-dts-allwinner-h6-Add-hdmi-sound-card.patch'                    # Allwinner H6 HDMI audio (by Furkan)
        '1016-arm64-dts-allwinner-h6-Enable-hdmi-sound-card-on-boards.patch'       # Allwinner H6 HDMI audio (by Furkan)
        '1017-arm64-dts-allwinner-add-OrangePi-3-LTS.patch'                        # Orange Pi 3 LTS (by Furkan)
        '1018-arm64-dts-rockchip-add-rk3568-station-p2.patch'                      # Firefly Station P2 (by Furkan)
        '1019-Add-support-for-the-Hardkernel-ODROID-M1-board.patch'                # Odroid M1; From list: https://patchwork.kernel.org/project/linux-rockchip/list/?series=680647
        '1020-arm64-dts-meson-radxa-zero-add-support-for-the-usb-t.patch'          # Radxa Zero (by Furkan)
        '1021-arm64-dts-rockchip-add-OrangePi-4-LTS.patch'                         # Orange Pi 4 LTS (by Furkan)
        '1022-Add-YT8531C-phy-support.patch'                                       # Motorcomm PHY (by Furkan)
        '1023-add-phy-rockchip-Support-PCIe-v3.patch'                              # Rockchip; (applied in linux-next) 
        '1024-arm64-dts-rockchip-rk3568-Add-PCIe-v3-nodes.patch'                   # Rockchip; (applied in linux-next) 
        '2001-staging-add-rtl8723cs-driver.patch'                                  # Realtek WiFi;  Not upstreamable
        '2002-brcmfmac-USB-probing-provides-no-board-type.patch'                   # Bluetooth;  Will be submitted upstream by Dragan
        '2003-arm64-dts-rockchip-Work-around-daughterboard-issues.patch'           # Pinebook Pro microSD;  Will be submitted upstream by Dragan
        '3001-irqchip-gic-v3-add-hackaround-for-rk3568-its.patch'                  # Quartz64 and associated patches that are still being upstreamed: START
        '3002-arm64-dts-rockchip-Enable-video-output-on-Quartz64-B.patch'          # (applied in linux-next)
        '3003-arm64-dts-rockchip-Add-hdmi-cec-assigned-clocks-to-r.patch'
        '3004-arm64-dts-rockchip-Add-PCIe-support-to-Quartz64-B.patch'
        '3005-arm64-dts-rockchip-Add-Quartz64-B-eeprom.patch'
        '3006-arm64-dts-rockchip-Add-PCIe-support-to-SoQuartz-CM4-.patch'
        '3007-arm64-dts-rockchip-Enable-video-output-on-SoQuartz-C.patch'
        '3008-dt-bindings-Add-Rockchip-rk817-battery-charger-suppo.patch'          # (applied in linux-next)
        '3009-mfd-Add-Rockchip-rk817-battery-charger-support.patch'                # (applied in linux-next)
        '3010-power-supply-Add-charger-driver-for-Rockchip-RK817.patch'            # (applied in linux-next)
        '3011-drm-panel-simple-Add-init-sequence-support.patch'
        '3012-arm64-dts-rockchip-Move-Quartz64-A-to-mdio-setup.patch'
        '3013-arm64-dts-rockchip-Add-Quartz64-A-battery-node.patch'
        '3015-arm64-dts-rockchip-Add-HDMI-sound-node-to-Quartz64-B.patch'          # (applied in linux-next)
        '3016-arm64-dts-rockchip-Add-HDMI-sound-node-to-SoQuartz-C.patch'
        '3017-arm64-dts-rockchip-Add-PCIe-2-nodes-to-quartz64-b.patch'             # Quartz64 and associated patches that are still being upstreamed: END (applied in linux-next)
        '3018-arm64-dts-rockchip-Enable-video-output-on-rk3566-roc-pc.patch'       # Station M2; (by Furkan)
        '3019-board-rock3a-gmac1.patch'
        'config')
md5sums=('74ac1c85195834015c0f1e0389b273ae'
         '9aa0591c2d601a104d664a802a44728c'
         'e6fe272dc95a1c0a8f871924699fea16'
         '9f27b2a05eaeb1995fc0fcf6a8b923c4'
         '6f592c11f6adc1de0f06e5d18f8c2862'
         'f8f0b124c741be61d86bea8d44e875f9'
         '564136ab1c75b6dc67be02b54e695ae5'
         '245858f26512dfc48adbf509b6fc8364'
         '3384afa63fcfec1661dcb4a5e13a4b2a'
         '1b92d7617e60d3c525a4b18ab4351185'
         '28982d87c45ed8f5aab966d82f8455d8'
         '19e2279811700cd8aa4ab326603d2f61'
         'a0f649f78c857a01e1680b89b58b05eb'
         'a0cf3209d3f856522ef14c4618837ae7'
         '680aec843f385e7233763d37b98ed2e0'
         'f666606de61576007a756e6e80e1f1fe'
         '717c673c7caa564fc06e76ff9a0eebaa'
         'e285b47405d8eab611ba17bcbf2f9cbf'
         'aca8e5610b67e054176b6ff02c4830b0'
         'e621a901ec9a313a5465903196bfbb85'
         '9799998aa9b72fae2eb55e92d840dad5'
         '227466ec46ffce1684835c87640c46c2'
         '77200aa6b89276b9035f13c4bb422b98'
         '8cf60a66691809a648a1c763a62ec5de'
         '37221482c9228c84cfd7f969d9735740'
         '9f2deefc9cd4f6b07386fc866ba76ff8'
         'd2654df7fc87e5c874505a2d98cbce1c'
         '59c20ef6082f4b4c6b54c4f532931ff4'
         'a829e0d4711d8feff5fee1973938b25a'
         'b10035b89284bff674fab588bc9a6630'
         '467b3ff965db6867f4289f5d256ca93e'
         'a136e3196eadbfd182652be0c04701c8'
         '56605685714f21646f88fbc187a4bf47'
         '5829f0ed70aa5e506f175d9bca5fe8f1'
         '6083ec098a6401c8ba0172ed46d8a753'
         '396bddfe770b2211d49810d587ab2d68'
         '7064a13bc729ace382027dec0b18b0aa'
         '1a34dd9c8fb49b974c2cbeb9aaa0de46'
         '742bcd8aa51845850a8e5144221ea770'
         '61ed22ed1254727bd97902ce849d3df4'
         'fa9babdfffadf76454b00fc22593eaba'
         'a2271452ecf71f2ee160ad76f8bcadef'
         '7a39de5aa1c29e81d03096c2f9163456'
         '92d5c7dd3052f5d7a670bd06213d75fb'
         'b241ca1a4566d37bd29cde8db238762d'
         'e8ea5b4f0937c3799a846991a9259b4b'
         'c73904a3eab2bb8e1cfa63e501abefa5')

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

  cd "linux-${pkgver}"

  # Assorted Manjaro ARM patches
  apply_patches 1

  # Assorted Pinebook, PinePhone and PineTab patches
  apply_patches 2
  
  # Assorted rk356x patches
  apply_patches 3

  # Apply our kernel configuration
  cat "${srcdir}/config" > .config

  # Add pkgrel to extraversion
  sed -ri "s|^(EXTRAVERSION =)(.*)|\1 \2-${pkgrel}|" Makefile

  # Don't run depmod on "make install", we'll do that ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh
}

build() {
  cd "linux-${pkgver}"

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

  cd "linux-${pkgver}"
  
  KARCH=arm64

  # get kernel version
  _kernver="$(make LOCALVERSION= kernelrelease)"

  mkdir -p "${pkgdir}"/{boot,usr/lib/modules}
  make LOCALVERSION= INSTALL_MOD_PATH="${pkgdir}/usr" INSTALL_MOD_STRIP=1 modules_install

  # systemd expects to find the kernel here to allow hibernation
  # https://github.com/systemd/systemd/commit/edda44605f06a41fb86b7ab8128dcf99161d2344
  cp arch/$KARCH/boot/Image "${pkgdir}/usr/lib/modules/${_kernver}/vmlinuz"

  # Used by mkinitcpio to name the kernel
  echo "${pkgbase}" | install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_kernver}/pkgbase"
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

  cd "linux-${pkgver}"
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
