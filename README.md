# Make OpenWrt

**编译自己的 OpenWrt 系统：**

- 固件源码来源：https://github.com/coolsnowwolf/lede
- 插件源码来源：
  - https://github.com/xiaorouji/openwrt-passwall-packages.git
  - https://github.com/xiaorouji/openwrt-passwall2.git

- 通用配置：

```ini
CONFIG_TARGET_KERNEL_PARTSIZE=128
CONFIG_TARGET_ROOTFS_PARTSIZE=1024

CONFIG_PACKAGE_luci-app-passwall2=y
CONFIG_PACKAGE_luci-app-passwall2_INCLUDE_NaiveProxy=y

CONFIG_PACKAGE_luci-app-wireguard=y
CONFIG_PACKAGE_luci-app-docker=y
CONFIG_PACKAGE_luci-app-dockerman=y

# CONFIG_PACKAGE_luci-app-accesscontrol is not set
# CONFIG_PACKAGE_luci-app-ddns is not set
# CONFIG_PACKAGE_luci-app-ipsec-vpnd is not set
# CONFIG_PACKAGE_luci-app-vsftpd is not set
# CONFIG_PACKAGE_luci-app-wol is not set
# CONFIG_PACKAGE_luci-app-xlnetacc is not set
```

-  R2S：

```ini
CONFIG_TARGET_rockchip=y
CONFIG_TARGET_rockchip_armv8=y
CONFIG_TARGET_rockchip_armv8_DEVICE_friendlyarm_nanopi-r2s=y
```

- x86：

```ini
CONFIG_TARGET_x86=y
CONFIG_TARGET_x86_64=y
CONFIG_TARGET_x86_64_DEVICE_generic=y
```

