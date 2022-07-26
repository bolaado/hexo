---
title: Markdown编辑公式
categories: Markdown
abbrlink: 11783
date: 2020-10-03 21:23:52
tags: 日用
cover: https://ss2.baidu.com/6ON1bjeh1BF3odCf/it/u=2516984350,531550819&fm=15&gp=0.jpg
top_img: https://ss2.baidu.com/6ON1bjeh1BF3odCf/it/u=2516984350,531550819&fm=15&gp=0.jpg

---

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/x-mathjax-config">
    MathJax.Hub.Config({ tex2jax: {inlineMath: [['$', '$']]}, messageStyle: "none" });
</script>

# Markdown编辑公式
## 行内与行间
* 行内公式   
  在公式代码块的基础上前面加上$ ，后面加上$ 组成
* 行间公式  
  在公式代码块前后使用$$ 和$$
## 希腊字母
| 名称 | 大写 | code | 小写 | code |
| ---- | ---- | ---- | ---- | ---- |
|alpha|A|A|$\alpha$|\alpha|
|beta|B|B|$\beta$|\beta|
|gamma|$\Gamma$|\Gamma|$\gamma$|\gamma|
|delta|$\Delta$|\Delta|$\delta$|\delta|
|epsilon|E|E|$\epsilon$|\epsilon|
|zeta|Z|Z|$\zeta$|\zeta|
|eta|H|H|$\eta$|\eta|
|theta|$\Theta$|\Theta|$\theta$|\theta|
|iota|I|I|$\iota$|\iota|
|kappa|K|K|$\kappa$|\kappa|
|lambda|$\Lambda$|\Lambda|$\lambda$|\lambda|
|mu|M|M|$\mu$|\mu|
|nu|N|N|$\nu$|\nu|
|xi|$\Xi$|\Xi|$\xi$|\xi|
|omicron|O|O|$\omicron$|\omicron|
|pi|$\Pi$|\Pi|$\pi$|\pi|
|rho|P|P|$\rho$|\rho|
|sigma|$\Sigma$|\Sigma|$\sigma$|\sigma|
|tau|T|T|$\tau$|\tau|
|upsilon|Y|Y|$\upsilon$|\upsilon|
|phi|$\Phi$|\Phi|$\phi$|\phi|
|chi|X|X|$\chi$|\chi|
|psi|$\Psi$|\Psi|$\psi$|\psi|
|omega|$\Omega$|\Omega|$\omega$|\omega|

## 上标和下标
<font color="DeepPink">默认情况下，上、下标符号仅仅对下一个组起作用。一个组即单个字符或者使用{..} 包裹起来的内容</font>
* 上标
  ^
* 下标
  _

## 括号
* 小括号和方括号
  * 使用原始的()和[]
  * 使用\left(或\right)使符号大小与邻近的公式相适应<font color="DeepPink">适用所有括号类型</font>
* 大括号
  * 使用`\{`和`\}`
  * 使用`\lbrace`和`\rbrace`
* 尖括号
  * 使用`\langle`和`\rangle`
* 上取整  
  * 使用`\lceil`和`\rceil`
* 下取整
  * 使用`\lfloor`和`\rfloor` 

## 求和与积分
* 求和  
<font color="DeepPink">`\sum` 用来表示求和符号，其下标表示求和下限，上标表示上限</font>
  * `$\sum_{r=1}^n$`表示 ：$\sum_{r=1}^n$
  * `$$\sum_{r=1}^n$$`表示 :
  $$\sum_{r=1}^n$$
* 积分  
`\int`用来表示积分符号，同样地，其上下标表示积分的上下限。如:`$\int_{r=1}^\infty$` ： $\int_{r=1}^\infty$   
多重积分同样使用 int ，通过 i 的数量表示积分导数：  
`$\iint$` : $\iint$
`$\iiint$` : $\iiint$
* 连乘
  * `$\prod {a+b}$`，输出：$\prod {a+b}$
  * `$\prod_{i=1}^{K}$`，输出：$\prod_{i=1}^{K}$
* 其他类似
  * `$\prod$` ：$\prod$
  * `$\bigcup$` ：$\bigcup$
  * `$\bigcap$` ：$\bigcap$
  * `$arg\,\max_{c_k}$` ：$arg\,\max_{c_k}$
  * `$arg\,\min_{c_k}$` ：$arg\,\min_{c_k}$
  * `$\mathop {argmin}_{c_k}$` : $\mathop {argmin}_{c_k}$
  * `$\mathop {argmax}_{c_k}$` : $\mathop {argmax}_{c_k}$
  * `$\max_{c_k}$` : $\max_{c_k}$
  * `$\min_{c_k}$` : $\min_{c_k}$

