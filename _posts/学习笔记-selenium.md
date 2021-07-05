---
title: 学习笔记-selenium
date: 2021-05-15 16:43:33
tags:
---
# selenium学习笔记
## 背景和原理
Selenium 是一个 Web 应用的自动化框架。
通过它，我们可以写出自动化程序，像人一样在浏览器里操作web界面。
    
Selenium 的自动化原理是：
```
Selenium客户端库 <-> 浏览器驱动 <-> 浏览器
```
    

## 操作流程
1.导入webdriver模块

```
form selenium import webdriver
```
2.创建webdriver实例化对象，并指明用chrome浏览器驱动
```
wd = webdriver.Chrome(r'浏览器驱动存储路径')
```
3.调用 get 方法，让浏览器打开指定网址
```
wd.get('http://www.baidu.com')
```
4.选择元素

5.操控元素

6.退出


## 选择元素




## 操控元素



# css表达式
通过 CSS Selector 选择单个元素的方法是
```
find_element_by_css_selector(CSS Selector参数)
```
选择所有元素的方法是
```
find_elements_by_css_selector(CSS Selector参数)
```
参数写法
```
tag名直接写
#id值
.class值
```
# frame切换




# 