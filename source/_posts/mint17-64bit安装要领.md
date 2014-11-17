title: mint17 64bit安装要领
date: 2014-11-17 19:02:38
tags:
- mint
- linux
- 环境配置
categories:
- 技术
---
打算作移动项目的时候也用 mint，用家里的老 mint 环境配置了下 cordova,结果发现开 android 模拟器的时候电脑硬件跟不上了（2G内存的老电脑）。
没办法只好在windows的机器上在装个 mint 成 dual OS。8G内存，GTX560ti,i5,几年前配的主机，当时花了4K，羡煞同学。由于不是第一安装 mint ，基本上算是轻车熟路。下面就说下几个安装时候的关键点。
<!-- more -->
## 如何dual OS
目前是 windows7+mint, 据说 windows8+mint同样可以（不需要那个easybcd)，我还没试过，有机会补上。
推荐做法是，在windows中找个剩余空间比较大的分区（d,e那种），然后用 windows 自带的硬盘分区工具对指定的分区进行压缩（压缩掉的空间就是以后用来安装 mint 的），80G其实就够了，
mint 可以 mount windows 的分区，所以空间不是问题。压缩完毕就OK下一步了。
## 安装介质（USB）
mint 系统本身带有USB镜像写入工具。利用它准备好U盘镜像，然后bois设置USB启动。
## live usb
启动后是直接进入U盘中的 mint 系统，提供了基本的系统功能，可以用它体验下 mint。
启动桌面上的安装系统程序，选择中文包，选在双系统安装选项，然后就OK了。
## 安装过程
安装中需要联网，下载一些其他的包，其中中文包可以 skip 节约安装时间。
完成后需要重启，重启前会有黑底白字提示把USB拔出，照着作即可。
## 系统更新
进入系统后会看到有很多包需要更新，在更新前现配置个163的更新源，速度比直接连美国的快很多。
开始菜单->系统管理->软件源->官方仓库->基础(trusty)中添加个中国的源就可以了。
然后更新起来就快了。
## 中文输入法
有搜狗linux版，但是那东西我没搞成。还是用ibus，基本上够用了。开始菜单->软件管理器中搜索 ibus,
找到 ibus-pinyin 安装下然后 logout 下就OK了。需要注意的是，如果用终端安装的话，则需要安装 ibus 的核心包，
直接 `sudo apt-get install ibus-pinyin` 是不会自动安装所依赖的ibus包。
## chrome
由于天朝GFW这个只有三条路可选:  
- 代理下载  
- 开VPN下载  
- 百度云的离线下载(^_^)  

## 编辑器
sublime text 其实非常好，非常优秀，但是ibus无法在编辑的时候输入中文(ST 居然放任这个 BUG 一直不修复)。
退而求其次，ATOM 其实也不错，在 mint 上我用它替代 sublime text。
## 二进制编辑器
windows 上有 winhex, linux 上有 ghex,够用了。
