## 介绍：

为NanoPi、OrangePi、Banana Pi、PINE64编译定制的OpenWRT固件,但是不提供树莓派型号支持。

**最新固件增加qmi支持，可以做4g路由**

- [安装过程](#安装过程)
- [使用说明](#使用说明)
- [提供Pi的型号有:](#支持的型号：)  比之前提供更多的Pi型号支持
- [添加的插件](#添加的插件)
- [本OpenWRT特性](explain/support.md)
- [大致编译过程](explain/compile.md)
- [编译时选择插件列表说明](explain/luciapp.md)
- [发行说明](#发行说明)

最新固件地址；https://github.com/Wygdbb/OpenWRT-For-Pi/releases

#### 过时固件，建议下载烧录最新固件（最新固件基于Lienol）
```
##### 已经编译的多版本固件（不提供树莓派支持）
https://github.com/Wygdbb/OpenWRT-For-Pi/releases/tag/v0.4

##### NanoPi NEO2 大乱交  ---> 真的很强
https://github.com/Wygdbb/OpenWRT-For-Pi/releases/tag/v0.4.2

##### 儿童节定制版NEO2轻NAS固件已经发布啦
https://github.com/Wygdbb/OpenWRT-For-Pi/releases/tag/v0.4.1
```

![nanopineo2](https://gitee.com/wygdbb/blog-image/raw/master/img/opgongneng.png)

![NanoPi NEO2](https://images.gitee.com/uploads/images/2020/0328/215207_b2c5a598_6514114.png "OpenWRT.png")



#### 安装过程：

```
Windows: win32diskimager
Linux:   sudo dd bs=4M if=openwrt.xxx.img of=/dev/sdb
```

#### 使用说明：
```
1. 默认Web管理地址： 192.168.1.1
2. root/password
3. 内存卡 > 512m 
```

#### 支持的型号：

**相比之前提供编译的Pi型号增多**
```
不提供树莓派支持！！！

Allwinner A64
[x] Nanopi NEO Plus2 (H5)
[x] Nanopi NEO2 (H5)
[x] Pine64 Plus A64
[x] Pine64 Sopine
[x] Xunlong Orange Pi PC2
[x] Xunlong Orange Pi Zero Plus

Allwinner A20/A3x
[x] OrangePi R1
[x] OrangePi Plus
[x] OrangePi ONE
[x] OrangePi Zero
[x] OrangePi PC
[x] OrangePi PC Plus
[x[ OrangePi 2
[x] Sinovoip Banana Pi M2 Plus
[x] Olimex A20-Olinuxino Micro
[x] Olimex A20-OLinuXino-LIME2-eMMC
[x] Olimex A20-OLinuXino-LIME2
[x] Olimex A20-OLinuXino-LIME
[x] Mele M9 top set box
[x] LinkSprite pcDuino3
[x] LeMaker Banana Pro
[x] LeMaker Banana Pi
[x] Lamobo R1
[x] FriendlyArm NanoPi M1 Plus
[x] FriendlyARM NanoPi NEO
[x] Cubietech Cubietruck
[x] Cubietech Cubieboard2
```


#### 添加的插件：

**if 有不合理或者需要增加的插件，请issues**
```
luci-app-adbyby-plus
luci-app-adguardhome
luci-app-advanced-reboot
luci-app-ahcp
luci-app-aria2
luci-app-arpbind
luci-app-attendedsysupgrade
luci-app-autoreboot
luci-app-baidupcs-web
luci-app-ddns
luci-app-diskman
luci-app-dockerman[Docker-CE/ttyd]
luci-app-firewall
luci-app-filetransfer
luci-app-frpc
luci-app-hd-idle
luci-app-https-dns-proxy
luci-app-kodexplorer
luci-app-mwan3
luci-app-mwan3helper
luci-app-nlbwmon
luci-app-noddos
luci-app-nps
luci-app-ntpc
luci-app-pagekitec
*** luci-app-passwall[ss/ssr/xray/v2ray/Trojan_Plus/Trojan_GO/Brook/NaiveProxy/kcptun/haproxy/ChinaDNS-NGHttps DNS Proxy(DoH)/dns2socks
luci-app-ramfree
luci-app-samba4
luci-app-sfe
luci-app-shairplay
luci-app-smartdns
luci-app-syncthing
luci-app-transmission
luci-app-ttyd
luci-app-unblockmusic[go&nodejs]
luci-app-usb-printer
luci-app-verysync
luci-app-vlmcsd
luci-app-vsftpd
luci-app-wrtbwmon
luci-app-zerotier
```

#### 发行说明

```
 - 2020.12.01 目前提供多版本固件支持，之后不久会做一次全面的重新编译调整，可能会取消H2芯片固件的编译，需要的请去 多版本 中下载

```
