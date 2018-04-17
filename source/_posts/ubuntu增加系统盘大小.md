---
title: ubuntu 无损扩展分区
date: 2018-04-16 20:37:04
tags: [ubuntu,linux]
---

&ensp;
<!--more-->

ubuntu 无损扩展分区
================

> 今天在ubuntu下安装virtual box虚拟机，用于安装win10，装完后系统提示系统剩余空间不足。找到一个比较好的方案，可以无损扩展系统分区。
---
> 系统环境ubuntu16.04，需要的工具Gparted。

1. 工具安装
    ```bash
    $sudo apt install gparted
    ```
2. 打开Gparted，找到挂载点 " / "。
3. 通过软件分割出空闲空间。
4. 一般情况下，空闲空间和系统根分区并不靠在一起，通过交换空间实现分区的移动。

[参考连接-Ubuntu 15.04 无损扩展分区](http://www.cnblogs.com/jackchiang/p/4524665.html)