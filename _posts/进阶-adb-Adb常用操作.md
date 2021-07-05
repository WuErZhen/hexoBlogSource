---
title: adb常用操作
date: 2020-07-04 23:43:12
tag: adb
category: 业务测试
description: "adb常用操作学习"
---
# Adb

## 常用adb命令

1.查看已连接设备
usb连接手机调试，记得调成开发者模式
```
adb devices 
    * off line  未连接
    * device    连接成功
    * no device 无设备
```
2.文件操作
```
* adb pull 命令从真机拷贝文件到pc上
* adb push 命令从pc上复制一份文件到真机上
```
3.抓取完整日志

```
adb bugreport bugreport.zip
```
4.安装apk
```
* 安装apk:adb install <apkfile>
* 强制安装apk: adb install -r <apkfile>
* 安装apk到Sd卡: adb install -s <apkfile>
* 卸载APP：adb uninstall <packagename>
```
5.基础命令
```
* 查看版本信息:adb version
* 查看帮助:adb -h
* 进入shell: adb shell
* 退出shell: exit
* 重启设备:adb reboot
* 终止adb服务:adb kill-server
* 启动adb服务:adb start-server
```
6.设备相关
可以看一些性能信息
```
*查看设备序列号adb get-serialno
*获取CPU信息：adb shell cat /proc/cpuinfo
*查看设备的内存信息：adb shell cat /proc/meminfo
*获取设备名称：adb shell cat /system/build.prop
*获取设备分辨率：adb shell wm size
```
```

```