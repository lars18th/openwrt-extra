#include $(TOPDIR)/rules.mk
#
#PKG_NAME:=socks-proxy-balancer
#PKG_VERSION:=5
#PKG_RELEASE:=1
#
#PKG_SOURCE_PROTO:=git
#PKG_SOURCE_URL:=https://github.com/David-Lor/socks-proxy-balancer.git
#PKG_SOURCE_DATE:=2022-03-28
#PKG_HASH:=skip
#
#PKG_MAINTAINER:=Andy Walsh <andy.walsh44+github@gmail.com>
#PKG_LICENSE:=MIT License
#PKG_LICENSE_FILES:=COPYING
#
#PKG_BUILD_DEPENDS:=golang/host
#PKG_BUILD_PARALLEL:=1
#PKG_BUILD_FLAGS:=no-mips16
#
#GO_PKG:=github.com/David-Lor/socks-proxy-balancer
##GO_PKG_BUILD_PKG:=github.com/David-Lor/socks-proxy-balancer/src
#
#include $(INCLUDE_DIR)/package.mk
#include ../../lang/golang/golang-package.mk
#CGO_ENABLED:=0
#
#define Package/socks-proxy-balancer
#  SECTION:=net
#  CATEGORY:=Network
#  SUBMENU:=Routing and Redirection
#  TITLE:=socks-proxy-balancer
#  URL:=https://github.com/showwin/speedtest-go
#endef
#
#define Package/socks-proxy-balancer/description
#  A SOCKS5 load balancing proxy that combines multiple SOCKS5 proxies into one.
#endef
#
#define Package/socks-proxy-balancer/install
#  $(call GoPackage/Package/Install/Bin,$(PKG_INSTALL_DIR))
#  $(INSTALL_DIR) $(1)/usr/bin/
#  $(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/socks-proxy-balancer $(1)/usr/bin/
#  $(INSTALL_DIR) $(1)/etc/config/
#  $(INSTALL_CONF) $(CURDIR)/files/socks-proxy-balancer.config $(1)/etc/config/socks-proxy-balancer
#  $(INSTALL_DIR) $(1)/etc/init.d/
#  $(INSTALL_BIN) $(CURDIR)/files/socks-proxy-balancer.init $(1)/etc/init.d/socks-proxy-balancer
#endef
#
#$(eval $(call GoBinPackage,socks-proxy-balancer))
#$(eval $(call BuildPackage,socks-proxy-balancer))
#
# Copyright (C) 2021 ImmortalWrt.org

include $(TOPDIR)/rules.mk

PKG_NAME:=speedtest-go
PKG_VERSION:=1
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/showwin/speedtest-go/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=70a2937d0759820fe7ee8f61b960d60c07b34c0d783ed11c0065b68fe2964aea

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=TeleostNaCl Dai <teleostnacl@gmail.com>

PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1
PKG_BUILD_FLAGS:=no-mips16

GO_PKG:=github.com/showwin/speedtest-go

include $(INCLUDE_DIR)/package.mk
include ../../lang/golang/golang-package.mk

define Package/speedtest-go
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Test Internet Speed
  URL:=https://github.com/showwin/speedtest-go
  DEPENDS:=$(GO_ARCH_DEPENDS) +ca-bundle
endef

define Package/speedtest-go/description
  Command Line Interface and pure Go API to
  Test Internet Speed using speedtest.net
endef

$(eval $(call GoBinPackage,speedtest-go))
$(eval $(call BuildPackage,speedtest-go))
