---
title: Python中的reshape()
tags: Python
abbrlink: 20215
date: 2020-10-02 20:43:01
cover: http://inews.gtimg.com/newsapp_bt/0/7002248365/1000/0
top_img: http://inews.gtimg.com/newsapp_bt/0/7002248365/1000/0
---

# Python中的reshape()
`reshape(x, newshape, order='C')`  
reshape函数用于改变数组形状，且原数据不发生变化
## order参数   
其中`order='C'`代表是按照行顺序，   
如果是F则是按照列顺序，  
如果是A则是按照数据在内存中存储的顺序来  
## x参数
代表新数组行数
## newshape参数
代表新数组列数    
<font color="HotPink">当x=-1的时候，newshape给定列数，行数则由Numpy自行计算  
当newshape=-1的时候，x给定行数，列数则由Numpy自行计算
</font>
 