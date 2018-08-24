---
title: git命令记录
date: 2018-04-04 12:37:04
tags: [git]
---
# Git删除、重命名远程分支和tag
#  
<!--more-->
### Git删除远程分支：
```
    $ git push origin --delete <branchName>
```
### Git删除远程tag：
```
    $git push origin --delete tag <tagname>
```
### Git删除本地分支
```
    $git branch -d <branchName>
```

### Git版本回退
```
    $git reset --hard head^
```
### Git本地版本和远程版本不一致，导致无法上传的问题解决
```
    $git push -u origin hexo -f
```
