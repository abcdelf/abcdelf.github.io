---
title: ubuntu 下使用stlink v2.1
date: 2018-04-19 15:17:04
tags: [ubuntu,stlink,stm32]
---

&ensp;
<!--more-->

ubuntu下使用stlink V2.1
===============

>问题：stlink V2.1带有串口功能，ubuntu下自带的驱动识别不出来
----------

>解决方法：

1. 下载[stlink_udev_rule.tar.bz2](http://www.openstm32.org/dl160)
2. 使用命令:
    ```bash
        $sudo tar -xf stlink_udev_rule.tar.bz2 -C /etc/udev/rules.d
    ```
