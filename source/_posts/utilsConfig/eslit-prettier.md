---
date: 2021-09-01 10:20:20
title: Eslint+Prettier配置
categories: 工具配置
tags: Eslint
---

### 安装插件
> npm install eslint -D
> 在.eslintrc.js中加配置如下
``` JavaScript
  module.exports = {
    root: true,
    env: {
      browser: true,
      commonjs: true,
      es2021: true,
    },
    parser: 'babel-eslint', // 必须知道解析器
    extends: [
      "eslint:recommended", // 第一个参数使用eslint推荐配置，
       "plugin:prettier/recommended", // 第二个参数使用prettier推荐配置
       "plugin:vue/vue3-recommended", // vue3.0推荐配置
       "plugin:vue/recommended" // 如果使用的是Vue2.x
       "plugin:react/recommended", // react推荐配置
       "plugin:react-hooks/recommended" // react-hooks配置
       ],
    parserOptions: {
      ecmaVersion: 12,
    },
    plugins: [], 
    rules: {
    },
  };
```
> 在.prettierrc.js中加配置如下
``` JavaScript
  module.exports = {
    singleQuote: true, // 单引号
    semi: false, // 末尾分号
    // 以及一些自己的规则
  };

```

**在.j中配置的好处是可以写注释，也推荐在.js中配置**有可能会需要安装一些其他相关插件，例如：eslint-config-prettier eslint-plugin-prettier prettier-eslint eslint-plugin-vue eslint-plugin-react eslint-plugin-react-hooks