---
title: 服务器版Ubuntu启用WIFI
date: 2018-02-08 21:22:41
tags: [ubuntu,linux,教程]
---

最近把曾经不用的上网本安装了一个Ubuntu-Server版，当成服务器来用，因为家庭网络布线问题，只好用自带的WIFI来连接网络，Server版也没有什么图形化的管理工具，之后手动编辑配置文件了。 
Server下面配置起来还是很方便的，首先安装连接WIFI需要的软件包：

`sudo apt-get install wpasupplicant`

然后编辑/etc/network/interfaces文件，添加以下内容：

```
auto wlan0

iface wlan0 inet dhcp

wpa-ssid xxxxxx

wpa-psk 12345678
```

其中wpa-ssid这行就是你的WIFI名称，最好是英文，wpa-psk就是你的WIFI连接密码，其中wlan0是WIFI接口名，请根据你的实际接口名填写。

这个配置是通过DHCP自动配置ip地址以及DNS，如果想要手动设置内容改成这样：

```
auto wlan0

iface wlan0 inet static

address 192.168.1.2

netmask 255.255.255.0

gateway 192.168.1.1

dns-nameservers 192.168.1.1 114.114.114.114

wpa-ssid xxxx

wpa-psk 12345678
```

修改好了之后执行下面命令启用WIFI：

首先关闭WIFI

`sudo ifdown wlan0`

然后启用WIFI

`sudo ifup -v wlan0`

现在WIFI已经连接上来，而且重启后也会自动连接。