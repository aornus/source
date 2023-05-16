---
title: Rss使用手册
abbrlink: rss
tags:
 - 自荐
 - 阅读
 - Kindle
categories:
  - 学习
  - ⌨️软件编程
cover: /images/20221012/RSS-03.svg
katex: true
description: RSS阅读流程的各种解决方法
root: ../../
date: 2022-11-26 13:31:22
update: 2022-11-26 13:31:22
comments:
copyright:
aside:
password:
hidden:
sticky:
keywords:
---
![](https://img2023.cnblogs.com/blog/2222783/202212/2222783-20221201231332000-1556226501.png)

{% markmap 200px %}

<!-- @import "[TOC]" {cmd="toc" depthFrom=2 depthTo=6 orderedList=true} -->


<!-- code_chunk_output -->

1. [订阅源](#订阅源)
    1. [格式](#格式)
    2. [源之源](#源之源)
        1. [Innoreader（2012~）](#innoreader2012~)
        2. [Feedx（2016.5~）](#feedx20165~)
        3. [RSSHub（2018~）](#rsshub2018~)
        4. [Feedd（2021~）](#feedd2021~)
2. [阅读器订阅](#阅读器订阅)
    1. [Fluent Reader（Windows）](#fluent-readerwindows)
    2. [Feeder（Android）](#feederandroid)
3. [邮箱订阅](#邮箱订阅)
    1. [格式](#格式-1)
    2. [自力更生](#自力更生)
        1. [rss2email（Python）](#rss2emailpython)
        2. [Calibre](#calibre)
    3. [第三方服务](#第三方服务)
        1. [Follow.it](#followit)
            1. [订阅源获取](#订阅源获取)
            2. [订阅源管理](#订阅源管理)
        2. [Blogtrottr.com](#blogtrottrcom)
    4. [体验结果](#体验结果)
4. [RSS阅读流程的简化](#rss阅读流程的简化)
    1. [RSS阅读流程](#rss阅读流程)
    2. [阅读流程](#阅读流程)
    3. [整合式订阅](#整合式订阅)
        1. [自力更生](#自力更生-1)
        2. [第三方服务](#第三方服务-1)
    4. [阅读与批注](#阅读与批注)
    5. [笔记整理](#笔记整理)

<!-- /code_chunk_output -->
{% endmarkmap %}

## 文章痕迹
```
{% timeline %}
<!-- timeline 11-21 13:30:45-->
【V0.1】创建文章
* 邮箱订阅源推荐
<!-- endtimeline -->
<!-- timeline 11-26 20:38:15-->
【V1.0】大幅修改，并发布。
* 增加对newsletter的体验
* 对阅读流程的思考
* 文章结构调整
<!-- endtimeline -->

<!-- timeline 12-5 16:12:15 -->
【V1.1】开始文章润色修改
<!-- endtimeline -->
{% endtimeline %}
```

> <q>RSS（英文全称：RDF Site Summary 或 Really Simple Syndication），中文译作简易信息聚合，也称聚合内容，是一种消息来源格式规范，用以聚合多个网站更新的内容并自动通知网站订阅者。使用 RSS 后，网站订阅者便无需再手动查看网站是否有新的内容，同时 RSS 可将多个网站更新的内容进行整合，以摘要的形式呈现，有助于订阅者快速获取重要信息，并选择性地点阅查看。</q>[^1]
> <p align="right">——维基百科编者</p>
## 楔子
在Web3.0逐渐兴起的背景下，老一代的网络Web 2.0弊端愈加凸显。
首先平台越来越封闭。纵观中文互联网，几乎所有的社交平台都越加向内发展，很多内容的阅读都限定了平台（甚至设备），稍微好点的，可以在平台外看，但却是一堆限制与弹窗。开放信息生存在夹缝之中，甚至小小的规则修改，就可能导致其烟消云散。
其次是内部订阅模式的兴盛。现在的大小软件、各种网站无一不是局域网内的“关注——被关注”，信息的获取隔着一个个账号、app的社交防火墙（Social Media Fire Wall），信息的互通甚至在一个母公司下也极为困难（比如QQ与微信）。
实际上，这种局面是我们想看到但又不想看到的。这种情形一方面体现了各个企业之间的蓬勃竞争与互联网的活力，信息的封闭导致用户的分离，进而可以有效避免一家独大，网络僵化的局面。但与此同时，信息的割裂也给内容创作者、读者带来了很多的不必要的鸿沟，从网上的“一站式发布平台”，“一站式订阅平台”都可略窥一二。

这个时代给予了我们海量的信息，但可悲的是：信息却被平台与算法控制，普通人在各种攻势下，兴趣变得单一，思维变得懒散，逐渐沦为“自己的”奴隶，沉醉在“我的世界”里不能自拔。我以为，摆脱这种局面的指导方法就是——**随机**。

**阅读**做为人类的基本行为之一，可以抽象成三个步骤是——**输入，处理，输出。** 

* 输入：信息的来源。可以是书籍、电子书、播客、视频、盲文书等人体通过视觉、听觉、触觉接收到的信息。
* 处理：信息的处理。就阅读而言，这一阶段就是在读、思考、批注等。
* 输出：处理的结果。简而言之就是知识的获得，可以留存于内心，也可以体现在笔记、批注等实体介质上。
* 噪音：这是所有阶段都不可避免的额外内容。比如一本书可以作为阅读的输入，那么书籍里面的广告、水印；阅读时工具的故障、环境的干扰；写笔记时，笔记本的选择，错别字的修改等一切不利于阅读流程的因素就是噪音。每个人对噪音的忍耐都有一个阈值，超过这个阈值，那么这就是一次糟糕的阅读。

> 根据控制论，此系统可以看作一个开环控制系统，当且仅当系统的各个部分性能稳定且外界干扰较小，才能保持一定的精度。比开环更高阶的是闭环系统，其核心是输出反作用于输入，也就是“吃一堑，长一智”。

## 订阅源
### 格式
RSS订阅源，本质上是一个xml类型的文件，在十来年前已经形成了业界标准，主要就是rss与atom以及整合了两者的rss2.0。它主要是把网站的主要内容分标签存到里面，可以看作没有样式的html，人们往往把它成为Feed。本站用atom生成的xml结构如下：

开头是网站的基本信息，体现到阅读器上就是标题、描述、logo等
```xml
<feed xmlns="http://www.w3.org/2005/Atom">
<title>Foundation</title>
<icon>https://blog.si-on.top/images/logo.svg</icon>
<subtitle>Sion's blog</subtitle>
<link href="https://blog.si-on.top/atom.xml" rel="self"/>
<link href="https://blog.si-on.top/"/>
<updated>2022-11-17T15:42:41.912Z</updated>
<id>https://blog.si-on.top/</id>
<author><name>Sion Tine</name></author>
<generator uri="https://hexo.io/">Hexo</generator>
```
主体内容：包括文章的标题，描述，发布更新时间、分类、标签等
```xml
<entry>
	<title>📸500px 网页相册</title>
	<link href="https://blog.si-on.top/2022/Anti500px"/>
	<id>https://blog.si-on.top/2022/Anti500px</id>
	<published>2022-11-10T15:21:25.000Z</published>
	<updated>2022-11-17T15:42:41.912Z</updated>
	<content type="html">
	...
	</content>
	<summary type="html">通过referrerPolicy属性实现500px反防盗链引用图片。</summary>
	<category term="生活" scheme="https://blog.si-on.top/categories/%E7%94%9F%E6%B4%BB/"/>
	<category term="杂谈" scheme="https://blog.si-on.top/categories/%E7%94%9F%E6%B4%BB/%E6%9D%82%E8%B0%88/"/>
	<category term="奇技淫巧" scheme="https://blog.si-on.top/tags/%E5%A5%87%E6%8A%80%E6%B7%AB%E5%B7%A7/"/>
	<category term="摄影" scheme="https://blog.si-on.top/tags/%E6%91%84%E5%BD%B1/"/>
</entry>
```
这样的xml文件可以很好的分离开内容与样式，让信息只留有最纯粹的内容。

### 源之源
最好最稳定的订阅源永远是原生的，也就是网站本身提供的。这类网站也不少，比如少数派的[Feed](https://sspai.com/feed),书伴的[Feed](https://feeds.feedburner.com/bookfere),博客园为用户提供的[Feed](https://www.cnblogs.com/aornus/rss)。最近几年的一个项目RSSHub提供了制作了大量网站的rss源，但经过我长时间的体验，特别是某些质量总归没有内容所有者自己发布的好，所以能找来原生的就尽量不要用抓取来的源。
好在现在大部分有点开放思维的网站都提供了Feed，我们可以非常简单地获取，但是也有许多网站没有提供，比如微信微博知乎之类。但是**哪里有需要，哪里就有对策**。这里分享几个可以获得稳定Feed的聚合网站：
#### Innoreader（2012~）
[重新掌控你的新闻订阅源 (innoreader.com)](https://www.innoreader.com/)
> 几度被墙，后以加n，重出江湖。
#### Feedx（2016.5~）
[献给那些至今还对RSS钟情的人们](https://feedx.fun/about)
#### RSSHub（2018~）
[万物皆可RSS](https://rsshub.netlify.app/)
> 国内稳定部署网站：https://rsshub.rssforever.com
#### Feedd（2021~）
[让信息重新汇聚到一起，以更自由的方式。](https://feeddd.org/feeds)
## 阅读器订阅
这一节该安利些RSS阅读器了。
### Fluent Reader（Windows）
可以自定义字体，排版。

![直排](../../../images/20221012/Pasted%20image%2020221126122715.png)

### Feeder（Android）
很理想的移动端阅读器
![](../../../images/20221012/Pasted%20image%2020221126123553.png)


## 邮箱订阅
E-mail,这个古老而又神奇的技术,在技术风云变幻的几十年间从未倒下,似乎用email来订阅是最完美的方案，~~而且比许多简洁(FuZa)的阅读器好用多了~~(我后悔说过这句话)
### 格式
电子邮箱里的邮件本质上就是个附加了格式的xml文件，如果你导出一封邮件就会发现它的后缀是——eml文件。

> EML格式是微软公司为Outlook和Outlook Express开发的文件格式。EML文件是将邮件归档后生成的文件，保留着原来的HTML格式和标题。

这里以一封有复杂内容的Newsletter邮件为例来简要说明eml的组成。
开头依旧是邮件的基本信息：
```xml
MIME-Version: 1.0
Date: Fri, 25 Nov 2022 22:21:40 +0800
From: follow.it <hi@follow.it>
Subject: =?utf-8?Q?=E5=B0=91=E6=95=B0=E6=B4=BE_-_new_message?=
Thread-Topic: =?utf-8?Q?=E5=B0=91=E6=95=B0=E6=B4=BE_-_new_message?=
Message-ID:
 <01070184af2a4b28-fffd5469-06a1-4714-96be-e56b09946f90-000000@eu-central-1.amazonses.com>
To: "siontian@outlook.com" <siontian@outlook.com>
Content-Transfer-Encoding: quoted-printable
Content-Type: text/html; charset="utf-8"

<head>
<meta http-equiv=3D"Content-Type" content=3D"text/html; charset=3Dutf-8"><!=
--[if !mso]><!--><meta http-equiv=3D"X-UA-Compatible" content=3D"IE=3Dedge"=
><!--<![endif]--><meta name=3D"viewport" content=3D"width=3Ddevice-width,in=
itial-scale=3D1.0"><meta name=3D"x-apple-disable-message-reformatting"><tit=
le>Newsletter</title>
```
然后是样式
```xml
<style type=3D"text/css">
img {
max-width: 100% !important;
height: auto !important;
}
html, body {
Margin: 0;
padding: 0;
}
table {
border-collapse: collapse;
}

...

</style><!--[if gte mso 9]>
```
最后是正文
```xml
太混乱了，这里无法描述.....
```
可见，这个文件试图把内容和样式聚合在一起，但结果可想而知，不但个人难以自定义eml样式，导出的内容还难以转化。最可恨的是，图片往往还是链接的形式，当源站垮掉的时候，当然也看不到图片了。总之，它不适合阅读。
### 自力更生
这里推荐个项目，都是可以实现推送与样式自定义的。
#### rss2email（Python）
A python script that converts RSS/Atom newsfeeds to email.
#### Calibre
可以把订阅制成电子书发送到邮箱。
### 第三方服务
#### Follow.it
这是一个理想化的邮件订阅系统,打开选取5种订阅来源。
##### 订阅源获取
1. Rss的feed地址
2. 网站自带的主流订阅源(英文为主)
3. 使用Follow.it的工具()
	1. Chrome拓展
	2. 小书签(这个NB啊)
	3. 加前链
4. OPML导入
5. 特殊订阅(还没有开发完成,有天气,Youtube提醒等小工具)
##### 订阅源管理
比较人性化的是，它会显示出来每个订阅在一周可以收到几条信息。
1. 过滤机制
	1. 关键词
	2. 标签
	3. 作者
2. 输出渠道
	1. 电子报(每天推送一次，可以自由设定推送时间)
	2. 邮件(对于每条订阅都会发送一封邮件)
	3. Follow.it的网页新闻阅读器以及拓展
	4. RSS输出
	5. 推送到电报,推特
#### Blogtrottr.com
这个网站的操作很简单:
1. 输入订阅源
2. 输入接收邮箱
3. 推送时间(还有即时类型的)
最后点击Feed.(注册了的话就不需要每次订阅进行人机验证了)
### 体验结果
我用了这两个网站提供的推送服务三天，体验很差，换句话说，这不是信息的整理归档，这简直就是在用低配的Low的不能再Low的文字阅读器，天杀的浪费了我两天的激情！缺点如下：
1. 文件臃肿
	上面的几个订阅服务提供商的确给了用户极大的自由度去推送，但是免费用户的限制也很多，就以Follow.it为例，当你把每条Rss订阅都设置为22:00推送全文推送时，它就在22:15左右推送给你，不过不是好几条，而是一条长长长长长长长长文。
	![Follow.it阅读界面，长得十个屏幕也截不下](../../../images/20221012/Pasted%20image%2020221126131552.png)
2. 结构混乱
	假设你已经设置好了邮箱归档，每条订阅都会按照指定规则归档到一个文件夹里。单单就一个订阅而言，它至少有三四条文章吧，连个快速跳转都没有。
3. 阅读体验差
	邮箱是用来传递简讯的，我却想把它搞成一个阅读器，这一开始就是个错。Newsletter的定位就是营销广告，怎么会有阅读体验呢（实际上，那根本没有体验）。
	免费的推送内容被污染。以摆脱信息轰炸而生的RSS,为摆脱设备软件依赖而生的Newsletter,两者的结合理应是优势互补的，好比两块有破洞的布，合在一起就能遮住各自的不足，但是结果恰恰相反，这两者的结合不是优势互补而是大部分的劣势互补。邮件正文往往有删不掉的提供商Logo，免费版必须有的广告之类的。
![Blogtrottr.com体验稍微好点，但免费版会在开头结尾加上广告](../../../images/20221012/Pasted%20image%2020221126131856.png)
## RSS阅读流程的简化
根据本文开头所讲的阅读/信息处理流程——**输入，处理，输出。** 我们可以这样思考，把从RSS获取到阅读展示的整个过程比作一个层，再把阅读到批注输出看作另一个层，每一层都包括三个步骤。
### RSS阅读流程
在RSS推送流程里可以这样理解：
* 输入的是RSS的原始层。
* 处理是一个中介软件或者供应商提供的推送、转换服务。以及自己制定订阅源分类，收件箱文件夹归档等。
* 输出是展示层，这里是阅读器或者邮件查看器。

Rss是把复杂的资讯抽取到一个简单的层，我们把这一层称为**输入层**。
就阅读性而言，这一层展示的是一堆json代码，没有阅读性可言。就内容而言，由于订阅源的关系，纯粹的内容是不可能的，一定会含有些许广告跟冗杂元素，由于这是不可能避免的，我们可以坦然接受。

RSS阅读器与邮箱推送本质上都是把原始xml代码转化为可以观看的内容，不考虑分类操作，我们把这两层合并称为**处理与输出层**。

就阅读性而言，前者再不济也比后者强。归档，分类操作都更加简单，甚至有的还提供了批注功能(这点很关键，涉及到阅读的处理操作)。但由于RSS阅读器的开发者能力与个性的差异，软件所适用的平台，内容阅读的UI，都有很大的局限性，很难满足所有人的需要，所以用阅读器也并不是一个很好的绝佳阅读方式。邮箱里的文章本质是把失却了js、css的xml文件附加上定制的丑B样式，客制化能力极为缺失。

就内容而言，后者的冗杂元素更少，占用空间更小。统一在格式化的邮件里，其可获得性也更广泛，适用于一切可以使用邮箱的设备。不过这唯一的优点也没有什么意义可言，没有几个人会成天拿个诺基亚读新闻吧。

### 阅读流程
这是第二个层，我们可以这样理解：
* 上述信息的获取流程可以作为阅读的**输入层**。
* **处理层**可以表示我们阅读行为的主要过程。
	* 依赖于手机屏幕，纸质书，电纸书阅读器等的阅读
	* 手写摘抄笔记(这个方法可能很少人用了吧) 
	* 用软件上的批注摘录功能来处理信息
	* 整理归纳笔记
* **输出层**就不必说了，那就是阅读的作用。可以是知识的获取，也可以是一个想法，念头，一个动机，一次生活方式的改变，甚至另一篇博文的诞生。

那么问题来了，是否有一种方法可以用来简化这两个流程呢？确实是有的。那就是————

**把RSS订阅直接制做成一个排版优良的电子书，然后在设备上去阅读批注，最后自动导出笔记并进行整理归纳。**

### 整合式订阅
随着Kindle退出中国，Kindle已然成为继诺基亚、黑莓以后的一种新的设备情怀，很多优秀的项目都出自于读者们对阅读的热爱，后面推荐的几个软件与网站无一不是如此。
这种方式不存在硬件限制。kindle简单地讲就是一个不伤眼的epub/pdf/mobi/azw...阅读器，这种软件在各个平台上多如牛毛，只要你有一个设备，就可以用这种方式整合RSS订阅进行阅读。
#### 自力更生
Calibre的RSS抓取制书功能很强，是一个首选，具体操作参考书伴的这篇文章：[Calibre 使用教程之抓取 RSS 制成电子书](https://bookfere.com/post/256.html)。
#### 第三方服务
https://inkread.com/
这个网站是我最先的选择，但是限制太多了，直到看到了后者......
http://wheremylife.cn
这是现阶段最佳的选择，就文件而言，排版没有太大错误，文首还有推送情况介绍，每篇文章都有目录，跳转极为方便，没有付费服务，作者用爱发电好多年......
![推送概况与目录](../../../images/20221012/Pasted%20image%2020221126183318.png)

### 阅读与批注
就文件格式而言，epub，pdf格式是通用的，epub的阅读性是更胜一筹。然后再找一个阅读器就可以很好的阅读批注了，至于各个平台上理想的阅读器，推荐读这篇文章：[Foliate安装](/2022/foliate)。
foliate的epub批注功能是最强的，而且可以导出为html、md等格式的文件。
![导出的html批注文件](../../../images/20221012/Pasted%20image%2020221126184001.png)
### 笔记整理
用Obsidian处理足矣。
一般的话可以考虑用Foliate导出为md，加标签进行整理。Kindle的话，有个Kindle Highlights插件可以很好的导入批注。
![](../../../images/20221012/Pasted%20image%2020221126184548.png)

[^1]:维基百科编者. RSS[G/OL]. 维基百科, 2022(20220516)[2022-05-16]. [https://zh.wikipedia.org/w/index.php?title=RSS&oldid=71669757](https://zh.wikipedia.org/w/index.php?title=RSS&oldid=71669757).