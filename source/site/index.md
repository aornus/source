---
title: 网站琐记📜
mathjax: true
date: 2022-02-18 21:50:32
updated:
type:
description:
keywords:
top_img:
aplayer:
aside: false
highlight_shrink:
---

{% echarts 400 '85%' %}
{
    title: {
        text: "",
        subtext: "2021-8~2022-5"
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["文章统计"],
        selectedMode: false
    },
    toolbox: {
        show: false,
        feature: {
            mark: {
                show: true
            },
            dataView: {
                show: true,
                readOnly: true
            },
            magicType: {
                show: false,
                type: ["line", "bar", "stack", "tiled"]
            },
            restore: {
                show: true
            },
            saveAsImage: {
                show: true
            }
        }
    },
    calculable: true,
    xAxis: [
        {
            type: "category",
            boundaryGap: true,
            data: ["8", "9", "10", "11", "12", "1", "2", "3", "4"],
            position: "bottom",
            name: "月份",
            nameLocation: "end",
            splitNumber: 0,
            scale: true,
            nameTextStyle: {
                baseline: "top"
            },
            axisLabel: {
                show: true,
                formatter: "{value}月"
            },
            splitLine: {
                show: true,
                lineStyle: {
                    type: "dashed"
                }
            }
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "文章",
            nameLocation: "end",
            nameTextStyle: {
                align: "right",
                baseline: "middle"
            },
            axisLine: {
                show: true
            },
            axisLabel: {
                formatter: ""
            },
            splitLine: {
                lineStyle: {
                    type: "dashed"
                },
                show: true
            }
        }
    ],
    series: [
        {
            type: "line",
            itemStyle: {
                normal: {
                    areaStyle: {
                        type: "default"
                    },
                    color: "rgb(0, 191, 191)",
                    label: {
                        show: true,
                        position: "top",
                        textStyle: {
                            color: "rgb(0, 0, 0)"
                        }
                    }
                }
            },
            name: "文章",
            data: [4, 12, 11, 6, 6, 1, 8, 9, 8,],
            symbol: "emptyCircle",
            smooth: true,
            markPoint: {
                data: []
            }
        }
    ]
}
{% endecharts %}
<div class="btn-center">
{% btn '/categories/Code/',编程,far fa-hand-point-right,outline blue larger %}
{% btn '/categories/周刊',周刊,far fa-hand-point-right,outline pink larger %}
{% btn '/categories/数学/',数学,far fa-hand-point-right,outline red larger %}
{% btn '/categories/杂谈/',杂谈,far fa-hand-point-right,outline purple larger %}
{% btn '/categories/材料科学/',材料科学,far fa-hand-point-right,outline orange larger %}
{% btn '/categories/Hexo/',Hexo,far fa-hand-point-right,outline green larger %}
</div>

# 网站小事记

{% timeline 2020 %}

<!-- timeline 3-20 -->
起源：突发奇想，购买阿里云轻量级应用服务器，使用LNMP+WordPress建站。

