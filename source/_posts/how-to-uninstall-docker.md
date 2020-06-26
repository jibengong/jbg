---
title: how to completely uninstall docker
date: 2020-06-26 08:53:21
index_img: https://cdn.pixabay.com/photo/2015/01/08/18/24/programming-593312_960_720.jpg
tags: [docker,linux,ubuntu]
---

step1:

```
sudo apt-get autoremove docker docker-ce docker-engine  docker.io  containerd runc
```

step2:

```
dpkg -l | grep docker
```

step3:

```
dpkg -l |grep ^rc|awk '{print $2}' |sudo xargs dpkg -P
```

step4:

```
sudo apt-get autoremove docker-ce-*
```

step5:

```
sudo rm -rf /etc/systemd/system/docker.service.d
sudo rm -rf /var/lib/docker
```

check:

```
docker --version
```

