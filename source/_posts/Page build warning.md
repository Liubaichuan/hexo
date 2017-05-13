---
title: Page build warning
date: 2017-5-13 21:56:44
tags:
- 一顿烧烤
categories:
- 解决方案
- Hexo&Next
---

#### 症状

每次有修改用Github进行Sync后，一封如鬼影随行般的Page build warning邮件便发送到注册Github的邮箱中。虽然可以正常部署且正常访问（这一点我和下面所列的参考中的情况不同，他好像是不能正常访问），但是这是要逼死强迫症啊啊啊[○･｀Д´･ ○]

贴上邮件内容

> The page build completed successfully, but returned the following warning for the `master` branch:
>
> You are attempting to use a Jekyll theme, "next", which is not supported by GitHub Pages. Please visit https://pages.github.com/themes/ for a list of supported themes. If you are using the "theme" configuration variable for something other than a Jekyll theme, we recommend you rename this variable throughout your site. For more information, see https://help.github.com/articles/adding-a-jekyll-theme-to-your-github-pages-site/.
>
> For information on troubleshooting Jekyll see:
>
>   https://help.github.com/articles/troubleshooting-jekyll-builds
>
> If you have any questions you can contact us by replying to this email.

#### 原因

小白的我在网上试图找到原因及解决方案，但没有找到大神解释原因，所以**原因不明**。个人的感觉可能是修改主题配置时有写进介于正确和错误之间的配置代码，使得Github认为这是一个Jekyll主题，莫名莫名。

#### 解决方案

##### 方案一

印象中，早先我遇到这个问题时，在Github中将用来编辑博客的仓库删去，再将Github远程仓库克隆到本地（←_←本质上，我觉得这没什么改变啊），就不会再有Page build warning邮件了，若死灰复燃，请尝试方案二。

##### 方案二

从头开始，哈哈哈！没错， reinstall hexo and next ！！！

> 参考：https://github.com/iissnan/hexo-theme-next/issues/1513