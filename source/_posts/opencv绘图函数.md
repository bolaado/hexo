---
title: opencv绘图函数
tags: ['Python', 'OpenCV']
categories: [视觉, OpenCV]
abbrlink: 16562
date: 2020-10-02 19:24:03
cover: https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=845020296,961297363&fm=11&gp=0.jpg
top_img: https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=845020296,961297363&fm=11&gp=0.jpg
---

# opencv绘图函数
<font color='BlueViolet'>首先要创造一个背景图，
```Python
    img=np.zeros((像素高,像素宽,3), np.uint8)
    # 3代表BGR三种颜色，uint8是用0-255表示所有颜色，此时为黑色背景
```
其实np.zeros()只两个参数，第一个是创建的图片矩阵大小，第二个是数据类型，所以`np.uint8`可以被`(B, G, R)`代替，这样就可以改变背景颜色
</font>
## 直线
```
    cv2.line(图像名, 起点坐标, 终点坐标, 颜色数组, 线宽)
```  
## 矩形
```
    cv2.rectangle(图像名, 左上顶点坐标, 右下顶点左边, 颜色数组, 线宽)
```  
<font color="DeepPink">当线宽为-1时，表示封闭图形的颜色填充</font>
## 圆
```Python
    cv2.circle(图像名, 圆心坐标, 半径, 颜色数组, 线宽)
```
## 椭圆
```
    cv2.ellipse(图像名, 中心坐标, (长轴长, 短轴长), 椭圆沿逆时针方向旋转的角度, 长轴顺时针方向起始的角度, 结束角度, 颜色数组, 线宽)
```
## 多边形
```Python   
    pts = np.array([顶点列表], np.int32)
    pts = pts.reshape((-1,1,2))
    img = cv2.polylines(图像名, [pts], True, 颜色数组, 线宽)
```
<font color="Yellow">关于`reshape()`函数可以看我的另一篇博客</font>  
<https://bolaado.github.io/2020/10/02/Python%E4%B8%AD%E7%9A%84reshape/>

