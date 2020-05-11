---
title: inequality
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-04-04 19:53:35
tags:
toc: true
---

## 一元二次不等式

分式不等式解法

\\(\\)\begin{aligned}
    &\frac{f(x)}{g(x)} > 0 (<0) \hArr f(x) \cdot g(x) > 0 (<0) \\
    &\frac{f(x)}{g(x)} \geqslant 0 (\leqslant 0) \hArr
    \begin{cases}
        g(x) \neq 0, \\
        f(x) \cdot g(x) \geqslant 0 \, (\leqslant 0)
    \end{cases}
\end{aligned}
\\(\\)

## 二元一次不等式与简单线性规划

### 二元一次不等式表示平面区域

一般地, 直线 \\(y=kx+b\\) 把平面分成两个部分
* \\(y>kx+b\\) 表示直线上方的平面区域;
* \\(y<kx+b\\) 表示直线下方的平面区域;

"选点法": 任选一个不在只显示的点. 若满足不等式, 则该点所在的一侧为不等式所表示的平面区域; 否则, 直线另一侧为不等式表示的平面区域 (若直线不过原点, 通常选择原点带入)

### 简单的线性规划问题

解题思路:
1. 根据题目列出约束条件 (那一堆不等式)
2. 作出目标函数 (题目要求的最大/最小值的东西)
3. 画出可行域图 (将约束条件转成二元一次方程也就是直线, 然后确定每条线规划的平面区域, 它们的重合部分即是满足所有线性要求的区域)
4. 一般来说目标函数的最值在该区域的顶点或边界上取到

## 基本不等式

\\(\sqrt{ab}\leqslant\frac{a+b}{2} \quad (a\geqslant 0, b\geqslant 0)\\) 称为基本不等式

\\(\sqrt{ab}\\) 称为 \\(a, b\\) 的几何平均数; \\(\frac{a+b}{2}\\) 称为 \\(a, b\\) 的算术平均数

推论:
1. \\(a+\frac{1}{a}\geqslant2 \quad (a\geqslant 0)\\) , 当且仅当 \\(a=1\\) 时相等
2. \\(\frac{b}{a}+\frac{a}{b}\geqslant2 \quad (ab>0)\\), \\(\frac{b}{a}+\frac{a}{b}\leqslant-2 \quad (ab<0)\\) , 当且仅当 \\(a=b\\) 时相等
3. \\(a^2+b^2\geqslant2ab\\), 其中 \\(a\in R, b\in R\\) , 当且仅当 \\(a=b\\) 时相等
4. \\(\frac{2}{\frac{1}{a}+\frac{1}{b}}\leqslant\sqrt{ab}\leqslant\sqrt{\frac{a^2+b^2}{2}} \quad (a>0, b>0)\\) , 当且仅当 \\(a=b\\) 时相等
5. \\(4ab\leqslant(a+b)^2\leqslant2(a^2+b^2)\\) , 即 \\(ab\leqslant(\frac{a+b}{2})^2\leqslant\frac{a^2+b^2}{2}\\) , 其中 \\(a\in R, b\in R\\) , 当且仅当 \\(a=b\\) 时相等

基本不等式应用: "一正, 二定, 三相等"
1. 一正 \\((a, b\geqslant 0)\\) 
2. 二定 \\((\sqrt{ab}定, \frac{a+b}{2}有最小值; 反之若后者定, 前者有最大值)\\)
3. 三相等 \\((a=b 时, \sqrt{ab}=\frac{a+b}{2})\\)

## 不等式选讲

### 绝对值不等式

绝对值不等式解法:
\\(\\)
\begin{aligned}
    当 c>0 时,\, &|ax+b|\leqslant c \hArr -c \leqslant ax+b \leqslant c \\
    &|ax+b|\geqslant c \hArr ax+b \leqslant -c \,或\, ax+b \geqslant c
\end{aligned}
\\(\\)

绝对值不等式性质:
1. \\(|a|+|b|\geqslant |a+b|\\)
2. \\(|a|-|b|\leqslant |a+b|\\)
3. \\(|a|-|b|\leqslant |a-b| \leqslant |a|+|b|\\)

### 柯西不等式

1. 柯西不等式的代数形式: 设 \\(a, b, c\\) 均为实数, 则 \\((a^2+b^2)(c^2+d^2)\geqslant(ac+bd)^2\\), 等号当且仅当 \\(ad=bc\\) 时成立.
2. 柯西不等式的向量形式: 设 \\(\alpha,\, \beta\\) 为平面上的两个向量, 则 \\(|\alpha||\beta|\geqslant|\alpha\cdot\beta|\\) , 等号当且仅当 \\(\alpha,\, \beta\\) 共线时成立.
3. 三角形不等式: 设 \\(x_1, y_2; x_2, y_2; x_3, y_3 \in R\\) , 则
   \\(\sqrt{(x_1-x_2)^2+(y_1-y_2)^2}+\sqrt{(x_2-x_3)^2-(y_2-y_3)^2}\geqslant \sqrt{(x_1-x_3)^2+(y_1-y_3)^2}\\)
   几何意义为两边之长大于第三边
