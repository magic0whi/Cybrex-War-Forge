---
title: mit-linear-algebra-18.06
toc: true
category: mathematics
lang: zh-cn
date: 2021-02-23 14:18:32
tags:
---

线性代数修正

<!-- more -->

## 列空间和零空间

设矩阵 \\(A_{m\times n}\\)、\\(x_{n\times 1}\\)、\\(b_{m\times 1}\\) , 有
<div>
$$
Ax=b\hArr\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1(n-1)} & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2(n-1)} & a_{2n} \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{m(n-1)} & a_{mn}
\end{bmatrix}
\cdot\begin{bmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{n-1} \\
x_{n}
\end{bmatrix}
=\begin{bmatrix}
b_{1} \\
b_{2} \\
\vdots \\
b_{m}
\end{bmatrix}
$$
</div>

列空间: \\(A\\) 的列向量生成的子空间称为 \\(A\\) 的列空间, 记作 \\(\operatorname{C}(A)\\)
零空间: \\(A\\) 的零空间(null space)是 \\(Ax=0\\) 的解的集合, 记作 \\(\operatorname{N}(A)\\)
\\(Ax=b\\) 有非零解当且仅当 \\(b\subset \operatorname{C}(A)\\)

## 求解 Ax=0, 主变量, 特解

例: \\(A_{3\times 4}=\begin{bmatrix} 1 & 2 & 2 & 2 \\\ 2 & 4 & 6 & 8 \\\ 3 & 6 & 8 & 10 \end{bmatrix}\\) , 求 \\(Ax=0\\) 的特解:
1. 找出主变量(pivot variable):
   <div>
   $$
   A=\begin{bmatrix}
   1 & 2 & 2 & 2 \\
   2 & 4 & 6 & 8 \\
   3 & 6 & 8 & 10
   \end{bmatrix}
   \underrightarrow{\text{消元}}
   \begin{bmatrix}
   \underline{1} & 2 & 2 & 2 \\
   0 & 0 & \underline{2} & 4 \\
   0 & 0 & 0 & 0 \\
   \end{bmatrix}
   =U
   $$
   </div>

   主变量(下划线元素)的个数为 2, 则矩阵的秩 \\(\operatorname{rank}(A)=2\\)
   主变量所在的列称为主列, 其余列为自由列, 自由列中的变量称为自由变量, 自由变量个数 \\(n-r=4-2=2\\)
2. 通常给自由变量赋值为 0 或 1, 去求主列变量的值,
   如令 \\(x_2=1\\)、\\(x_4=0\\) 求得特解 \\(x=c_1\begin{bmatrix} -2 \\\ 1 \\\ 0 \\\ 0 \end{bmatrix}\\)
   再令 \\(x_2=0\\)、\\(x_4=1\\) 求得特解 \\(x=c_2\begin{bmatrix} 2 \\\ 0 \\\ -2 \\\ 1 \end{bmatrix}\\)
3. 矩阵 \\(U\\) 还能进一步化为简化行阶梯形矩阵矩阵 \\(R\\) (Reduced row echelon form):
   <div>
   $$
   U=\begin{bmatrix}
   \underline{1} & 2 & 2 & 2 \\
   0 & 0 & \underline{2} & 4 \\
   0 & 0 & 0 & 0 \\
   \end{bmatrix}
   \underrightarrow{\text{化简}}
   \begin{bmatrix}
   \underline{1} & 2 & 0 & -2 \\
   0 & 0 & \underline{1} & 2 \\
   0 & 0 & 0 & 0 \\
   \end{bmatrix}
   =R
   $$
   </div>

   在简化行阶梯形式中，主元上下的元素都是 0
   <div>
   $$
   R=\begin{bmatrix}
   \underline{1} & 2 & 0 & -2 \\
   0 & 0 & \underline{1} & 2 \\
   0 & 0 & 0 & 0
   \end{bmatrix}
   \underrightarrow{\text{列交换}}
   \left[
   \begin{array}{cc|cc}
   1 & 0 & 2 & -2 \\
   0 & 1 & 0 & 2 \\
   \hline
   0 & 0 & 0 & 0
   \end{array}
   \right]
   =\begin{bmatrix}
   I & F \\
   0 & 0
   \end{bmatrix}
   $$
   </div>
   
   其中 \\(I\\) 为单位矩阵(Identity), \\(F\\) 为自由变量矩阵(Free)
   性质: \\(\begin{bmatrix} I & F\end{bmatrix}\begin{bmatrix} x_{\text{pivot}} \\\ x_{\text{free}} \end{bmatrix}=0 \hArr x_{\text{pivot}}=-Fx_{\text{free}}\\)
   零空间矩阵(nullspace matrix): \\(N=\begin{bmatrix} -F \\\ I \end{bmatrix}\\)

   本例中 \\(N=\begin{bmatrix} -2 & 2 \\\ 0 & -2 \\\ 1 & 0 \\\ 0 & 1 \\\ \end{bmatrix}\\) , 可对比一下上面的两个特解

## 求解 Ax=b: 可解性和解的结构

例: (同上一讲) \\(A_{3\times 4}=\begin{bmatrix} 1 & 2 & 2 & 2 \\\ 2 & 4 & 6 & 8 \\\ 3 & 6 & 8 & 10 \end{bmatrix}\\) , 求 \\(Ax=b\\) 的特解
1. 写出其增广矩阵(augumented matrix) \\(\left[\begin{array}{c|c} A & b \end{array}\right]\\)
   <div>
   $$
   \left[
   \begin{array}{cccc|c}
   1 & 2 & 2 & 2 & b_1 \\
   2 & 4 & 6 & 8 & b_2 \\
   3 & 6 & 8 & 10 & b_3
   \end{array}
   \right]
   \underrightarrow{\text{消元}}
   \left[
   \begin{array}{cccc|c}
   1 & 2 & 2 & 2 & b_1 \\
   0 & 0 & 2 & 4 & b_2-2b_1 \\
   0 & 0 & 0 & 0 & b_3-b_2-b_1
   \end{array}
   \right]
   $$
   </div>

   讨论: \\(Ax=b\\) 有解的条件:
   * \\(b\subset \operatorname{C}(A)\\)
   * 若各行线性组合得到全零行, 则 \\(b\\) 端分量做同样线性组合, 结果也为零时, 方程有解
2. 令所有自由变量取 0, 则有 \\(\begin{cases} x_1+2x_3=1 \\\ 2x_3=3 \end{cases}\\) , 解得 \\(\begin{cases} x_1=-2 \\\ x_3=\frac{3}{2} \end{cases}\\) , 代入 \\(Ax=b\\) 求得特解 \\(x_p=\begin{bmatrix} -2 \\\ 0 \\\ \frac{3}{2} \\\ 0 \end{bmatrix}\\)
   基于 \\(\begin{cases} Ax_p=b \\\ Ax_n=0 \end{cases}\underrightarrow{\text{两式相加}}A(x_p+x_n)=b\\)
   有通解 \\(x_{\text{complete}}=\begin{bmatrix} -2 \\\ 0 \\\ \frac{3}{2} \\\ 0 \end{bmatrix} + c_1\begin{bmatrix} -2 \\\ 1 \\\ 0 \\\ 0 \end{bmatrix} + c_2\begin{bmatrix} 2 \\\ 0 \\\ -2 \\\ 1 \end{bmatrix}\\)
3. 对于 \\(A_{m\times n}\\) , 秩 \\(r\leqslant\operatorname{min}(m,n)\\)
4. 列满秩(\\(r=n<m\\)): \\(A=\begin{bmatrix} 1 & 3 \\\ 2 & 1 \\\ 6 & 1 \\\ 5 & 1 \end{bmatrix}\\) , \\(\operatorname{rank}(A)=2\\)
   要使 \\(Ax=b\enspace\\) (\\(m\\) 维列向量 \\(b\neq 0\\)) 有非零解, \\(b\\) 必须取 \\(A\\) 中各列的线性组合(即 \\(b\subset R^n\\))
   此时 \\(A\\) 的零空间中只有零向量
5. 行满秩(\\(r=m<n\\)): \\(A=\begin{bmatrix} 1 & 2 & 6 & 5 \\\ 3 & 1 & 1 & 1 \end{bmatrix}\\) , \\(\operatorname{rank}(A)=2\\)
   \\(\forall b\in R^m\\) 都为 \\(x\neq 0\\) 的解, 因为此时 \\(A\\) 的列空间为 \\(R^m\\) , \\(m\\) 维列向量 \\(b\in R^m\\) 恒成立
   组成 \\(A\\) 的自由变量有 \\(n-r\\) 个
6. 行列满秩(\\(r=m=n\\)): \\(A=\begin{bmatrix} 1 & 2 \\\ 3 & 4 \end{bmatrix}\\) , 则 \\(A\\) 最终可化简为 \\(R=I\\)
   其零空间只有零向量

总结:
<div>
$$
\begin{array}{c|c|c|c}
r=m=n & r=n\lt m & r=m\lt n & r\lt m,r\lt n \\
R=I & R=\begin{bmatrix} I \\ 0 \end{bmatrix} & R=\begin{bmatrix} I & F \end{bmatrix} & R=\begin{bmatrix} I & F \\ 0 & 0 \end{bmatrix} \\
1\ \text{solution} & 0\ \text{or}\ 1\ \text{solution} & \infty\ \text{solution} & 0\ \text{or}\ \infty\ \text{solution}
\end{array}
$$
</div>

## 线性相关性、基、维数

矩阵 \\(A_{m\times n}\\) 有列向量 \\(v_1,\dots,v_n\\)
若 \\(A\\) 的零空间有且仅有零向量, 则各列向量线性无关, \\(\operatorname{rank}(A)=n\\)
若存在非零向量 \\(c\\) 使 \\(Ac=0\\) , 则存在线性相关列向量, \\(\operatorname{rank}(A)<n\\)
向量空间的一组基向量具有两个性质: 相互线性无关, 可以生成该向量空间

对于向量空间 \\(R^n\\) , 如果 \\(n\\) 个向量组成的矩阵可逆, 则这 \\(n\\) 个向量为空间的一组基, 该空间的维数为 \\(n\\)
如 \\(A=\begin{bmatrix} 1 & 2 & 3 & 1 \\\ 1 & 1 & 2 & 1 \\\ 1 & 2 & 3 & 1 \end{bmatrix}\\) , 第一列和第四列线性相关, 其零空间有非零向量,
所以 \\(\operatorname{rank}(A)=2=\\) 主元存在列数 \\(=\\) 列空间维数
可以很容易地求得 \\(Ax=0\\) 的两个解, 如 \\(x_1=\begin{bmatrix} -1 \\\ -1 \\\ 1 \\\ 0 \end{bmatrix}\\)、\\(x_2=\begin{bmatrix} -1 \\\ 0 \\\ 0 \\\ 1 \end{bmatrix}\\)
所以 \\(n-\operatorname{rank}(A)=2=\\) 自由变量存在的列数 \\(=\\) 零空间维数(特解的个数就是自由变量的个数)
因此得到: 列空间维数 \\(\text{dim}\operatorname{C}(A)=\operatorname{rank}(A)\\) , 零空间维数 \\(\text{dim}\operatorname{N}(A)=n-\operatorname{rank}(A)\\)

## 四个基本子空间

例1: 对于行空间 \\(A=\begin{bmatrix} 1 & 2 & 3 & 1 \\\ 1 & 1 & 2 & 1 \\\ 1 & 2 & 3 & 1 \end{bmatrix}\underrightarrow{\text{消元、化简}}\begin{bmatrix} 1 & 0 & 1 & 1 \\\ 0 & 1 & 1 & 0 \\\ 0 & 0 & 0 & 0 \end{bmatrix}\\)
由于做了行变换, 所以 \\(A\\) 的列空间受到影响(显然 \\(\begin{bmatrix} 1 \\\ 1 \\\ 1 \end{bmatrix}\\) 在 A 的列空间中但不在 R 的列空间中), 即 \\(\operatorname{C}\(R\)\neq\operatorname{C}(A)\\) ,
而行变换并不影响行空间, 所以可在 \\(R\\) 中看出前两行就是行空间的一组基

所以可得出无论对于 \\(A\\) 还是 \\(R\\) , 其行空间的一组基可由 \\(R\\) 矩阵的前 \\(r\\) 行向量组成

例2: 例1中的矩阵符合左零空间(\\(A\\) 转置的零空间)
对于左零空间, 有 \\(A^Ty=0\rArr(A^Ty)^T=0^T\rArr y^TA=0^T\\)
采用 Gauss-Jordan 消元, 将增广矩阵 \\(\left[\begin{array}{c|c} A_{m\times n} & I_{m\times m} \end{array}\right]\\) 中 \\(A\\) 简化为行阶梯形式 \\(\left[\begin{array}{c|c} R_{m\times n} & E_{m\times m} \end{array}\right]\\) . 此时矩阵 \\(E\\) 会将所有的行变换记录下来, 即 \\(EA=R\\)
而当 \\(A\\) 是 \\(m\\) 阶可逆方阵时, \\(R\\) 即是 \\(I\\) (可逆方阵可最终化简为 \\(I\\)), 则 \\(EA=I=A^{-1}A\rArr E=A^{-1}\\)
本例中
<div>
$$
\left[\begin{array}{c|c} A_{m\times n} & I_{m\times m} \end{array}\right]
=\left[\begin{array}{cccc|ccc}
1 & 2 & 3 & 1 & 1 & 0 & 0 \\
1 & 1 & 2 & 1 & 0 & 1 & 0 \\
1 & 2 & 3 & 1 & 0 & 0 & 1
\end{array}\right]
\underrightarrow{\text{消元、化简}} \\
\left[\begin{array}{cccc|ccc}
1 & 0 & 1 & 1 & -1 & 2 & 0 \\
0 & 1 & 1 & 0 & 1 & -1 & 0 \\
0 & 0 & 0 & 0 & -1 & 0 & 1
\end{array}\right]
=\left[\begin{array}{c|c} R_{m\times n} & I_{m\times m} \end{array}\right]
$$
</div>

则
<div>
$$
EA=R\hArr
\begin{bmatrix}
-1 & 2  & 0 \\
1  & -1 & 0 \\
-1 & 0  & 1
\end{bmatrix}
\cdot\begin{bmatrix}
1 & 2 & 3 & 1 \\
1 & 1 & 2 & 1 \\
1 & 2 & 3 & 1
\end{bmatrix}
=\begin{bmatrix}
1 & 0 & 1 & 1 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 0
\end{bmatrix}
$$
</div>

左零空间的维数 \\(m-r\\) 即 \\(3-2=1\\) , 意味着只有一个基向量, 它就是 \\(E\\) 的最后一行
很明显, \\(E\\) 的最后一行对 \\(A\\) 的行做线性组合后, 得到 \\(R\\) 的最后一行, 即零向量,

设 \\(A_{m\times n}\\) , 秩 \\(r=\operatorname{rank}(A)\\)
* 行空间 \\(\operatorname{C}(A^T)\in\mathbb{R}^n\\) , \\(\text{dim}\operatorname{C}(A^T)=r\\) (基见例1)
* 零空间 \\(\operatorname{N}(A)\in\mathbb{R}^n\\) , \\(\text{dim}\operatorname{N}(A)=n-r\\) (自由元所在的列组成零空间的基)
* 列空间 \\(\operatorname{C}(A)\in\mathbb{R}^m\\) , \\(\text{dim}\operatorname{C}(A)=r\\) (主元所在的列组成列空间的一组基)
* 左零空间(\\(A\\) 转置的零空间) \\(\operatorname{N}(A^T)\in\mathbb{R}^m\\) , \\(\text{dim}\operatorname{N}(A^T)=m-r\\) (基见例2)

最后, 引入矩阵空间的概念, 矩阵可以同向量一样做求和、数乘
举例, 设所有 \\(3\times 3\\) 矩阵组成的矩阵空间 \\(M\\)
观察一下对角矩阵, 如果取 \\(\begin{bmatrix} 1 & 0 & 0 \\\ 0 & 0 & 0 \\\ 0 & 0 & 0 \end{bmatrix}\\)、\\(\begin{bmatrix} 1 & 0 & 0 \\\ 0 & 3 & 0 \\\ 0 & 0 & 0 \end{bmatrix}\\)、\\(\begin{bmatrix} 0 & 0 & 0 \\\ 0 & 0 & 0 \\\ 0 & 0 & 7 \end{bmatrix}\\) 可以发现, 任何三阶矩阵对角矩阵均可用这三个矩阵的线性组合生成, 因此他们生成了三阶对角矩阵, 即这三个矩阵是三阶对焦矩阵的一组基

## 矩阵空间、秩 1 矩阵和小世界图

1. 矩阵空间
   接上一讲, 使用 \\(3\times 3\\) 矩阵举例, 其矩阵空间记为 \\(M\\)
   则 \\(M\\) 的一组基为:
   <div>
   $$
   \begin{bmatrix}
   1 & 0 & 0 \\
   0 & 0 & 0 \\
   0 & 0 & 0
   \end{bmatrix}
   \begin{bmatrix}
   0 & 1 & 0 \\
   0 & 0 & 0 \\
   0 & 0 & 0
   \end{bmatrix}
   \begin{bmatrix}
   0 & 0 & 1 \\
   0 & 0 & 0 \\
   0 & 0 & 0
   \end{bmatrix}
   \\
   \begin{bmatrix}
   0 & 0 & 0 \\
   1 & 0 & 0 \\
   0 & 0 & 0
   \end{bmatrix}
   \begin{bmatrix}
   0 & 0 & 0 \\
   0 & 1 & 0 \\
   0 & 0 & 0
   \end{bmatrix}
   \begin{bmatrix}
   0 & 0 & 0 \\
   0 & 0 & 1 \\
   0 & 0 & 0
   \end{bmatrix}
   \\
   \begin{bmatrix}
   0 & 0 & 0 \\
   0 & 0 & 0 \\
   1 & 0 & 0
   \end{bmatrix}
   \begin{bmatrix}
   0 & 0 & 0 \\
   0 & 0 & 0 \\
   0 & 1 & 0
   \end{bmatrix}
   \begin{bmatrix}
   0 & 0 & 0 \\
   0 & 0 & 0 \\
   0 & 0 & 1
   \end{bmatrix}
   $$
   </div>
   
   易得, \\(\text{dim}M=9\\)
   三阶对称矩阵空间有 \\(\text{dim}S=6\\) (因为对称矩阵能够对角化)、上三角矩阵空间有 \\(\text{dim}U=6\\)、对角矩阵空间有 \\(\text{dim}D=3\\)
   求并(intersect): \\(S\cup U=M\\) , \\(\text{dim}(S\cup U)=9\\)
   求交(sum): \\(S\cap U=M\\) , \\(\text{dim}(S\cap U)=3\\)
   \\(\text{dim}S+\text{dim}U=12=\text{dim}(S\cup U)+\text{dim}(S\cap U)\\)