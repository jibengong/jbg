---
title: Mac下node.js卸载方法收集
date: 2018-02-08 21:12:32
tags: [Mac,nodejs,教程]
---

### brew的安装方式
直接通过一条命令
`brew uninstall nodejs`

### 官网下载pkg安装包的
通过这条命令
`sudo rm -rf /usr/local/{bin/{node,npm},lib/node_modules/npm,lib/node,share/man/*/node.*}`

### 其它方式干净卸载

去这个网址下载sh文件：
[https://github.com/jesseyu/uninstallNodejs/blob/master/uninstallNodejs.sh](https://github.com/jesseyu/uninstallNodejs/blob/master/uninstallNodejs.sh)

内容为：

```
#!/bin/bash
lsbom -f -l -s -pf /var/db/receipts/org.nodejs.pkg.bom \
| while read i; do
  sudo rm /usr/local/${i}
done
sudo rm -rf /usr/local/lib/node \
     /usr/local/lib/node_modules \
     /var/db/receipts/org.nodejs.*
```

下载回来的文件需要修改权限，输入：
`chmod 777 uninstallNodejs.sh`

然后在终端运行此文件
