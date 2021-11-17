---
date: 2021-08-31 21:04:47
title: React初始化一些需要安装的插件
categories: JavaScript
tags: React
---

### 高阶组件装饰器配置
>  使用**npm install @babel/plugin-proposal-decorators --save-dev**安装插件。在package.json加配置如下。就可以使用装饰器语法 <font color="red">{@函数名}<font>

``` Json  
  {
    "babel": {
      "plugins": [
        [
          "@bable/plugin-proposal-decorators",
          {"legace": true}
        ]
      ]
    }
  }
```

