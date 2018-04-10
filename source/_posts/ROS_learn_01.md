---
title: ROS学习小知识(一)
date: 2018-04-10 12:37:04
tags: [ros, ]
---
#  
<!--more-->

一
======
 ROS初始化一个catkin_ws工作目录后,需要 
 ``` bash
 $ source /opt/ros/kinetic/setup.bash   //初始化全局ROS环境配置
 $ source ~/catkin_ws/devel/setup.bash  //初始化当前工作区的ROS配置，避免出现[rospack] Error: no such package beginner_tutorials的问题
 ```
