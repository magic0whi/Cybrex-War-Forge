---
title: linear-algebra
toc: true
category: linear-algebra
lang: zh-cn
date: 2021-01-02 17:32:52
tags:
---

<!-- more -->

## 行列式

### 二阶三阶行列式

二阶行列式: \\(\begin{vmatrix} a & b \\\ c & d \end{vmatrix}=ad-bc\\)

{% asset_img 1.png %}

排列: 由 \\(1,2,\dots,n\\) 组成的一个**有序**数组, 叫作 \\(n\\) 级排列(中间不能缺数)
\\(3\\) 级排列有 \\(123,132,213,231,312,321\\) 共 \\(6\\) 种
\\(n\\) 级排列有 \\(n!\\) 种

逆序: 排列中大数排在小数前面的情况
(奇、偶)逆序数: 出现逆序的总数, 用 \\(N(\text{排列内容})\\) 表示
如何数逆序数:
1. 从第一个开始, 数后面有几个比它小的
2. 顺序不可乱来
{% asset_img 2.png %}

\\(n\\) 级标准排列(自然排列的逆序数: \\(N(1234\dots n)=0\\)
\\(n\\) 级逆序排列的逆序数: \\(N=(n(n-1)(n-2)\dots 321)=(n-1)+(n-2)+\dots+3+2+1+0=\frac{(n-1)+0}{2}\cdot n=\frac{n(n-1)}{2}\\)

对换: 交换两个数
如 \\(N(54123)=4+3+0+0=7\to N(54213)=4+3+1+0=8\\)

定理1: 一个对换, 奇偶性改变
定理2: \\(n\\) 组排列中, 奇排列, 偶排列各占 \\(\frac{n!}{2}\\)

### n 阶行列式

第一种定义(按行展开): 行标取标准排列, 列表取排列的所有可能, 从不同行不同列取出 \\(n\\) 个元素相乘, 符号由列标排列的奇偶性决定(奇负偶正)
\\(\begin{vmatrix} a_{11} & a_{12} & \dots & a_{1n} \\\ a_{21} & a_{22} & \dots & a_{2n} \\\ \vdots & \vdots & \ddots & \vdots \\\ a_{n1} & a_{n2} & \dots & a_{nn} \end{vmatrix}=\displaystyle\sum_{j_1j_2\dots j_n} (-1)^{N(j_1j_2\dots j_n)}\cdot a_{1j_1}a_{2j_2}\dots a_{nj_n}\\)

如 \\(\begin{vmatrix} a_{11} & a_{12} & a_{13} \\\ a_{21 }& a_{22} & a_{23} \\\ a_{31} & a_{32} & a_{33} \end{vmatrix}=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}-a_{12}a_{21}a_{33}-a_{11}a_{23}a_{32}\\)
{% asset_img 3.png %}

1. 主对角线元素相乘(上三角、下三角、对角形)
   {% asset_img 4.png %}
2. 次对角线元素相乘(上三角、下三角、对角形)
   {% asset_img 5.png %}

第二种定义(按列展开): 列标取自然排列, 行标取所有可能, 不同行不同列取 \\(n\\) 个元素相乘, 符号由行标排列的奇偶性决定.
\\(\displaystyle\sum_{i_1i_2\dots i_n} (-1)^{N(i_1i_2\dots i_n)}\cdot a_{i_11}a_{i_22}\dots a_{i_nn}\\)

第三种定义(既不按行也不按列): \\(\sum (-1)^{N(i_1i_2\dots i_n)+N(j_1j_2\dots j_n)}\cdot a_{i_1j_1}a_{i_2j_2}\dots a_{i_nj_n}\\)

### 行列式的性质

转置: \\(D=\begin{vmatrix} 1 & 2 & 3 \\\ 1 & 1 & 1 \\\ 8 & 8 & 8 \end{vmatrix}\\) , \\(D^T=\begin{vmatrix} 1 & 1 & 8 \\\ 2 & 1 & 8 \\\ 3 & 1 & 8 \end{vmatrix}\\) , \\((D^T)^T=\begin{vmatrix} 1 & 2 & 3 \\\ 1 & 1 & 1 \\\ 8 & 8 & 8 \end{vmatrix}=D\\)

性质 1: 行列式转置后值不变 \\(D^T=D\\)

性质 2: 两行(列)互换, 值变号

性质 3: 若有两行(列)相等, 则值为零. (因为要满足性质 2 则 \\(D=-D=0\\))

