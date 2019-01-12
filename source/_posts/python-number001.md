---
title: 当出现 not supported between instances of 'str' and 'int' 的错误时
date: 2019-01-12 21:28:53
tags: [python,教程]
---

这是因为input()返回的数据类型是str类型，不能直接和整数进行比较，必须先把str转换成整型，使用int()方法：age = int(input ("请输入你的年龄:"))

即可！