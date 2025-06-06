include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-taskplan
PKG_VERSION:=2.2.2
PKG_RELEASE:=20250409
LUCI_TITLE:=LuCI support for Task Plan setting
LUCI_PKGARCH:=all
LUCI_DEPENDS:=+luci-base

# 添加 TITLE 字段
define Package/$(PKG_NAME)
    SECTION:=luci
    CATEGORY:=LuCI
    SUBMENU:=3. Applications
    TITLE:=LuCI support for Task Plan setting
    PKGARCH:=all
    DEPENDS:=+luci-base
endef

define Package/$(PKG_NAME)/conffiles
/etc/config/taskplan
endef

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)/install
    $(INSTALL_DIR) $(1)/www/luci-static/taskplan
    $(CP) ./htdocs/* $(1)/www/luci-static/taskplan/ 2>/dev/null || true
    $(INSTALL_DIR) $(1)/usr/lib/lua/luci/i18n
    $(CP) ./po/* $(1)/usr/lib/lua/luci/i18n/ 2>/dev/null || true
    $(INSTALL_DIR) $(1)/
    $(CP) ./root/* $(1)/ 2>/dev/null || true
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
