---
title: DEBUG: Telnet console listening on 127.0.0.1:6023
date: 2018-3-30 20:33:36
tags:
- 爬虫
- Scrapy
categories:
- 解决方案
---

#### 原因

多半是挂着科学上网用的梯子导致报错。

#### 解决方案

多半把梯子退出也不能解决问题，Scrapy还是会使用代理，哈哈哈哈哈！正确姿势是在settings.py中修改：

```python
DOWNLOADER_MIDDLEWARES = {

'scrapy.downloadermiddlewares.useragent.UserAgentMiddleware': None,

}
```