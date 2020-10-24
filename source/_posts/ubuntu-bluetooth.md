---
title: Blueman Protocol not available
date: 2020-10-24 20:50:36
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

