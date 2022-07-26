---
title: Github出现连接超时
tags:
  - github
  - Windows
categories: 万千问题
cover: >-
  http://5b0988e595225.cdn.sohucs.com/images/20190711/f7e81e945aef429aad20510b6618e714.jpeg
top_img: >-
  http://5b0988e595225.cdn.sohucs.com/images/20190711/f7e81e945aef429aad20510b6618e714.jpeg
abbrlink: 31623
date: 2021-02-06 15:40:06
---

# Github出现连接超时

## <font color = hotpink>解决办法</font>

### 修改hosts文件  
<font color = pink>用记事本打开即可</font>  
文件路径在`C:\Windows\System32\drivers\etc`  
添加上，如下图  
![1](Github出现连接超时/1.png)


#### <font color = purple>获取要访问的相关网站的IP</font>   
访问[查询IP](https://www.ipaddress.com)  
搜索框内分别输入`github.com`和`github.global.ssl.fastly.net`查询对应的IP地址，然后如上图所示格式添加上配置就可以了

## 测试  
powershell里`ping`一下   
```
    ping github.com
```
