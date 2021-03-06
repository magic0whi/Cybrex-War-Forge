---
title: linear-algebra
toc: true
category: linear-algebra
lang: zh-cn
date: 2021-01-02 17:32:52
tags:
---

基于[Sakura丶落桜的线性代数整理](https://www.bilibili.com/read/readlist/rl333931)
等学习完毕开始完善此笔记格式
线性代数的题目如果有多个解, 注意带回原题检查, 很多时候能能消掉一个

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

1. 第一种定义(按行展开)
   <div>
   $$
   \begin{vmatrix}
    a_{11} & a_{12} & \dots & a_{1n} \\
    a_{21} & a_{22} & \dots & a_{2n} \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{n1} & a_{n2} & \dots & a_{nn}
   \end{vmatrix}
   =\displaystyle\sum_{j_1j_2\dots j_n} (-1)^{N(j_1j_2\dots j_n)}\cdot a_{1j_1}a_{2j_2}\dots a_{nj_n}
   $$
   </div>
   
   行标取标准排列, 列表取排列的所有可能, 从不同行不同列取出 \\(n\\) 个元素相乘, 符号由列标排列的奇偶性决定
   
   如 \\(\begin{vmatrix} a_{11} & a_{12} & a_{13} \\\ a_{21 }& a_{22} & a_{23} \\\ a_{31} & a_{32} & a_{33} \end{vmatrix}=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}-a_{12}a_{21}a_{33}-a_{11}a_{23}a_{32}\\)
   {% asset_img 3.png %}
   
   1. 主对角线元素相乘(上三角、下三角、对角形)
      {% asset_img 4.png %}
   2. 次对角线元素相乘(上三角、下三角、对角形)
      {% asset_img 5.png %}
   
2. 第二种定义(按列展开): 列标取自然排列, 行标取所有可能, 不同行不同列取 \\(n\\) 个元素相乘, 符号由行标排列的奇偶性决定.
   \\(\displaystyle\sum_{i_1i_2\dots i_n} (-1)^{N(i_1i_2\dots i_n)}\cdot a_{i_11}a_{i_22}\dots a_{i_nn}\\)
3. 第三种定义(既不按行也不按列): \\(\sum (-1)^{N(i_1i_2\dots i_n)+N(j_1j_2\dots j_n)}\cdot a_{i_1j_1}a_{i_2j_2}\dots a_{i_nj_n}\\)

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

1. 余子式: (即剩**余子**集行列**式**) 划去某个点所在的行和列所形成的新行列式. 符号 \\(M_{ij}\\)
   如行列式 \\(\begin{vmatrix} 1 & 1 & 0 & 3 \\\ 1 & 1 & 1 & 1 \\\ 2 & 2 & 3 & 4 \\\ 5 & 5 & 6 & 6 \end{vmatrix}\\) 中, 点 \\(a_{32}\\) 对应的余子式 \\(M_{32}=\begin{vmatrix} 1 & 0 & 3 \\\ 1 & 1 & 1 \\\ 5 & 6 & 6 \end{vmatrix}\\)
2. 代数余子式: 在余子式的基础上加上一个根据行号和列号判断正负的代数. 符号 \\(A_{ij}=(-1)^{i+j}M_{ij}\\)
   如行列式 \\(\begin{vmatrix} 1 & 1 & 0 & 3 \\\ 1 & 1 & 1 & 1 \\\ 2 & 2 & 3 & 4 \\\ 5 & 5 & 6 & 6 \end{vmatrix}\\) 中, 点 \\(a_{32}\\) 对应的代数余子式 \\(A_{32}=(-1)^{3+2}\begin{vmatrix} 1 & 0 & 3 \\\ 1 & 1 & 1 \\\ 5 & 6 & 6 \end{vmatrix}\\)
3. 行列式展开:
   * 在第 \\(k\\) 行展开 \\(D=\displaystyle\sum_{j=1}^n a_{kj}\cdot A_{kj}\\)
   * 在第 \\(k\\) 列展开 \\(D=\displaystyle\sum_{i=1}^n a_{ik}\cdot A_{ik}\\)
   
   技巧: 一般选 0 较多的行(列)展开
   定理:
   * 异乘变零: 某行元素与另一行元素的代数余子式乘积之和为 \\(0\\)
     证明:
     设行列式 \\(\begin{vmatrix} 1 & 1 & 2 & 3 \\\ 0 & 0 & 8 & 9 \\\ 2 & 5 & 5 & 4 \\\ 9 & 9 & 9 & 10 \end{vmatrix}\\)
     用第四行元素乘第一行元素的代数余子式有 \\(9\times A_{11}+9\times A_{12}+9\times A_{13}+10\times A_{14}\\)
     等价于 \\(\begin{vmatrix} 9 & 9 & 9 & 10 \\\ 0 & 0 & 8 & 9 \\\ 2 & 5 & 5 & 4 \\\ 9 & 9 & 9 & 10 \end{vmatrix}=0\\) (行列式性质 3 两行相等值为零)
   * 拉普拉斯定理:
     * \\(k\\) 阶子式: 从行列式中取 \\(k\\) 行 \\(k\\) 列得到的子式和余子式.
       如 \\(\begin{vmatrix} 1 & 2 & 3 & 4 \\\ 1 & 1 & 2 & 5 \\\ 1 & 1 & 0 & 8 \\\ 9 & 9 & 9 & 10 \end{vmatrix}\\)
       取 1、2 行和 1、2 列
       得到二阶子式 \\(\begin{vmatrix} 1 & 2 \\\ 1 & 1 \end{vmatrix}\\) ,
       余子式 \\(\begin{vmatrix} 0 & 8 \\\ 9 & 10 \end{vmatrix}\\)
       代数余子式(所有行号和列号相加) \\((-1)^{1+2+1+2}\begin{vmatrix} 0 & 8 \\\ 9 & 10 \end{vmatrix}\\)
     * 拉普拉斯展开: 取定 \\(k\\) 行, 由 \\(k\\) 行元素组成的所有 \\(k\\) 阶子式与代数余子式乘积之和.
       某些特殊的行列式用拉普拉斯展开可以比按行(列)展开更省力
       例:
       \\(D=\begin{vmatrix} 1 & 2 & 0 & 0 & 0 \\\ 3 & 4 & 0 & 0 & 0 \\\ 1 & 2 & 3 & 4 & 5 \\\ 1 & 1 & 1 & 1 & 1 \\\ 6 & 6 & 8 & 3 & 1 \end{vmatrix}\\)
       取 1、2 行, 则列有 \\(C_5^2=10\\) 种选择, 但观察可以发现这个矩阵只有在选择 1、2 列的时候它的二阶子式才不为零.
       即 \\(D=\begin{vmatrix} 1 & 2 \\\ 3 & 4 \end{vmatrix}\times(-1)^{1+2+1+2}\times\begin{vmatrix} 3 & 4 & 5 \\\ 1 & 1 & 1 \\\ 8 & 3 & 1 \end{vmatrix}+0+0+0+\dots\\)

