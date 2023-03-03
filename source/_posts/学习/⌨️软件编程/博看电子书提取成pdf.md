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

> <center>当你在引用别人的时候，你在引用自己。</center>
> <p align="right">——Sion</p>
## 文章痕迹
{% timeline %}
<!-- timeline 2022-12-18 20:28:44-->
开始汇总
<!-- endtimeline -->
{% endtimeline %}

-----
## 脚本(Linux)
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

## OCR识别
[python pdf转图片，图片转pdf - 『编程语言区』 - 吾爱破解 - LCG - LSG |安卓破解|病毒分析|www.52pojie.cn](https://www.52pojie.cn/thread-1639458-1-1.html)

## Latexpdf制作模板
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