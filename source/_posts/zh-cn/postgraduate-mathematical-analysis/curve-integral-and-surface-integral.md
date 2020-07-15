---
title: curve-integral-and-surface-integral
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:02:36
tags:
---

## 对弧长的曲线积分

1. 定义: \\(\int_F f(x, y)ds\\)
2. 性质
   1. \\(\int_L \alpha f+\beta gds=\alpha\int_L fds+\beta\int_L gds\\)
   2. \\(L=L_1+L_2\\) 且 \\(L_1\cap L_2=\varnothing\\) , 则 \\(\int_L f(x, y)ds=\int_{L_1} f(x, y)ds+\int_{L_2} f(x, y)ds\\)
   3. \\(\int_L 1ds=L\\)
   4. 在 L 上当 \\(f(x, y)\leqslant g(x, y)\\) , 则 \\(\int_L f(x, y)ds\geqslant\int_L g(x, y)ds\\)
   5. \\(|\int_L f(x, y)ds|\leqslant\int_L|f(x, y)|ds\\)
3. 对弧长曲线积分计算方法
   对 \\(\int_L f(x, y)ds\\)
   1. L 为直角坐标形式
      1. \\(L: y=\varphi(x) \enspace(a\leqslant x\leqslant b)\\)
      2. \\(ds=\sqrt{(dx)^2+(dy)^2}=\sqrt{1+(\frac{dy}{dx})^2}dx=\sqrt{1+[f'(x)]^2}dx\\)
      3. \\(\int_L f(x, y)ds=\int_a^b f[x, \varphi(x)]\sqrt{1+[f'(x)]^2}dx\\)
   2. L 为参数形式
      \\(L: \begin{cases} x=\varphi(t) \\\ y=\psi(t) \end{cases} \enspace(\alpha\leqslant t\leqslant\beta)\\)
      1. \\(L: \begin{cases} x=\varphi(t) \\\ y=\psi(t) \end{cases} \enspace(\alpha\leqslant t\leqslant\beta)\\)
      2. \\(ds=\sqrt{[\varphi'(t)]^2+[\psi'(t)]^2}dt\\)
         \\(\int_L f(x, y)ds=\int_\alpha^\beta f[\varphi(t), \psi(t)]\cdot\sqrt{[\varphi'(t)]^2+[\psi'(t)]^2}dt\\)

## 对坐标的曲线积分(第二类曲线积分)

1. 定义
   * 二维: \\(\int_L P(x, y)dx+Q(x, y)dy\\) , 其中 \\(\int_L P(x, y)dx\\) 称为函数 \\(P(x, y)\\) 在有向曲线段 L 上对坐标 x 的曲线积分.
   * 三维: \\(\int_L P(x, y, z)dx+Q(x, y, z)dy+R(x, y, z)dz\\)
2. 性质
   1. \\(\int_L [af_1(x, y)+bf_2(x, y)]dx=a\int_L f_1(x, y)dx+b\int_L f_2(x, y)dx\\)
   2. \\(\int_{L^-}P(x, y)dx+Q(x, y)dy=-\int_L P(x, y)dx+Q(x, y)dy\\)
3. 对坐标的曲线积分基本计算法(2维)
   定积分法:
   1. 直角坐标法
      对 \\(\int_L P(x, y)dx+Q(x, y)dy\\)
      1. \\(L: y=\varphi(x)\\) (起点 x=a, 终点 x=b)
      2. \\(\int_L P(x, y)dx+Q(x, y)dy=\int_a^b P[x, \varphi(x)]dx+Q[x, \varphi(x)]\cdot\varphi'(x)dx\\)
   2. 参数方程法
      1. \\(L: \begin{cases} x=\varphi(x) \\\ y=\psi(t) \end{cases}\\) (起 \\(t=\alpha\\) , 终 \\(t=\beta\\)))
      2. \\(\int_L P(x, y)dx+Q(x, y)dy=\int_\alpha^\beta P[\varphi(t), \psi(t)]\varphi'(t)dt+Q[\varphi(t), \psi(t)]\psi'(t)dt\\)

## 格林公式及应用

定义:
1. 设 D 为连通区域, L 为 D 的<u>正向边界</u>
2. \\(P(x, y), Q(x, y)\\) 在 D 上连续可偏导, 则
   \\(\oint_L Pdx+Qdy=\iint_D\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}d\sigma\\)

## 对面积的曲面积分

计算方法: 二重积分法
\\(\iint_\Sigma f(x, y, z)ds\\)
1. \\(\Sigma: z=\varphi(x, y) \enspace(x, y)\in Dxy\\)
2. \\(ds=\sqrt{1+[z_x^']^2+[z_y^']^2}d\sigma\\)
3. \\(\iint_\Sigma f(x, y, z)ds=\iint_D f[x, y, \varphi(x, y)]\cdot\sqrt{1+[\varphi_x^']^2+[\varphi_y^']^2}d\sigma\\)

## 对坐标的曲面积分

### 对坐标的曲面积分的定义

\\(\Sigma\\) 有侧曲面块, \\(P(x, y, z) , Q(x, y, z) , R(x, y, z)\\) 在有侧曲面上有界
1. \\(\Sigma\\) 分为 \\(\overrightarrow{\Delta S_1} , \overrightarrow{\Delta S_2} , \dots , \overrightarrow{\Delta S_n}\\)
2. \\(overrightarrow{\Delta S_i}\\) 在 yOz 面, xOz 面, xOy 面投影为
   \\((\Delta S_i)yz , (\Delta S_i)xz , (\Delta S_i)xy , P(\xi_i, \eta_i, \zeta_i)\in\overrightarrow{\Delta S_i}\\) ,
   作
   \\(\displaystyle\sum_{i=1}^n P(\xi_i, \eta_i, \zeta_i)(\Delta S_i)yz\\)
   \\(\displaystyle\sum_{i=1}^n Q(\xi_i, \eta_i, \zeta_i)(\Delta S_i)xz\\)
   \\(\displaystyle\sum_{i=1}^n R(\xi_i, \eta_i, \zeta_i)(\Delta S_i)xy\\)
3. 令 \\(\lambda\\) 为 \\(\overrightarrow{\Delta S_1} , \overrightarrow{\Delta S_2} , \dots , \overrightarrow{\Delta S_n}\\) 直径最大值
   若 \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n P(\xi_i, \eta_i, \zeta_i)(\Delta S_i)yz\\) 存在, 则
   \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n P(\xi_i, \eta_i, \zeta_i)(\Delta S_i)=\iint_\Sigma P(x, y, z)dydz \enspace\\) (P 在有侧曲面 \\(\Sigma\\) 上对坐标 y, z 的曲面积分)
   \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n Q(\xi_i, \eta_i, \zeta_i)(\Delta S_i)xz=\iint_\Sigma Q(x, y, z)dxdz\\)
   \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n R(\xi_i, \eta_i, \zeta_i)(\Delta S_i)xy=\iint_\Sigma R(x, y, z)dxdy\\)
   \\(\iint_\Sigma Pdydz+\iint_\Sigma Qdxdz+\iint_\Sigma Rdxdy=\iint_\Sigma Pdydz+Qdxdz+Rdxdy\\)

性质:
1. \\(\iint_\Sigma=\iint_{\Sigma_1}+\iint_{\Sigma_2}\\)
2. \\(\iint_{\Sigma^-}=-\iint_\Sigma\\)

### 对坐标的曲面积分基本计算法-二重积分法

TODO: 分析例题

### 两类曲面积分关系

TODO: 补充图片
对 \\(\iint_\Sigma Pdyd+Qdzdx+Rdxdy\\)
\\(dydz=ds\cdot\cos\alpha\\)
\\(dxdz=ds\cdot\cos\beta\\)
\\(dxdy=ds\cdot\cos\gamma\\)
\\(\iint_\Sigma Pdydz+Qdxdz+Rdxdy=\iint_\Sigma (P\cos\alpha+Q\cos\beta+R\cos\gamma)ds\\)

## 高斯公式

定义:
1. \\(\Omega\\) 为集合体, \\(\Sigma\\) 为 \\(\Omega\\) 的外表面
2. \\(P, Q, R\\) 在 \\(\Omega\\) 上连续可偏导, 则
   \\(\oiint_\Sigma Pdydz+Qdzdx+Rdxdy=\iiint_\Omega(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z})dV\\)

## 斯托克斯公式

定义:
1. \\(\Sigma\\) 为光滑曲面块, \\(\Gamma\\) 为 \\(\Sigma\\) 的界, \\(\Sigma\\) 的侧与 \\(\Gamma\\) 的方向按右手确定
2. \\(P, Q, R\\) 在 \\(\Sigma\\) 连续可偏导, 则
   \\(\oint_L Pdx+Qdy+Rdz=\iint_\Sigma \begin{vmatrix} dydz & dzdx & dxdy \\\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\\ P & Q & R \end{vmatrix}=\iint_\Sigma \begin{vmatrix} \cos\alpha & \cos\beta & \cos\gamma \\\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\\ P & Q & R \end{vmatrix}ds\\)
   其中 \\(\cos\alpha, \cos\beta, \cos\gamma\\) 为曲面 \\(\Sigma\\) 法向量的方向余弦
