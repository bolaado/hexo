---
title: C#写上位机调用dll推理库
abbrlink: 40961
date: 2021-02-06 16:05:17
tags: [C++, PaddleX, Paddle, dll, C sharp]
catagories: 
        -[深度学习]
        -[上位机]
cover: https://ss1.baidu.com/6ON1bjeh1BF3odCf/it/u=907043365,3337927768&fm=15&gp=0.jpg
top_img: https://ss1.baidu.com/6ON1bjeh1BF3odCf/it/u=907043365,3337927768&fm=15&gp=0.jpg
---
# C#写上位机调用dll推理库
## 生成dll文件  
移步我的另一篇博客  
[生成可供调用的dll推理库](/2021/02/06/生成可供调用的dll推理库/) 
## C#上位机调用 
会写的都会写，就没必要多说了，主要是添加上
```C sharp
using System.Runtime.InteropServices;
namespace WindowsFormsApp1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        [DllImport("video_detector.dll", EntryPoint = "CreateModel", CharSet = CharSet.Ansi)]
        public static extern IntPtr CreateModel();    
    }
}        
```
然后正常用就完了

## 结果
![](C%20sharp写上位机调用dll推理库/1.jpg)