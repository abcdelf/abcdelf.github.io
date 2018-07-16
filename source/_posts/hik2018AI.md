---
title: 海康威视2018软件精英挑战赛
date: 2018-06-24 10:27:04
tags: [hik2018,A-Star,比赛]
---


#  
<!--more-->

[海康威视2018软件精英挑战赛-官网](http://codechallenge.hikvision.com/index.aspx)

[海康威视2018比赛规则镜像(侵删)](/assets/HIK2018_Commemorate/海康威视2018软件精英挑战赛.html)

前言
====
机缘巧合下，参加了海康威视2018软件精英挑战赛。

本科期间参加了大大小小的比赛也不少了，最终也是通过科创个性化保研走上读研之路。开始读研之后，除了指导一些比赛也就没有参加什么比赛了。之前一直在学习各种知识，从硬件设计到软件编写，不知不觉中，已经走过了六七年的时间。学习中逐渐接触到了开源这一精神，刚开始也是不太了解大神们为何如此推崇开源精神。期间开发无人机项目更是接触到了很多的开源项目，赫赫有名的便数APM和PX4了。

话不多说，下面便是我此次参赛的最终代码。(由于参赛时间紧迫，能力有限，软件框架构思加实现用了两三天的时间，仅供大家参考，存在问题，大家轻喷)。

软件源码
=======
工程基于的是官方的C++Demo，由于寻路算法中使用了C++11的特性，修改了官方的MakeFile，工程支持QtCreator打开，使用VScode也可以。(本工程是在Ubuntu下实现；在window中没有测试；在Mac下可以编译通过，但是执行会出问题)

软件执行流程图如下：
-----------------
![主流程图](/assets/img/hik2018_mainCycle.bmp)

源代码地址:[HIK2018无人机AI大赛-HEU-AutoCopter最终源码](https://github.com/abcdelf/hik2018)


寻路算法参考资料
==============
> [A-Star 参考资料](https://www.jianshu.com/p/74ca39e670ba)
>
> [PathFind 参考源码(C,C++,java,js)](https://github.com/abcdelf/Pathfinding)
>
> [通俗易懂的A*讲解](https://www.cnblogs.com/leoin2012/p/3899822.html)
