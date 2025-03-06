include $(TOPDIR)/rules.mk

PKG_NAME:=go-dispatch-proxy
PKG_VERSION:=1
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/lars18th/go-dispatch-proxy.git
PKG_SOURCE_VERSION:=e69d9421014f2ed9a2e7b436240d3ed12c0c19dd
PKG_SOURCE_DATE:=2025-03-06
PKG_HASH:=skip

PKG_MAINTAINER:=Andy Walsh <andy.walsh44+github@gmail.com>
PKG_LICENSE:=MIT License
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1
PKG_BUILD_FLAGS:=no-mips16

GO_PKG:=github.com/extremecoders-re/go-dispatch-proxy

include $(INCLUDE_DIR)/package.mk
#include ../../lang/golang/golang-package.mk
include ../lang/golang/golang-package.mk

define Package/go-dispatch-proxyr
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Routing and Redirection
  TITLE:=go-dispatch-proxy - SOCKS5 load balancing proxy
  URL:=https://github.com/extremecoders-re/go-dispatch-proxy
endef

define Package/go-dispatch-proxy/description
  A SOCKS5 load balancing proxy to combine multiple internet connections into one.
  It can also be used as a transparent proxy to load balance multiple SSH tunnels.
endef

define Package/go-dispatch-proxy/install
  $(call GoPackage/Package/Install/Bin,$(PKG_INSTALL_DIR))
  $(INSTALL_DIR) $(1)/usr/bin/
  $(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/go-dispatch-proxy $(1)/usr/bin/
#  $(INSTALL_DIR) $(1)/etc/config/
#  $(INSTALL_CONF) $(CURDIR)/files/go-dispatch-proxy.config $(1)/etc/config/go-dispatch-proxy
#  $(INSTALL_DIR) $(1)/etc/init.d/
#  $(INSTALL_BIN) $(CURDIR)/files/go-dispatch-proxyr.init $(1)/etc/init.d/go-dispatch-proxy
endef

$(eval $(call GoBinPackage,go-dispatch-proxy))
$(eval $(call BuildPackage,go-dispatch-proxy))
