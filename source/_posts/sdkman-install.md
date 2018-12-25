---
title: sdkman  好东西,用过的都说好
date: 2018-12-25 16:16:29
tags: [linux,教程]
---

Installing SDKMAN! on UNIX-like platforms is as easy as ever. SDKMAN! installs smoothly on Mac OSX, Linux, Cygwin, Solaris and FreeBSD. We also support Bash and ZSH shells.
Simply open a new terminal and enter:
```
$ curl -s "https://get.sdkman.io" | bash
```
Follow the instructions on-screen to complete installation.
Next, open a new terminal or enter:
```
$ source "$HOME/.sdkman/bin/sdkman-init.sh"
```
Lastly, run the following code snippet to ensure that installation succeeded:
```
$ sdk version
```
If all went well, the version should be displayed. Something like:
```
  sdkman 5.0.0+51
```

URL： https://sdkman.io/install