4. 柯西不等式可推广为如下一般形式:
   设 \\(n\\) 为大于 1 的自然数, \\(a_i,\, b_i \, (i=1, 2, ..., n)\\) 为实数, 则 \\((a_1^2 + a_2^2 + ... + a_n^2)(b_1^2 + b_2^2 + ... + b_n^2)\geqslant(a_1b_1 + a_2b_2 + ... + a_nb_n)^2\\)

#### 参数配方法讨论柯西不等式一般情形

\\(\\)
\sum_{i=1}^n a_i^2 \cdot \sum_{i=1}^n b_i^2 \geqslant \sum_{i=1}^n (a_ib_i)^2
\\(\\)

### 排序不等式

\\(\\)
设两组实数 a_1, a_2, ..., a_n 与 b_1, b_2, ..., b_n , 且 a_1   \leqslant a_2 \leqslant ... \leqslant a_n, b_1 \leqslant b_2   \leqslant ... \leqslant b_n \\
c_1, c_2, ..., c_n 为 b_1, b_2, ..., b_n 的任意一个排列, \\

则和数 a_1c_1 + a_2c_2 + ... + a_nc_n 在 a_1, a_2, ..., a_n 与b_1,    b_2, ..., b_n 同序时最大, 反序时最小, \\
即 a_1b_1 + a_2b_2 + ... + a_nb_n \geqslant a_1c_1 + a_2c_2 + .. +    a_nc_n \geqslant a_1b_n + a_2b_{n-1} + ... + a_nb_1 \\
等号当且仅当 a_1=a_2=...=a_n 或 b_1=b_2=...=b_n 时成立
\\(\\)

### 伯努利不等式

\\(\\)
\begin{aligned}
    &有实数\, x>-1 \\
    &当 n \geqslant 1,\, &则\, (1+x)^n\geqslant 1+nx \\
    &当 0 \leqslant n \leqslant 1,\, &则\, (1+x)^n \leqslant 1+nx \\
    &当且仅当\, n = 0, 1\,或\, x=0\, 时等号成立
\end{aligned}
\\(\\)

### 数学归纳法

(例)用数学归纳法证明伯努利不等式:
1. 当 \\(n=1\\) 时显然成立 \\(1+x\geqslant 1+x\\)
2. 假设 \\(n=k\\) 时成立, 那么当 \\(n=k+1\\) 时, 由假设:
   \\((1+x)^{k+1}=(1+x)^k(1+x) \underrightarrow{\small 带入 (1+x)^k\geqslant(1+kx)} (1+x)^k(1+x)\geqslant(1+kx)(1+x)\\)
   展开得到:
   \\((1+x)^{k+1}\geqslant kx^2 + 1 + (k+1)x \geqslant 1 + (k+1)x\\)
   所以命题对于 \\(n\in N^+\\) 成立

另请参见章节 \[逻辑\]->推理与证明->数学归纳法
TODO: 补充链接

### 平均值不等式

跟*基本不等式*很像

\\(\\)
若 a_1, a_2, ..., a_n 为正数, 则 \frac{a_1+a_2+...+a_n}{n}\geqslant\sqrt[n]{a_1a_2...a_n} \\
等号当且仅当 a_1=a_2=...=a_n 时成立. \\
\frac{a_1+a_2+...+a_n}{n} 称为算术平均数 \\
\sqrt[n]{a_1a_2...a_n} 称为几何平均数
\\(\\)

这个不等式通常称为 算术-几何平均不等式, 也称平均值不等式

### 证明不等式基本方法

#### 比较法

比较法分比差法/比商法, 
比差法利用基本事实 \\(a-b>0 \hArr a>b\\) ;
比商法利用基本事实 \\(\frac{a}{b}>1 \hArr a>b (其中 a>0, b>0)\\)

#### 综合法

从已知条件出发, 利用不等式的有关性质或定理, 经过推理论证, 最终推导出所要证明的不等式成立.

#### 分析法

从待证不等式出发, 逐步寻求使它成立的充分条件, 直到将待证不等式归结为一个已成立的不等式(已知条件\定理等).

#### 反证法

运用反证法证明不等式, 主要有以下两个步骤:
1. 作出与所证不等式相反的假设;
2. 从条件和假设出发, 应用正确的推理方法, 推出矛盾的结论, 否定假设, 从而证明原不等式成立

#### 放缩法

在证明不等式时, 有时要把所证不等式的一边适当放大或缩小以利于化简, 并使它与不等式的另一边的不等关系更为明显, 从而得出原不等式成立. 这种方法称为放缩法.

\\(\\)
\begin{aligned}
    证明A<B,\, &放大A,\, 有A\leqslant C,\, 且容易证明 C<B \\
    或&缩小B,\, 有B \geqslant C,\, 且容易证明C>A
\end{aligned}
\\(\\)
