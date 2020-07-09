---
title: multivariate-function-differential-and-its-application
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:00:56
tags:
toc: true
---

## 多元函数的基本概念

### 平面点集

平面点集中的:
1. 邻域 TODO: 补充图片
   \\(M_0(x_0, y_0)\in D\\) , 取 \\(\delta>0\\)
   1. 领域:
      称 \\(\\{(x, y)|\sqrt{(x-x_0)^2+(y-y_0)^2}<\delta\\}\\) 为 \\(M_0\\) 的 \\(\delta\\) 邻域
      记 \\(U(M_0, \delta)\\)
   2. 去心邻域:
      称 \\(\\{(x, y)|0<\sqrt{(x-x_0)^2+(y-y_0)^2}<\delta\\}\\) 为 \\(M_0\\) 的去心 \\(\delta\\) 邻域
      记 \\(\mathring{U}(M_0, \delta)\\)
2. 开集
   设 D 为 xOy 面上的点集,
   \\(\forall M_0(x_0, y_0)\in D\\) ,
   有 \\(\exist\delta>0\\) , 使 \\(U(M_0, \delta) \subset D\\) , 称 D 为开集
   若能取到边界上, 则称 D 为闭集
3. 区域: 连通的开集称为区域(开区域)
   闭区域: 开区域连同边界称为闭区域(或者说连通的闭集)

### 多元函数的概念

(空间中的一个曲面)
D 为区域, x, y, z 为变量, 若 \\(\forall(x, y)\in D\\)
\\(\exist z\\) 与 (x, y) 对应, 称 z 为 (x, y) 的函数, 记 \\(z=f(x, y)\\)
D 为定义域, 值域 \\(R=\\{z|z=f(x, y), (x, y)\in D\\}\\)

### 多元函数的极限

回顾一下一元函数极限定义:
\\(y=f(x) , (x\in D)\\) ,
若 \\(\forall\varepsilon>0\\) ,
\\(\exist\delta>0\\) , 当 \\(0<|x-x_0|<\delta\\) 时, 有 \\(|f(x)-A|<\varepsilon\\)
称 A 为 f(x) 当 \\(x\to x_0\\) 的极限, 记 \\(\lim\limits_{x\to x_0}f(x)=A\\)

二元函数极限定义:
设 \\(z=f(x, y) , ((x, y)\in D)\\) , \\(M_0(x_0, y_0)\\) ,
若 \\(\forall\varepsilon>0\\) ,
\\(\exist\delta>0\\) , 当 \\(0<\sqrt{(x-x_0)^2-(y-y_0)^2}<\delta\\) 时, 有 \\(|f(x, y)-A|<\varepsilon\\)
称 A 为 \\(f(x, y)\\) 当 \\((x, y)\to(x_0, y_0)\\) 的极限, 记 \\(\lim\limits_{\substack{x\to x_0 \\\ y\to y_0}}f(x, y)=A\\)

### 多元函数连续性与性质