### 行列式的计算

行列式相乘(同阶): 行列式中 \\(a_{ij}\\) 元素的值为前者第 \\(i\\) 行的每项分别乘后者第 \\(j\\) 列的对应项再相加 (\\(a_{ij}=\displaystyle\sum_{k=1}^{n} a_{ik}\cdot a_{kj}\\))
若不同阶行列式相乘, 直接计算行列式的值再相乘即可

* 一般构造上三角来计算
  若 \\(a_{11}=0\\) 的情况则需要交换行或拿其他的行加第一行使 \\(a_{11}\neq 0\\)
  若用默认的第一行构造上三角时出现计算时碰到的分数太多的问题也建议交换行
* 针对求只余子式的问题, 通过构造一个抵消代数余子式符号的式子并构造这个式子的行列式然后计算这个行列式的值即可
  {% asset_img 6.png %}
* 针对主对角线都是 \\(x\\) , 其余地方都是 \\(a\\) 的行列式, 可通过将一列后面所有的列加到第一列上然后提公因子使一列元素全变为 \\(1\\) , 再将一列乘以 \\(-a\\) 分别去加后面的列, 从而构造出一个下三角.
  {% asset_img 7.png %}
* 加边法(可用拉普拉斯展开推导)
  {% asset_img 8.png %}
* 范德蒙德行列式(可用数学归纳法推导)
  <div>
  $$
  \begin{vmatrix}
  1 & 1 & 1 & \dots & 1 \\
  x_1 & x_2 & x_3 & \dots & x_n \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
  x_1^{n-2} & x_2^{n-2} & x_2^{n-2} & \dots & x_n^{n-2} \\
  x_1^{n-1} & x_2^{n-1} & x_1^{n-1} & \dots & x_n^{n-1}
  \end{vmatrix}
  =\Pi(x_i-x_j)\enspace (1\leqslant j< i\leqslant n)
  $$
  </div>

  \\(\Pi\\) 表示全体同类因子的乘积(见下面例子)
  {% asset_img 9.png %}
* 反对称行列式
  1. 主对角线全为 0
  2. 上下位置对应成相反数(\\(a_{ij}=-a{ji}\\))
   
  * 奇数阶反对称行列式值为 0
    证明: (行列式转置后值不变)
    <div>
    $$
    D=
    \begin{vmatrix}
     0 & a & b \\
     -a & 0 & c \\
     -b & -c & 0
    \end{vmatrix}
    \xrightarrow{\text{将三行公因子}-1\text{提出}}
    (-1)^3
    \begin{vmatrix}
     0 & -a & -b \\
     a & 0 & -c \\
     b & c & 0
    \end{vmatrix}
    =-D^T=-D \\
    \therefore D=-D=0
    $$
    </div> 
* 对称行列式
  1. 主对角线无要求
  2. 上下位置对应相等(\\(a_{ij}=a{ji}\\))

### 克莱姆(Cramer)法则

(克莱姆法则由于计算量太大不适合人来算, 主要应用于计算机解方程)

1. 前提:
   1. 方程个数等于未知量个数
   2. \\(D\neq 0\\)
2. 克莱姆法则: 方程的解 \\(x_j=\frac{D_j}{D}\\) (\\(D_j\\) 为用方程右边系数替换系数行列式 \\(D\\) 中的 \\(j\\) 列形成的行列式)
   例:
   如方程 \\(\begin{cases} x_1+x_2+x_3=1 \\\ x_1-x_2+5x_3=6 \\\ -x_1+x_2+6x_3=9 \end{cases}\\) (3 个方程, 3 个未知量)
   则有 \\(x_1=\frac{D_1}{D}\\) , \\(x_2=\frac{D_2}{D}\\) , \\(x_3=\frac{D_3}{D}\\)
   其中 \\(D=\begin{vmatrix} 1 & 1 & 1 \\\ 1 & -1 & 5 \\\ -1 & 1 & 6 \end{vmatrix}\\) , \\(D_1=\begin{vmatrix} 1 & 1 & 1 \\\ 6 & -1 & 5 \\\ 9 & 1 & 6 \end{vmatrix}\\) , \\(D_2=\begin{vmatrix} 1 & 1 & 1 \\\ 1 & 6 & 5 \\\ -1 & 9 & 6 \end{vmatrix}\\) , \\(D_3=\begin{vmatrix} 1 & 1 & 1 \\\ 1 & -1 & 6 \\\ -1 & 1 & 9 \end{vmatrix}\\)
