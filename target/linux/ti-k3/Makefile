# SPDX-License-Identifier: GPL-2.0-only
#
# Copyright (c) 2026 Aerlync Labs Inc.

include $(TOPDIR)/rules.mk

BOARD:=ti-k3
BOARDNAME:=TI K3
FEATURES:=ext4 usb usbgadget fpu audio squashfs rootfs-part boot-part
SUBTARGETS:=am625

KERNEL_PATCHVER:=6.18

define Target/Description
	Build firmware images for TI K3-based boards (AM62x and later K3
	generation SoCs).
endef

include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES += uboot-envtools partx-utils e2fsprogs kmod-gpio-button-hotplug

KERNELNAME:=Image dtbs

$(eval $(call BuildTarget))
