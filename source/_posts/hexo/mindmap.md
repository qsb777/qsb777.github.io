---
date: 2021-10-06 22:50:02
title: 在hexo中使用思维导图
categories: 软件使用
tags: Hexo
---


### 使用方法

> 在hexo根目录下安装插件：npm install hexo-markmap， 然后在文章写作中执行下面格式的代码就行了


```
  {% markmap 300px %}
    # Testa
    ## test1
    ## test2
    # Testb
    ## test1
    ## test2
  {%endmarkmap%}

```
{% markmap 300px %}
# Testa
## test1
## test2
# Testb
## test1
## test2
{%endmarkmap%}



  参考链接: [https://zhangmaimai.com/2021/02/23/hexo-mindmap-plugin/](https://zhangmaimai.com/2021/02/23/hexo-mindmap-plugin/)