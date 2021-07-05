---
title: Android抓取错误日志
date: 2020-08-06 20:43:15
tags:Monkey
category: 性能测试
description: "使用Monkey来对APP进行普通压测方法"
---
# Android

## 抓取错误日志步骤

```
1. touch 0321.txt #在终端创建日志文件
2. 手机连接USB到电脑
3. adb logcat -v time >电脑存放路径\名称
4. 输出停止：ctrl+C
```
## 没有抓到的话

```F

 抓取完整日志：adb bugreport bugreport.zip
 
```