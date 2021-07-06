---
title: git常用操作
date: 2020-12-01 20:14:15
tags: "git"
category: "业务测试"
description: "本文主要是对git的基本操作学习，包括项目部署、常用操作命令"
---
# Git操作

Git 是一个开源的分布式版本控制系统，可以有效高速的处理任何或小或大的项目

GitLab 是开发团队建立在内网上的，用来托管代码

Github 则是一个开源的代码库

网址https://github.com/

## 项目部署

部署git的ssh（这个步骤是将机器上面的凭证发到github上面，之后机器就不用验证了）

```
1. 终端ssh-keygen -o
2. cd ~/.ssh/
3. ls
4. cat ~/.ssh/id_rsa.pub
5. 复制ssh秘钥
6. 回到Git，个人中心Settings - SSH and GPG keys
7. 粘贴秘钥配置一下
```
## Git 常用操作命令

```
1. git clone #克隆项目
2. git add .  #添加所有修改过的文件到缓冲区
3. git commit -m  #将本地暂存的修改提交到版本库，并添加提交信息
4. git push #将本地分支的更新，推送到远程主机
5. git pull #将远程主机的代码，拉取到本地
6. git stash #本地的更改丢到储藏区存起来，本地就变成未修改状态了



```