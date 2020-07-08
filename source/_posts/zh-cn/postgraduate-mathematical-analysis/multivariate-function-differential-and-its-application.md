---
title: multivariate-function-differential-and-its-application
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:00:56
tags:
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

## 全微分

## 多元复合函数求导法则

## 隐函数求导法则

## 多元函数微分学的几何应用

## 方向导数与梯度

## 代数应用 -- 多元函数的极值