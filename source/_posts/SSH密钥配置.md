---
title: SSH密钥配置
date: 2018-04-04 12:37:04
tags: [git,ssh]
---
# 同一台电脑需要配置多个ssh密钥，用于GitHub以及gitlab
#  
<!--more-->
1.ssh密钥制作：使用git bash 
```
    ssh-keygen -t rsa -C "your.email@example.com" -b 4096
```

2.复制密钥命令
```
    pbcopy < ~/.ssh/id_rsa.pub//(macos)
    cat ~/.ssh/id_rsa.pub | clip//(windows使用git bash)
    xclip -sel clip < ~/.ssh/id_rsa.pub//(linux)
```
### 使用多个密钥时需要注意
```
    eval $(ssh-agent -s)//运行ssh客户端
    ssh-add ~/.ssh/other_id_rsa//添加自定义的ssh密钥
```
### 以上命令是暂时向ssh客户端添加自定义密钥，关闭ssh客户端就会失效。若密钥工作正常，则可以使用配置文件对ssh进行配置。在~/.ssh/目录下添加config文件。
```
    nano ~/.ssh/config
```
示例如下：
```
    Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa_github

    Host gitlab.com
    HostName gitlab.com
    User git
    IdentityFile ~/.ssh/id_rsa
```


