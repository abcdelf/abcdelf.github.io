---
title: IIC_SPI_UART等协议
date: 2018-08-16 20:07:04
tags: [IIC,SPI,UART,CAN.IIS]
---


#  
<!--more-->

IIC_SPI_UART等协议
==============

一、IIC协议
========

IIC使用时需上拉。
IIC总线空闲时，SCL和SDA均为高电平状态。

IIC开始信号：SCL为高电平下，SDA由高电平变为低电平，表示IIC协议的开始。

IIC结束信号：SCL为高电平下，SDA由低电平变为高电平，表示IIC协议的结束。

因此，在数据传输过程中，SDA只能在SCL为低电平的情况下进行电平变化。

> [IIC参考资料](https://www.cnblogs.com/hechengfei/p/4117840.html)

二、SPI协议
==========




三、UART协议
===========


四、CAN协议
=============