3. 齐次方程: 等号右边都为 0 的方程组, 齐次方程至少有零解
   若齐次线性方程组的方程个数=未知数个数且 \\(D\neq 0\\), 则只有零解.
   若齐次线性方程组有非零解, 它的系数行列式 \\(D=0\\)

## 矩阵

### 矩阵概念

1. 定义: \\(m\\) 行 \\(n\\) 列的矩阵 \\(A_{m\times n}=\begin{pmatrix} a_{11} & a_{12} & \dots & a_{1n} \\\ a_{21} & a_{22} & \dots & a_{2n} \\\ \vdots & \vdots & \ddots & \vdots \\\ a_{m1} & a_{m2} & \dots & a_{mn} \end{pmatrix}\\)
2. 矩阵和行列式区别:
   1. 本质: 行列式是一个数, 而矩阵是数表
   2. 符号: 行列式是 \\(||\\) , 矩阵是 \\(()\\) 或 \\([]\\)
   3. 形状: 行列式行数=列数, 矩阵行数不一定等于列数
3. 行矩阵: 只有一行的矩阵
   列矩阵: 只有一列的矩阵
   实矩阵: 由实数构成
   复矩阵: 由复数构成
   零矩阵: 由 0 构成的矩阵
   负矩阵: \\(A\to -A\\)
   方阵: 行数=列数, \\(A_{n\times n}\\) (\\(A_n\\))
   单位矩阵: \\(E_n=\begin{bmatrix} 1 & & & \\\ & 1 & & \\\ & & \ddots & \\\ & & & 1 \end{bmatrix}\\)
   同型矩阵: 行数和列数相等的矩阵, 如 \\(A_{3\times 5}\\) 与 \\(B_{3\times 5}\\) 形状相同. 同型矩阵是矩阵相等必要条件. (所以两个零矩阵不一定相等)
4. 主对角线: 左上到右下
   次对角线: 右上到左下

### 矩阵运算

1. 加法: \\(\begin{pmatrix} a_{11} & a_{12} & a_{13} \\\ a_{21} & a_{22} & a_{23}\\\ a_{31} & a_{32} & a_{33}\end{pmatrix}+\begin{pmatrix} b_{11} & b_{12} & b_{13} \\\ b_{21} & b_{22} & b_{23}\\\ b_{31} & b_{32} & b_{33} \end{pmatrix}=\begin{pmatrix} a_{11}+b_{11} & a_{12}+b_{12} & a_{13}+b_{13} \\\ a_{21}+b_{21} & a_{22}+b_{22} & a_{23}+b_{23} \\\ a_{31}+b_{31} & a_{32}+b_{32} & a_{33}+b_{33} \end{pmatrix}\\)
   减法: \\(\begin{pmatrix} a_{11} & a_{12} & a_{13} \\\ a_{21} & a_{22} & a_{23}\\\ a_{31} & a_{32} & a_{33}\end{pmatrix}-\begin{pmatrix} b_{11} & b_{12} & b_{13} \\\ b_{21} & b_{22} & b_{23}\\\ b_{31} & b_{32} & b_{33} \end{pmatrix}=\begin{pmatrix} a_{11}-b_{11} & a_{12}-b_{12} & a_{13}-b_{13} \\\ a_{21}-b_{21} & a_{22}-b_{22} & a_{23}-b_{23} \\\ a_{31}-b_{31} & a_{32}-b_{32} & a_{33}-b_{33} \end{pmatrix}\\)
   **只有同型矩阵才能加减**
   运算律:
   1. 交换律 \\(A+B=B+A\\)
   2. 结合律 \\((A+B)+C=A+(B+C)\\)
   3. \\(A+0=A\\) (\\(A\\) 与 \\(0\\) 为同型)
   4. \\(A+(-A)=0\\) (\\(A\\) 与 \\(0\\) 为同型)
   5. \\(A+B=C\hArr A=C-B\\)
2. 数乘: \\(k\begin{pmatrix} a_{11} & a_{12} & a_{13} \\\ a_{21} & a_{22} & a_{23}\\\ a_{31} & a_{32} & a_{33}\end{pmatrix}=\begin{pmatrix} ka_{11} & ka_{12} & a_{13} \\\ ka_{21} & ka_{22} & ka_{23}\\\ ka_{31} & ka_{32} & ka_{33}\end{pmatrix}\\)
   提公因子: 矩阵所有元素均有公因子, 公因子外提一次(行列式中一行提一次)
   运算律:
   1. \\(k(A+B)=kA+kB\\)
   2. \\((k+l)A=kA+lA\\)
   3. \\(k(lA)=(kl)A\\)
