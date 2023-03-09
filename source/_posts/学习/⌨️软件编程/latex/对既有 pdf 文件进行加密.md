---
title: latex自带的pdf加密指令
tags:
  - LaTeX
  - 奇技淫巧
  - 加密
categories:
  - 学习
  - ⌨️软件编程
  - latex
cover: ../../../../images/bg.svg
description: （转载）让你的latex体验更完美
copyright: true
copyright_author: Chennan ZHANG
copyright_url: 'http://chennanzhang.github.io/2021/02/09/PDF-utility/'
copyright_info: 根据BY-NC-SA 协议转载
abbrlink: LaTeX-Encrypt
date: 2021-12-10 18:40:13
update: 2022-02-25 20:15:20
katex:
comments:
aside:
password:
hidden:
---

> ~~找了好久，突然发现了则篇文章，但现在不知道出处了，原谅我，作者。~~

使用 LaTeX 撰写文档并生成 `PDF` 文件时，可以通过 Knuth 在 TeX 里留的一个后门：`\special` 命令来让后面的驱动完成这些工作（牛人就是牛）。这条命令一般放在 `\documentclass` 之前，对于文档加密来说，命令的格式为：

```tex
\special{pdf:encrypt userpw (<userpassword>) ownerpw (<ownerpassword>) length <num1> perm <num2>}
\documentclass{xxxx}
```

简单解释一下几个参数：

- `<userpassword>` 填写用户密码，提供打开阅读权限，一般可以留空，文章写了总是给人看的，除非是特别机密的文件，才有设置的必要；
- `<userpassword>` 填写拥有者密码，用于提供权限解除其他限制；
- `<num1>` 加密键长度，必须为 40～128 之间的 8 的倍数或 256，默认为 40；
- `<num2>` 加密标识，这是一个 32 位无符号整数转化的十进制数；各数位含义为：

| 数位 | 含义                                                         |
| :--: | :----------------------------------------------------------- |
| `3`  | 允许打印文档                                                 |
| `4`  | 允许除 `6`、`9`、`11` 位控制的其他修改操作                   |
| `5`  | 允许从文档中复制文字和图形                                   |
| `6`  | 允许添加修改文字注释，创建和填写表单（表单操作 `4` 位也可以控制） |
| `9`  | 允许填写现有的表单字段（包括签名字段）                       |
| `10` | 支持文字和图形的提取（针对有障碍用户的可访问性或用于其他目的）PDF 2.0 中已弃用 |
| `11` | 允许重组文件，如插入页面、删除页面、旋转页面、提取页面等。不受 `4` 位的控制。 |
| `12` | 允许高质量打印，如果此位清除，仅设置 `3` 位，将以低质量方式打印。 |

如果希望文档仅仅允许高质量打印，则 `12` 位与 `3` 位应设置为 `1`，其余位设置为 `0`，即 `100000000100`，该数值转化为十进制数即为：`2052`；假定加密键长度为 128，用户密码留空，所有者密码为 `mypassword`，则编译文档中这条命令应写成为：

```latex
\specail{pdf:encrypt userpw () ownerpw (mypassword) length 128 perm 2052}
```

文件加密也可以通过 `xdvipdfmx` (或 `dvipdfm(x)`) 命令参数实现，编译命令为：

```bash
xdvipdfmx -S -K <num1> -P <0xNUM2> file.xdv
```

这里 `<num1>` 与前相同，`<0xNUM2>` 则需要将 `<num2>` 转换为 16 进制表示，并且，该命令只能对 `dvi` 或 `xdv` 文件使用，命令使用时需要在命令行交互输入用户和拥有者密码，相对比较麻烦。

## 对既有 `pdf` 文件进行加密

上述方法是在撰写文档时对文档进行加密的方法。大多数情况下，我们是面对一个既有 `pdf` 文件希望对其进行加密处理，这时可以借用 `pdfpages` 宏包重新生成文档的方式，在编译中对其进行加密。假定加密语句同上，对于一个既有 `file.pdf` 文档，可以编写如下 `tex` 源代码：

```latex
\specail{pdf:encrypt userpw () ownerpw (mypassword) length 128 perm 2052}
\documentclass{article}
\usepackage{pdfpages}
\begin{document}
  \includepdf[fitpaper,pages=-]{file.pdf}
\end{document}
```

编译此文档后，将生成一个加密后的文件，间接实现了加密。
