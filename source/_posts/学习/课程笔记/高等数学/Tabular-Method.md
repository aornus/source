---
title: Tabular Method
tags:
  - 高等数学
  - 不定积分
  - 奇技淫巧
categories:
  - 学习
  - 课程笔记
cover: ../../../../images/bg.jpg
description: 直排|此乃妖法！
katex: true
swiper_index: 6
abbrlink: Tabular-Method
date: 2022-01-03 21:32:02
comments:
copyright:
aside:
password:
hidden:
---

<div class="heti heti--vertical", align="right",style="font-family: 'Noto Serif SC', serif;" > 
	<h1>Tabular Method 表格法</h1>
    <p>
        <blockquote>
            竖排版测试页，感觉还是不好达到那种<br / >
            公式横排，文字竖排的那种理想效果<br / >
            而且ketex一到直排环境符号就满天飞舞
	    </blockquote>
    </p>
    <p>还在为求积分头疼吗？ </p>
    <p>还在为分部积分公式记不清烦恼吗？</p>
    <p>还在为求积公式用错而后悔不已吗？ </p>
    <p>来使用表格法吧！</p>
	<p>让你彻底摆脱分部积分！</p>
    <p>让你解题总快人一步！</p>
     <h1> 什么是表格法？</h1>
    <p> 表格法是一种更加简洁，优美的，</p> <p> 很大程度上可以取代分部积分法（Integration</p> <p>  by Parts）的求解方法，定理如下：</p>
</div>



$$
\int f(x) g(x)dx 
 =\sum_{j=0}^{n-1} (-1)^jf^j(x) g^{-(j+1)}(x) + (-1)^n \int f^{n}(x)g^{-n}(x)dx
$$

$$
f g^{(-1)}-f^{(1)} g^{(-2)}+f^{(2)} g^{(-3)}-\cdots+(-1)^{n-1} f^{(n-1)} g^{(-n)}+(-1)^{n} \int f^{(n)} g^{(-n)} d x
$$

> $$
> f^{(-n)}=\int \cdots \int_{\mathbf{D}} f\left(x_{1}, x_{2}, \ldots, x_{n}\right) \mathrm{d} x_{1} \ldots \mathrm{d} x_{n}
> $$

<div class="heti heti--vertical", align="right",style="font-family: 'Noto Serif SC', serif;" > 

那么上式就可以列成这样的表格：


|     正负号     |  D（导数）  |   I（积分）  |             代表的积分              |
| -------------: | :---------: | :------------: | :---------------------------------- |
|       +        |   $f(x)$    |      g(x)      |         $\int f^(x)g(x)dx$          |
|       -        |  $f^{(1)}$  |   $g^{(-1)}$   | $-1 \cdot \int f^{(1)}(x)g^{-1}(x)dx$ |
|       +        |  $f^{(2)}$  |   $g^{(-2)}$   |  $\int f^{(2)}(x)g^{(-2)}(x)dx$  |
|       -        |  $f^{(3)}$  |   $g^{(-3)}$   | $\int f^{(3)}(x)g^{(-3)}(x)dx$ |
|    $\vdots$    |  $\vdots$   |    $\vdots$    | $\vdots$ |
| $(-1)^{(n-1)}$ | $f^{(n-1)}$ | $g^{(-(n-1))}$ | $(-1)^{(n-1)} \int f^{n-1}(x)g^{-n+1}(x)dx$ |
|  $(-1)^{(n)}$  |  $f^{(n)}$  |   $g^{(-n)}$   |  $(-1)^n \int f^{n}(x)g^{-n}(x)dx$  |

看到这里，相信大家已经会了吧。那么今天就此结束，咱们下次见。

什么？要例子？这都说的多清楚了，要什么例子。

看不懂？好吧，那就给几个例子吧
</div>
<div class="heti heti--vertical", align="right",style="font-family: 'Noto Serif SC', serif;" > 
# 表格法展开停止条件

## 遇到0

例题一：求解下面无穷积分：
$$
\int_0^{\infty} x^2 e^{-x}dx
$$
解：根据表格法，可以其不定积分的表格如下：

|      |   D   |     I     |         rep         |
| :--: | :---: | :-------: | :-----------------: |
|  +   | $x^2$ | $e^{-x}$  | $\int x^2 e^{-x}dx$ |
|  -   | $2x$  | $-e^{-x}$ | $\int 2x e^{-x}dx$  |
|  +   |  $2$  | $e^{-x}$  |  $\int 2 e^{-x}dx$  |
|  -   |  $0$  | $-e^{-x}$ |     $\int 0 dx$     |

</div>


$$
\therefore \int x^2 e^{-x}dx = -x^2e^{-x}-2xe^{-x}-2e^{-x}+C
$$


<div class="heti heti--vertical", align="right",style="font-family: 'Noto Serif SC', serif;" > 

## 遇到循环

例题二：求解下面不定积分：
$$
\int e^x sin(x) dx
$$
解：根据表格法，可以该不定积分的表格如下：

|      |     D     |    I     |          rep          |
| :--: | :-------: | :------: | :-------------------: |
|  +   | $sin(x)$  | $e^{x}$  | $\int e^{x}sin(x)dx$  |
|  -   | $cos(x)$  | $e^{x}$  | $\int e^{x}cos(x)dx$  |
|  +   | $-sin(x)$ | $e^{x}$  | $-\int e^{x}sin(x)dx$ |
|  -   | $-cos(x)$ | $e^{x}$  | $\int cos(x) e^x dx$  |

在上面的表格中，我们发现它可以无限往下面展开，但我们只需要看清楚第三次展开的结果，发现了吗？它就是原积分的相反数（这是特殊情况，一般只要呈现出倍数关：系就可以停止展开了），这时结束展开，可以得到:
</div>


$$
\int e^x sin(x) dx=sin(x)e^x-cos(x)e^x-\int e^{x}sin(x)dx
$$

<div class="heti heti--vertical", align="right",style="font-family: 'Noto Serif SC', serif;" > 

## 可以写成简单积分

例题三：求解下面不定积分：
$$
\int x^4 lnx dx
$$
解：根据表格法，可以该不定积分的表格如下：

|      |   D    |   I   |        rep        |
| :--: | :----: | :---: | :---------------: |
|  +   | $x^4$  | $lnx$ | $\int x^4 lnx dx$ |
|  -   | $4x^3$ |   ?   |        ？         |

$lnx$的积分不会求怎么办？换个位不就行了$lnx$的导数总是简单了吧

|      |       D       |        I         |           rep           |
| :--: | :-----------: | :--------------: | :---------------------: |
|  +   |     $lnx$     |      $x^4$       |    $\int x^4 lnx dx$    |
|  -   | $\frac{1}{x}$ | $\frac{1}{5}x^5$ | $\frac{1}{5}\int x^4dx$ |
|  +   |     ----      |      -----       |          -----          |

当发现出现了贼简单的一个式子时，就不要在展开了，直接就出答案了
</div>

$$
\therefore \int x^4 lnx dx = lnx\cdot \frac{1}{5}x^5- \frac{1}{5}\int x^4 dx
$$

什么？不想用！好吧给你个分部积分的记忆公式吧：
$$
\begin{aligned}
&(u\cdot v)'=u'v+v'u\\
&u'v=(u\cdot v)'-v'u\\
&\int v du=(u\cdot v)-\int udv
\end{aligned}
$$
讲到这里，你总该满意了吧，谢谢支持！某年某月，我们再见！

> [1]:1988年的电影《为人师表 / Stand and Deliver》,里面有这个表格法的片段。“Tic, Tac, Toe, Simple!”
</div>
