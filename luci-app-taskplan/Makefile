include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-taskplan
LUCI_TITLE:=LuCI support for Task Plan setting
LUCI_PKGARCH:=all

PKG_VERSION:=2.2.2
PKG_RELEASE:=20250409

define Package/$(PKG_NAME)/conffiles
/etc/config/taskplan
endef

include $(INCLUDE_DIR)/package.mk

# call BuildPackage - OpenWrt buildroot signature
