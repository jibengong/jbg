---
title: MAC在Docker上安装centos以及运行
date: 2019-01-06 20:53:23
tags: [MAC,docker,教程]
---

安装docker部分省略，参考官方网站。

#### 一、安装centos

`docker pull centos:6 #数字是说要安装哪个版本的centos`

#### 二、运行docker里的centos

`docker run --privileged=true -it centos:6 #--privileged是以获取系统权限的形式运行， -it是互动模式，跟本地的系统进行交互,调用的本地的终端`

#### 三、注意

如果需要退出，直接用 exit 就可以退出，但是docker是不会保存你再容器中做过的修改的，第二次进来容器，之前安装过的东西都得重新安装一遍，那怎么办呢

解决办法

在未退出来之前，另开一个窗口

先 docker ps

你可以看到里面的ID编码和容器名称

然后docker commit d83c4279f146 centos:6 #d83c4279f146是CONTAINER ID，centos:6是IMAGE，容器名

看到生成一串sha256码就说明保存成功了，现在可以回到原窗口（运行centos那个）输入exit退出。
