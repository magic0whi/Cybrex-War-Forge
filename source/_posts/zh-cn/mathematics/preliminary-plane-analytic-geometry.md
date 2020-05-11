---
title: preliminary-plane-analytic-geometry
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-03-25 17:52:43
tags:
toc: true
---

## 直线与方程

### 斜率

若\\(A(x_1, y_1),\, B(x_2, y_2)\\) 则 \\(AB\\) 所在直线斜率为 \\(k_{AB} = \frac{y_2-y_1}{x_2-x_1}\\)

### 点斜式

\\(y-y_0 = k(x-x_0) \qquad 适用于斜率存在的直线\\)

### 两点式

\\(\frac{y-y_2}{y_1-y_2} = \frac{x-x_2}{x_1-x_2} \quad (x_1 \neq x_2, y_1 \neq y_2) \qquad 适用于斜率存在的直线\\)

### 一般式

\\(Ax + By + C = 0\\)

### 两点间距离公式

\\(|AB| = \sqrt{(x_1-x_2)^2 + (y_1-y_2)^2}\\)

### 点到直线距离公式

\\(d = \frac{|Ax_0+By_0+C|}{\sqrt{A^2+B^2}}\\)

### 平行线距离公式

设有
\\(\\)
l_1: Ax + By + C_1 = 0 \\
l_2: Ax + By + C_2 = 0
\\(\\)

则其距离公式为
\\(\\)
\frac{|C_1 - C_2|}{\sqrt{(A+B)}}
\\(\\)

## 圆与方程

\\(\\)\begin{aligned}
&标准方程: (x-a)^2+(y-b)^2=r^2 \rArr 圆心 (a, b) \\
&一般方程: x^2+y^2+Dx+Ey+F=0 \quad (D^2+E^2-4F >0) \\
&半径长 \frac{1}{2}\sqrt{D^2+E^2-4F} \\
&圆心 (-\frac{D}{2}, -\frac{E}{2})
\end{aligned}
\\(\\)

### 直线与圆的位置关系

若 \\(y=kx+b \qquad x^2+y^2+Dx+Ey+F=0, \qquad A(x_1, y_1),\, B(x_2, y_2)\\) 为直线与圆的交点, (x_0, y_0) 为圆上一点

则

\\(\\)\begin{aligned}
&弦长公式 \enspace |AB|=\sqrt{1+k^2}\sqrt{(x_1+x_2)^2-4x_1x_2}=\sqrt{1+(\frac{1}{k})^2}\sqrt{(y_1+y_2)^2-4y_1y_2} \\
&切线方程 \enspace x_0x+y_0y=r^2 \qquad (圆心在原点上适用)
\end{aligned}
\\(\\)

\\(\\)\begin{aligned}
&C_1: x^2+y^2+D_1x+E_1y+F_1=0 \qquad C_2: x^2+y^2+D_2x+E_2y+F_2=0 \\
&且两圆相交于A, B两点 \\
&则 AB 所在的直线方程为 \quad (D_1-D_2)x + (E_1-E_2)y + F_1 - F_2 = 0 \\
&经过两圆公共点的圆系方程为 \\
&x^2+y^2+D_1x+E_1y+F_1-\lambda(x^2+y^2+D_2x+E_2y+F_2)=0 \quad (\lambda \neq -1)
\end{aligned}
\\(\\)
