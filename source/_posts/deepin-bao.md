---
title: Deepin-Ubunt无法找到add-apt-repository解决方法
date: 2018-08-25 15:54:18
tags: [linux,ubuntu,deepin,教程]
---
网上查了一下资料，原来是需要

```
python-software-properties
```

于是
```
apt-get install python-software-properties
```
除此之外还要安装
```
software-properties-common
```
于是
```
apt-get install software-properties-common
```
然后就能用add-apt-repository了