---
title: Hexo添加tikz支持
tags:
  - 博客
  - 奇技淫巧
  - 自荐
categories:
  - 学习
  - ⌨️软件编程
  - hexo
cover: 'https://www.ctan.org/teaser/pkg/pgf'
description: 通过添加引用tikzjax.js实现hexo对tikz的支持。
katex: true
hidden: true
abbrlink: hexo-tikz-support
keywords: 'Tikz, LaTeX, Hexo'
date: 2022-02-27 10:54:48
update: 2022-03-18 15:03:15
comments:
copyright:
aside:
password:
---
> 声明：本教程是在主题`butterfly 4.1.0`上进行测试的，该主题提供了现成的引用接口，对于其他主题可以参考[这篇文章](https://stackoverflow.com/questions/63066096/hexo-can-not-load-style-sheet)实现。

> 3月18日更新：由于此js严重影响页面的**加载速度**，（在所有页面中都加载了此js文件）现在将其关闭，下面例子不会显示是<u>正常情况</u>。

-----

[Tikzjax](https://github.com/kisonecat/tikzjax)是一个遵循tikz语法，并将其并转化成相应svg图的项目，本文将采用此项目的js代码实现目的。

## 前置

在butterfly主题的配置文件中有引用接口，head下面可以添加css文件引用，bottom下可以添加js文件引用。

```xml
# Inject
# Insert the code to head (before '</head>' tag) and the bottom (before '</body>' tag)
# 插入代码到头部 </head> 之前 和 底部 </body> 之前
inject:
  head:
      # - <link rel="stylesheet" href="/xxx.css">
  bottom:
      # - <script src="xxxx"></script>
```

## 调用

下载tikzjax.js文件到`/themes/butterfly/source/js/tikzjax.js`，可以在github里下载，也可以在此处[📄](https://link.jscdn.cn/1drv/aHR0cHM6Ly8xZHJ2Lm1zL3UvcyFBcmNKVWVEVGN1X1d2QTFVdDRJMlJtelNxMVpLP2U9NE56ak1x.js)下载



在配置文件在添加引用

```xml
...
 head:
<link rel="stylesheet" type="text/css" href="http://tikzjax.com/v1/fonts.css">
bottom:
  - <script type="text/javascript" src="/js/tikzjax.js"></script>
...
```

## 使用

不出意外的话，现在就在文章中写tikz代码了🎉，就像下面这样：

````md
### 画一个圆

```
<script type="text/tikz">
  \begin{tikzpicture}
    \draw (0,0) circle (1in);
  \end{tikzpicture}
</script>
```

````

下面举几个例子：

{% tabs 例子 %}

<!-- tab ⚪ -->

<script type="text/tikz">
  \begin{tikzpicture}
    \draw (0,0) circle (1in);
  \end{tikzpicture}
</script>

<!-- endtab -->

<!-- tab 二次函数 -->

<script type="text/tikz">
\begin{tikzpicture}[scale=2]
    \draw[help lines,step=0.5]
    (-1,-1) grid (1,1);
    \draw[->] (-1.5,0) -- (1.5,0);
    \draw[->] (0,-1.5) -- (0,1.5);
    \draw[domain=-1:1]
    plot(\x,{\x*\x*2 -1});
\end{tikzpicture}
</script>

<!-- endtab -->

<!-- tab sinx -->

<script type="text/tikz">
\begin{tikzpicture}[scale=3]
\clip (-0.1,-0.2) rectangle (1.1,1.51);
\draw[step=.5cm,gray,very thin] (-1.4,-1.4) grid (1.4,1.4);
\draw[->] (-1.5,0) -- (1.5,0);
\draw[->] (0,-1.5) -- (0,1.5);
\draw (0,0) circle (1cm);
\filldraw[fill=green!20,draw=green!50!black] (0,0) -- (3mm,0mm) arc
(0:30:3mm) -- cycle;
\draw[red,very thick] (30:1cm) -- +(0,-0.5);
\draw[blue,very thick] (30:1cm) ++(0,-0.5) -- (0,0);
\draw[orange,very thick] (1,0) -- (intersection of 1,0--1,1 and 0,0--30:1cm);
\end{tikzpicture}
</script>
<!-- endtab -->

<!-- tab 复杂例子 -->

<script type="text/tikz">
\begin{tikzpicture}
\def \n {5}
\def \radius {3cm}
\def \margin {8} % margin in angles, depends on the radius

\foreach \s in {1,...,\n}
{
  \node[draw, circle] at ({360/\n * (\s - 1)}:\radius) {$\s$};
  \draw[->, >=latex] ({360/\n * (\s - 1)+\margin}:\radius) 
    arc ({360/\n * (\s - 1)+\margin}:{360/\n * (\s)-\margin}:\radius);
}
\end{tikzpicture}
</script>

<!-- endtab -->

{% endtabs %}

### 官方Demo

在这里你也可以测试一下tikzjax对代码的支持度，

{% iframe 'https://tikzjax-demo.glitch.me/' 100% 500px %}
