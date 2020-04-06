---
title: inequality
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-04-04 19:53:35
tags:
---

## 一元二次不等式

分式不等式解法

$$\begin{aligned}
    &\frac{f(x)}{g(x)} > 0 (<0) \hArr f(x) \cdot g(x) > 0 (<0) \\
    &\frac{f(x)}{g(x)} \geqslant 0 (\leqslant 0) \hArr
    \begin{cases}
        g(x) \neq 0, \\
        f(x) \cdot g(x) \geqslant 0 \, (\leqslant 0)
    \end{cases}
\end{aligned}
$$

## 二元一次不等式与简单线性规划

### 二元一次不等式表示平面区域

一般地, 直线 $y=kx+b$ 把平面分成两个部分
* $y>kx+b$ 表示直线上方的平面区域;
* $y<kx+b$ 表示直线下方的平面区域;

"选点法": 任选一个不在只显示的点. 若满足不等式, 则该点所在的一侧为不等式所表示的平面区域; 否则, 直线另一侧为不等式表示的平面区域 (若直线不过原点, 通常选择原点带入)

### 简单的线性规划问题

解题思路:
1. 根据题目列出约束条件 (那一堆不等式)
2. 作出目标函数 (题目要求的最大/最小值的东西)
3. 画出可行域图 (将约束条件转成二元一次方程也就是直线, 然后确定每条线规划的平面区域, 它们的重合部分即是满足所有线性要求的区域)
4. 一般来说目标函数的最值在该区域的顶点或边界上取到

## 基本不等式

$\sqrt{ab}\leqslant\frac{a+b}{2} \quad (a\geqslant 0, b\geqslant 0)$ 称为基本不等式

$\sqrt{ab}$ 称为 $a, b$ 的几何平均数; $\frac{a+b}{2}$ 称为 $a, b$ 的算术平均数

推论:
1. $a+\frac{1}{a}\geqslant2 \quad (a\geqslant 0)$ , 当且仅当 $a=1$ 时相等
2. $\frac{b}{a}+\frac{a}{b}\geqslant2 \quad (ab>0)$, $\frac{b}{a}+\frac{a}{b}\leqslant-2 \quad (ab<0)$ , 当且仅当 $a=b$ 时相等
3. $a^2+b^2\geqslant2ab$, 其中 $a\in R, b\in R$ , 当且仅当 $a=b$ 时相等
4. $\frac{2}{\frac{1}{a}+\frac{1}{b}}\leqslant\sqrt{ab}\leqslant\sqrt{\frac{a^2+b^2}{2}} \quad (a>0, b>0)$ , 当且仅当 $a=b$ 时相等
5. $4ab\leqslant(a+b)^2\leqslant2(a^2+b^2)$ , 即 $ab\leqslant(\frac{a+b}{2})^2\leqslant\frac{a^2+b^2}{2}$ , 其中 $a\in R, b\in R$ , 当且仅当 $a=b$ 时相等

基本不等式应用: "一正, 二定, 三相等"
1. 一正 $(a, b\geqslant 0)$ 
2. 二定 $(\sqrt{ab}定, \frac{a+b}{2}有最小值; 反之若后者定, 前者有最大值)$
3. 三相等 $(a=b 时, \sqrt{ab}=\frac{a+b}{2})$

## 不等式选讲

### 绝对值的几何意义

### 柯西不等式

#### 参数配方法讨论柯西不等式一般情形

### 向量递归法讨论排序不等式

### 数学归纳法

### 伯努利不等式

### 平均值不等式

### 证明不等式基本方法

#### 比较法

#### 综合法

#### 分析法

#### 反证法

#### 放缩法