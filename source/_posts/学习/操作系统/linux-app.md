---
title: 栈选软件总录
tags:
  - Linux
  - 安卓
categories:
  - 学习
  - 软件编程
cover: ../../../../images/bg.jpg
description: 各个平台软件推荐及个别加速下载地址汇集
abbrlink: apps
swiper_index: 6
date: 2021-12-20 10:15:02
update: 2022-11-29 20:20:20
katex:
comments:
copyright:
aside:
password:
hidden:
---
{% markmap 400px %}
<!-- @import "[TOC]" {cmd="toc" depthFrom=2 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [声音可视化](#声音可视化)
  - [cava](#cava)
  - [Recidia](#recidia)
  - [glava-git](#glava-git)
  - [projectm-pulseaudio](#projectm-pulseaudio)
  - [Panon](#panon)
- [播客](#播客)
  - [Vocal-（为现代桌面而生，播客客户端巨作）](#vocal-为现代桌面而生播客客户端巨作)
  - [gPodder-（古老的免费播客客户端）](#gpodder-古老的免费播客客户端)
  - [Gonme podcast](#gonme-podcast)
  - [Spotify](#spotify)
  - [Clemencine](#clemencine)
- [社交](#社交)
  - [微信客户端](#微信客户端)
    - [微信安装](#微信安装)
    - [评测](#评测)
- [其他软件](#其他软件)
  - [Spotify](#spotify-1)
  - [Nekogram](#nekogram)
  - [Obsidian](#obsidian)

<!-- /code_chunk_output -->
{% endmarkmap %}
## 声音可视化
### cava
基于终端的的ALSA[^1]音频可视化工具。
主要控制方式是在进入界面后按以下按键：
* Up ------>        体高灵敏度
* Down ------>      降低灵敏度
* Left  ------>     减少分割栏数
* Right  ------>   增大分割栏数
* r  ------>        重载配置文件
* c  ------>        仅仅重载颜色
* f  ------>       循环前景色
* b  ------>       循环背景色
* q  ------>       退出
![](/images/20221012/pic-28232152.png)
### Recidia
默认模式相对于cava多了很多可控性。（自带的“宇宙”背景很烧内存。）
![](images/20221012/pic-29001731.png)
### glava-git
以驱动OpenGL，绘制一个音频可视化的窗口。这个很有意思，使用`-d`指令可以直接在桌面上添加一个类似挂件的可视化频谱，很是实用。其效果与cava差不多，都是对称分布的频谱。
![](images/20221012/pic-29000736.png)
### projectm-pulseaudio
ProjectM(M计划)是一个基于Milkdrop插件Windows/Winamp的开源音乐可视化工具。它现在有一个QtGUI，除了libvisual组件外，它还可以通过JACK或PulseAudio[^2]可视化音频输出。这个很好玩，在GUI里按m可以打开菜单，有几个自带的插件：
1. 魔性小人
	![](/images/20221012/pic-28235721.png)
2. Fractal坠落
	![](/images/20221012/pic-28235926.png)
其他的几个都比较花哨，颜色比较混乱。
### Panon
虽然它只是KDE的一个插件，但是里面的特效贼好看

![](/images/20221012/pic-29002743.png)
![](/images/20221012/pic-29002442.png)
[^1]:ALSA是Advanced Linux Sound Architecture的缩写，高级Linux声音架构的简称,它在Linux操作系统上提供了音频和MIDI（Musical Instrument Digital Interface，音乐设备数字化接口）的支持。
[^2]:PulseAudio（以前叫Polypaudio）是一个跨平台的、可通过网络工作的声音服务，其一般使用于Linux和FreeBSD操作系统。它可以用来作为一种简易改进的开放声音后台（ESD）替换。



## 播客
### Vocal-（为现代桌面而生，播客客户端巨作）

![Vocal](../../../../images/blogimage/raw/master/Aornus_shot_20211220_102138.png)

主要从iTunes获取播客，外观很现代，可以管理订阅，在线播放，离线下载，也可以导入订阅列表。

![主界面](../../../../images/blogimage/raw/master/Aornus_shot_20211220_102626.png)

![详细页面](../../../../images/blogimage/raw/master/Aornus_shot_20211220_102545.png)

### gPodder-（古老的免费播客客户端）

![gPodder](../../../../images/blogimage/raw/master/Aornus_shot_20211220_102038.png)

确实很强大，在很多软件里都有gpodder的插件，同步功能很强大，但我就是不能注册，真令人头痛，明明官网好好的，可能被滥用以至于停止注册了，客户端里搜索太慢。总是卡住，不是太好用。

### Gonme podcast

很简单，很现代，但是很慢！无法在线播放，只能下载之后播放。

### Spotify

这个不必多说，声田本身就是一个很好的播客客户端，包括流媒体，下载，同步等各种功能，唯一不能做的就是外部网站的订阅。

### Clemencine

内存占用不大，反应快速，功能强大。

囊括了网络收音机，网盘音乐播放，podcast订阅...等等等各种东西，单网络电台而言，二十四小时不重样，新闻，音乐，一辈子都听不完。

这里推荐几个自带的能用的电台源：

1. https://www.radio-browser.info/ 分类详细，中国的频道也很全，跨越国界，跨越文化。
2. SomaFM 頻道不多，主要是电子音乐。
3. ICEcast 很细致，按风格流派分，简直能跟spotify想媲美。

回到播客上，其功能如图所示，可以在自带的播客源中搜索，也可以倒入OPML文件。

![搜索界面](../../../../images/blogimage/raw/master/20211222202212.png)

![播放页面](../../../../images/blogimage/raw/master/20211222211953.png)

## 社交
### 微信客户端

> 写于时间：2021-12-31 21:40:17

下午看RSS订阅时,发现微信linux版居然官宣了，起初不信，但看到优麒麟的广告，不由得信了，我只希望不要跟QQlinux2008那般破烂。这是微信linux在Arch里的描述：

![aur](../../../../images/blogimage/raw/master/202112312124189.png)

废话不多说，软件装起来。

#### 微信安装

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

#### 评测

* 支持群聊，文件与图片发送，*输入好像有问题，每修改一次，光标自动回到句尾了*

* 不支持搜索，公众号，小程序，纯粹的一个聊天软件

* 每次登陆需要扫码

* 不能停留后台

![](../../../../images/blogimage/raw/master/202112312130578.png)

![](../../../../images/blogimage/raw/master/202112312132942.png)

>  下次更新不知道要到猴年马月了

## 其他软件

### Spotify
破解**随机播放**的安卓版声田，来自[Spotify Craccato](https://t.me/Spotify_Crack)的分享。

{% note success  %}
https://sionapk.lanzoue.com/b012gxu9c 密码：ezoj
{% endnote %}


### Nekogram
自带魔法的电报第三方
{% note success %}
https://sionapk.lanzoue.com/b012gxw4j 密码：1u0j
{% endnote %}


### Obsidian
黑曜石笔记的镜像
{% note success %}
https://sionapk.lanzoue.com/b012abedc 密码：sion
{% endnote %}



