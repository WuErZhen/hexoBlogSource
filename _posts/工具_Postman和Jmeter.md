---
title: postman和jmeter调试接口
date: 2020-07-23 19:25:13
tags: "postman"
category: "测试工具"
description: "介绍下postman调试curl和jmeter基础操作"
---
# postman和jmeter来调试接口

## postman 调试
可以很方便的用curl来重新调接口：发专辑或者退款

开发调试报错信息也用curl比较多，可以规避掉cookie和参数获取的问题
```
1.获取curl信息：客户端用Charles抓，浏览器F12

2.启动postman：右上角import — Rawtext - Continue

3.修改即可
```

## jmeter
同postman，可以用来调用接口，进行常规的接口测试和性能测试
```
新增测试计划
一、线程组——测试计划-添加-线程组
	1 HTTP请求——线程组-添加-Sampler-HTTP请求
		1.1添加断言——HTTP请求-添加-断言-响应断言
		1.2断言结果——HTTP请求-添加-监听器-断言结果
	2查看结果树——线程组-添加-监听器-查看结果树
	3用户自定义变量——线层组-添加-配置元件-用户自定义变量
	4.添加聚合报告——线程组-添加-监听器-聚合报告
```