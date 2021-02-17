---
layout: post
title: Markdown的基本语法
categories: Markdown
description: 介绍 Markdown 的一些基本用法。
keywords: Markdown
---

==注意==：这里我没有给出Markdown的原始写法，只展现了写好以后的效果。有兴趣的朋友可以下载和参考我这篇文章的[github repo](https://github.com/chauby/chauby.github.io)，在路径`_posts/markdown/2019-12-13-markdown-basic-skills.md`可以找到。同时欢迎大家star和fork这个github库。

## 一. 普通示范

这里是中文的正文示范，各种格式的字体都可以在下面找到。

**加粗文字**

*斜体*

***加粗斜体***

<u>下划线</u>

~~删除线~~



This is the example of English.

### 1. 有序列表

1. 第一个
2. 第二个
3. 第三个



- 一级列表
    + 二级列表
        * 三级列表

### 2. 无序列表

- 第一个

- 第二个
- 第三个



#### 2.1 任务列表：

- [ ] 吃饭

- [ ] 睡觉

- [ ] 打豆豆

  

### 3. 表格

| 编号 | 项目 | 金额 | 备注               |
| :--: | ---- | ---- | ------------------ |
|  1   | 吃饭 | 108  | Beef               |
|  2   | 打车 | 25   | 从天府广场去春熙路 |
|  3   | 买菜 | 32   | 白菜、萝卜         |

### 4. 文本链接

[百度搜索](https://www.baidu.com)

[谷歌](https://www.google.com)



### 5. 地址链接

<http://www.zhihu.com>




## 二. 高级用法

### 下标

H~2~O



### 上标

X^2^



### 行内公式

这是一个行内公式 $x^2 + y^2 = 1$, 表示二维平面内圆的公式。



### LaTex公式块

二维平面内的一条直线可以表示为
$$
y=k\cdot x+b \label{eq:line}
$$

带根号的表达式
$$
z =\pm \sqrt{x^2+y^2} \label{eq:sqrt}
$$
求和公式
$$
s = \sum^N_n x_n \label{eq:sum}
$$
更复杂的公式 --- 矩阵表示
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
\label{eq:matrix}
$$


公式的自动编号由Typora的软件设定，非Markdown的用法。对公式 ($\ref{eq:line}$)的引用可以用这种方式来实现，比如引用公式($\ref{eq:matrix}$)，对图片的引用还没搞懂，貌似只能手动引用，例如图1。



### 插入图片

这是一个示例图片。

<center>
    <img src="/images/posts/markdown/latex.png" alt="Latex" style="zoom:50%;" />
    <br>
</center>

<center>
    图1.图片的标题可以这样表示
</center>



### emoji表情

:smile:

:horse:

:cloud_with_snow:

:hammer:



### 行内代码

行内代码可以这样表示 `x=y[0];`，但是行内代码表示时不会有代码高亮。



### 代码段

C++语言

```c++
#include <iostream>
using namespace std;

int main(void)
{
    cout << "Hello, world" << endl;
    return 0;
}
```



Python语言

```python
import numpy as np
import matplotlib as plt
def function():
    for i in range(100):
        t = 0.01*i
        x = sin(t)
    plt.plot(t, x)
    plt.show()
    pass
```



Matlab语言

```matlab
clear;
close all;
t=1:0.01:2*pi;
x = sin(t);

figure
plot(t, x)
title('sine wave')
```



点击锚点处的示范可跳转到这里 <a name="here"></a>









## 三. 引用

### 普通引用

> 这是一句普通文本的引用，产生的是特殊格式



### 链接引用

[参考百度学术首页](http://xueshu.baidu.com "点击访问百度学术首页")

[参考本目录下的另一个文件：reference](./reference.md "reference.md")

[参考本文档的某个章节：行内代码](#行内代码)

[打开桌面文件夹](file:///C:/users/zouchaobin/Desktop)

锚点的用法，跳转到[指定位置](#here)



### 参考文献写法

这里的参考文献主要写法为[参考文献1][1]



[1]:参考文献标题，作者，年份...	"此处是参考文献示范"

