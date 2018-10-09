---
title: 一键更新内核并安装bbr
date: 2017-09-14 20:42:39
tags: [linux,教程]
---
```
wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh

```
18.04开启自带bbr：

`echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf
echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf`
保存生效：
`sysctl -p`
查看是否已开启bbr：
`sysctl net.ipv4.tcp_available_congestion_control`
查看是否启动了bbr：
`lsmod | grep bbr`
安装完成后，脚本会提示需要重启 VPS，输入 y 并回车后重启。
重启完成后，进入 VPS，验证一下是否成功安装最新内核并开启 TCP BBR，输入以下命令：
```
uname -r

```
查看内核版本，含有 4.12 就表示 OK 了
```
sysctl net.ipv4.tcp_available_congestion_control

```
返回值一般为：
net.ipv4.tcp_available_congestion_control = bbr cubic reno
```
sysctl net.ipv4.tcp_congestion_control

```
返回值一般为：
net.ipv4.tcp_congestion_control = bbr
```
sysctl net.core.default_qdisc

```
返回值一般为：
net.core.default_qdisc = fq
```
lsmod | grep bbr

```
返回值有 tcp_bbr 模块即说明bbr已启动。
