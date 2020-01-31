---
title: 手动安装java以及环境配置
date: 2019-05-02 18:40:36
tags: [linux,ubuntu,教程]
---

##### 1.修改环境变量
```
sudo vi ~/.bashrc
```
##### 在文件末尾追加下面内容：
```
#set oracle jdk environment
export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_144  ## 这里要注意目录要换成自己解压的jdk 目录
export JRE_HOME=${JAVA_HOME}/jre  
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib  
export PATH=${JAVA_HOME}/bin:$PATH 
```

##### 2.使环境变量马上生效：
```
source ~/.bashrc
```
##### 3.系统注册此jdk
```
sudo update-alternatives –install /usr/bin/java java /usr/lib/jvm/jdk1.7.0_60/bin/java 300
```
##### 查看java版本，看看是否安装成功：
```
java -version
```

DEB版本安装后续：

###### 需要检查并生成环境变量

```
sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-13.0.1/bin/java 2
sudo update-alternatives --config java
```

