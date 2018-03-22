---
title: NodeJieba安装记
date: 2018-3-22 20:59:22
tags:
- Hexo&Next
categories:
- 解决方案
---

#### 介绍

[NodeJieba](https://github.com/yanyiwu/nodejieba)是"结巴"中文分词的 Node.js 版本实现， 由[CppJieba](https://github.com/yanyiwu/cppjieba)提供底层分词算法实现， 是兼具高性能和易用性两者的 Node.js 中文分词组件。性能杠杠的，应该是目前性能最好的 Node.js 中文分词库，没有之一。

#### 症状

安装失败

贴上Error info：

> Error: The module '\\?

> \E:\Blog\hexo\node_modules\pinyin\node_modules\nodejieba\build\Release\nodejieba.node'
> was compiled against a different Node.js version using
> NODE_MODULE_VERSION 48. This version of Node.js requires
> NODE_MODULE_VERSION 59. Please try re-compiling or re-installing
> the module (for instance, using `npm rebuild` or `npm install`).

<!-- more -->

#### 原因

其实，一眼就能瞅出是Node.js版本的问题

报错信息的正确理解应该是Nodejieba需要的是NODE_MODULE_VERSION为48的Node.js，而现在Node.js的NODE_MODULE_VERSION是59。然而，我给理解反了，找NODE_MODULE_VERSION为59的挨个试，直到一次试探性安装······哎，毕竟too young，还是speak very poor English

  #### 解决方案

Node.js下载：https://nodejs.org/zh-cn/download/releases/



> 参考：https://blog.csdn.net/fengxiaoxiao_1/article/details/77073918