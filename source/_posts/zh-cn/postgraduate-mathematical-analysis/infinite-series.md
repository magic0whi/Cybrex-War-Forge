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
      (这里拓展了一下, 和 \\(\lim\limits_{n\to\infty}|\dfrac{a_{n+1}}{a_n}|\\) 是一样的)
      若 \\(\lim\limits_{n\to\infty}\dfrac{a_{n+1}}{a_n}=P\\)
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
2. \\(\displaystyle\sum_{n=1}^\infty \frac{1}{n^p} \begin{cases} p>1 , 收敛 \\\ p\leqslant 1 , 发散 \end{cases}\\) (敛散性使用根值法)

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

### 函数项级数的概念

\\(\\{u_n(x)\\}\\) 为函数列, \\(\displaystyle\sum_{n=1}^\infty u_n(x)\\) 称为函数项级数.
对 \\(\displaystyle\sum_{n=1}^\infty u_n(x)\\)
当 \\(x=x_0\\) 时, \\(\displaystyle\sum_{n=1}^\infty u_n(x_0)\\) 收敛, \\(x=x_0\\) 称为 \\(\displaystyle\sum_{n=1}^\infty u_n(x)\\) 收敛点
当 \\(x=x_1\\) 时, \\(\displaystyle\sum_{n=1}^\infty u_n(x_1)\\) 发散, \\(x=x_1\\) 称为 \\(\displaystyle\sum_{n=1}^\infty u_n(x)\\) 发散点
\\(\displaystyle\sum_{n=1}^\infty u_n(x)\\) 的一切收敛点而成的集合称为 \\(\displaystyle\sum_{n=1}^\infty u_n(x)\\) 的收敛域, 记为 \\(D\\)
\\(\forall x\in D , \displaystyle\sum_{n=1}^\infty u_n(x)=S(x)\\) (S(x) 称为和函数)

举个例子, 如 \\(x+x^2+x^3+x^4+\dots=\displaystyle\sum_{n=1}^\infty x^n\\)
当 \\(x=\dfrac{2}{3}\\) 时, \\(\displaystyle\sum_{n=1}^\infty (\dfrac{2}{3})^n\\) 收敛, \\(x=\dfrac{2}{3}\\) 称为 \\(\displaystyle\sum_{n=1}^\infty x^n\\) 的收敛点;
当 \\(x=2\\) 时, \\(\displaystyle\sum_{n=1}^\infty 2^n\\) 发散, \\(x=2\\) 称为 \\(\displaystyle\sum_{n=1}^\infty x^n\\) 的发散点;

### 幂级数概念与基本定理

1. 定义:
   形如 \\(\displaystyle\sum_{n=0}^\infty a_n x^n=a_0+a_1x+a_2x^2+\dots\\)
   或 \\(\displaystyle\sum_{n=0}^\infty a_n(x-x_0)^n=a_0+a_1(x-x_0)+a_2(x-x_0)^2+\dots\\)
   称为幂级数
2. 基本定理(abel定理)
   对 \\(\displaystyle\sum_{n=0}^\infty a_n x^n\\)
   1. 当 \\(x=x_0 (\neq0)\\) 时, \\(\displaystyle\sum_{n=0}^\infty a_n x_0^n\\) 收敛. 则当 \\(|x|<|x_0|\\) 时, \\(\displaystyle\sum_{n=0}^\infty a_n x^n\\) 绝对收敛;
   2. 当 \\(x=x_1\\) 时, \\(\displaystyle\sum_{n=0}^\infty a_n x_1^n\\) 发散. 则当 \\(|x|<|x_1|\\) 时, \\(\displaystyle\sum_{n=0}^\infty a_n x^n\\) 发散;

### 收敛半径与收敛域

收敛域 \\(D\in(-R, +R)\\)

收敛半径 \\(R\\) 的求法:
对 \\(\displaystyle\sum_{n=0}^\infty a_n x^n\\)
1. 定理1
   设 \\(\lim\limits_{n\to\infty}|\dfrac{a_{n+1}}{a_n}|=\rho \quad\begin{cases} 1. &\rho=0 &\rArr R=+\infty \\\ 2. &\rho=+\infty &\rArr R=0 \\\ 3. &0<\rho<+\infty &\rArr R=\dfrac{1}{\rho} \end{cases}\\)
2. 定理2
   设 \\(\lim\limits_{n\to\infty}\sqrt[n]{|a_n|}=\rho \quad\begin{cases} 1. &\rho=0 &\rArr R=+\infty \\\ 2. &\rho=+\infty &\rArr R=0 \\\ 3. &0<\rho<+\infty &\rArr R=\dfrac{1}{\rho} \end{cases}\\)

(原理: \\(x^n\\) 这边抵消级数 \\(a_n\\) 带来的收敛/发散影响)

Note:
对 \\(\displaystyle\sum_{n=0}^\infty a_n x^{2n+1}=a_0x+a_1x^3+a_2x^5+\dots\\)
\\(\lim\limits_{n\to\infty}|\dfrac{a_{n+1}}{a_n}|=\rho \quad\begin{cases} 1. &\rho=0 &\rArr R=+\infty \\\ 2. &\rho=+\infty &\rArr R=0 \\\ 3. &0<\rho<+\infty &\rArr R=\sqrt{\dfrac{1}{\rho}} \end{cases}\\)

### 幂级数和函数的分析性质

设 \\(\displaystyle\sum_{n=0}^\infty a_n x^n\\) 的和函数为 \\(S(x)\\)
1. 定理1
   \\(\displaystyle\sum_{n=0}^\infty a_n x^n\\) 的和函数 \\(S(x)\\) 在其收敛域上可积
   则 \\(\int_0^x S(x)dx=\int_0^x (\displaystyle\sum_{n=0}^\infty a_n x^n)dx=\displaystyle\sum_{n=0}^\infty\int_0^x a_nx^ndx=\displaystyle\sum_{n=0}^\infty\dfrac{a_n}{n+1}x^{n+1}\\)
   且 \\(\displaystyle\sum_{n=0}^\infty a_n x^n\\) 与 \\(\displaystyle\sum_{n=0}^\infty \dfrac{a_n}{n+1}x^{n+1}\\) 收敛半径相同(逐项可积性)
2. 定理2
   \\(\displaystyle\sum_{n=0}^\infty a_n x^n\\) 的和函数 \\(S(x)\\) 在其收敛域上可积
   则 \\((\displaystyle\sum_{n=0}^\infty a_n x^n)'=\displaystyle\sum_{n=0}^\infty (a_n x^n)'=\displaystyle\sum_{n=1}^\infty n a_n x^{n-1}\\)
   且 \\(\displaystyle\sum_{n=0}^\infty a_n x^n\\) 与 \\(\displaystyle\sum_{n=1}^\infty n a_n x^{n-1}\\) 收敛半径相同(逐项可导性)

## 函数展开成幂级数



## 函数的幂级数展开式的应用

## 函数项级数的一致收敛性及一致收敛级数的基本性质

## 傅里叶级数

## 一般周期函数的傅里叶级数