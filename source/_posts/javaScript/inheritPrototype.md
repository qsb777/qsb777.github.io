---

date: 2021-08-24 21:39:24
title: JavaScript中继承的方法
categories: JavaScript
---

*** 实现一个父类

``` JavaScript
  function People () {
    this.name = '小李'
    this.age = 23
    this.job = function() {
      return '程序员'
    }
  }
  People.prototype.say = function () {
    console.log(this.name+'是一个' + this.age + '的' + this.job)
  }
```

*** 方法一

> - 缺点:

> - 优点:

``` JavaScript
  
```
