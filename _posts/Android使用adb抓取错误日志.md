---
title: Android抓取错误日志
date: 2021-07-04 23:43:12
tags:
---
#Android

##抓取错误日志步骤

```aidl
1. touch 0321.txt #在终端创建日志文件
2. 手机连接USB到电脑
3. adb logcat -v time >电脑存放路径\名称
4. 输出停止：ctrl+C
```
##没有抓到的话

```aidl

 抓取完整日志：adb bugreport bugreport.zip
 
```