定义
\\(z=f(x, y) \enspace((x, y)\in D\\) , \\(M_0(x_0, y_0)\in D\\)
若 \\(\lim\limits_{\substack{x\to x_0 \\\ y\to y_0}}f(x, y)=f(x_0, y_0)\\) , 称 \\(f(x, y)\\) 在 \\((x_0, y_0)\\) 处连续

### 多元函数在有界闭区域上的性质

设 D 为 闭区域 , 若 \\(\exist R>0\\) ,
使 \\(D=\\{(x, y)|x^2+y^2<R\\}\\)
称 D 为有界闭区域

1. 最值定理
   设 D 为有界闭区域, f(x, y) 在 D 上连续
   则 f(x, y) 在 D 上取到最小值 m 和最大值 M
2. 有界定理
   设 D 为有界闭区域, f(x, y) 在 D 上连续
   则 \\(\exist k>0 , \forall(x, y)\in D\\) , 有 \\(|f(x, y)|\leqslant k\\)
3. 界值定理
   f(x, y) 在 D 上连续, 
   则 \\(\exist下界m和上界M , \forall\delta\in[m, M]\\) ,
   \\(\exist(\xi, n)\in D\\) 使 \\(f(\xi, n)=\delta\\)

## 偏导数

### 定义

\\(z=f(x, y) \enspace((x, y)\in D), M_0(x_0, y_0)\in D\\)

1. 偏增量
   * f(x, y) 在 \\(M_0\\) 处关于 x 的偏增量 \\(\Delta Z_x=f(x_0+\Delta x, y_0)-f(x_0, y_0) \enspace(=f(x, y_0)-f(x_0, y_0))\\)
   * f(x, y) 在 \\(M_0\\) 处关于 y 的偏增量 \\(\Delta Z_y=f(x_0, y_0+\Delta y)-f(x_0, y_0) \enspace(=f(x_0, y)-f(x_0, y_0))\\)
   * f(x, y) 在 \\(M_0\\) 处的全增量 \\(\Delta Z=f(x_0+\Delta x, y_0+\Delta y)-f(x_0, y_0) \enspace(=f(x, y)-f(x_0, y_0))\\)
2. 偏导数
   * 若 \\(\lim\limits_{\Delta x\to0}\frac{\Delta Z_x}{\Delta x}\\) 存在
     称 f(x, y) 在 \\(M_0\\) 处关于 x 可偏导, 
     该极限称为 f(x, y) 在 \\(M_0\\) 处关于 x 的偏导数, 记 \\(f_x^'(x_0, y_0)\\) 或 \\(\frac{\partial z}{\partial x}|_{(x_0, y_0)}\\)
   * 若 \\(\lim\limits_{\Delta y\to0}\frac{\Delta Z_y}{\Delta y}\\) 存在
     称 f(x, y) 在 \\(M_0\\) 处关于 y 可偏导,
     该极限称为 f(x, y) 在 \\(M_0\\) 处关于 y 的偏导数, 记 \\(f_y^'(x_0, y_0)\\) 或 \\(\frac{\partial z}{\partial y}|_{(x_0, y_0)}\\)
   * 若 \\(\forall(x, y)\in D\\) , f(x, y) 对 x, y 皆可偏导, 称 \\(f_x^'(x, y) , f_y^'(x, y)\\) 为 f(x, y) 对 x, y 的偏导数

(求偏导数时, 其余参数视为常数)

### 高阶偏导数

定义:
设\\(z=f(x, y)\\) 在 D 内对 x, y 可偏导,
\\(\frac{\partial z}{\partial x}=f_x^'(x, y)\\) 为 f(x, y) 对 x 偏导数,
\\(\frac{\partial z}{\partial y}=f_y^'(x, y)\\) 为 f(x, y) 对 y 偏导数.
1. * 若 \\(f_x^'(x, y)\\) 对 x 可偏导, 其对 x 的偏导数称为 f(x, y) 对 x 的二阶偏导数, 记 \\(f_{xx}^{''}\\) 或 \\(\frac{\partial^2z}{\partial x^2}\\)
   * 若 \\(f_y^'(x, y)\\) 对 y 可偏导, 其对 y 的偏导数称为 f(x, y) 对 y 的二阶偏导数, 记 \\(f_{yy}^{''}\\) 或 \\(\frac{\partial^2z}{\partial y^2}\\)
2. * 若 \\(f_x^'(x, y)\\) 对 y 可偏导, 其对 y 的偏导数称为 f(x, y) 对先x后y的二阶混合偏导数, 记 \\(f_{xy}^{''}(x, y)\\) 或 \\(\frac{\partial^2z}{\partial x\partial y}\\)
   * 若 \\(f_y^'(x, y)\\) 对 x 可偏导, 其对 x 的偏导数称为 f(x, y) 对先y后x的二阶混合偏导数, 记 \\(f_{yx}^{''}(x, y)\\) 或 \\(\frac{\partial^2z}{\partial y\partial x}\\)

定理:
若 z=f(x, y) 的二阶混合偏导数 \\(\frac{\partial^2z}{\partial x\partial y} , \frac{\partial^2z}{\partial y\partial x}\\) 皆连续,
则 \\(\frac{\partial^2z}{\partial x\partial y}=\frac{\partial^2z}{\partial y\partial x}\\) ,
即 \\(f_{xy}^{''}=f_{yx}^{''}\\)

## 全微分

### 二元函数全微分定义

### 结论

## 多元复合函数求导法则

## 隐函数求导法则

## 多元函数微分学的几何应用

## 方向导数与梯度

## 代数应用 -- 多元函数的极值