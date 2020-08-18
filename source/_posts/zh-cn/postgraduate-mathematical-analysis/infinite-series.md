---
title: infinite-series
lang: zh-cn
category: postgraduate-mathematical-analysis
date: 2020-08-15 17:14:49
tags:
toc: true
---

无穷级数

<!-- more -->

## 常数项级数的概念和性质

1. 定义: 
   设 \\(\{a_n\}\\) 常数列, 称 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 为常数项级数
   \\(S_n=a_1 + a_2 + \dots + a_n\\) 为部分和
   \\(\lim\limits_{n\to\infty}S_n \begin{cases} =A &, 收敛于A 且 S_n=\displaystyle\sum_{n=1}^\infty a_n \\\ 不存在 &, 发散  \end{cases}\\)
2. 常数项级数性质:
   1. \\(\displaystyle\sum_{n=1}^\infty a_n=A , \displaystyle\sum_{n=1}^\infty b_n=B\\) , 则 \\(\begin{cases} \displaystyle\sum_{n=1}^\infty (a_n+b_n)=A+B \\\ \displaystyle\sum_{n=1}^\infty (a_n-b_n)=A-B \end{cases}\\)
   2. \\(\displaystyle\sum_{n=1}^\infty a_n=A\\) , 设 \\(k\in R\\) , 则 \\(\displaystyle\sum_{n=1}^\infty ka_n=kA\\)
   3. 级数中添加、减少、改变有限项, 级数的收敛性质不变
   4. 添加括号后收敛性不降低(即收敛性可能会提高)
      如 \\(S_n=1-1+1-1+\dots\\) 发散
      但 \\(S_n=(1-1)+(1-1)+\dots\\) 收敛于0
   5. 收敛必要条件: 设 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 收敛, 则 \\(\lim\limits_{n\to\infty} a_n=0\\) , <u>反之不对</u>(如[调和级数](#harmonic_series))

Note: (几何级数) \\(\displaystyle\sum_{n=1}^\infty aq^n \begin{cases} |q|\geqslant1 , 发散 \\\ |q|<1 , =\frac{首项}{1-公比} \end{cases}\\) (公式推导参考等比数列)

## 常数项级数的审敛法

TODO: 前章讲过, 属于冗余内容
对\\(\displaystyle\sum_{n=1}^\infty a_n\\) :
1. \\(S_n=a_1+a_2+\dots+a_n\\)
   \\(\lim\limits_{n\to\infty}S_n \begin{cases} =A , S_n=\displaystyle\sum_{n=1}^\infty a_n \\\ 无 , 发散 \end{cases}\\)
2. \\(\lim\limits_{n\to\infty} a_n\neq0 \rArr \displaystyle\sum_{n=1}^\infty a_n\\) 发散

### 正向级数及审敛法

1. 定义: 设 \\(\displaystyle\sum_{n=1}^\infty a_n\\) , 若 \\(\forall n\\) , \\(a_n\geqslant0\\) , 称 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 为正向级数

Note:
\\(S_1\leqslant S_2\leqslant S_3\leqslant\dots\\) , 即 \\(\\{S_n\\}\uarr\\) (表示 \\(S_n\\) 单调递增);
情况1：\\(\\{S_n\\}\\) 无上介 \\(\rArr \lim\limits_{n\to\infty} S_n=+\infty \rArr \displaystyle\sum_{n=1}^\infty a_n\\) 发散
情况2: \\(S_n\leqslant M \rArr \lim\limits_{n\to\infty} S_n\\) 存在 \\(\rArr \displaystyle\sum_{n=1}^\infty a_n\\) 收敛
2. 审敛法
   1. 比较法
      \\(a_n\leqslant b_n\\) 且 \\(\displaystyle\sum_{n=1}^\infty b_n\\) 收敛, 则 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 收敛
      \\(a_n\geqslant b_n\\) 且 \\(\displaystyle\sum_{n=1}^\infty b_n\\) 发散, 则 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 发散
   2. 比较法(极限形式)
      设正项级数 \\(\displaystyle\sum_{n=1}^\infty a_n\\) , \\(\displaystyle\sum_{n=1}^\infty b_n\\)
      若 \\(\lim\limits_{n\to\infty}\dfrac{b_n}{a_n}=l \quad(0<l<+\infty)\\)
      则 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 与 \\(\displaystyle\sum_{n=1}^\infty b_n\\) 敛散性相同
   3. 比值法
      设正项级数 \\(\displaystyle\sum_{n=1}^\infty a_n\\)
      若 \\(\lim\limits_{n\to\infty}\dfrac{a_n+1}{a_n}=P\\)
      则 \\(P<1\\) 时, 级数收敛;
      \\(\mskip{1em} P>1\\) 时, 级数发散.
   4. 根值法
      设正项级数 \\(\displaystyle\sum_{n=1}^\infty a_n\\)
      若 \\(\lim\limits_{n\to\infty}\sqrt[n]{a_n}=P\\)
      则 \\(P<1\\) 时, 级数收敛;
      \\(\mskip{1em} P>1\\) 时, 级数发散.


<span id="harmonic_series"></span>
Notes:
1. \\(\displaystyle\sum_{n=1}^\infty \frac{1}{n^p}\\) 称为 p-级数
   若 \\(p=1\\) , 称 \\(\displaystyle\sum_{n=1}^\infty \frac{1}{n}\\) 为调和级数
2. \\(\displaystyle\sum_{n=1}^\infty \frac{1}{n^p} \begin{cases} p>1 , 收敛 \\\ p\leqslant 1 , 发散 \end{cases}\\) (敛散性使用柯西判别法)

### 交错级数及审敛法

1. 定义
   形如 \\(a_1-a_2+a_3-a_4+\dots\\) 或 \\(-a_1+a_2-a_3+a_4-\dots \quad(\forall n, a_n\geqslant0)\\)
   即 \\(\displaystyle\sum_{n=1}^\infty (-1)^{n-1}a_n\\) 或 \\(\displaystyle\sum_{n=1}^\infty (-1)^n a_n \quad(\forall n, a_n\geqslant0)\\)
2. 审敛性
   1. 莱布尼茨法
      对 \\(\displaystyle\sum_{n=1}^\infty (-1)^{n-1}a_n \quad(\forall n, a_n\geqslant0)\\)
      若\\(\\{a_n\\}\darr\\) 且 \\(\lim\limits_{n\to\infty}a_n=0\\)
      则 \\(\displaystyle\sum_{n=1}^\infty (-1)^{n-1}a_n\\) 收敛, 且 \\(S\leqslant a_1\\)

### 绝对收敛与条件收敛

0. 取绝对值(提高发散性): \\(\displaystyle\sum_{n=1}^\infty a_n \rarr \displaystyle\sum_{n=1}^\infty |a_n|\\)
1. 定义
   1. 当 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 收敛, 而 \\(\displaystyle\sum_{n=1}^\infty |a_n|\\) 发散, 称 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 条件收敛
      如 \\(\displaystyle\sum_{n=1}^\infty \dfrac{(-1)^{n-1}}{n}=1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\dots\\) 收敛
      但 \\(\displaystyle\sum_{n=1}^\infty |\dfrac{(-1)^{n-1}}{n}|=\displaystyle\sum_{n=1}^\infty \frac{1}{n}\\) 发散 (原因见p-级数)
   2. 当 \\(\displaystyle\sum_{n=1}^\infty |a_n|\\) 收敛, 称 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 绝对收敛
2. 结论
   若 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 绝对收敛 (即 \\(\displaystyle\sum_{n=1}^\infty |a_n|\\) 收敛), 则 \\(\displaystyle\sum_{n=1}^\infty a_n\\) 收敛

## 幂级数的概念与分析性质

## 函数展开成幂级数

## 函数的幂级数展开式的应用

## 函数项级数的一致收敛性及一致收敛级数的基本性质

## 傅里叶级数

## 一般周期函数的傅里叶级数