## 分式与根式
* 分式
  * 使用`\frac ab`，`\frac`作用于其后的两个组,<font color="BlueViolent">可以用{}来分组</font>，如`$\frac {a+c+1}{b+c+2}$` 表示 $\frac {a+c+1}{b+c+2}$
  * 使用`\over`来分隔一个组的前后两部分，如`${a+1\over b+1}$`：${a+1\over b+1}$
* 连分数  
  使用`\cfrac`代替`\frac`或者`\over`
* 根式
  * 使用 `\sqrt` 来表示
  * 开平方：`$\sqrt {a+b}$`：$\sqrt {a+b}$
  * 开四次方：`$\sqrt[4]{\frac xy}$` : $\sqrt[4]{\frac xy}$
  
## 多行表达式
* 分类表达式  
  <font color="DeepPink">定义函数的时候经常需要分情况给出表达式，使用`\begin{cases}…\end{cases}` 。其中：</font>
  * 使用`\\` 来分类
  * 使用`&` 指示需要对齐的位置
  * 使用`\+空格`表示空格
例：
```
$$
f(n)
\begin{cases}
\cfrac n2, &if\ n\ is\ even\\
3n + 1, &if\  n\ is\ odd
\end{cases}
$$
```
表示：
$$
f(n)
\begin{cases}
\cfrac n2, &if\ n\ is\ even\\
3n + 1, &if\  n\ is\ odd
\end{cases}
$$
```
$$
L(Y,f(X)) =
\begin{cases}
0, & \text{Y = f(X)}  \\
1, & \text{Y $\neq$ f(X)}
\end{cases}
$$
```
表示：
$$
L(Y,f(X)) =
\begin{cases}
0, & \text{Y = f(X)}  \\
1, & \text{Y $\neq$ f(X)}
\end{cases}
$$
<font color="DeepPink">如果想分类之间的垂直间隔变大，可以使用`\\[2ex]` 代替`\\` 来分隔不同的情况。`(3ex,4ex` 也可以用，`1ex` 相当于原始距离）。如下所示：</font>
```
$$
L(Y,f(X)) =
\begin{cases}
0, & \text{Y = f(X)} \\[5ex]
1, & \text{Y $\neq$ f(X)}
\end{cases}
$$
```
表示：
$$
L(Y,f(X)) =
\begin{cases}
0, & \text{Y = f(X)} \\[5ex]
1, & \text{Y $\neq$ f(X)}
\end{cases}
$$
* 多行表达式  
  <font color="DeepPink">有时候需要将一行公式分多行进行显示</font>
