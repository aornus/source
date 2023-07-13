---
title: waline评论的邮箱提醒
tags:
  - 博客
  - 奇技淫巧
categories:
  - 学习
  - ⌨️软件编程
  - hexo
description: waline评论的配置、顺便申请一个略有限制的域名邮箱。
abbrlink: waline
date: 2023-05-19 23:14:33
cover:  /images/Cover/waline.svg
comments:
copyright:
aside:
password:
sticky:
---

## 楔子

用了这么久Waline，发现这个项目越来越好了，起初配置时邮箱提醒没有配置好，近来想再次尝试下。原本想申请一个域名邮箱来专门当做回复机器人，后经过一番搜罗，感觉Zoho提供的免费服务可以满足要求，但是它却不支持SMTP，只好申请了一个163邮箱来做。
## Waline 配置
这个CDN速度挺不错
* waline_js: https://unpkg.com/@waline/client@v2/dist/waline.js
* waline_css: https://unpkg.com/@waline/client@v2/dist/waline.css

本站waline的配置文件如下，其中<u>评论区的等级标签</u>采用泰拉瑞亚不同稀有度的矿石来设计；<u>文章反应</u>选择了3d质感的emoji；
```
waline:
  serverURL: https://www.sion.tk/
  pageview: true
  avatar: mp 
  avatarCDN: 
  bg: /images/blogimg/bunny.gif 
  visitor: false
  option:
    locale: {
      nick: '署名',
      mail: '邮箱',
      link: '域名',
      placeholder: '有朋自远方来，不亦乐乎！(无需登录，输入邮箱，回复可得通知)',
      requiredMeta: [],
      mailError: '你的邮件格式不对哦',
      nickError: 昵称不满足条件的错误信息,
      wordHint: 当前字数为$2个字，最少$0个字，最多$1个字哦,
      sofa: '显现与隐没都来自于自我，表达与沉默都是一种态度。',
      comment: 评论,
      uploading: 上载中,
      refresh: 重载中,
      anonymous: 无名氏,
      login: 登录,
      level0: '🔘青铜',
      level1: '🔲黑铁',
      level2: '🤍白银',
      level3: '🔵铂金',
      level4: '🟦钴蓝',
      level5: '💙钯金',
      level6: '🟠秘银',
      level7: '🟧山铜',
      level8: '🧡精金',
      level9: '🟣钛金',
      level10: '🟪叶绿',
      level11: '🔴夜明',
      level12: '🟥天顶',
      }
    emoji: [
        'https://cdn.jsdelivr.net/gh/norevi/waline-blobcatemojis@1.0/blobs',
        ]
    reaction: [
    'https://www.emojiall.com/images/60/microsoft-teams/1f31e.png',
    'https://www.emojiall.com/images/60/microsoft-teams/1f973.png',
    'https://www.emojiall.com/images/60/microsoft-teams/1f4aa.png',
    'https://www.emojiall.com/images/60/microsoft-teams/1f525.png',
    'https://www.emojiall.com/images/60/microsoft-teams/1f611.png',
    'https://www.emojiall.com/images/60/microsoft-teams/1f4a9.png',
    'https://www.emojiall.com/images/60/microsoft-teams/1f494.png',
        ]
    requiredMeta: ['nick', 'mail']
    wordLimit: [5, 1000]
    copyright: false
```

## Waline 邮箱回复-通用配置（以网易邮箱为例）

### 服务提供商端

1. 申请邮箱
2. 开启SMTP服务（一般是用手机发短信来验证开通）
3. 得到SMTP授权密码

![SMTP](../../../../images/202205/image-20220517115224333.png)

> 这一步之后，你应该获得：
>
> 1. 邮箱地址：`mail4sion@163.com`
>
> 2. SMTP授权密码：`42424242424`

### 个性化选项

主要是邮箱回复内容的配置

1. 网站名称：`Foundation`
2. 网站地址：`https://si-on.top`
3. 博主邮箱：（就是不提醒站长自己的评论） `agapehydor2@gmail.com`

### waline变量设置

经过以上选择之后，我们可以得到以下变量列表，将其依次填入waline的环境变量里。

> 填写了服务提供商，就不必要再填写SMTP地址了。

| 环境变量名称   | 值                      | 备注                                                         |
| -------------- | ----------------------- | ------------------------------------------------------------ |
| `SMTP_SERVICE` | 163                     | SMTP 邮件发送服务提供商                                      |
| `SMTP_HOST`    | —                       | SMTP 服务器地址，一般可以在邮箱的设置中找到。                |
| `SMTP_PORT`    | —                       | SMTP 服务器端口，一般可以在邮箱的设置中找到。                |
| `SMTP_USER`    | `mail4sion@163.com`     | SMTP 邮件发送服务的用户名，一般为登录邮箱。                  |
| `SMTP_PASS`    | `42424242424`           | SMTP 邮件发送服务的密码，一般为邮箱登录密码，部分邮箱(例如 163)是单独的 SMTP 密码。 |
| `AUTHOR_EMAIL` | `agapehydor2@gmail.com` | 博主邮箱                                                     |
| `SITE_NAME`    | `Foundation`            | 博客名称                                                     |
| `SITE_URL`     | `https://si-on.top`     | 博客地址                                                     |

> 以下是选填的环境变量:
>
> - `SENDER_NAME`: 自定义发送邮件的发件人
> - `SENDER_EMAIL`: 自定义发送邮件的发件地址
> - `MAIL_SUBJECT`: 自定义评论回复邮件标题
> - `MAIL_TEMPLATE`: 自定义评论回复邮件内容
> - `MAIL_SUBJECT_ADMIN`: 自定义新评论通知邮件标题
> - `MAIL_TEMPLATE_ADMIN`: 自定义新评论通知邮件内容

环境变量添加之后，重新部署

![Redploy](../../../../images/202205/image-20220517120458214.png)

### 结果展示

1. 用户**Moreread**以`2322748973@qq.com`为邮箱地址发表评论
2. 受到**Sion**的回复
3. **Moreread**收到提醒

![发表评论](../../../../images/202205/image-20220519120814137.png)

![Moreread的邮箱提醒](../../../../images/202205/image-20220519121032573.png)

> ![机器人端](../../../../images/202205/image-20220519120706936.png)
## （副产品）Zoho域名邮箱

> Zoho什么都好，但SMTP服务居然要付费，太狗了！（再次鄙视我白嫖的自己😒）

> 免费版的特性：
> - 5 个自定义用户,每用户5GB储存，邮件的附件不能超过25MB。
> - 仅Web端访问。
> - 支持1个域名的邮箱托管。


1. [注册链接（无推广）](https://mail.zoho.com.cn/signup)

2. 选择免费版

   ![image-20220517112508301](../../../../images/202205/image-20220517112508301.png)

3. 添加域名
![点击添加域名](../../../../images/202205/image-20220517112618667.png)
![填写域名信息](../../../../images/202205/image-20220517112700513.png)

4. DNS验证
![获取DNS解析代码](../../../../images/202205/image-20220517112755336.png)![Cloudflare添加txt解析](../../../../images/202205/image-20220517112934391.png)5. 创建账户
![创建名为`mailbot`的账户](../../../../images/202205/image-20220517113313413.png)
![仅付费用户可用IMAP！](../../../../images/202205/image-20220517113732393.png)

这个域名邮箱挺好，唯一不足的就是不能与QQ邮箱互发压缩文件，我就踩了好几回坑😫。