3. 乘法:
   \\(c_{ij}=\displaystyle\sum_{k=1}^{n} a_{ik}\cdot b_{kj}\\)
   矩阵相乘条件: \\(A\times B=C\\) 中, \\(A\\) 的列数 \\(= B\\) 的行数
   其中 \\(C\\) 的行数 \\(= A\\) 的行数, \\(C\\) 的列数 \\(= B\\) 的列数
   例:
   <div>
   $$
   \begin{pmatrix}
    a_{11} & a_{12} & a_{13} \\
    a_{21} & a_{22} & a_{23}
   \end{pmatrix}
   \times\begin{pmatrix}
    b_{11} & b_{12} \\
    b_{21} & b_{22} \\
    b_{31} & b_{32}
   \end{pmatrix}
   =\begin{pmatrix}
    (a_{11}\times b_{11}+a_{12}\times b_{21}+a_{13}\times b_{31}) & (a_{11}\times b_{12}+a_{12}\times b_{22}+a_{13}\times b_{32}) \\
    (a_{21}\times b_{11}+a_{22}\times b_{21}+a_{23}\times b_{31}) & (a_{21}\times b_{12}+a_{22}\times b_{22}+a_{23}\times b_{32})
   \end{pmatrix}
   $$
   </div>

   矩阵乘法不满足:
   1. 分配律 \\(AB\neq BA\\)
   2. \\(AB=0\nRightarrow A=0\\) 或 \\(B=0\\)
   3. \\(AB=AC\\) , \\(A\neq 0\nRightarrow B=C\\)

   与零矩阵相乘: \\(A_{4\times 3}\times 0_{3\times 2}=0_{4\times 2}\\)

   运算律:
   1. 结合律 \\((AB)C=A(BC)\\)
   2. 分配律 \\((A+B)C=AC+BC\\) , \\(C(A+B)=CA+CB\\)
   3. \\(k(AB)=(kA)B=A(kB)\\)
4. 以矩阵表达方程组
   例:
   \\(\begin{cases} x_1=y_1-y_2 \\\ x_2=y_1+y_2 \end{cases}\hArr\begin{pmatrix} x_1 \\\ x_2 \end{pmatrix}=\begin{pmatrix} 1 & -1 \\\ 1 & 1 \end{pmatrix}\begin{pmatrix} y_1 \\\ y_2 \end{pmatrix}\\)
   \\(\begin{cases} y_1=z_1+z_2+2z_3 \\\ y_2=z_1-2z_2+z_3 \end{cases}\hArr\begin{pmatrix} y_1 \\\ y_2 \end{pmatrix}=\begin{pmatrix} 1 & 1 & 2 \\\ 1 & -2 & 1 \end{pmatrix}\begin{pmatrix} z_1 \\\ z_2 \\\ z_3 \end{pmatrix}\\)
   \\(\begin{cases} z_1=u_1+u_2 \\\ z_2=u_1 \\\ z_3=-u_1+u_2 \end{cases}\hArr\begin{pmatrix} z_1 \\\ z_2 \\\ z_3 \end{pmatrix}\begin{pmatrix} 1 & 1 \\\ 1 & 0 \\\ -1 & 1 \end{pmatrix}\begin{pmatrix} u_1 \\\ u_2 \end{pmatrix}\\)
   三组方程可组合成:
   \\(\begin{pmatrix} x_1 \\\ x_2 \end{pmatrix}=\begin{pmatrix} 1 & -1 \\\ 1 & 1 \end{pmatrix}\times\begin{pmatrix} 1 & 1 & 2 \\\ 1 & -2 & 1 \end{pmatrix}\times\begin{pmatrix} 1 & 1 \\\ 1 & 0 \\\ -1 & 1 \end{pmatrix}\times\begin{pmatrix} u_1 \\\ u_2 \end{pmatrix}\\)
5. 幂 \\(A^k=\underbrace{A\dots A}_{k\text{个}}\\) , \\(A^0=E\\)
   运算律:
   1. \\(A^{k_1}A^{k_2}=A^{k_1+k_2}\\) (\\(A\\) 为方阵)
   2. \\((A^{k_1})^{k_2}=A^{k_1k_2}\\)
   3. 一般 \\((AB)^k\neq A^kB^k\\) , \\((A\pm B)^2\neq A^2\pm 2AB+B^2\\)
      但 \\((A\pm E)^2=A^2\pm 2AE+E^2=A^2\pm 2A+E^2\\)
6. 转置
   定义: \\(A=\begin{pmatrix} 1 & 2 & 3 \\\ 1 & 1 & 1 \end{pmatrix}\_{2\times 3}\\) , \\(A^T=\begin{pmatrix} 1 & 1 \\\ 2 & 1 \\\ 3 & 1 \end{pmatrix}\_{3\times 2}\\) , \\((A^T)^T=A\\)
   1. 性质1: \\((A^T)^T=A\\)
   2. 性质2: \\((A+B)^T=A^T+B^T\\)
   3. 性质3: \\((kA)^T=kA^T\\)
   4. 性质4: \\((AB)^T=B^TA^T\\) , \\((A_1A_2A_3A_4)^T=A_4^TA_3^TA_2^TA_1^T\\)

### 特殊矩阵

