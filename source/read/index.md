---
title: 阅读📚
mathjax: true
date: 2023-08-26 09:00:32
updated:
type:
aside: false
description: 阅读管理与备忘
keywords: 阅读，书摘
top_img: "repeating-linear-gradient(90deg, hsla(285,0%,67%,0.05) 0px, hsla(285,0%,67%,0.05) 1px,transparent 1px, transparent 96px),repeating-linear-gradient(0deg, hsla(285,0%,67%,0.05) 0px, hsla(285,0%,67%,0.05) 1px,transparent 1px, transparent 96px),repeating-linear-gradient(0deg, hsla(285,0%,67%,0.08) 0px, hsla(285,0%,67%,0.08) 1px,transparent 1px, transparent 12px),repeating-linear-gradient(90deg, hsla(285,0%,67%,0.08) 0px, hsla(285,0%,67%,0.08) 1px,transparent 1px, transparent 12px),linear-gradient(90deg, rgb(79, 30, 203),rgb(252,69,69));"
aplayer: true
comments: false
highlight_shrink:
---
{% note success %}
本页从属于秉蕳的**阅读、摄影、音乐、写作统计计划**
<p align="right">✍更新于2023.8.26</p>
{% endnote %}

## 阅读统计：
我主要使用Notion做统计：读完一本书后，添加一些必要的数据，打标签，闲了再从相机里(实体书)或豆瓣里(电子书)上传封面，很是方便：

https://sionreading.notion.site/


{% echarts %}
{
    title : {
        text: '阅读媒介统计',
        subtext: '纸媒、数媒与混媒',
        x:'center'
    },
    tooltip : {
        trigger: 'item',
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: 'vertical',
        left: 'left',
        data: ['💻数媒','📜纸媒','➰混媒']
    },
    series : [
        {
            name: '数量',
            type: 'pie',
            radius : '55%',
            center: ['50%', '60%'],
            data:[
                {value:60, name:'💻数媒'},
                {value:225, name:'📜纸媒'},
                {value:5, name:'➰混媒'}
            ],
            itemStyle: {
                emphasis: {
                    shadowBlur: 10,
                    shadowOffsetX: 0,
                    shadowColor: 'rgba(0, 0, 0, 0.5)'
                }
            }
        }
    ]
}
{% endecharts %}
![阅读年度统计](https://pic.si-on.top/2023/08/%E9%98%85%E8%AF%BB%E5%B9%B4%E5%BA%A6%E7%BB%9F%E8%AE%A1.png)

## 书摘
这一部分是从[书见](https://memo.bookfere.com)里导出的书摘，以pdf为格式：
 <div>overflow-hidden rounded" style="height: 90vh;"><iframe src="https://mozilla.github.io/pdf.js/web/viewer.html?file=https://blog.si-on.top/pdf/书摘.pdf" frameborder="0" width="100%" height="100%"></iframe></div>



