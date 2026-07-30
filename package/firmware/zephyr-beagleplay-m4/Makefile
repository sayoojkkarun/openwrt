# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=zephyr-beagleplay-m4
PKG_RELEASE:=1

PKG_MAINTAINER:=Sayooj K Karun <sayooj@aerlync.com>
PKG_LICENSE:=Apache-2.0

include $(INCLUDE_DIR)/package.mk

define Package/zephyr-beagleplay-m4
  SECTION:=firmware
  CATEGORY:=Firmware
  TITLE:=Zephyr RPMsg demo firmware for the BeaglePlay Cortex-M4F
  DEPENDS:=@TARGET_ti_k3
endef

define Package/zephyr-beagleplay-m4/description
  Prebuilt Zephyr RTOS image for the AM625 MCU-domain Cortex-M4F remote
  processor, based on Zephyr's openamp_rsc_table sample. Proves the
  remoteproc/RPMsg pipeline by echoing messages back to Linux's
  rpmsg_client_sample.ko test module and backing an rpmsg_tty channel.
endef

define Build/Compile
	true
endef

define Package/zephyr-beagleplay-m4/install
	$(INSTALL_DIR) $(1)/lib/firmware
	$(INSTALL_DATA) \
		./files/am62-mcu-m4f0_0-fw \
		$(1)/lib/firmware/am62-mcu-m4f0_0-fw
endef

$(eval $(call BuildPackage,zephyr-beagleplay-m4))
