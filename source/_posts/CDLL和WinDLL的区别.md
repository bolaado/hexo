---
title: CDLL和WinDLL的区别
tags:
  - Python
  - C语言
  - Windows
categories: 万千问题
cover: >-
  http://5b0988e595225.cdn.sohucs.com/images/20190711/f7e81e945aef429aad20510b6618e714.jpeg
top_img: >-
  http://5b0988e595225.cdn.sohucs.com/images/20190711/f7e81e945aef429aad20510b6618e714.jpeg
abbrlink: 34989
date: 2021-02-06 21:56:07
---

# CDLL和WinDLL的区别
## 区别
Python要调用C语言或者C++写的动态连接库，要用到`ctypes`库     
而`ctypes`库其实背后做了很多，它提供了三个easy载入动态连接库的对象：`cdll`、`windll`和`oledll`   
通过访问这三个对象的属性，就能够调用动态连接库的函数了  
<font color = pink>其中
* `cdll`主要用来载入C语言调用方式（`cdecl`）  
* `windll`主要用来载入WIN32调用方式（`stdcall`）
* `oledll`使用WIN32调用方式（`stdcall`）且返回值是Windows里返回的HRESULT值</font>  
<font color = BlueViolet>而调用时，最需要注意的去别在于</font>   
<font color = Violet>`cdll`是使用调用者清除的栈的方式。而`windll`和`oledll`是使用被调用者清除的方式</font>   

## 使用
### 引入`ctypes`库  
```Python
    from ctypes import *
```
### 加载dll 
#### `stdcall`调用约定  
```Python
    Objdll = ctypes.WinDLL("dllpath") 
```
#### `cdecl`调用约定
```Python
    Objdll = ctypes.CDLL("dllpath")
```
## 如果有更复杂的使用需求，访问这个
https://www.cnblogs.com/baihuitestsoftware/articles/5345089.html