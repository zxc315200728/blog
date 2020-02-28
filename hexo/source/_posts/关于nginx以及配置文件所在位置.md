---
title: 关于nginx以及配置文件所在位置
date: 2020-02-28 10:58:41
tags: nginx
categories: nginx
---

# 关于nginx以及配置文件所在位置
## 程序在运行中  查询nginx文件位置

    [root@iz2ze783u2o2utti58eckwz ~]# ps -ef | grep nginx
    root      5349     1  0 Feb27 ?        00:00:00 nginx: master process /usr/sbin/nginx
    nginx    17687  5349  0 10:14 ?        00:00:00 nginx: worker process
    root     17770 17740  0 11:07 pts/3    00:00:00 grep --color=auto nginx

## 查看软件安装路径

    [root@iz2ze783u2o2utti58eckwz ~]# whereis nginx
    nginx: /usr/sbin/nginx /usr/lib64/nginx /etc/nginx /usr/share/nginx /usr/share/man/man8/nginx.8.gz /usr/share/man/man3/nginx.3pm.gz

## 查询运行文件所在路径

    [root@iz2ze783u2o2utti58eckwz ~]# which nginx
    /usr/sbin/nginx

## 通过Nginx自身的功能找到配置文件的位置

    [root@iz2ze783u2o2utti58eckwz ~]# /usr/sbin/nginx -t
    nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
    nginx: configuration file /etc/nginx/nginx.conf test is successful

# 遇到的问题

## service nginx reload 但是配置文件不生效
> 个人理解service nginx reload不重新加载配置文件 只是重启上次的服务
> 到nginx目录下执行 nginx -s reload 才会重新加载nginx.conf  修改的才会生效











