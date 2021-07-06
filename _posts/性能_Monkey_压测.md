---
title: monkey使用
date: 2021-01-09 20:25:01
tags: "monkey"
---
# Monkey测试
monkey是一款很强大的Android性能测试工具，可以用来进行压测

## 操作流程
```
1.确定连接设备：adb devices

2.找到指定包名：adb shell pm list package -3  
我们小喜马apk包名是 com.ximalaya.ting.kid

3.先创建一个存放日志的文件

4.设置参数并执行

5.停止monkey

```

## 常用脚本
```
adb shell monkey -p com.ximalaya.ting.kid -v -v -v --pct-touch 40 --pct-motion 50 --pct-appswitch 10 --throttle 200 --ignore-crashes --ignore-timeouts 10000 > /Users/xmly/Documents/log/monkeylog.txt

```
```
Ps 
-p是指定apk
--throttle <毫秒数> 指定用户操作（事件）间的时延
-s用于指定伪随机数生成器的seed值
-v 三个级别，级别越高，输出的日志越详细
最后的数字（这里是500）：表示Monkey程序模拟500次随机用户操作事件。
>输出测试结果到/Users/xmly/Documents/log/monkeylog.txt
```
## 停止monkey
```
先ctrl + c 停止打印日志
	adb shell ps |grep monkey  #获取pie进程ID
	adb shell kill pid#进程号
```