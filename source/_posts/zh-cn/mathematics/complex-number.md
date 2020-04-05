---
title: complex_number
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-04-04 19:57:21
tags:
---

## 复数概念

$$
复数
\begin{cases}
    实数
    \begin{cases}
        有理数 \\
        无理数
    \end{cases} \\
    虚数
    \begin{cases}
        纯虚数 \\
        非纯虚数
    \end{cases}
\end{cases}
$$

形如 $a+bi (a, b \in R)$ 的数叫做复数, $i$ 叫做复数单位

当 $a=0$ 且 $b\neq0$ 时. 叫做纯虚数.

虚数 $i$ 的周期性:
$$
\begin{aligned}
    &i^{4n+1}=i \\
    &i^{4n+2}=-1 \\
    &i^{4n+3}=-i \\
    &i^{4n}=1 \\
    T为4
\end{aligned}
$$

共轭复数: 一般地, 当两个复数的实部相等, 虚部互为相反数时, 这两个复数互为共轭复数; 虚部不等于O的两个共轭复数也叫做共轭虚数.

## 复数四则运算

复数的乘法运算 $(a+bi)(c+di)=ac+adi+bci+bdi^2=(ac-bd)+(ad+bc)i$
复数的除法运算 $(a+bi)\div(c+di)=\frac{a+bi}{c+di}=\frac{(a+bi)(c-di)}{(c+di)(c-di)}=\frac{ac+bd}{c^2-d^2}+\frac{bc-ad}{c^2-d^2}i$

有复数 $Z=a+bi \, (a,b \in R)$ 对应复平面上的点$Z$. 则 $Z(a, b)$ 到原点距离为 $\sqrt{a^2+b^2}$ , 复数 $|Z|=|\vec{OZ}|=\sqrt{a^2+b^2}$