性质 4: 行列式某一行有公因子 \\(k\\) , 可将 \\(k\\) 提出
\\(D=\begin{vmatrix} 1 & 2 & 3 \\\ 4k & 5k & 6k \\\ 7 & 8 & 9 \end{vmatrix}=k\begin{vmatrix} 1 & 2 & 3 \\\ 4 & 5 & 6 \\\ 7 & 8 & 9 \end{vmatrix}\\)

性质 5: 若有两行对应成比例, 则值为零. (基于性质 3 和性质 4)
\\(D=\begin{vmatrix} 1 & 2 & 3 \\\ 1 & 1 & 1 \\\ 8 & 8 & 8 \end{vmatrix}=8\begin{vmatrix} 1 & 2 & 3 \\\ 1 & 1 & 1 \\\ 1 & 1 & 1 \end{vmatrix}=0\\)
推论: 若某一行全为 \\(0\\) , 则值为零

总结:
\\(D=0\gets\begin{cases} \text{两行相等} \\\ \text{两行对应成比例} \\\ \text{某一行全为} 0 \end{cases}\\)

性质 6: 某一行数字为两数之和, 可拆分为两个行列式相加, 其余行不变.
\\(\begin{vmatrix} b+c & c+a & a+b \\\ a+b & b+c & c+a \\\ c+a & a+b & b+c \end{vmatrix}=\begin{vmatrix} b & c & a \\\ a+b & b+c & c+a \\\ c+a & a+b & b+c \end{vmatrix}+\begin{vmatrix} c & a & b \\\ a+b & b+c & c+a \\\ c+a & a+b & b+c \end{vmatrix}=\cdots\\)

性质 7: 某一行(列)乘以一个数加到另一行(列)上去, 值不变. (基于性质 6)
<div>
$$
D=
\begin{vmatrix}
 1 & 2 & 3 \\
 1 & 1 & 0 \\
 9 & 9 & 10
\end{vmatrix}
\xrightarrow[\text{加到第二行}]{\text{第一行}\times 5}
\begin{vmatrix}
 1 & 2 & 3 \\
 1+5 & 1+10 & 0+15 \\
 9 & 9 & 10
\end{vmatrix}
=\begin{vmatrix}
 1 & 2 & 3 \\
 1 & 1 & 0 \\
 9 & 9 & 10
\end{vmatrix}
+5\begin{vmatrix}
 1 & 2 & 3 \\
 1 & 2 & 3 \\
 9 & 9 & 10
\end{vmatrix}
=\begin{vmatrix}
 1 & 2 & 3 \\
 1 & 1 & 0 \\
 9 & 9 & 10
\end{vmatrix}
+0=D
$$
</div>

例 3: 求 \\(D=\begin{vmatrix} 1 & 2 & 0 & 1 \\\ 2 & 3 & 10 & 0 \\\ 0 & 3 & 5 & 18 \\\ 5 & 10 & 15 & 4 \end{vmatrix}\\)
(思路: 尽量化为上三角再计算, 先处理第一列, 再第二列、第三列. 第一列处理完后, 第一行不再参与运算)
<div>
$$
\xrightarrow[\text{加到第二行}]{\text{第一行}\times(-2)}
\begin{vmatrix}
 1 & 2 & 0 & 1 \\
 0 & -1 & 10 & -2 \\
 0 & 3 & 5 & 18 \\
 5 & 10 & 15 & 4
\end{vmatrix}
\xrightarrow[\text{加到第四行}]{\text{第一行}\times(-5)}
\begin{vmatrix}
 1 & 2 & 0 & 1 \\
 0 & -1 & 10 & -2 \\
 0 & 3 & 5 & 18 \\
 0 & 0 & 15 & -1
\end{vmatrix}
\xrightarrow[\text{加到第三行}]{\text{第二行}\times 3}
\begin{vmatrix}
 1 & 2 & 0 & 1 \\
 0 & -1 & 10 & -2 \\
 0 & 0 & 35 & 12 \\
 0 & 0 & 15 & -1
\end{vmatrix}
\xrightarrow[\text{加到第四行}]{\text{第三行}\times(-\frac{3}{7})}
\begin{vmatrix}
 1 & 2 & 0 & 1 \\
 0 & -1 & 10 & -2 \\
 0 & 0 & 35 & 12 \\
 0 & 0 & 0 & -\frac{43}{7} 
\end{vmatrix}
=1\times(-1)\times 35\times(-\frac{43}{7})=215
$$
</div>

### 行列式按行(列)展开

### 行列式的计算

## 矩阵

## 向量组

