---
title: 测试传说中Linux上最好用的Markdown编辑器Typora
date: 2019-05-18 16:30:15
tags: [linux,教程]
---

### step1:

```
# or run:
# sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE
wget -qO - https://typora.io/linux/public-key.asc | sudo apt-key add -
```

### step2:

```
# add Typora's repository
sudo add-apt-repository 'deb https://typora.io/linux ./'
sudo apt-get update
```

### step3:

```
# install typora
sudo apt-get install typora
```

这样就安装完成了！