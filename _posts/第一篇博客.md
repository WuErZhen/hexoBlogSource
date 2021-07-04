---
title: Api接口测试
date: 2021-07-03 23:13:06
tags: 接口测试
---
#Api接口测试

##前言

接口分为内部接口和外部接口

其中内部接口一般在联调和提测时已经跑通了，不需要我们进行接口测试

需要进行接口测试的外部接口，可以使用Python中的requests库来进行测试

##测试流程

1.评审接口文档

2.根据接口文档，写接口测试用例

3.编写接口用例，通常可以采用条件组合、边界值、错误猜测等方法

4.使用软件工具，直接通过消息接口对被测系统进行消息收发，验证被测系统行为是否正确

###构建url参数


###构建请求消息头


###构建请求消息体


###检查http响应


##使用requests程序抓包，可以方便查看结果

```
import requests

proxies = {
  'http': 'http://127.0.0.1:8888',
  'https': 'http://127.0.0.1:8888',
}

response = requests.get('http://mirrors.sohu.com/', proxies=proxies)
print(response.text)

```



