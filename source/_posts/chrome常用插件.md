---
title: chrome插件推荐
date: 2020-06-29 12:16:00
updated: 2020-06-29 14:30:00
tags: 
    - chrome
categories: 软件
keywords: 
description: chrome作为google开发的一款浏览器，市面上大部分的浏览器内核使用的都是基于chromium内核开发的，国内由于被墙，google搜索不能使用，这篇文章介绍如何使用google搜索引擎以及谷歌应用商店等
top_img: http://picture.saintblog.top/ide/ide.jpg
cover: http://picture.saintblog.top/ide/ide.jpg
comment: true
---

## 开发者模式

如果没有办法翻墙，无法访问谷歌的相关的东西，所以需要使用自行添加的chrome扩展程序，默认是无法添加非谷歌应用商店的扩展程序。

如果要使用第三方扩展程序，那么就要先开启chrome的开发者模式。

![扩展程序](http://picture.saintblog.top/chrome/chrome_extension.png)

开启右上角的开发者模式

![开发者模式](http://picture.saintblog.top/chrome/chrome_dev.png)

然后就可以使用第三方扩展程序了

## 谷歌访问助手

[https://www.crx4chrome.com/](https://www.crx4chrome.com/)  访问这个国内可访问的chrome插件网站，搜索`谷歌访问助手`，或链接[https://www.crx4chrome.com/crx/72437/](https://www.crx4chrome.com/crx/72437/)  ,点击`Download crx file from Crx4Chrome`

![ghelper](http://picture.saintblog.top/chrome/GHelper.png)

然后根据上面的图**打开扩展程序页面，将下载的文件拖进chrome**，然后可以看到右上角出现谷歌访问助手的图表，点击就会跳转需要登录注册的一个网页，用可以用的邮箱注册一个就可以用了。这样是已经成功登录并已经打开的状态了

![GHelper_on](http://picture.saintblog.top/chrome/GHelper_on.png)

这样就是已经可以使用谷歌搜索引擎和google应用市场等功能了。

**PS：chrome的扩展程序最好是在chrome网上应用店来下载，因为可以直接下载并安装，比较正规，避免chrome经常报一些第三方扩展程序的警告**

直接访问[chrome://apps/](https://chrome.google.com/webstore/category/extensions?utm_source=chrome-ntp-icon)

## 扩展程序推荐

### 1. Tampermonkey

知名的油猴管理器。记得当初看着这么一句话，用了chrome不用油猴，建议去用IE6。好像确实是这么一回事。为什么把tampermonkey放第一个推荐呢？？那是因为如果让我选择chrome上只安装一个扩展，那肯定是油猴，油猴可以另外再安装许多网站的js脚本，来解除网站的规定所带来的各种限制。

说到这里可能还是不怎么听的懂，举个栗子：百度文库的文章不能复制粘贴; 视频网站的片头广告; 访问的网站有一堆广告; 慕课网课等等。这些是否在日常生活中困扰到各位？？如果是的话，那赶紧装一个tempermonkey来爽一爽吧，如果不是那还是建议装一个，万一在什么地方用到了呢？

![tempermonkey](http://picture.saintblog.top/chrome/chrome_tempermonkey.png)

在chrome网上应用商店安装的只是管理脚本的管理器，需要的脚本还要另外装，推荐三个网站：

[https://openuserjs.org/](https://openuserjs.org/)、[https://greasyfork.org/zh-CN](https://greasyfork.org/zh-CN)、[https://userscripts-mirror.org/](https://userscripts-mirror.org/)

其中https://greasyfork.org/zh-CN对中文的适配最友好，推荐如果有需要就在这里安装需要的脚本

找到需要的脚本后，点击网页上的`安装此脚本`然后会跳转到tempermonkey的安装页面

![greasyfory](http://picture.saintblog.top/chrome/greasyfory_install.png)

在tempermonkey的安装界面，选择继续安装或取消，下面则是脚本的代码

![tempermonkey_install](http://picture.saintblog.top/chrome/tempermonkey_install.png)

油猴的脚本推荐建议看知乎的这个话题：[有哪些超神的油猴脚本？](https://www.zhihu.com/question/22210090)

### 2. 扩展管理器（Extension Manager）

一键管理所有扩展，快速开启/禁用、批量闪电管理，智能排序，右键卸载、锁定、选项配置，角标提醒，大小布局随心配。快捷、简单、安全。

![Extension Manager](http://picture.saintblog.top/chrome/chrome_extensionmanager.png)

把必要的主动性的插件放在chrome上方便操作，把被动性的插件放到扩展管理器中，避免chrome上一堆插件看的很不舒服

![Extension Manager](http://picture.saintblog.top/chrome/extensionmanager.png)

### 3. Adblock 

广告拦截器，当然也可以选择使用tempermonkey中安装广告拦截器，不过我jio得这个功能更加强大

![Extension Manager](http://picture.saintblog.top/chrome/chrome_adblock.png)

> ```
> 请注意：当安装 Adblock Plus for Chrome 时，您的浏览器会显示一个警告，它说 Adblock Plus for Chrome 会访问您的浏览历史和数据。这是一个标准的消息，我们从不、绝不会收集任何信息！
> 
> 最近，Adblock Plus 社区提出了可接受广告概念。通过允许一些小的和静态的广告，您可以支持那些依赖于广告，但选择一些非侵入式广告的网站。此功能可以在任何时候禁用，到 http://adblockplus.org/zh_CN/acceptable-ads 可以了解更多细节。
> ```

另外还可以添加某个网站到Adblock的白名单中，`知乎`就会提示最好添加到白名单中

![Extension Manager](http://picture.saintblog.top/chrome/adblock_zhihu.png)

### 4. Imagus

也可以说是一款非常好用的插件了，把鼠标放到图片上会自动放大。

![Extension Manager](http://picture.saintblog.top/chrome/imagui.gif)

### 5. 沙拉查词

一款单词查询的插件，双击某个单词就会出现一个沙拉查词的小图标，点击即可翻译

![Extension Manager](http://picture.saintblog.top/chrome/shalachaci.gif)