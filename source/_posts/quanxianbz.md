---
title: configure 权限不够
date: 2018-02-08 21:52:32
tags: [ubuntu,linux,教程]
---

linux下运行一个文件时 提示权限不够，说明这个文件没有可执行权限
我们可以在属性里面手动为这个文件加上可执行权限也可以使用命令的方式

命令方式：
例如：   
```bash: ./configure: 权限不够```
给文件加上可执行权限： 
```chmod +x configure```
再输入 ```./configure``` 就可以了;


当然也可以右键属性设置；
双系统要放置到Ubuntu系统中；