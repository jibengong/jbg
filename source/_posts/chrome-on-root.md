---
title: Run chrome as root
date: 2019-01-13 16:07:18
tags: [linux,chrome,教程]
---

```
vim /usr/bin/google-chrome
```

set:
exec -a "$0" "$HERE/chrome" "$@" 

into:
exec -a "$0" "$HERE/chrome" "$@" --user-data-dir --no-sandbox