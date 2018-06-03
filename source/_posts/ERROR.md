---
title: ERROR
date: 2018-3-30 20:33:36
tags:
- 爬虫
- Scrapy
categories:
- 解决方案
---

#### `DEBUG:Telnet console listening on 127.0.0.1:6023`

##### 原因

多半是使用代理导致报错。

##### 解决方案

多半退出代理也不能解决问题，Scrapy还是会使用代理。正确姿势是在settings.py中修改：

```python
DOWNLOADER_MIDDLEWARES = {
'scrapy.downloadermiddlewares.useragent.UserAgentMiddleware': None,
}
```

<!--more -->

#### `IndexError:list index out of range`

##### 原因

###### 原因一

访问超出范围

###### 原因二

如果是访问第一个元素就出现这样的报错，那多半是xpath写的不对。至于xpath怎么不对，这可就五花八门了。所以，以下解决方案也是基于会写xpath，觉得自己写的正确，但list就是为空的情况。

##### 解决方案

说起来，查看page source，注意是源代码，而不是developer tool，就基本可以避免这一问题。然而，也有对照着源代码写xpath最后list一样为空的情况。真要是遇到这种情况，还有一把万能钥匙：启用[Scrapy shell](http://scrapy-chs.readthedocs.io/zh_CN/0.24/topics/shell.html)，一步步尝试，查看response，同时对照page source，这样可以节约时间。

#### `ImportError: No module named items`

##### 原因

多半是新司机才会掉的坑，原因很简单：爬虫的名字和爬虫项目的名字搞成一样的了。By the way，请区别一下爬虫名，爬虫文件名和爬虫项目名。

##### 解决方案

改爬虫项目名或是改爬虫名