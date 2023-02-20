---
title: linux 常用命令记录
tags:
  - 奇技淫巧
categories:
  - 学习
  - "\U0001F4BB操作系统"
cover: /images/top-5-linux-shells-and-how-to-install-them.jpg
description: 解决的不仅仅是一个问题，而是整个世界！--Sun
abbrlink: linuxnote
date: 2021-08-02 18:31:36
updated:
keywords:
copyright:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
highlight_shrink:
---

## 方法
### debian/ubuntu/raspberry 扩充root空间
1. 用cfdisk扩充/dev/mmcblk0空间
2. 用`resize2fs /dev/mmcblk0p2`修复分区
## Snap

  ```
   snap list                   列出所有已安装的snap软件包
   snap find <keyword>         按照keyword来寻找可以安装的snap软件包
   snap install <software>           安装软件
   snap refresh <software>           更新软件
   snap refresh all                  更新所有的软件
   snap remove <software>            卸载软件
   snap revert <software>            将软件还原到之前的版本
  ```

> 错误：
>
> ```bash
> error: cannot list snaps: cannot communicate with server: Get "http://localhost/v2/snaps": dial unix /run/snapd.socket: connect: no such file or directory
> ```
>
> 原因：未启动snapd服务
>
> 解决方法：
>
> ```shell
> sudo systemctl start snapd
> ```

## Pacman

- pacman -S 包名：安装多个包，需以空格分隔包名。  
- pacman -Sy 包名：与上面命令不同的是，该命令将在同步包数据库后再执行安装。
- pacman -Sv 包名：在显示一些操作信息后执行安装。
- pacman -U：安装本地包，其扩展名为 pkg.tar.gz。
- `pacman -U: http://www.example.com/repo/example.pkg.tar.xz 安装一个远程包（不在 pacman 配置的源里面）`   

---------

-  pacman -R 包名：该命令将只删除包，保留其全部已经安装的依赖关系
-  `pacman -Rs 包名：在删除包的同时，删除其所有没有被其他已安装软件包使用的依赖关系`
-  pacman -Rsc 包名：在删除包的同时，删除所有依赖这个软件包的程序
-  pacman -Rd 包名：在删除包时不检查依赖。

------

-  pacman -Ss 关键字：在仓库中搜索含关键字的包。
-  pacman -Qs 关键字： 搜索已安装的包。
-  pacman -Qi 包名：查看有关包的详尽信息。
-  pacman -Ql 包名：列出该包的文件。

------

-  pacman -Sw 包名：只下载包，不安装。
-  pacman -Scc：清理所有的缓存文件
-  ~~pacman -Sc~~：清理未安装的包文件，包文件位于 /var/cache/pacman/pkg/ 目录。

> 上面为不推荐命令，会删除所有旧版本包，正确的清理方式如下[^1]  
> 查看占用空间：
>
> ```shell
> du -sh /var/cache/pacman/pkg/ 
> ```
>
> 清理占用：
>
> ```shell
> sudo paccache -r -k 1
> ```

## Node.js

```
node -v 查看版本

npm -v

npm install -g npm 更新npm

npm cache clean -f 清除npm缓存

npm install -g n 安装n模块

n stable 升级node.js到最新稳定版
```

## SSH使用

### ssh参数说明

* -c：选择所加密的密码型式 （blowfish|3des 预设是3des）
* -F：指定ssh指令的配置文件
* **-i：指定身份文件（预设是在使用者的家目录 中的 .ssh/identity）**
* -l：指定连接远程服务器登录用户名
* **-p：指定远程服务器上的端口（默认22）**
* -q：静默模式
* -t：强制配置 pseudo-tty
* -v：打印更详细信息
* -L listen-port:host:port 指派本地的 port 到达端机器地址上的 port

### ssh-keygen 参数说明

* -B	显示指定的公钥/私钥文件的摘要。
* **-b    指定密钥长度。对于RSA密钥，最小要求768位，默认是2048位。**DSA密钥必须恰好是1024位(FIPS 186-2 标准的要求)。
* **-C	提供一个新注释**
* -c    要求修改私钥和公钥文件中的注释。。
* **-f	指定密钥文件名。**
* -l	显示公钥文件的指纹数据。它也支持 RSA1 的私钥。对于RSA和DSA密钥，将会寻找对应的公钥文件，然后显示其指纹数据。
* -N	提供一个新的密语。
* -p	要求改变某私钥文件的密语而不重建私钥。程序将提示输入私钥文件名、原来的密语、以及两次输入新密语。
* -t	指定要创建的密钥类型。可以使用："rsa1"(SSH-1) "rsa"(SSH-2) "dsa"(SSH-2)
* -y	读取OpenSSH专有格式的公钥文件，并将OpenSSH公钥显示在 stdout 上。

下面举一个例子：生成4200位的RSA密钥。

```shell 例子：
ssh-keygen -t rsa -b 4200 -C "redmi10@termux" -f redmi10
```

> ssh连接成功但用ssh，`gitclone`仍然失败的解决办法:在`.ssh/`下创建`config`，内容如下：
>
> ```
> Host github.com
> HostName github.com
> User aornus(用户名)
> IdentityFile ~/.ssh/私匙名
> IdentitiesOnly yes
> 
> Host gitee.com
> HostName gitee.com
> User aornus(用户名)
> IdentityFile ~/.ssh/私匙名
> IdentitiesOnly yes
> ```

## Git使用

- git init - 初始化仓库。
- git add . - 添加文件到暂存区。
- git commit - 将暂存区内容添加到仓库中。

> ![git](https://www.runoob.com/wp-content/uploads/2015/02/011500266295799.jpg)

## 杂项

* 查看字体：`fc-list`  

* 更新grub：   

```
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

* 强制清空回收站： 

```
sudo rm -rf ~/.local/share/Trash/*
```

* latex指定编译命令： 

```
% !TeX program = xelatex
```

> 使用htlatex可以把文档编译成html格式

###  Pandoc使用：

[pandoc 强大的文档格式转换工具 | Omics - Hunter](https://evvail.com/2021/02/02/2184.html)


[^1]:[The Recommended Way To Clean The Package Cache In Arch Linux](https://ostechnix.com/recommended-way-clean-package-cache-arch-linux/) 