```
$$
\begin{equation}\begin{split}  
a&=b+c-d \\  
&\quad +e-f \\  
&=g+h\\  
&= i
\end{split}\end{equation}
$$
```
表示：
$$
\begin{equation}\begin{split}
a&=b+c-d \\ 
&\quad +e-f \\ 
&=g+h\\ 
& =i 
\end{split}\end{equation}
$$
<font color="DeepPink">其中`begin{equation}` 表示开始方程，`end{equation}` 表示方程结束；`begin{split}` 表示开始多行公式，`end{split}` 表示结束；公式中用`\\` 表示回车到下一行，`&` 表示对齐的位置</font>
* 方程组  
<font color="DeepPink">使用`\begin{array}...\end{array}` 与`\left \{ `与`\right.` 配合表示方程组:</font>  
```
$$
\left \{ 
\begin{array}{c}
a_1x+b_1y+c_1z=d_1 \\ 
a_2x+b_2y+c_2z=d_2 \\ 
a_3x+b_3y+c_3z=d_3
\end{array}
\right.
$$
```
表示：
$$
\left \{ 
\begin{array}{c}
a_1x+b_1y+c_1z=d_1 \\ 
a_2x+b_2y+c_2z=d_2 \\ 
a_3x+b_3y+c_3z=d_3
\end{array}
\right.
$$
<font color="Tomato">通常MathJax通过内部策略自己管理公式内部的空间，因此`a…b` 与`a…….b` （.表示空格）都会显示为`ab` 。可以通过在`ab` 间加入`\` ,增加些许间隙，`\;` 增加较宽的间隙，`\quad` 与`\qquad` 会增加更大的间隙</font>

## 特殊函数与符号
* 三角函数
  * `sin(x)` : $sin(x)$
  * `arctan(x)` : $arctan(x)$
  * `cos(x)` : $cos(x)$
* 比较运算符
  * 小于(`\lt`)：$\lt$    
  * 大于(`\gt`)：$\gt$    
  * 小于等于(`\le`)：$\le$    
  * 大于等于(`\ge`)：$\ge$   
  * 不等于(`\ne`) : $\ne$   
  * 可以在这些运算符前面加上`\not` ，如`\not\lt` : $\not\lt$  
* 集合关系与运算   
  * 并集(`\cup` ): $\cup$
  * 交集(`\cap` ): $\cap$
  * 差集(`\setminus` ): $\setminus$
  * 子集(`\subset` ): $\subset$
  * 子集(`\subseteq` ): $\subseteq$
  * 非子集(`\subsetneq` ): $\subsetneq$
  * 父集(`\supset` ): $\supset$
  * 属于(`\in` ): $\in$
  * 不属于(`\notin` ): $\notin$
  * 空集(`\emptyset` ): $\emptyset$
  * 空(`\varnothing` ): $\varnothing$
* 排列
  * `\binom{n+1}{2k}` ： $\binom{n+1}{2k}$
  * `{n+1 \choose 2k}` : ${n+1 \choose 2k}$
* 箭头   
  * `\to` : $\to$   
  * `\rightarrow` : $\rightarrow$    
  * `\leftarrow` : $\leftarrow$    
  * `\Rightarrow` : $\Rightarrow$     
  * `\Leftarrow` : $\Leftarrow$   
  * `\mapsto` : $\mapsto$
* 逻辑运算符
  * `\land` : $\land$
  * `\lor` : $\lor$
  * `\lnot` : $\lnot$
  * `\forall` : $\forall$
  * `\exists` : $\exists$
  * `\top` : $\top$
  * `\bot` : $\bot$
  * `\vdash` : $\vdash$
  * `\vDash` : $\vDash$
* 操作符  
  *`\star` : $\star$  
  *`\ast` : $\ast$  
  *`\oplus` : $\oplus$  
  *`\circ` : $\circ$  
  *`\bullet` : $\bullet$
* 等于  
  *`\approx` : $\approx$  
  *`\sim` : $\sim$  
  *`\equiv` : $\equiv$
  *`\prec` : $\prec$
* 范围  
  *`\infty` : $\infty$  
  *`\aleph_o` : $\aleph_o$  
  *`\nabla` : $\nabla$    
  *`\Im` : $\Im$    
  *`\Re` : $\Re$    
* 模运算  
  *`\pmod` : $b \pmod n$  
  如`a \equiv b \pmod n` : $a \equiv b \pmod n$  
* 点  
  *`\ldots` : $\ldots$  
  *`\cdots` : $\cdots$  
  *`\cdot` : $\cdot$  
  其区别是点的位置不同，`\ldots`位置稍低，`\cdots`位置居中
  ```
  $$
  \begin{equation}
  a_1+a_2+\ldots+a_n \\ 
  a_1+a_2+\cdots+a_n
  \end{equation}
  $$
  ```  
  表示：
  $$
  \begin{equation}
  a_1+a_2+\ldots+a_n \\
  a_1+a_2+\cdots+a_n
  \end{equation}
  $$
## 顶部符号
对于单字符，`\hat x` ：$\hat x$  
多字符可以使用`\widehat {xy}` ：$\widehat {xy}$  
类似的还有:  
(\overline x ): \overline x
矢量`\vec` : $\vec x$  
向量`\overrightarrow {xy}` : $\overrightarrow {xy}$  
`\dot x ` : $\dot x$  
`\ddot x ` : $\ddot x$  
(`dot {\dot x} ` : 

## 表格
使用`\begin{array}{列样式}…\end{array}` 这样的形式来创建表格，列样式可以是`clr` 表示居中，左，右对齐，还可以使用`| `表示一条竖线。表格中各行使用`\\` 分隔，各列使用`& `分隔。使用`\hline`在本行前加入一条直线。 例如:
```
$$
\begin{array}{c|lcr}
n & \text{Left} & \text{Center} & \text{Right} \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i \\
\end{array}
$$
```
得到：  
$$
\begin{array}{c|lcr}
n & \text{Left} & \text{Center} & \text{Right} \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i \\
\end{array}
$$
## 矩阵
### 基本内容
使用 `\begin{matrix}…\end{matrix}` 这样的形式来表示矩阵，在`\begin` 与`\end` 之间加入矩阵中的元素即可。矩阵的行之间使用`\\` 分隔，列之间使用`&` 分隔，例如:
```
$$
\begin{matrix}
1 & x & x^2 \\
1 & y & y^2 \\
1 & z & z^2 \\
\end{matrix}
$$
```
得到:  
$$
\begin{matrix}
1 & x & x^2 \\
1 & y & y^2 \\
1 & z & z^2 \\
\end{matrix}
$$
### 括号 
如果要对矩阵加括号，可以像上文中提到的一样，使用`\left` 与`\right` 配合表示括号符号。也可以使用特殊的`matrix` 。即替换`\begin{matrix}…\end{matrix}` 中`matrix` 为`pmatrix` ，`bmatrix` ，`Bmatrix` ，`vmatrix` , `Vmatrix`     
    pmatrix`$\begin{pmatrix}1 & 2 \\ 3 & 4\\ \end{pmatrix}$` : $\begin{pmatrix}1 & 2 \\ 3 & 4\\ \end{pmatrix}$  
    bmatrix`$\begin{bmatrix}1 & 2 \\ 3 & 4\\ \end{bmatrix}$` : $\begin{bmatrix}1 & 2 \\ 3 & 4\\ \end{bmatrix}$  
    Bmatrix`$\begin{Bmatrix}1 & 2 \\ 3 & 4\\ \end{Bmatrix}$` : $\begin{Bmatrix}1 & 2 \\ 3 & 4\\ \end{Bmatrix}$  
    vmatrix`$\begin{vmatrix}1 & 2 \\ 3 & 4\\ \end{vmatrix}$` : $\begin{vmatrix}1 & 2 \\ 3 & 4\\ \end{vmatrix}$  
### 元素省略
可以使用`\cdots` ：⋯，`\ddots`：⋱ ，`\vdots`：⋮ 来省略矩阵中的元素，如：  
```
$$
\begin{pmatrix}
1&a_1&a_1^2&\cdots&a_1^n\\
1&a_2&a_2^2&\cdots&a_2^n\\
\vdots&\vdots&\vdots&\ddots&\vdots\\
1&a_m&a_m^2&\cdots&a_m^n\\
\end{pmatrix}
$$
```
表示：  
$$
\begin{pmatrix}
1&a_1&a_1^2&\cdots&a_1^n\\
1&a_2&a_2^2&\cdots&a_2^n\\
\vdots&\vdots&\vdots&\ddots&\vdots\\
1&a_m&a_m^2&\cdots&a_m^n\\
\end{pmatrix}
$$
### 增广矩阵
增广矩阵需要使用前面的表格中使用到的 `\begin{array} ... \end{array}` 来实现
```
$$
\left[  \begin{array}  {c c | c} %这里的c表示数组中元素对其方式：c居中、r右对齐、l左对齐，竖线表示2、3列间插入竖线
1 & 2 & 3 \\
\hline %插入横线，如果去掉\hline就是增广矩阵
4 & 5 & 6
\end{array}  \right]
$$
```
显示为：
$$
\left[  \begin{array}  {c c | c} %这里的c表示数组中元素对其方式：c居中、r右对齐、l左对齐，竖线表示2、3列间插入竖线
1 & 2 & 3 \\
\hline %插入横线，如果去掉\hline就是增广矩阵
4 & 5 & 6
\end{array}  \right]
$$

## 公式标记与引用
  使用`\tag{yourtag}` 来标记公式，如果想在之后引用该公式，则还需要加上`\label{yourlabel}` 在`\tag` 之后，如`$$a = x^2 - y^3 \tag{1}\labe{1}$$` 显示为：  
$$a := x^2 - y^3 \tag{1}\labe{1}$$
  如果不需要被引用，只使用`\tag{yourtag}` ，`$$x+y=z\tag{1.1}$$`显示为：  
$$x+y=z\tag{1.1}$$
  `\tab{yourtab}` 中的内容用于显示公式后面的标记。公式之间通过`\label{}` 设置的内容来引用。为了引用公式，可以使用`\eqref{yourlabel}` ，如`$$a + y^3 \stackrel{\eqref{1}}= x^2$$` 显示为：
$$a + y^3 \stackrel{\eqref{1}}= x^2$$

或者使用`\ref{yourlabel}` 不带括号引用，如`$$a + y^3 \stackrel{\ref{111}}= x^2$$` 显示为:
$$a + y^3 \stackrel{\ref{1}}= x^2$$

## 字体
### 黑板粗字体
此字体经常用来表示代表实数、整数、有理数、复数的大写字母。
`$\mathbb ABCDEF$`：$\mathbb ABCDEF$  
`$\Bbb ABCDEF$`：$\Bbb ABCDEF$
### 黑体字
`$\mathbf ABCDEFGHIJKLMNOPQRSTUVWXYZ$` : $\mathbf ABCDEFGHIJKLMNOPQRSTUVWXYZ$
`$\mathbf abcdefghijklmnopqrstuvwxyz$` : $\mathbf abcdefghijklmnopqrstuvwxyz$
### 打印机字体
`$\mathtt ABCDEFGHIJKLMNOPQRSTUVWXYZ$` : $\mathtt ABCDEFGHIJKLMNOPQRSTUVWXYZ$

## 参考文档
直接输入地址

## Emoji小表情
https://www.webfx.com/tools/emoji-cheat-sheet/