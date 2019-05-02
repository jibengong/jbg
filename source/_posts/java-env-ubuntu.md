---
title: linux下java版本管理工具jenv使用介绍
date: 2019-05-02 17:46:36
tags: [linux,ubuntu,教程]
---

###### 不同的项目使用的java版本不同，每次切换时都需要手动去修改java的环境变量，麻烦至极。jenv可以管理java版本，轻松实现管理多个java的问题。

##### 一、下载jenv
```
$ git clone https://github.com/gcuisinier/jenv.git ~/.jenv
```

##### 二、配入环境变量
```
$ echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.bash_profile
```

##### 三、执行 jenv init -命令，这样每打开一个 bash 终端就可以调用 jenv 命令，并且默认执行一次 jenv init - 命令。
```
$ echo 'eval "$(jenv init -)"' >> ~/.bash_profile
$ source ~/.bash_profile
```

##### 四、查看当前的java版本，输出是1.8.0_44
```
$ java -version
```

##### 五、找到jdk1.8和jdk1.7的文件夹路径，加入到jenv的管理库：
```
$ jenv add /opt/Java/jdk1.8.0_144
$ jenv add /opt/Java/jdk1.7.0_80
```

##### 六、查看已经添加的java版本
```
$ jenv versions
```

##### 七、配置要使用的JVM。有三种方式：global：按全局、lacal：按目录、shell：shell
```
$ jenv global jdk1.7.0_80
```
##### 或
```
$ jenv local jdk1.7.0_80
```
##### 或
```
$ jenv shell jdk1.7.0_80
```
##### 八、查看当前java版本。发现版本已经变成了jdk1.7.0_80
```
$ java -version
```
##### 至此，以后再也不用自己手动修改环境变量改变java版本了。
