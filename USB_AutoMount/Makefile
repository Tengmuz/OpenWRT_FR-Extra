#
# Copyright (C) 2014 huanet <hua.net@163.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=usb_automount
PKG_VERSION:=2014-06-03
PKG_RELEASE:=1
PKG_MAINTAINER:=huanet <hua.net@163.com>
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git@github.com:huanet/OpenWRT_USBAutoMount.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=43554dbe410d33163bbcc3d06815296a08ef1fc6
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/usb_automount
  SECTION:=firefly-extra
  CATEGORY:=Firefly-Extra
  TITLE:=Auto mount the usb disk.
  URL:=https://github.com/huanet/OpenWRT_USBAutoMount
  PKGARCH:=all
endef

define Build/Compile
endef

define Package/usb_automount/install
	$(INSTALL_DIR) $(1)/etc/hotplug.d/block
	$(CP) $(PKG_BUILD_DIR)/automount $(1)/etc/hotplug.d/block/30-mount
endef

$(eval $(call BuildPackage,usb_automount))