1. 数量矩阵
   <div>
   $$
   \begin{pmatrix}
    a & & & & \\
    & a & & & \\
    & & a & & \\
    & & & \ddots & \\
    & & & & a
   \end{pmatrix}
   =aE
   $$
   </div>

   零矩阵与单位矩阵为特殊的数量矩阵.
   \\((aE)B=B(aE)=aB\\)
   \\(AE=EA=A\\) (注意两边的 \\(E\\) 不一定相同, 如 \\(A_{2\times 3}E_3=E_2A_{2\times 3}\\)
2. 对角形矩阵:
   <div>
   $$
   \begin{pmatrix}
    a_1 & & & & \\
    & a_2 & & & \\
    & & a_3 & & \\
    & & & \ddots & \\
    & & & & a_n
   \end{pmatrix}
   =\text{diag}(a_1,a_2,\dots,a_n)
   $$
   <div>
   {% asset_img 10.png %}

   数量矩阵是特殊的对角形矩阵
3. 三角形矩阵:
   {% asset_img 11.png %}
4. 对称矩阵: \\(a_{ij}=a_{ji}\\) , \\(A^T=A\\)
   * 若 \\(A\\)、\\(B\\) 同阶对称(\\(A^T=A\\) , \\(B^T=B\\)) , 则有:
     \\((A\pm B)^T=A^T\pm B^T=A\pm B\\)
     \\((kA)^T=kA^T=kA\\)
     \\((AB)^T=B^T\cdot A^T=BA\neq AB\\)
   * 定理: \\(A\\)、\\(B\\) 对称, \\(AB\\) 对称 \\(\hArr AB=BA\\)
5. 反对称矩阵: \\(a_{ij}=-a_{ij}\\) 且主对角线全为 0, \\(A^T=-A\\)

### 逆矩阵

1. 方阵的行列式:
   \\(A=\begin{pmatrix} 2 & 2 & 2 \\\ 3 & 3 & 3 \\\ 1 & 1 & 1 \end{pmatrix}\\) , \\(|A|=\begin{vmatrix} 2 & 2 & 2 \\\ 3 & 3 & 3 \\\ 1 & 1 & 1 \end{vmatrix}\\)
2. 性质1: \\(|A^T|=|A|\\) (行列式转置值不变)
   性质2: \\(|kA|=k^n|A|\\)
   性质3: \\(|AB|=|A|\cdot|B|\\)
3. 伴随矩阵: (只有方阵有伴随矩阵)
   通过:
   1. 求所有元素的代数余子式
   2. 按行求得代数余子式**按列放**
   
   构成的矩阵
   <div>
   $$
   A^*=
   \begin{pmatrix}
    A_{11} & A_{21} & \dots & A_{n1} \\
    A_{12} & A_{22} & \dots & A_{n2} \\
    \vdots & \vdots & \ddots & \vdots\\
    A_{1n} & A_{2n} & \dots & A_{nn}
   \end{pmatrix}
   $$
   </div>

   * 定理: \\(AA^\*=A^\*A=|A|\cdot E\\)
     推论: \\(|AA^\*|=||A|\cdot E|\rArr|A|\cdot|A^\*|=|A|^n\cdot 1\rArr|A^\*|=|A|^{n-1}\\)
4. 逆矩阵:
   设 \\(n\\) 阶方阵 \\(A\\)、\\(B\\) , 若 \\(AB=BA=E\\) , 则 \\(A^{-1}=B\\)
   1. 注意:
      1. 未必所有方阵均可逆
         零矩阵不可逆 (\\(0B=B0=0\neq E\\))
      2. 若可逆, 则逆矩阵唯一
   2. 定理: \\(|A|\neq 0\hArr A\\) 可逆, \\(A^{-1}=\frac{1}{|A|}A^\*\\)
      证明:
      \\(AA^\*=A^\*A=|A|E\\)
      \\(\hArr\frac{1}{|A|}(AA^\*)=\frac{1}{|A|}(A^\*A)=E\\)
      \\(\hArr A(\frac{1}{|A|}A^\*)=(\frac{1}{|A|}A^\*)A=E\\)
      由定义知, \\(AB=BA=E\\) , \\(A^{-1}=B\\) , 则得证
   3. 求 \\(A^{-1}\\)
      1. 伴随矩阵法: 算出 \\(|A|\\) 和 \\(A^\*\\) , 然后代入 \\(A^{-1}=\frac{1}{|A|}A^\*\\)
      2. 初等变换法(优先这个, 见矩阵初等变换章节)
         例: \\(A+B=AB\\) , 求 \\(A-E\\) 可逆
         (思路, 凑 \\((A-E)\cdot ?=E\\))
         \\(A+B=AB\\)
         \\(\hArr AB-A-B=0\\)
         \\(\hArr AB-A-B+E=E\\)
         \\(\hArr(A-E)B-(A-E)=E\enspace\\) (提公因子 \\(B\\) , 同时 \\(B=EB\\))
         \\(\hArr(A-E)(B-E)=E\\)
         故 \\(A-E\\) 的逆矩阵为 \\(B-E\\)
   4. 逆矩阵性质
      1. 若 \\(A\\)、\\(A^{-1}\\) 可逆, 则 \\((A^{-1})^{-1}=A\\)
      2. 若 \\(A\\)、\\(B\\)、\\(AB\\) 可逆, 则 \\((AB)^{-1}=B^{-1}A^{-1}\\) , \\(AB\cdot B^{-1}A^{-1}=AEA^{-1}=E\\)
      3. 若 \\(A\\)、\\(A^{T}\\) 可逆, 则 \\((A^{T})^{-1}=(A^{-1})^T\\)
      4. 若 \\(k\neq 0\\) , 则 \\((kA)\frac{1}{k}A^{-1}=E\\)
      5. 若 \\(A\\) 可逆, 则 \\(|A^{-1}|=|A|^{-1}\\)
      6. 若 \\(A\\)、\\(A^{\*}\\) 可逆, 则 \\((A^\*)^{-1}=\frac{1}{|A|}A\\)
         证明: 结合 \\(AA^\*=A^\*A=|A|E\\) 和 \\(A^{-1}=\frac{1}{|A|}A^\*\\) 可推导
5. 矩阵方程注意:
   1. 要注意左乘还是右乘
   2. 矩阵不能直接和常数加减乘, 要加个 \\(E\\)
   3. 矩阵不能做分母, 只能用逆矩阵消去
   4. 先判定可逆, 再写逆矩阵

### 分块矩阵

1. 标准型(左上开始一串 0 不间断或全 0. 标准型不一定是方阵)
   <div>
   $$
   \left(\begin{array}{ccc:ccc}
    1 & & & & & \\
    & \ddots & & & & \\
    & & 1 & & & \\ \hdashline
    & & & 0 & & \\
    & & & & \ddots & \\
    & & & & & 0
   \end{array}\right)_{m\times n}
   \xrightarrow{\text{可分块为}}
   \begin{pmatrix}
    E_{r\times r} & 0_{r\times(n-r)} \\
    0_{(m-r)\times r} & 0_{(m-r)\times(n-r)}
   \end{pmatrix}
   $$
   </div>
2. 分块加法 \\(\begin{pmatrix} A_1 & A_2 \\\ A_3 & A_4 \end{pmatrix}+\begin{pmatrix} B_1 & B_2 \\\ B_3 & B_4 \end{pmatrix}=\begin{pmatrix} A_1+B_1 & A_2+B_2 \\\ A_3+B_3 & A_4+B_4 \end{pmatrix}\\)
3. 数乘: \\(k\begin{pmatrix} A_1 & A_2 \\\ A_3 & A_4 \end{pmatrix}=\begin{pmatrix} kA_1 & kA_2 \\\ kA_3 & kA_4 \end{pmatrix}\\)
4. 乘法: \\(\begin{pmatrix} A_1 & A_2 \\\ A_3 & A_4 \end{pmatrix}\times\begin{pmatrix} B_1 & B_2 \\\ B_3 & B_4 \end{pmatrix}=\begin{pmatrix} A_1B_1+A_2B_3 & A_1B_2+A_2B_4 \\\ A_3B_1+A_4B_3 & A_3B_2+A_4B_4 \end{pmatrix}\\)
5. 分块矩阵转置: \\(A=\begin{pmatrix} A_1 & A_2 & A_3 \\\ A_4 & A_5 & A_6\end{pmatrix}\\) , \\(A^T=\begin{pmatrix} A_1^T & A_4^T \\\ A_2^T & A_5^T \\\ A_3^T & A_6^T \end{pmatrix}\\)

### 初等变换

1. 初等行(列)变换(注意矩阵变换用 \\(\to\\) 不能用 \\(=\\))
   1. 交换两行
   2. 用 \\(k(k\neq 0)\\) 乘某一行
   3. 某一行的 \\(l\\) 倍加到另一行
2. 定理: 任何矩阵都可通过初等变换化为标准形
3. 等价: \\(A\\) 经初等变换得到 \\(B\\) , 称 \\(A\cong B\\)
   1. 反射性: \\(A\cong A\\)
   2. 对称性: \\(A\cong B\to B\cong A\\)
   3. 传递性: \\(A\cong B\\) , \\(B\cong C\to A\cong C\\)
   4. 任何矩阵 \\(\cong\\) 标准型
4. 初等方阵: 对 \\(E\\) 做一次初等变换得到的方阵
   1. 交换 \\(i\\)、\\(j\\) 行: \\(E(i,j)\\)
   2. 用 \\(k(k\neq 0)\\) 乘 \\(i\\) 行: \\(E(i(k))\\)
   3. \\(j\\) 行乘 \\(l\\) 倍加到 \\(i\\) 行: \\(E(i,j(l))\\)
   
   初等方阵均可逆, 其逆矩阵也为初等方阵, 初等方阵的转置也是初等方阵.
   \\(E(i,j)^{-1}=E(j,i)\\) , \\(E(i(k))^{-1}=E(i(\frac{1}{k}))\\) , \\(E(i,j(l))^{-1}=E(i,j(-l))\\)

   初等方阵的作用:
   初等方阵左乘 \\(A\\) , 相当于对 \\(A\\) 实施同种行变换;
   初等方阵右乘 \\(A\\) , 相当于对 \\(A\\) 实施同种列变换
   {% asset_img 12.png %}

   定理:
   1. 对于任意矩阵 \\(A\\) , 存在初等矩阵 \\(P1\\)、\\(P_2\dots P_s\\) , \\(Q_1\\)、\\(Q_2\dots Q_t\\)
      使得 \\(P_s\dots P_2P_1\cdot A\cdot Q_1Q_2\cdot Q_t\\) 为标准型(实际上就是任何矩阵都可通过初等变换化为标准形)
      推论: \\(A\\)、\\(B\\) 等价 \\(\hArr\\) 存在可逆矩阵 \\(P\\)、\\(Q\\) 使 \\(PAQ=B\\)
   2. \\(A\\) 可逆 \\(\hArr A\\) 的标准型为 \\(E\\)
   3. \\(A\\) 可逆 \\(A=P_1\dots P_S\\)
5. 初等变换法求逆矩阵(只做行)
   给定 \\(A\\) , 求 \\(A^{-1}\\)
   将 \\((A,E)=\left(\begin{array}{ccc:ccc} 1 & 0 & 1 & 1 & 0 & 0 \\\ 2 & 1 & 0 & 0 & 1 & 0 \\\ -3 & 2 & -5 & 0 & 0 & 1 \end{array}\right)\\)
   经过一系列**初等行变换**后变为 \\((E,A^{-1})\\), 即将前面的矩阵化为 \\(E\\) , 此时后面的矩阵即为 \\(A\\) 的逆矩阵 \\(A^{-1}\\)
   {% asset_img 13.png %}

   注意:
   1. 先处理第 1 列, 再第 2 列
   2. 第 1 列处理完后, 第一行不再拿来用
   3. 只做初等行变换
   4. 不管是否可逆, 若左边无法化为 \\(E\\) , 则 \\(A\\) 不可逆

### 矩阵的秩

1. 秩: 矩阵中非零子式能取到的最高阶数, 记作 \\(r(A)=r\\) , 规定 \\(r(0)=0\\)
   定理:
   * \\(r(A)=r\hArr\\) 有一个 \\(r\\) 阶子式不为零, 所有 \\(r+1\\) 阶子式全为零(用行列式按行展开可证)
   * 初等行(列)变换不改变秩
   
   性质:
   * \\(r(A)=r(A^T)\\)
   * 矩阵乘以可逆方阵, 秩不变:
     设 \\(A_{m\times n}\\) , 可逆方阵 \\(P_m\\)、\\(Q_n\\)
     有 \\(r(A)=r(PA)=r(AQ)=r(PAQ)\\)
     (可逆方阵可表示为一系列初等方阵的乘积, 所以相当于对 \\(A\\) 作初等行(列)变换)
2. 满秩:
   设 \\(A_{m\times n}\\) , 则 \\(0\leqslant r(A)\leqslant\text{min}\\{m,n\\}\\)
   若 \\(r(A)=m\\) , 称为行满秩;
   若 \\(r(A)=n\\) , 称为列满秩
   (行满秩和列满秩统称为满秩)
   若 \\(r(A)<\text{min}\\{m,n\\}\\) , 则叫降秩.
   性质: 设方阵 \\(A_n\\) , \\(A\\) 满秩 \\(\hArr|A|\neq 0\hArr A\\) 可逆
3. 阶梯型: (初等行(列)变换不改变秩, 所以可将矩阵化为阶梯型从而得到矩阵的秩)
   1. 若有零行, 零行在非零行下面.
   2. 阶梯每层左起首个非零元素左边零的个数随行数增加而严格增加.
      (即横线可跨多个数, 竖线只跨一个数)
      {% asset_img 14.png %}
   3. 行简化阶梯型: (行简化阶梯型的秩数=首非零元的数量)
      1. 非零行的首非零元是 1
      2. 首非零元所在列其余元素为 0
      
      {% asset_img 15.png %}

## 向量组

### n 维向量及其运算

1. 向量的定义
   \\(n\\) 个数 \\(a_1\dots a_n\\) 组成的有序数数组 \\((a_1,\dots,a_n)\\) , 常用符号 \\(\alpha,\beta,\gamma\\) 表示
   行向量: \\((a_1,a_2,a_3)\\)
   列向量: \\(\begin{pmatrix} a_1 \\\ a_2 \\\ a_3 \end{pmatrix}\\)
   零向量: 分量全为 0
   负向量: 分量均取相反数
   两向量相等前提: 同维向量(两矩阵相等: 同型矩阵)
   运算律:
   1. \\(\vec{\alpha}+\vec{\beta}=\vec{\beta}+\vec{\alpha}\\)
   2. \\((\vec{\alpha}+\vec{\beta})+\vec{\gamma}=\vec{\alpha}+(\vec{\beta}+\vec{\gamma})\\)
   3. \\(\vec{\alpha}+\vec{0}=\vec{\alpha}\\)
   4. \\(\vec{\alpha}+(-\vec{\alpha})=\vec{0}\\)
   5. \\(1\times\vec{\alpha}=\vec{\alpha}\\)
   6. \\(k(l\vec{\alpha})=(kl)\vec{\alpha}\\)

   性质: \\(k\vec{\alpha}=\vec{0}\hArr k=0\\) 或 \\(\vec{\alpha}=\vec{0}\\) (矩阵中, \\(AB=0\nRightarrow A=0\\) 或 \\(B=0\\))

### 向量间的线性关系

1. 线性组合: \\(\vec{\beta},\vec{\alpha_1},\dots,\vec{\alpha_n}\\) 均为 \\(n\\) 维向量, 若存在 \\(k_1,\dots,k_n\\) , 使得 \\(\vec{\beta}=k_1\vec{\alpha_1}+\dots+k_n\vec{\alpha_n}\\) .
   则称 \\(\vec{\beta}\\) 可用向量组 \\(\\{\vec{\alpha_1}\dots\vec{\alpha_n}\\}\\) 线性表示.
   \\(k_1,\dots,k_n\\) 为组合系数
   性质:
   1. 零向量可由任意向量组表示(\\(\vec{0}=0\times\vec{\alpha_1}+\dots+0\times\vec{\alpha_n}\\))
   2. 向量组中任一向量可由此向量组表示(\\(\vec{\alpha_3}=0\times\vec{\alpha_1}+0\times\vec{\alpha_2}+1\times\vec{\alpha_3}+\dots+0\times\vec{\alpha_n}\\))
   3. 任意向量可由 \\(\vec{\epsilon_1}=(1,0,0,\dots,0),\vec{\epsilon_2}=(0,1,0,\dots,0),\dots,\vec{\epsilon_n}=(0,0,\dots,1)\\) 线性表示(类似于平面向量正交分解)
2. 求组合系数 \\(k_1,\dots,k_n\\)
   例: 有 \\(\vec{\beta}=(-3,2,-4)\\) , 求 \\(\vec{\alpha_1}=(1,0,1)\\)、\\(\vec{\alpha_2}=(2,1,0)\\)、\\(\vec{\alpha_3}=(-1,1,-2)\\) 构成的线性表示
   解:
   列方程组:
   \\(\begin{cases} k_1+2k_2-k_3=-3 \\\ k_2+k_3=2 \\\ k_1-2k_3=-4 \end{cases}\\)
   解得 \\(k_1=2\\) , \\(k_2=-1\\) , \\(k_3=3\\) , 故 \\(\vec{\beta}=2\vec{\alpha_1}-\vec{\alpha_2}+3\vec{\alpha_3}\\)
   (有线性组合 \\(hArr\\) 方程有解)
3. 向量组的等价
   若向量组 \\(\\{\vec{\alpha_1}\dots\vec{\alpha_m}\\}\\) , \\(\\{\vec{\beta_1}\dots\vec{\beta_n}\\}\\) 同维且可相互线性表示,
   则这两个向量组等价, 记作 \\(\\{\vec{\alpha_1}\dots\vec{\alpha_m}\\}\cong\\{\vec{\beta_1}\dots\vec{\beta_n}\\}\\)
   1. 反身性: \\(\\{\vec{\alpha_1}\dots\vec{\alpha_m}\\}\cong\\{\vec{\alpha_1}\dots\vec{\alpha_m}\\}\\)
   2. 对称性: \\(\\{\vec{\alpha_1}\dots\vec{\alpha_m}\\}\cong\\{\vec{\beta_1}\dots\vec{\beta_n}\\}\hArr\\{\vec{\beta_1}\dots\vec{\beta_n}\\}\cong\vec{\alpha_1}\dots\vec{\alpha_m}\\}\\)
   3. 传递性: \\(\\{\vec{\alpha_1}\dots\vec{\alpha_m}\\}\cong\\{\vec{\beta_1}\dots\vec{\beta_n}\\}\\) , \\(\\{\vec{\beta_1}\dots\vec{\beta_n}\\}\cong\\{\vec{\gamma_1}\dots\vec{\gamma_s}\\}\rArr\\{\vec{\alpha_1}\dots\vec{\alpha_n}\\}\cong\\{\vec{\gamma_1}\dots\vec{\gamma_s}\\}\\)

