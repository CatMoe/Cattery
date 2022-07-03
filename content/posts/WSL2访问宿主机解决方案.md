---
title: WSL2访问宿主机解决方案
date: 2022-06-17 17:20:14
---

```
export winip=$(ip route | grep default | awk '{print $3}')
export http_proxy="http://${winip}:1080"
export HTTP_PROXY="http://${winip}:1080"
export https_proxy="http://${winip}:1080"
export HTTPS_PROXY="http://${winip}:1080"
export ftp_proxy="http://${winip}:1080"
export FTP_PROXY="http://${winip}:1080"
export rsync_proxy="http://${winip}:1080"
export RSYNC_PROXY="http://${winip}:1080"
export ALL_PROXY="$socks5://${winip}:1080"
export all_proxy="$socks5://${winip}:1080"
git config --global http.proxy "${http_proxy}"
git config --global https.proxy "${https_proxy}"
```