#
# Copyright (C) 2022 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=libucontext
PKG_VERSION:=1.3.2

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/kaniini/libucontext
PKG_SOURCE_VERSION:=$(PKG_NAME)-$(PKG_VERSION)
PKG_MIRROR_HASH:=eef55c05aca03c6d62672838638f49daa95ab8f9bf87126df32cedfe150e333c

PKG_LICENSE:=ISC
PKG_LICENSE_FILES:=LICENSE
PKG_CPE_ID:=

include $(INCLUDE_DIR)/host-build.mk
include $(INCLUDE_DIR)/meson.mk

CFLAGS="$(HOST_CFLAGS) -DEXPORT_UNPREFIXED"

MESON_HOST_ARGS += \
	-Ddefault_library=static

$(eval $(call HostBuild))
