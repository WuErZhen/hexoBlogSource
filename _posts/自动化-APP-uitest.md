---
layout:
  - draft
title: APP自动化测试框架uitest的使用
date: 2021-07-04 23:43:12
tag: uitest
category: 自动化测试
description: "小喜马APP自动化测试框架uitest的使用"
---
# APP自动化测试
本文介绍下喜马自动化测试框架 uitest 和自动化脚本的编写

uitest是通用Airtest框架的定制版，基于图像和控件识别，是一个跨平台的自动化测试编辑器，写脚本和查看报告都很方便

## 工作环境

Python版本 >= 3.7

支持Android和iOS

```
连接手机启动IDE（确保连通）执行根目录下面的：
run.sh
```
## 脚本编写
很久之前写的一个首次启动app并登陆的脚本做示例，适用于小喜马APPv2.17.0 ，2.18.0及以上版本登录页有修改

ps：由此引出了ui自动化的一个弊端，版本更新变动大的话自动化脚本要重新去维护，需要排期和人力支持

```
# -*- encoding=utf8 -*-
__author__ = "xmly"
from importlib import reload

from airtest.core.api import *

from aiautotest.core.decorator import run

from aiautotest.plugins.android.android import poco #导入poco api(用于元素识别，打开录制会自动导入)

time = 1 #设置全局变量
phone  = "13000000181"
pwd = "111111"

def first_start_APP():  #首次启动APP
    stop_app("com.ximalaya.ting.kid")
    clear_app("com.ximalaya.ting.kid")
    start_app("com.ximalaya.ting.kid")
    sleep(time)
    
def agree_PrivacyPolicy():  #同意隐私条款
    poco(text="同意").click()
    sleep(time)
    
def skip_Sex(): #跳过性别选择
    poco(text="跳过").click()
    sleep(time)
    
def agree_permission(): #同意权限请求
    poco(text="允许").click()
    sleep(time)
    poco(text="允许").click()
    sleep(time)
    
def skip_popup(): #跳过弹窗
    poco("com.ximalaya.ting.kid:id/img_firework_close").click()
    sleep(time)
    
def go_personal_center(): #去到个人中心
    poco("com.ximalaya.ting.kid:id/btn_me").click() #第一次点击是跳过浮窗
    sleep(time)
    poco("com.ximalaya.ting.kid:id/btn_me").click()
    sleep(time)
    
def open_longin_page():#打开登录页
    poco("com.ximalaya.ting.kid:id/btn_login").click()
    sleep(time)
    
def phone_login():#输入手机号并验证码登陆
    poco("com.ximalaya.ting.kid:id/et_txt").click()
    sleep(time)
    text(phone) #输入手机号
    sleep(time)
    poco("com.ximalaya.ting.kid:id/cbAgreement").click() #勾选用户协议
    sleep(time)
    poco("com.ximalaya.ting.kid:id/ivSendSms").click() #确认
    sleep(time)
    text(pwd)
    sleep(time)
def test_login():
    first_start_APP();
    agree_PrivacyPolicy();
    skip_Sex();
    agree_permission();
    skip_popup();
    go_personal_center();
    open_longin_page();
    phone_login();
```
