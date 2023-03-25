#
# Copyright (C) 2021 Keenetic Limited
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

ARCH:=mips
BOARD:=tc3262
BOARDNAME:=TC3262 / EN75xx
FEATURES:=squashfs usb usbstorage hwnat
CFLAGS:=-O2 -pipe -mips32r2 -mtune=34kc
SUBTARGETS:=en7526

# BOARD_CPPFLAGS:=-D__EN7526__
KERNEL_PATCHVER:=5.15

define Target/Description
	Build firmware image for boards decending from TrendChip TC3262
	Including EcoNet EN7526
endef

# include the profiles
include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES+=kmod-ensoc_eth kmod-mips-wdt

$(eval $(call BuildTarget))
