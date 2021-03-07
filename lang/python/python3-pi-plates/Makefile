# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=pi-plates
PKG_VERSION:=7.1
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=68910d7c91b982828e0ba062c92c87153ff617d0f5cfe0bf59d3be36a2777f06

PKG_MAINTAINER:=Jerry Wasinger <support@pi-plates.com>
PKG_LICENSE:=BSD
#PKG_LICENSE_FILES:=LICENSE.rst
#PKG_CPE_ID:=cpe:/a:doceme:spidev

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-pi-plates
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=pi-plates
  URL:=https://www.pi-plates.com/
  DEPENDS:=+python3 +python3-setuptools +python3-spidev +python3-rpi.gpio
endef

define Package/python3-spidev/description
  A python module for interfacing with pi-plates devices.
endef

$(eval $(call Py3Package,python3-pi-plates))
$(eval $(call BuildPackage,python3-pi-plates))
$(eval $(call BuildPackage,python3-pi-plates-src))
