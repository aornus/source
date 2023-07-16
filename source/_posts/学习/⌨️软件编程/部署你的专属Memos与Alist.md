---
title: 一分钟免费部署你的专属Memos
abbrlink: deploy-memos-in-60s
katex: false
root: ../../
categories:
  - 学习
  - ⌨️软件编程
hidden: 
date: 2023-03-22 22:22:16
update: 2023-03-22 22:22:16
tags:
- 奇技淫巧
- 技术
cover: /images/Cover/memos.svg
comments:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
aside: false
password:
description: 使用Zeabur快速免费部署Memos与Alist 
sticky:
keywords: 
---

> <center>一片飞雪，坠入炉火，继而升腾，无影无踪。</center>
> <p align="right">——秉蕳</p>


>这是篇讨巧于**时机与信息传播速度**的投机教程，其内容本身没有太大技术含量，也并非本站的主要内容，我很抱歉Bing把这篇文章的权重调的太高。

{% tip warning %}
Zeabur免费版现在(2023/7/17)需要每七天按时点击才能保持运行，也可以绑定支付方式的方式持续运行，不过可能会误扣费⚠。
{% endtip %}
{% markmap 300px %}
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [楔子](#楔子)
- [急速部署](#急速部署)
  - [部署Memos](#部署memos)
    - [Memos的使用](#memos的使用)
    - [使用Cloudflare提供的R2储存作为图床](#使用cloudflare提供的r2储存作为图床)
    - [木木木木木博主的Memos折腾文章](#木木木木木博主的memos折腾文章)
    - [安卓客户端](#安卓客户端)
    - [Obsidian使用Memos](#obsidian使用memos)
  - [部署Alist](#部署alist)

<!-- /code_chunk_output -->
{% endmarkmap %}



## 楔子
近日来，一个类似于Railway的可以部署项目的新兴网站——[Zeabur](http://zeabur.com/)吸引了我的注意。根据介绍，它不仅可以部署类似于hexo、next.js等轻量级的静态页面，还可以部署一些后端的数据库、Serverless等 

###  Zeabur详细的支持内容 
以下框架可以被 Zeabur 自动识别并进行相关优化：

-   [Next.js(opens in a new tab)](https://nextjs.org/)
-   [create-react-app(opens in a new tab)](https://create-react-app.dev/)
-   [Vite(opens in a new tab)](https://vitejs.dev/)
-   [Remix(opens in a new tab)](https://remix.run/)
-   [Umi.js(opens in a new tab)](https://umijs.org/)
-   [Nuxt.js(opens in a new tab)](https://nuxtjs.org/)
-   [vue-cli(opens in a new tab)](https://cli.vuejs.org/)
-   [Qwik(opens in a new tab)](https://qwik.builder.io/)
-   [NestJS](https://nestjs.com/)

下面的项目都可以部署
* 静态站点：比如hugo、hexo等
* Java: [Spring Boot(opens in a new tab)](https://spring.io/projects/spring-boot)
* Go: 所有基于 [Go Modules(opens in a new tab)](https://blog.golang.org/using-go-modules) 的项目都可以部署。
* Python: 项目根目录有 `main.py` 或 `app.py`，Zeabur 会自动以 Python 项目的方式进行部署。
* Deno
* MongoDB、MySQL、Redis、PostgreSQL数据库


在[Tg群](https://t.me/zeabur_app)观望了几天之后，网站终于在今天下午有了些引人注目的改进。中午时分，在一些群友的呼吁下，Memos部署被提上了议程。网站负责人的效率非常高，从决定支持到上线仓库商店，不到一个小时时间。接下来我就简要介绍一下如何快速部署Memos，真的非常非常简单。

>这个Zeabur网站是一个新兴网站，处于建设初期，后期发展起来的话可能会有许多人部署，说不一定会有些乱七八糟的东西导致被GFW掉，所以不会导入导出Memos数据的话（我暂时也不知道如何操作），谨慎把这个Memos当作主力记录工具。


## 急速部署
1. 打开Zeabur的官网：[Zeabur](https://dash.zeabur.com/projects)
![官网的界面，大体看来是主要面向中文用户](../../../images/20230304/Pasted%20image%2020230322223104.png)
2. 使用Github账户登录（现在需要两步验证了，建议使用微软的Authenticator APP来进行密码管理）
3. 进入控制台后新建一个项目(Project)：名称随意，
![新建一个名为**Memos**的项目](../../../images/20230304/Pasted%20image%2020230322225344.png)
4. 点击进入项目，然后点击添加服务
![](../../../images/20230304/Pasted%20image%2020230322225939.png)
5. 从市场中选择部署
![Zeabur的两种部署来源](../../../images/20230304/Pasted%20image%2020230322230157.png)
### 部署Memos
接下来下拉找到集成好的Memos项目
![点击最下面的Memos项目后点击部署，几秒钟后就可以部署完成](../../../images/20230304/Pasted%20image%2020230322230302.png)
7. 生成Zeabur提供的域名
![找到Domin，输入一个合适的名字（不能有特殊字符）](../../../images/20230304/Pasted%20image%2020230322230658.png)
8. （自定义域名）在Cloudflare里添加一个指向`zeabur.app`的`CNAME`，（记得关闭这条DNS的代理，一会就可以访问了，不然会出现多次重定向的错误）
![](../../../images/20230304/Pasted%20image%2020230322230933.png)
9. 部署成功
![成品展示](../../../images/20230304/Pasted%20image%2020230322231336.png)

#### Memos的使用

>Memos[^1]就是记录闪念的一个工具，其实记录念头最最方便的还是纸笔，过于依赖这玩意儿并不会让生活变得更好，因为充实的生活才是一切感想、念头、文章、工具...的动力与来源。


这里简单提几个技巧，诸位有心再折腾的可以参考这些文字/工具进一步玩弄：
#### 使用Cloudflare提供的R2储存作为图床
可以参考这篇文章[Configuring Cloudflare R2 Storage in Memos - memos (usememos.com)](https://usememos.com/docs/storage)进行配置
我的配置如下：
![使用了自定义域](../../../images/20230304/Pasted%20image%2020230322231911.png)
#### 木木木木木博主的Memos折腾文章
[Hi，Memos](https://immmmm.com/hi-memos/)

#### 安卓客户端
这里力荐[MoeMemos](https://f-droid.org/packages/me.mudkip.moememos/)只用输入域名、账户、密码就可以用了

![Fdroid的第三方客户端NeoStore中展示的MoeMemos应用](../../../images/20230304/Pasted%20image%2020230322232631.png)
![输入登录信息](../../../images/20230304/Pasted%20image%2020230322232924.png)


#### Obsidian使用Memos
通过这个插件[Quorafind/Obsidian-Memos](https://github.com/quorafind/obsidian-memos)可以在Obsidian中实现相似的体验，不过这个插件似乎不能导出。
![我已经用了好久了，一直就把它当作日记的一部分【SeedCollecter 种子收集】](../../../images/20230304/Pasted%20image%2020230322233954.png) 

### 部署Alist
{% tip ban %}
Zeabur 由于流量费用问题，于2023-3-27晚间下架所有包括已部署的Alist服务。
{% endtip %}


Zeabur一个项目可以部署很多个服务，这里就在上面创建的Memos项目里添加一个Alist[^2]项目
![](../../../images/20230304/Pasted%20image%2020230325200857.png)
部署完会得到初始密码与账户，记得登陆后立即修改之！
![初始密码](../../../images/20230304/Pasted%20image%2020230325201753.png)
接着添加域名与DNS记录
![自定义域名](../../../images/20230304/Pasted%20image%2020230325201513.png)
![alist.si-on.top](../../../images/20230304/Pasted%20image%2020230325201416.png)
记得修改密码添加两步验证（建议使用微软的Authenticator APP），备份配置文件
![成品](../../../images/20230304/Pasted%20image%2020230325205907.png)
[^1]: https://usememos.com/
[^2]: https://alist.nn.ci/zh/