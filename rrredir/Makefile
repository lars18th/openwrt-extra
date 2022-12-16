include $(TOPDIR)/rules.mk

PKG_NAME:=rrredir
PKG_RELEASE:=2

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/lars18th/rrredir.git
PKG_SOURCE_DATE:=2022-12-16
PKG_SOURCE_VERSION:=f475a140c5236cd8a8f626317c5f934e1d7c1a41
PKG_MIRROR_HASH:=skip

PKG_MAINTAINER:=Andy Walsh <andy.walsh44+github@gmail.com>
PKG_LICENSE:=MIT License
PKG_LICENSE_FILES:=COPYING

include $(INCLUDE_DIR)/package.mk

define Package/rrredir
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Routing and Redirection
  TITLE:=RR Redir - Round-Robin Port Redirector.
  DEPENDS:=+libpthread
endef

define Package/rrredir/description
  This is a port redirector program like the well-known redir,
  but with the ability to specify more than one target ip/port
  which will be tried one after the other in round-robin fashion, until the connection succeeds.
endef

define Package/rrredir/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/rrredir $(1)/usr/bin/
endef

$(eval $(call BuildPackage,rrredir))
