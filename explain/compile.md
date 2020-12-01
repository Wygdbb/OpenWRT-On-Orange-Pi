### 大致编译过程
1.[编译环境搭建](https://www.wygdbb.com/2020/05/19/diy-openwrt-for-pi/)
2.[编译深度定制](https://www.wygdbb.com/2020/05/19/diy-openwrt-for-pi-plus/)

- 完整的编译步骤：

```
# 编译环境Ubuntu19.04
sudo apt-get install build-essential subversion git-core libncurses5-dev zlib1g-dev gawk flex quilt libssl-dev xsltproc libxml-parser-perl mercurial bzr ecj cvs unzip

sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint

git clone https://github.com/coolsnowwolf/lede
echo "src-git lienol https://github.com/Lienol/openwrt-package" >> feeds.conf.default
./scripts/feeds update -a
./scripts/feeds install -a
make defconfig
make menuconfig
make download V=s
make V=99 # 或者 make -j1 V=s    //推荐

make -j$(($(nproc) + 1)) V=s    //第二次编译
make -j8 V=s
make -j5 V=99 2>&1 |tee build.log |grep -i error
```

- 编译单个插件步骤：
```
./scripts/feeds update -a 
cd package
git clone https://github.com/maxlicheng/luci-app-unblockmusic.git
cd ..
./scripts/feeds install -a
make menuconfig
#在luci->application选中插件,编译
make package/luci-app-unblockmusic/compile V=99
```

- 参考：
  - lede(coolsnowwolf):https://github.com/coolsnowwolf/lede
  - luci-app-unblockmusic(maxlicheng):https://github.com/maxlicheng/luci-app-unblockmusic
  - https://mlapp.cn/374.html

```
