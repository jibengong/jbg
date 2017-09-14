---
title: 解决Ubuntu下Sublime Text 3无法输入中文
date: 2017-09-14 20:54:40
tags: [教程,linux,ubuntu]
---
## 前言
sublime很好用，但是ubuntu下不能输入中文，这是一个很大的问题。不知道为什么开发者一直也不解决，好在还是有高手在，总能找到方法。网上方法很多，但是也很乱，现在我将自己的经验总结一下。

### 最简单的方法
使用git克隆以下工具
`git clone https://github.com/lyfeyaj/sublime-text-imfix.git
`

然后在终端中打开它
`cd sublime-text-imfix`

然后输入以下内容
`./sublime-imfix`

好了，接下来应该能够输入中文了
![](https://github.com/hackskylin/sublime-text-imfix/raw/master/image/fcitx.png)
