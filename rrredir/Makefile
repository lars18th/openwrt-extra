include $(TOPDIR)/rules.mk

PKG_NAME:=rrredir
PKG_RELEASE:=3

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/lars18th/rrredir.git
PKG_SOURCE_DATE:=2025-03-04
PKG_SOURCE_VERSION:=75ff13f9b528047562cfeee477184a0bb9b1cc3f
PKG_MIRROR_HASH:=6c829865aed2a30373cf61e61f7a58e31c189864b5b0aa8f1534f973b005bf01

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
