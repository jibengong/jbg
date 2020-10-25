---
title: Blueman Protocol not available
date: 2020-10-24 20:50:36
index_img: https://cdn.pixabay.com/photo/2020/07/03/04/47/bluetooth-headset-5365166_960_720.jpg
tags: [linux,lubuntu,bluetooth]
---

If your try to connect the bluetooth earpod, and get this:

```
Connection Failed: blueman.bluez.errors.DBusFailedError: Protocol Not available
```

then you can code this:

```
$ sudo apt-get install pulseaudio-module-bluetooth
$ pactl load-module module-bluetooth-discover
```

