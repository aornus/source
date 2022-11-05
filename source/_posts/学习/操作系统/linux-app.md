---
title: linux 开源播客客户端评测
tags:
  - 奇技淫巧
categories:
  - 学习
  - 软件编程
cover: ../../../../images/bg.jpg
description: 播客客户端
abbrlink: linuxapp
date: 2021-12-20 10:15:02
update: 2022-02-25 20:20:20
katex:
comments:
copyright:
aside:
password:
hidden:
---

> 声明：我没有资格对这些开源软件评头论足，只是作为使用者的看法。

## Vocal-（为现代桌面而生，播客客户端巨作）

![Vocal](../../../../images/blogimage/raw/master/Aornus_shot_20211220_102138.png)

主要从iTunes获取播客，外观很现代，可以管理订阅，在线播放，离线下载，也可以导入订阅列表。

![主界面](../../../../images/blogimage/raw/master/Aornus_shot_20211220_102626.png)

![详细页面](../../../../images/blogimage/raw/master/Aornus_shot_20211220_102545.png)

## gPodder-（古老的免费播客客户端）

![gPodder](../../../../images/blogimage/raw/master/Aornus_shot_20211220_102038.png)

确实很强大，在很多软件里都有gpodder的插件，同步功能很强大，但我就是不能注册，真令人头痛，明明官网好好的，可能被滥用以至于停止注册了，客户端里搜索太慢。总是卡住，不是太好用。

## Gonme podcast

很简单，很现代，但是很慢！无法在线播放，只能下载之后播放。

## Spotify

这个不必多说，声田本身就是一个很好的播客客户端，包括流媒体，下载，同步等各种功能，唯一不能做的就是外部网站的订阅。

## 终极解决方案：Clemencine

内存占用不大，反应快速，功能强大。

囊括了网络收音机，网盘音乐播放，podcast订阅...等等等各种东西，单网络电台而言，二十四小时不重样，新闻，音乐，一辈子都听不完。

这里推荐几个自带的能用的电台源：

1. https://www.radio-browser.info/ 分类详细，中国的频道也很全，跨越国界，跨越文化。
2. SomaFM 頻道不多，主要是电子音乐。
3. ICEcast 很细致，按风格流派分，简直能跟spotify想媲美。

回到播客上，其功能如图所示，可以在自带的播客源中搜索，也可以倒入OPML文件。

![搜索界面](../../../../images/blogimage/raw/master/20211222202212.png)

![播放页面](../../../../images/blogimage/raw/master/20211222211953.png)

## 微信客户端

> 写于时间：2021-12-31 21:40:17

下午看RSS订阅时,发现微信linux版居然官宣了，起初不信，但看到优麒麟的广告，不由得信了，我只希望不要跟QQlinux2008那般破烂。这是微信linux在Arch里的描述：

![aur](../../../../images/blogimage/raw/master/202112312124189.png)

废话不多说，软件装起来。

## 微信安装

本人使用的Garuda linux,去年发行的arch系，个人感觉比manjaro跟漂亮，更安全（文件系统默认`btrfs`），各种工具都包装好了，简直就是一个开源软件大杂烩，这个教程理论上适用于所有Arch系的操作系统。

1. 安装yay包管理器

```shell
sudo pacman -Syu && sudo pacman -S yay
```

2. 安装原生微信

```shell
yay -S com.tencent.weixin 
```

> 软件包 com.tencent.weixin-2.1.1-5
>
> 全部安装大小：  423.39 MiB

## 评测

* 支持群聊，文件与图片发送，*输入好像有问题，每修改一次，光标自动回到句尾了*

* 不支持搜索，公众号，小程序，纯粹的一个聊天软件

* 每次登陆需要扫码

* 不能停留后台

![](../../../../images/blogimage/raw/master/202112312130578.png)

![](../../../../images/blogimage/raw/master/202112312132942.png)

>  下次更新不知道要到猴年马月了