---
title: Markdown与标签外挂的语法笔记
date: 2023-01-11
update: 2023-01-11
abbrlink: demo4markdown
tags:
- Markdown
- 标签外挂
categories:
- 学习
- 软件编程
cover:
katex: true
comments:
copyright:
aside: 
password:
hidden:
description: Markdown语法复习与butterfly标签外挂的实例。
sticky: 
keywords:
root: ../../
---

> <center>让感兴更有力地表达！</center>
> <p align="right">——秉蕳</p>
## 文章痕迹
{% timeline %}
<!-- timeline 2023-01-11-->
* 复习了Markdown经常忘记的语法
* 整理了把Butterfly主题的外挂标签

<!-- endtimeline -->
{% endtimeline %}

-----

## 基本语法
### 标题
除了`#`字符，文字下加线也可以作为一级或二级标题。
```md
一级标题
===============

二级标题
---------------
```
### 段落与换行
Markdown不支持空格（spaces）或制表符（ tabs）缩进段落，段落之间用一个空行来分隔，不同行之间用回车或`<br>`来换行。
### 文本样式
```md
- [ ] 精通Markdown
- [x] 整理Markdown语法
- [x] ~~列表、代码、分割线、链接、图片语法~~

> 引用一个句子。

下面是一个**更好看**的引用样式，内容居中，*作者或来源*右对齐。
> <center>让感兴更有力地表达！</center>
> <p align="right">——<i>秉蕳</i></p>

脚注示例，这是第一个脚注[^注脚名1]，这是第二个脚注[^注脚名2]，这是第三个脚注[^注脚名3]
[^注脚名1]:我是脚注一.
[^注脚名2]:我是脚注二.
[^注脚名3]:我是脚注三.


```
- [ ] 精通Markdown
- [x] 整理Markdown语法

> 引用一个句子。

下面是一个**更好看**的引用样式，内容居中，*作者或来源*右对齐。
> <center>让感兴更有力地表达！</center>
> <p align="right">——<i>秉蕳</i></p>

脚注示例，这是第一个脚注[^注脚名1]，这是第二个脚注[^注脚名2]，这是第三个脚注[^注脚名3]

[^注脚名1]:我是脚注一.
[^注脚名2]:我是脚注二.
[^注脚名3]:我是脚注三.

## 标签外挂
{% note simple %}
默認 提示塊標籤
{% endnote %}

{% note default modern %}
default 提示塊標籤
{% endnote %}

{% note primary flat %}
primary 提示塊標籤
{% endnote %}

{% note success no-icon %}
success 提示塊標籤
{% endnote %}

{% note info simple %}
info 提示塊標籤
{% endnote %}

{% note warning simple %}
warning 提示塊標籤
{% endnote %}

{% note danger simple %}
danger 提示塊標籤
{% endnote %}

-------

This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,,outline %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,larger %}

{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block center larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block right outline larger %}

{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,blue larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,pink larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,red larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,purple larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,orange larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,green larger %}

<div class="btn-center">
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline blue larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline pink larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline red larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline purple larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline orange larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline green larger %}
</div>

臣亮言：{% label 先帝 %}创业未半，而{% label 中道崩殂 blue %}。今天下三分，{% label 益州疲敝 pink %}，此诚{% label 危急存亡之秋 red %}也！然侍衞之臣，不懈于内；{% label 忠志之士 purple %}，忘身于外者，盖追先帝之殊遇，欲报之于陛下也。诚宜开张圣听，以光先帝遗德，恢弘志士之气；不宜妄自菲薄，引喻失义，以塞忠谏之路也。
宫中、府中，俱为一体；陟罚臧否，不宜异同。若有{% label 作奸 orange %}、{% label 犯科 green %}，及为忠善者，宜付有司，论其刑赏，以昭陛下平明之治；不宜偏私，使内外异法也。

