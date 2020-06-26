---
title: hexo常用命令
date: 2020-06-26 11:23:00
updated: 2020-06-26 11:23:00
tags: 
	- hexo
categories: 博客
keywords: hexo
description: 经常忘记hexo的命令在这里总结一下
top_img: http://picture.saintblog.top/hexo/hexo.jpg
cover: http://picture.saintblog.top/hexo/hexo.jpg 
---







## hexo

```powershell
npm install hexo -g #安装
npm update hexo -g #升级
hexi init #初始化
```

## 缩写

```powershell
hexo n "我的博客" == hexo new "我的博客" #新建文章
hexo p == hexo publish
hexo g == hexo generate#生成
hexo s == hexo server #启动服务预览
hexo d == hexo deploy#部署
```

## hexo服务

```powershell
hexo server #Hexo 会监视文件变动并自动更新，您无须重启服务器。
hexo server -s #静态模式
hexo server -p 5000 #更改端口
hexo server -i 192.168.1.1 #自定义 IP

hexo clean #清除缓存 网页正常情况下可以忽略此条命令
hexo g #生成静态网页
hexo d #开始部署
```

## 静态文件

```powershell
hexo generate #使用 Hexo 生成静态文件快速而且简单
hexo generate --watch #监视文件变动
```

## 部署hexo

```powershell
hexo deploy -g
hexo server -g
```

## 草稿

```powershell
hexo publish [layout] <title>
```

## 模板

```powershell
hexo new "postName" #新建文章
hexo new page "pageName" #新建页面
hexo generate #生成静态页面至public目录
hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
hexo deploy #将.deploy目录部署到GitHub

hexo new [layout] <title>
hexo new photo "My Gallery"
hexo new "Hello World" --lang tw
```

```markdown
title: 使用Hexo搭建个人博客
layout: post
date: 2014-03-03 19:07:43
comments: true
categories: Blog
tags: [Hexo]
keywords: Hexo, Blog
description: 生命在于折腾，又把博客折腾到Hexo了。给Hexo点赞。
```

## 文章摘要

```markdown
以上是文章摘要 <!--more--> 以下是余下全文 
```

## 写作

```
hexo new page <title>
hexo new post <title>
```

## 推送到GitHub

```
hexo n #写文章
hexo g #生成
hexo d #部署 #可与hexo g合并为 hexo d -g
```