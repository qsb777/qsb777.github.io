---
title: 一些常用的函数
date: 2021-08-11 08:53:00
categories: JavaScript
tags: JavaScript
---

### 深拷贝
``` JavaScript
function clone (data) {
  if (Array.isArray(data)) {
    data.map(clone)
  } else if (data && typeof(data) === 'object') {
    let obj = {}
    for(let key in data) {
      obj[key] = clone(data[key])
    }
  } else {
    return data
  }
}
```