<!-- ![逐云雀·新希望](https://cdn.jsdelivr.net/gh/aornus/blogimg/2022b&amp_bo_HgedAwAAAAARALA_&rf_viewer_311.jpg) --> 

域名：[ **sky-lark.top**](https://sky-lark.top)

<!-- endtimeline -->

<!-- timeline 6-15 -->
重装系统为centos，使用宝塔后台+Wordpress休整。

<!-- endtimeline -->

<!-- timeline 9-17 -->
读勃朗宁夫人的十四行诗，觉得**Aornus**(印度的山，意为无鸟山)这个词很好听。

<!-- endtimeline -->

<!-- timeline 10-1 -->
网站被土耳其黑客入侵，你们不是站起来的狼，是死的不能再死的死狗！

恢复到9-25，还好只丢失了几天的数据。

<!-- endtimeline -->

{% endtimeline %}

{% timeline 2021 %}

<!-- timeline 3-25 -->
域名与服务器到期，觉得没什么意思，没有续期，第一次建站结束。

<!-- endtimeline -->

<!-- timeline 5-15 -->
得知git托管平台+hexo可以免费建站，初次尝试失败。

<!-- endtimeline -->

<!-- timeline 08-29 -->
摸索了一个下午，成功在本地termux上部署hexo,配合gitee的pages服务(等了几个月了)，第二次建站开始。

域名：**aornus.gitee.io**

<!-- endtimeline -->

<!-- timeline 09-07 -->

修改主题为`butterfly`，爱不释手。

<!-- endtimeline --> 

<!-- timeline 09-13 -->

增加数学公式的支持，美化了页面。

<!-- endtimeline --> 

<!-- timeline 11-25 -->

删除了所有不必要的内容，封笔，进入了短暂的休整期。

<!-- endtimeline --> 

<!-- timeline 12-27 -->

进入期末复习，更新了一些学习笔记。

<!-- endtimeline --> 


{% endtimeline %}

{% timeline 2022 %}

<!-- timeline 02-05 -->

开始紫晶子计划-**金石周刊**，

<!-- endtimeline --> 

<!-- timeline 02-13 -->

转移部署到githubpages，

域名：**aornus.github.io**

<!-- endtimeline --> 

<!-- timeline 02-14 -->

使用Freenom免费域名服务+Cloudflare CDN

域名：**aornus.tk**

<!-- endtimeline --> 

<!-- timeline 02-20 -->

起了一个英文名sion，更改域名

域名：**sion.tk**

<!-- endtimeline --> 

<!-- timeline 02-22 -->

“贰”的狂欢：更换主字体为思源宋体。

<!-- endtimeline --> 

<!-- timeline 03-09 -->

购买新域名，配合cloudflare反代了tg频道

域名:  [**si-on.top**]( https://si-on.top)

<!-- endtimeline --> 

<!-- timeline 03-18 -->
添加了 mindmap 与 echarts支持，
<!-- endtimeline --> 

<!-- timeline 03-19 -->
更换评论系统vline 为[Wline](https://waline.js.org/)
<!-- endtimeline --> 

<!-- timeline 03-24 -->
建立写作专用子域：[🪶](https://ink.si-on.top/)
<!-- endtimeline -->

<!-- timeline 03-28 -->
成功加入十年之约，虫洞走起!
<a href="https://www.foreverblog.cn/go.html" target="_blank"> <img src="https://img.foreverblog.cn/wormhole_3_tp.gif" alt="" style="width:auto;height:32px;" title=" "></a>
<!-- endtimeline -->

<!-- timeline 03-29 -->
利用Vercel建立云盘，名之为[SionCloud](https://sionedrive.vercel.app)
<!-- endtimeline -->

<!-- timeline 04-15 -->
1. 关闭访问量、阅读量统计以及访客地图。
2. 创建主页：[Home](https://home.si-on.top/)
<!-- endtimeline -->

<!-- timeline 04-16 -->
听说Vercel速度不错，开启了镜像站，顺便绑定上上了之前的两个域名。
1. [Vercel镜像站](http://sion.tk/)=[vercel](https://sion-eta.vercel.app/)
2. [Netify镜像站](https://aornus.tk)=[netlify](https://625a6bec72983054d0757833--cheery-fudge-471d5e.netlify.app/)
[![Netlify Status](https://api.netlify.com/api/v1/badges/cd86e249-261e-449c-832f-ae47b14d3f78/deploy-status)](https://app.netlify.com/sites/cheery-fudge-471d5e/deploys)

> 由于找不到哪里有违禁内容，一个多月来，giteepages一直部署不了。4月16日，彻底跟gitee断绝关系，网站源码转移到github上。
<!-- endtimeline -->

<!-- timeline 04-17 -->
开启赞赏功能，目前仅支持加密货币（赞赏二维码采用极限识别设计，inspired by Minor'book.）
<!-- endtimeline -->

{% endtimeline %}