## 本人编译的OpenWRT对文件系统，命令工具的一些支持。

#### 特点说明：
###### 全部固件均支持ipv6
```
1.文件系统支持
    - udf [macOS/Linux/Windows 都支持读写，DVD格式，怎么格式化U盘为udf：https://github.com/JElchison/format-udf]
    - ntfs
    - squashfs
    - vfat [默认]
    - ext4 [默认]
    - exfat [默认]

2. USB2/3支持[未添加SMB自动挂载]
    - 增加qmi支持，可以做4g路由
    - kmod-usb-core
    - kmod-usb-net
    - kmod-usb-net-qmi-wwan
    - kmod-ohci
    - kmod-usb-serial-option
    - kmod-usb2
    - kmod-usb3
    - kmod-uhci
3. 添加的工具
    - nano
    - curl
    - htop
    - screen
    - vim-fuller
    - lsblk
    - wget
4. 多主题
    - argon-dark-mod
    - argon-light-mod
    - material
    - bootstrap-mod
    - freifunk-generic
    - bootstrap-blue
5. USB无线网卡需要自己手动添加驱动
```
