---
title: Docker
abbrlink: docker
categories:
  - 学习
  - ⌨️软件编程
root: ../../
katex: false
theme: xray
hidden: true
published: false
date: 2023-05-12 22:12:44
update: 2023-05-12 22:12:44
tags:
cover:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
aside:
comments:
password:
description:
sticky:
keywords:
---
>此笔记所记录的环境如下
>
|   项目   |          内容          |
|:--------:|:----------------------:|
| 操作系统 |      Garuda Linux      |
| 系统类型 |          64位          |
| 内核版本 | Linux 6.3.1-zen1-1-zen |
|   时间   |       2023.5.12        |

## 安装
linux上安装软件，一般不需要查教程，直接安装即可
```shell
sudo pacman -S docker
# 在写作本文时安装的docker版本为1:23.0.6-1
```

```shell 运行结果
软件包 (3) containerd-1.7.0-1  runc-1.1.7-1  docker-1:23.0.6-1

下载大小：       55.00 MiB
全部安装大小：  233.40 MiB
```