---
title: 修复 Telegram 中文输入
date: 2017-09-15 17:28:52
tags: [教程,linux,ubuntu]
---

最新版本的telegram在Ubuntu下无法使用搜狗输入法来输入中文，上网找了一下方法，找到一个完美解决了问题。

步骤如下：

```
编辑 ~/.local/share/applications/telegramdesktop.desktop 文件
修改 Exec 该行，添加环境变量 env QT_IM_MODULE=ibus ，使用 fcitx 的用户，把 ibus 替换成 fcitx

```

最后修改效果如图

![](https://ww2.sinaimg.cn/large/a15b4afegy1fhjn68w3c2j20qp0ifwg8)

设置完毕后，保存该文件并重启telegram即可。




