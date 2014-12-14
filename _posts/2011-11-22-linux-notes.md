---
layout: post
title: Linux使用手记
---

# {{ page.title }}

## 命令

- 配置文件路径
```
# 网络配置
/etc/network/interface
# DNS服务器配置
/etc/resolv.conf
```

- 显示无线网络信息
```
$ iwconfig
```

- 启用和禁用网络接口
```
$ ifup interface
$ ifdown interface
```

- 查看本机开放端口
```
$ netstat -lnp
```

- 查看指定进程数，如httpd
```
$ ps -ef | grep httpd | wc -l
```

- 统计最常用命令
```
history | awk '{CMD[$2]++;count++;} END { for (a in CMD )print CMD[ a ]" " CMD[ a ]/count*100 "% " a }' | grep -v "./" | column -c3 -s " " -t |sort -nr | nl | head -n10
```
