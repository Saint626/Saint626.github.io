---
title: docker入门
date: 2020-08-02 14:32
updated: 2020-08-02 14:32
tags: 
    - docker
categories: docker
keywords: 
description: 什么是docker?? 虚拟机与容器的区分, docker在Linux上与windows上的安装
top_img: http://picture.saintblog.top/docker/docker.jpg
cover: http://picture.saintblog.top/docker/docker.jpg
comment: true
---

## 什么是Docker

在了解docker之前，需要先清楚两个概念：容器和虚拟机。

### 虚拟机

不少同学都或多或少知道甚至使用过虚拟机，我们经常使用的虚拟机就像VMware、visualBox等等的模拟机器设备包括硬件，他可以在一种操作系统中运行另外一种操作系统，比如在windows系统里运行ubuntu系统。

由于每一台虚拟机都包括应用、库、完整的GUI操作界面等，所以虚拟机看上去与真实的系统一摸一样，但是虚拟机一旦开启，预先分配的资源就全部被该虚拟机占用。

用过虚拟机的同学都知道，虚拟机开启的那一瞬间，电脑的散热的转速也跟着上去了😂，所以使用虚拟机是**非常占用资源**的；安装一个虚拟机还需要下载对应操作系统的ISO，然后再到VMware中安装，**冗余的步骤多**；最后的虚拟机的**启动速度比较慢**。

由于这次参加的比赛，使用到提供的一个`eve-ng`的虚拟机，开久了重启速度太感人了，重启一下起码半小时过去了

![0](https://picture.saintblog.top/biaoqing/1590332771734.jpeg)

### 容器 

说了这么多虚拟机的缺点，那么`容器`又是什么？？

正是因为虚拟机存在的缺点，Linux发展出了另一种虚拟化的技术：**Linux容器**

Linux 容器不是模拟一个完整的操作系统，而是对进程进行隔离。有了这个容器，就可以实现将软件运行所需要的资源、环境打包到一个受到隔离的容器中。

容器相比于虚拟机，容器不需要捆绑一整套的操作系统，只要软件运行时需要的资源，所以容器更加**轻量**；容器内的应用进程是直接运行在宿主的内核中，容器是没有自己的内核的，也不需要对硬件虚拟，所以容器更加**轻便**；并且每个容器之间是相互隔离的，**不会影响到其他容器的进程**，每个容器都有自己的文件系统。

### Docker

那Docker与容器又有什么关系？？

Docker是Linux容器的一种封装，提供简单易用的容器来使用接口。

Docker是将应用程序与该程序的依赖，都打包在一个文件里，在docker中运行这个文件，就会生成一个容器，程序在这个容器中运行与在真实的物理机中运行是一样的。

![1](https://picture.saintblog.top/biaoqing/1427e0fa092a40d8ef937fcd1cc9dd7b.png)

在传统的开发中，我们写了一个helloworld项目就要跑在一个虚拟机中，又写了一个web项目又要一个虚拟机，又写了一个……想想脑壳就疼，在docker中，我们就只要启动10个容器就完事儿了！！简直不要太香

## Docker安装

Docker支持Linux、Mac、Windows平台，并且有CE（社区版）和EE（企业版），不用说，社区版肯定是免费的，企业版肯定是收费的。所以这里我都是以社区版为例

### Ubuntu

#### 系统要求

- 支持Ubuntu 16及更高版本

#### 卸载旧版本

可以在终端中输入 `docker --version`查看系统是否安装了docker，旧版本的docker名为`docker`、`docker.io`或`docker-engine`。

如果存在，使用以下命令来卸载旧版本

```shell
sudo apt-get remove docker docker-engine docker.io containerd runc
```

#### 使用官方脚本自动安装

```shell
curl -fsSL https://get.docker.com | bash -s docker --mirror Aliyun
```

#### 手动安装

英语好的同学可以参考官方教程：https://docs.docker.com/engine/install/ubuntu/

或菜鸟教程：https://www.runoob.com/docker/ubuntu-docker-install.html

#### 测试

测试 Docker 是否安装成功，输入以下指令

```shell
$ sudo docker run hello-world
```

这个指令下载一个测试的镜像并别运行在一个容器内，当这个容器运行时，他会打印一个信息然后退出

### Centos

官网的centos版本提示

> 要安装Docker引擎，需要CentOS 7的维护版本。不支持或测试存档版本。必须启用centos-extras存储库。默认情况下该存储库是启用的，但是如果您已经禁用了它，则需要重新启用它。

#### 卸载旧版本

与Ubuntu一样，都需要先查看是否存在旧版本的docker，存在的话就要先卸载，所以安装前先运行这个命令就没错

```shell
$ sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
```

#### 使用官方安装脚本自动安装

```shell
curl -fsSL https://get.docker.com | bash -s docker --mirror Aliyun
```

#### 手动安装

英语好的同学可以参考官方教程：https://docs.docker.com/engine/install/centos/

或菜鸟教程：https://www.runoob.com/docker/centos-docker-install.html

### Windows

window中分为win10与win7或win8的，两个安装的步骤不一样，其中win10需要**专业版**才能安装，所以家庭版的同学可以先去看看怎么升级专业版

#### win7、win8 系统

win7、win8 等需要利用 docker toolbox 来安装，国内可以使用阿里云的镜像来下载

下载地址：http://mirrors.aliyun.com/docker-toolbox/windows/docker-toolbox/

安装比较简单，双击运行，点下一步即可，可以勾选自己需要的组件，一般都勾上，电脑装过git了可以不勾git

安装完成后点击 Docker QuickStart 图标来启动 Docker Toolbox 终端

如果系统显示 User Account Control 窗口来运行 VirtualBox 修改你的电脑，选择 Yes。

然后就可以输入`docker run hello-world`来测试是否安装成功

![hello-world](http://picture.saintblog.top/docker/docker_hello_world.png)

#### win10

现在 Docker 有专门的 Win10 专业版系统的安装包，需要开启 Hyper-V

快捷键`win+x+f`打开应用和功能，选择最底下的程序和功能

![win10-1](http://picture.saintblog.top/docker/docker_win10_1.png)

启用或关闭Windows功能

![win10-1](http://picture.saintblog.top/docker/docker_win10_2.png)

勾选Hyper-V

![win10-1](http://picture.saintblog.top/docker/docker_win10_3.png)

下载`docker for windows`：https://www.docker.com/get-started

![win10-1](http://picture.saintblog.top/docker/docker_win10_4.png)

下载好后直接运行安装，默认勾选的就好了

安装好后任务栏会出现鲸鱼的图标，表示docker正在运行，可以打开cmd输入命令来查看docker安装

分别输入`docker version`和`docker run hello-world`

![win10-1](http://picture.saintblog.top/docker/docker_win10_5.png)

![hello-world](http://picture.saintblog.top/docker/docker_hello_world.png)

这样就是安装好啦

![1](https://picture.saintblog.top/biaoqing/1427e0fa092a40d8ef937fcd1cc9dd7b.png)