### 线性相关线性无关

1. 线性相关与无关
   \\(\vec{\alpha_1}\dots\vec{\alpha_n}\\) 是 \\(n\\) 个 \\(m\\) 维向量, 若存在一组不全为 0 的组合系数 \\(k_1,\dots,k_n\\) , 使得 \\(k_1\vec{\alpha_1}+\dots+k_n\vec{\alpha_n}=\vec{0}\\) , 称 \\(\vec{\alpha_1},\dots,\vec{\alpha_n}\\) 线性相关
   线性无关:
   1. 不相关即无关
   2. 找不到一组不全为 0 的 \\(k_1,\dots,k_n\\) 使之成立
   3. 式子成立, \\(k_1,\dots,k_n\\) 必全为 0

   结论:
   1. 向量组中两向量成比例, 则此向量组成线性相关
   2. 含零向量的任意向量组必线性相关
   3. 一个向量线性相关当且仅当该向量为零向量
   4. 单个非零向量必线性无关
   5. 存在部分组线性相关 \\(\to\\) 整体组线性相关
      整体组线性无关 \\(\to\\) 所有部分组线性无关
   6. 将线性无关的向量组中每个向量相同位置随意增加一些分量得到的高维向量组仍线性无关.
      向量组线性无关 \\(\to\\) 接长向量组线性无关(列方程可证, 升维只增加了方程组式子的数量, 但原来的式子条件依旧要满足组合系数 \\(k_1=\dots=k_n=0\\))
      向量组线性相关 \\(\to\\) 截短向量组线性相关
   7. \\(n\\) 个 \\(n\\) 维向量构成行列式 \\(D\\)
      若 \\(D\neq 0\hArr\\) 线性无关
      若 \\(D=0\hArr\\) 线性相关
   9. \\(n\\) 维单位向量组 \\(\\{\epsilon_1\dots\epsilon_n\\}\\) 线性无关
   8. 线性相关 \\(\hArr\\) 方程组有非零解
      线性无关 \\(\hArr\\) 方程组只有零解

### 向量组的秩

## 线性方程组

### 线性方程组

### 线性方程组有解判定

### 齐次方程组的解

### 方程组解的结构

## 特征向量与特征值, 相似, 对角化

### 矩阵的特征值与特征向量

### 特征值和特征向量的性质

### 相似矩阵和矩阵可对角化的条件

### 实对称矩阵的对角化

## 二次型

### 二次型定义

### 二次型化标准型(配方法)

###　二次型化标准型(初等变换法和正交替换法)
