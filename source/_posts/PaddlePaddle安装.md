---
title: PaddlePaddle安装
tags: ['Windows', 'paddle']
categories: 安装
abbrlink: 45050
date: 2020-10-01 22:19:37
cover: http://inews.gtimg.com/newsapp_bt/0/7002248090/1000/0
top_img: http://inews.gtimg.com/newsapp_bt/0/7002248090/1000/0
---

# 安装paddle（飞桨）  
cmd里敲   
CPU版  
`conda install paddlepaddle`    
GPU版  
```
    # CUDA 9，cuDNN 7.3+:
    conda install paddlepaddle-gpu cudatoolkit=9.0
    # CUDA 10.0，cuDNN 7.3+
    conda install paddlepaddle-gpu cudatoolkit=10.0
```
没有vpn的话就得换源，输入
```
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/Paddle/
    conda config --set show_channel_urls yes   
```
<font color="DeepPink">在命令行里可能敲了`-`之后，`-`以及它后面的命令都不会被显示出来，直到有一个空格，也就是说`-add`可能不会显示出来，这都是正常的，我也不知道为什么之前是不会隐藏的现在突然变了，可能有的人使用的时候并不会</font>

如果出现了问题，看我的另一篇博客
<https://bolaado.github.io/2020/10/01/Solving-environment-failed-with-initial-frozen-solve-Retrying-with-flexible-solve/>


