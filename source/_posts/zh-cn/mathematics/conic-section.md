---
title: conic-section
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-03-26 16:51:46
tags:
---

TODO参考书本重新排版

## 圆锥曲线

### 椭圆
椭圆第二定义: 平面内到定点(焦点)的距离与到定直线(准线)距离之比为常数(离心率)的点的轨叫椭圆. 

椭圆的标准方程:
$$\begin{aligned}
    &\frac{x^2}{a^2}+\frac{y^2}{b^2}=1 \qquad (a>b>0) \qquad 此时焦点在x轴 \quad(分母大的焦点就在哪个轴)\\
    &\frac{y^2}{a^2}+\frac{x^2}{b^2}=1 \qquad (a>b>0) \qquad 此时焦点在y轴 \\
    &a^2=b^2+c^2 \quad 离心率为e=\frac{c}{a} \quad (0<e<1) \\
    &e越大, 椭圆越扁\\
    &e越小, 椭圆越接近于圆
\end{aligned}
$$

椭圆准线方程: $x=\pm \frac{a^2}{c}$ 或 $y=\pm \frac{a^2}{c}$
$\star$ 当椭圆焦点不确定在哪个轴上时可设该方程为 $mx^2+ny^2=1 (m>0, n>0, m\neq    n)$
$\star$ 若已知椭圆上一点为P. $\angle{F_1PF_2}=\theta$. 则有 $S_{\triangleF_1PF_2}=b^2\tan\frac{\theta}{2}$

### 双曲线
双曲线第二定义: 平面内到定点(焦点)的距离到定直线(准线)的距离之比为常数(离心率)的点的迹叫双曲线.

$$\begin{aligned}
&\frac{x^2}{a^2}-\frac{y^2}{b^2}=1 \quad (a>0, b>0) \quad 此时焦点在x轴 \rArr 近线方程为 y=\pm\frac{b}{a}x \quad (被减数是哪个焦点就在哪个上) \\
&\frac{y^2}{x^2}-\frac{x^2}{b^2}=1 \quad (a>0, b>0) \quad 此时焦点在y轴 \rArr 近线方程为 y=\pm\frac{a}{b}x
\end{aligned}
$$

双曲线关于 x 轴, y 轴, 原点对称
等轴双曲线: 实虚轴相等. 此时 $e\sqrt{2}$, 渐近线方程为 $y=\pm x$
$\star$ 当双曲线的焦点不确定在哪个轴上时可设方程为 $mx^2+ny^2=1 \quad (mn<0)$
$\star$ 若已知双曲线的渐近线方程为 $\frac{x}{a}\pm\frac{y}{b}=0$. 求双曲线方程时,可设该双曲线方程为 $\frac{x^2}{a^2}-\frac{y^2}{b^2}=\lambda \quad (\lambda\neq0$. 再根据题意求 $\lambda$ 的值
$\star$ 若已知双曲线上一点为P. $\angle F_1PF_2=\theta$. 则有 $S_{\triangleF_1PF_2}=b^2\cot\frac{\theta}{2}$
### 抛物线
定义: 抛物线上的点到焦点的距离等于该点到准线的距离
| 公式 | 焦点 | 准线 |
| ---- | --- | ---- |
| $y^2=2px \quad (p>0)$ | $(\frac{p}{2},0)$ | $x=-\frac{p}{2}$ |
| $y^2=-2px \quad (p>0)$ | $(-\frac{p}{2}, 0)$ | $x=\frac{p}{2}$ |
| $x^2=2py \quad (p>0)$ | $(0, \frac{p}{2})$ | $y=-\frac{p}{2}$ |
| $x^2=-2py \quad (p>0)$ | $(0, -\frac{p}{2})$ | $y=\frac{p}{2}$ |
抛物线的离心率 $e=1$
抛物线的相关结论: 设 $y=2px \quad (p>0)$, AB为其焦点弦, 其倾斜角为 $\theta$. $F$其焦点. $A(x_1, y_1), B(x_2, y_2)$
1. 以抛物线的焦点弦为直径的圆与抛物线的准线相切
2. $\star \, x_1x_2=\frac{p^2}{4} \quad y_1y_2=-p^2$
3. $\star \, \frac{1}{|AF|}+\frac{1}{|BF|}=\frac{2}{p}$
4. $\star \, |AB|=x_1+x_2+p$
5. $|AB|=\frac{2p}{\sin{^2\theta}}$
6. $S_{\triangle ABO}=\frac{p^2}{2\sin{^2\theta}}$
7. 过 A, B 分别作准线的垂线, 垂足分别为 $A_1, B_1$. 则 $A_1F \perp B_1F$ 此时 $A_1O, B$ 三点共线
8. 焦点弦中, <u>通经</u>最短 (垂直于对称轴的焦点弦, 长为2p)
$\triangle$ 当题中只有给一个点时, 不知对称性. 可设 $x^2=2my \quad (m \neq 0)$ 或$y^2=2mx \quad (m \neq 0)$