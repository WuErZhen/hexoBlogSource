---
title: ios使用Xcode查看崩溃日志
date: 2020-08-06 22:24:12
tags:ios
category: APP测试
description: "整理了一下Xcode中抓取ios崩溃日志的流程"
---
# ios

## Xcode 查看崩溃日志

```

1. 将设备链接至电脑
2. Xcode -- > Window -- > Devices and Simulators
3. 在弹出的窗后上，选中对应的设备后，点击 View Device logs 按钮：
4. This Device 就连接手机的所有日志，All Logs 是本台电脑上的所有崩溃日志
5. 选择All Logs ，找到相应时间的crash日志
6. 右击选择Export Logs导出

```