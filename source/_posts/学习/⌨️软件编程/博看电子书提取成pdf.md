---
title: 博看电子书制作
abbrlink: bookan-pdf-create-Script
tags:
  - LaTeX
categories:
  - 学习
  - ⌨️软件编程
katex: true
password: tools&fools
hidden: true
description: 为了防止被滥用以至于平台改变策略，本文不可见。
root: ../../
date: 2022-12-18 20:28:44
update: 2022-12-18 20:28:44
cover:
comments:
copyright:
aside:
sticky:
keywords:
---

{% note info %}
请注意：包括博看期刊、中国知网在内的众多数据库，在各大图书馆一般都有授权。**我们读者使用软件来免费地阅读，查阅资料，是一个非常正当的行为，与白嫖、使用破解软件存在本质的区别**。
{% endnote %}

## 博看期刊
此软件，看杂志之神器也。

第一次使用博看是在18年的高二，那时南阳市图书馆还待在市中心的不起眼的角落里，一台无人问津的阅读机放在二楼杂志阅览室的门口。一次无聊，我点看了那台无人问津的阅读器，发现上面可以看到好多新出来的杂志，很是喜欢。阅读器里的图书接口便是博看，机子上有个安卓端推广链接以及一个机构码。扫码下载，注册验证，之后就能用了。

软件的下载，应用商店搜索“博看书苑/博看期刊”即可。
关于机构码，各位可以去本地的图书馆看看，如果懒得去，可以试试本地图书馆/大学的拼音缩写：比如南阳市图书馆的授权码是`nystsg`、哈工大的授权码是`hrbgd`、河南大学的是`hndx`。



## 博看期刊原貌图书提取
这部分内容是去年疫情隔离在学校宿舍时候花了一个晚上琢磨出来的，脚本的具体细节我不做过多解释，如果你分析了博看app的文件夹，结合着脚本就会很容易明白。另外，生成的文件请勿传播。

通过下面这两个脚本可以把app离线保存的原貌(图片版)书籍转换成pdf。第一步图片转换脚本的环境是linux系统，第二步pdf生成需要$\LaTeX$进行编译。
### 提取图书解码图片脚本(Linux)
```bash
#!/bin/bash
#Tuesday, October 18, 2022 12:50:10 PM CST
echo 欢迎使用bookan2jpg脚本
echo 本脚本使用前请确保已经安装了 sed dos2unix 工具

echo 开始设置主变量
value=$( echo $(basename *.txt .txt) )

echo 读取索引文件$value.txt，并进行进行处理
sed -i "s/\/storage\/emulated\/0\/Android\/data\/cn.com.bookan\/files\/bookan\/magazine\/$value\// /g" `grep -rl "/storage/emulated/0/Android/data/cn.com.bookan/files/bookan/magazine/$value/"  ./`
dos2unix $value.txt

echo 索引文件处理结束
echo 创建输出目录
mkdir output
echo 创建变量i
i=1
cat $value.txt | while read line
do
    mv $value/$line output/$i.jpg
    i=$[$i+1]
done
echo 清除变量
unset i
unset value
echo 处理结束输出结果为：
ls output/

```

### Latex模板
```tex
\special{pdf:encrypt userpw () ownerpw (sion) length 128 perm 2052}
\documentclass{article}
\usepackage{graphicx}
\usepackage{tikz}
\usepackage{anysize}
%\papersize{26cm}{18.5cm}
%\marginsize{2.5cm}{2.1cm}{2cm}{2cm}
\usepackage{hyperref}
%\hypersetup{pdftitle=北京周报（英文版）,pdfauthor=《北京周报》编辑部,pdfsubject={党建之声，党建工作},pdfstartview=FitB}

%\hypersetup{pdftitle=英语世界,pdfauthor=《英语世界》杂志社有限公司,pdfsubject={英语学习，双语，月刊},pdfstartview=FitB}

\newcommand\includeFullPageGraphics[2][]{
	\newpage
	\thispagestyle{empty}
	\begin{tikzpicture}[remember picture, overlay, inner sep=0pt]
		\node at (current page.center) 
		{\includegraphics[width=\paperwidth, height=\paperheight, keepaspectratio=false,#1]{#2}};
	\end{tikzpicture}
	\newpage
}

\begin{document}
%	\includeFullPageGraphics{cover.jpg}
	\foreach \macro in {2,3,...,131}
	{	\includeFullPageGraphics{output/\macro.jpg} }
\end{document}

```