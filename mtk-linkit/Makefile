# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.

include $(TOPDIR)/rules.mk

PKG_NAME:=mtk-linkit
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/mtk-linkit
  TITLE:=Modified MTK LinkIt Smart board support package
  DEPENDS:=@TARGET_brcm2708_bcm2710_RaspberryPi_3 \
  	+gdbserver +curl +strace +coreutils +coreutils-stty \
  	+avahi-nodbus-daemon +mountd +mjpg-streamer \
	+uhttpd +rpcd +rpcd-mod-iwinfo +git +git-http +samba36-server \
	+python +python-pyserial +python-pip +hidapi \
	+libmraa +libupm +node +node-hid +node-cylon-firmata +yunbridge \
	+luci +luci-theme-openwrt +luci-app-mjpg-streamer +luci-app-samba +luci-lib-json \
	+rpcd-mod-rpcsys +cgi-io +avrdude +spi-tools +uboot-envtools \
	+kmod-fs-vfat +kmod-fs-exfat +kmod-i2c-core \
	+kmod-nls-base +kmod-nls-cp437 +kmod-nls-iso8859-1 \
	+kmod-nls-iso8859-15 +kmod-nls-iso8859-2 +kmod-nls-utf8 \
	+kmod-sdhci +kmod-usb-storage \
	+kmod-video-core +kmod-video-uvc \
	+kmod-sound-core +kmod-sound-arm-bcm2835 +madplay-alsa +alsa-utils \
	+mtk-linkit-webui +tcpdump-mini +wireless-tools +libuci

  CATEGORY:=Base system
  DEFAULT:=y
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Compile
        true
endef

define Package/mtk-linkit/install
	$(INSTALL_DIR) $(1)/sbin
	
	$(CP) ./files/* $(1)
endef

$(eval $(call BuildPackage,mtk-linkit))
