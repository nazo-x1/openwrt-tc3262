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
FEATURES:=pci squashfs hwnat
CFLAGS:=-O2 -pipe -mips32r2 -mtune=1004kc
SUBTARGETS:=en7528

# BOARD_CPPFLAGS:=-D__EN7528__
KERNEL_PATCHVER:=5.15

define Target/Description
	Build firmware image for boards decending from TrendChip TC3262
	Including EcoNet EN7528
endef

# include the profiles
include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES+=kmod-ensoc_eth kmod-mips-wdt kmod-mt7603 kmod-mt76x2

$(eval $(call BuildTarget))
