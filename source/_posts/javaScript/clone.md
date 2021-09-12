---
title: JavaScript深拷贝
date: 2021-08-11 08:53:00
categories: JavaScript
tags: JavaScript
---

### 方法一
> 这个方法的缺点是会把原型上的可枚举属性和方法一起克隆
``` JavaScript
function clone (data) {
  if (Array.isArray(data)) {
    return data.map(clone)
  } else if (data && typeof(data) === 'object') {
    let obj = {}
    for(let key in data) {
      obj[key] = clone(data[key])
    }
    return obj
  } else {
    return data
  }
}
```

### 方法二
> 这个方法只会克隆本身不会克隆原型上的属性和方法
``` JavaScript
function clone (data) {
  if (Array.isArray(data)) {
    return data.map(clone)
  } else if (data && typeof(data) === 'object') {
    let obj = {}
    for(let key in data) {
      if(data.hasOwnproperty(key)) {
        obj[key] = clone(data[key])
      }
    }
    return obj
  } else {
    return data
  }
}
```