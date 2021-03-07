# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=RPi.GPIO
PKG_VERSION:=0.7.0
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
#PKG_SOURCE_URL:=https://ixpeering.dl.sourceforge.net/project/raspberry-gpio-python/$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_HASH:=7424bc6c205466764f30f666c18187a0824077daf20b295c42f08aea2cb87d3f

PKG_MAINTAINER:=Ben Croston <ben@croston.org>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.rst
#PKG_CPE_ID:=cpe:/a:doceme:spidev

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-rpi.gpio
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=RPI.GPIO
  URL:=http://sourceforge.net/projects/raspberry-gpio-python/
  DEPENDS:=+python3 +python3-setuptools
endef

define Package/python3-rpi.gpio/description
  A Python class to control the GPIO on a Raspberry Pi.
endef

$(eval $(call Py3Package,python3-rpi.gpio))
$(eval $(call BuildPackage,python3-rpi.gpio))
$(eval $(call BuildPackage,python3-rpi.gpio-src))
