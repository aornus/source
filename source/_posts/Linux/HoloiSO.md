---
title: HoloiSO安装
tags:
- steam
categories:
  - Linux
katex: true
date: 2022-05-11 10:08:34
cover:
comments:
copyright:
aside:
password:
hidden:
description: 第三方SteamOS安装教程|不建议国内安装使用
sticky:
---

>  注意：本文主要是翻译自仓库里的说明，仅供参考。

> <center>Yes, Gabe. SteamOS functions well on a toaster.</center>
> <p align="right">——Adam Jafarov</p>

# HololSO简介

> 来自SteamOS 3(版本名:Holo)的archiso安装**脚本**，仅仅是个脚本而已。

此项目给最近新出来的Steam Deck的Holo操作系统了一个通用的、可安装的格式，使得其可以像普遍的linux发行版一样，可以在任何X86_64的PC上安装，而且HoloISo还提供一个接近官方的SteamOS体验。

## 更新记录

* SteamOS OOBE (Steam Deck UI 首次启动体验)
* Deck UI (独立会话)
* Deck UI (-gamepadui)
* TDP/FPS限制
* 全局FSR
* 着色器预缓存
* 从plasma 到plasma 切换桌面，没有用户中断。
* valve为KDE Plasma提供的独家Vapor外观
* Steam Deck pacman 镜像
* 看起来很酷的neofetch?
* 系统更新

已知的问题

* 不支持NVIDIA GPU。

> 在它们支持原子KMS、加速的Xwayland和Vulkan DMA-BUFF扩展之前，HoloISO无法在上面正常运行。

* 英特尔GPU/iGPU需要进行Gamescope和MESA降级，以便启动到Steam Deck会话。

> 请参考这个[gist](https://gist.github.com/drraccoony/8a8d0a9e3dfde9fafd3e374e418d2935)以获得进一步的指导。

# 安装

## 准备

* 4GB及以上大小的U盘，最好支持USB3.0，那样比较快（废话）
* 支持Vulkan和VDPAU的AMD GPU
* 支持UEFI的设备
* BIOS里禁用安全启动(secure boot)
* HoloIso安装镜像[^iso]
* U盘镜像写入工具[^upan]

## 安装类型

### 裸机安装

一个仅有操作系统的安装，类似于vanilla Arch Linux的安装。

不推荐，除非你是linux高手

## 仅游戏[^game]

仅限Steam Deck UI（仅限AMD GPU；无桌面），如前所述，这没有运送任何桌面环境，只安装了Steam Deck UI。

不推荐，未开发完全，不稳定

### Steam Deck体验

完整的SteamOS 3体验，包括流畅的会话切换，KDE桌面环境+KDE全家桶，以及预装的Chromium。

推荐，对普通人友好，安装简便

## 安装步骤

1. 从Release里下载镜像，使用 [BalenaEtcher](https://www.balena.io/etcher/), [Rufus](https://rufus.ie/)的DD模式烧录。
2. 从U盘启动该镜像
3. 在终端输入：`holoinstall`，回车运行
4. 当系统提示时，输入磁盘名称，例如`sda`或`nvme0n1`
5. 带上你喜欢的热饮☕，等待它的安装😑

### 安装后

安装成功后，重启。进入系统，你会看到Steam Deck的OOBE环境，在那里你会连接到你的网络，并登录到你的Steam账户，也可以通过在电源菜单中选择切换到桌面来无缝退出到KDE Plasma。

# 常见问题

* 这是官方的吗？

> 不是，但是它可能已经达到了99%的水平。代码和软件包都是直接来自Valve[^valve]，没有任何可能的编辑，ISO是在官方Steam Deck恢复镜像上建立的，在QEMU实例中运行。

* 我的镜像无法启动，有什么解决办法吗？

> 目前，ISO只有在使用BalenaEtcher、RosaImageWriter、Fedora Media Writer、4MB区块大小的DD或Rufus的DD模式下才能启动。

# 备注

这个配置包括Valve的pacman.conf仓库、holoinstall脚本和holoinstall安装后二进制文件。

这个配置建立了一个基于releng的ISO，这是默认的Arch Linux重新分配的风格。

# 踩坑记录

此系统的安装过程实则为arch的安装（曾经前前后后安装过七八次Arch，仅有两次成功，一看到那个iwctl我就烦），此项目不过是提供了一个脚本。

官方提供的`holoinstall`脚本在国内慢的要死，挂了代理都贼慢的那种，强烈不建议安装使用，还是等到steam OS 3正式版出来了，再用官方镜像的装吧。



[^valve]: **威尔乌**, 美国电子游戏开发和数字发行公司。steamOS的开发商。*2021年7月16日，Valve发布游戏掌机Steam Deck；Steam Deck可以登陆Steam账户，并同步用户数据。*
[^game]: 这部分目前正在开发中。
[^iso]: 官方地址： https://github.com/theVakhovskeIsTaken/holoiso/releases( 为了解决国内下载慢可以点击[这个地址](https://d7.serctl.com/downloads8/2022-05-11-09-36-17-holoiso-SteamOS_Holo-20220510_0636_amdgpu-x86_64.iso)加速)
[^upan]:推荐[BalenaEtcher](https://github.com/balena-io/etcher/releases)，另外，经过多次测试，万能的写入工具Ventoy这次不能引导了😞





