---
title: the-application-of-definite-integral
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 16:59:30
tags:
---

## 元素法

(看起来就是普通的解题套路)

经典积分思想: 分成无数细小的段然后加起来, 得到 A

元素法思想: 
求A(或原函数)
1. 取 \\([x, x+dx]\subset[a, b]\\)
2. \\(dA=f(x)dx\\)
3. \\(A=\int_a^b dA=\int_a^b f(x)dx\\)

## 几何应用

### 面积

1. 贴着x轴 TODO: 补充图片
   1. 取 \\([x, x+dx]\subset[a, b]\\)
   2. \\(dA=f(x)dx\\)
   3. \\(A=\int_a^b f(x)dx\\)
2. 浮空曲边 TODO: 补充图片
   1. 取 \\([x, x+dx]\subset[a, b]\\)
   2. \\(dA=[f(x)-g(x)]dx\\)
   3. \\(A=\int_a^b[f(x)-g(x)]dx\\)
3. 曲边扇形面积 \\(L=\Gamma(\theta) \quad(\alpha\leqslant\theta\leqslant\beta)\\) TODO: 补充图片
   (这里的 \\(\Gamma\\) 不是指 \\(\Gamma\\) 函数)
   1. 取 \\([\theta, \theta+d\theta]\subset[\alpha, \beta]\\)
   2. \\(dA=\frac{1}{2}\Gamma^2(\theta)d\theta\\)
   3. \\(A=\int_\alpha^\beta dA=\int_\alpha^\beta \frac{1}{2}\Gamma^2(\theta)d\theta\\)

### 体积

1. 旋转体的体积 TODO: 补充图片
   1. \\(V_x\\) : (旋转x轴)
      1. 取 \\([x, x+dx]\subset[a, b]\\)
      2. \\(dV_x=\pi f^2(x)dx\\)
      3. \\(V_x=\pi\int_a^b f^2(x)dx\\)
   2. \\(V_y\\) : (旋转y轴)
      1. 取 \\([x, x+dx]\subset[a, b]\\)
      2. \\(dV_y=2\pi|x|\cdot|f(x)|\cdot dx\\)
      3. \\(V_y=2\pi\int_a^b |x|\cdot|f(x)|dx\\)
2. 截口面积已知几何体体积 TODO: 补充图片
   1. 取 \\([x, x+dx]\subset[a, b]\\)
   2. \\(dV=A(x)dx\\)
   3. \\(V=\int_a^b A(x)dx\\)

### 弧长

TODO: 补充图片
1. \\(L: y=f(x) \quad(a\leqslant x\leqslant b\\)
   1. 取 \\([x, x+dx]\subset [a, b]\\)
   2. \\(ds=\sqrt{(dx)^2+(dy)^2}=\sqrt{1+(\frac{dy}{dx})^2}dx=\sqrt{1+[f'(x)]^2}dx\\)
   3. \\(l=\int_a^b\sqrt{1+[f'(x)]^2}dx\\)
2. \\(L: \begin{cases} x=\varphi(t) \\\ y=\psi(t) \end{cases} \quad(\alpha\leqslant t\leqslant\beta)\\)
   1. 取 \\([t, t+dt]\subset[\alpha, \beta]\\)
   2. \\(ds=\sqrt{(dx)^2+(dy)^2}=\sqrt{[\varphi'(x)]^2+[\psi'(x)]^2}dt\\)
   3. \\(\int_\alpha^\beta\sqrt{[\varphi'(x)]^2+[\psi'(x)]^2}dt\\)