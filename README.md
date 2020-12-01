## 介绍：

为NanoPi、OrangePi、Banana Pi、PINE64编译定制的OpenWRT固件,但是不提供树莓派型号支持。


- [安装过程](#安装过程)
- [使用说明](#使用说明)
- [提供Pi的型号有：}(#提供Pi的型号有：)
- [添加的插件](#添加的插件)
- [本OpenWRT特性](explain/support.md)
- [大致编译过程](explain/compile.md)
- [编译时选择插件列表说明](explain/luciapp.md)

##### 已经编译的多版本固件（不提供树莓派支持）
https://github.com/Wygdbb/OpenWRT-For-Pi/releases/tag/v0.4

##### NanoPi NEO2 大乱交  ---> 真的很强
https://github.com/Wygdbb/OpenWRT-For-Pi/releases/tag/v0.4.2

![nanopineo2](https://gitee.com/wygdbb/blog-image/raw/master/img/opgongneng.png)


##### 儿童节定制版NEO2轻NAS固件已经发布啦
https://github.com/Wygdbb/OpenWRT-For-Pi/releases/tag/v0.4.1


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
```
不提供树莓派支持！！！

Allwinner A64
[x] NanoPi NEO2
[x] NanoPi NEO Plus2
[x] Pine64 Plus
[x] Pine64 Sopine baseboard
[x] OrangePi PC2
[x] OrangePi Zero Plus

Allwinner A20/A3x/R40
[x] OrangePi ONE
[x] OrangePi Zero
[x] OrangePi PC
[x] OrangePi PC Plus
[x] BananaPi
[x] BananaPi Pro
[x] BananaPi-m2-ultra
[x] bananaPi-m2-plus
[x] NanoPi-neo
[x] Cubieboard2
```


#### 添加的插件：

```

|--系统
    |---TTYD终端
    |---Web管理
|--服务
    |---广告屏蔽大师 Plus+
    |---ShadowSocksR Plus+
    |---上网时间控制
    |---解锁网易云音乐[Go/Nodejs]
    |---动态DNS[DDNS]
    |---网络唤醒[Wol]
    |---Shairplay
    |---cpufreq
    |---Upnp
    |---Dnsforwarder
    |---FRP内网穿透
    |---网络共享[SMB4]
    |---KMS服务器
|--网络储存
    |---USB打印服务器
    |---硬盘休眠
    |---FTP服务器
|--VPN
    |---ZeroTier
|--网络
    |---Turbo ACC网络加速
|--带宽监控

```
