---
title: differential-equation
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:00:04
tags:
---

## 微分方程的基本概念

1. 定义1. 微分方程: 含有导数或微分的方程
   若微分方程中含一个自变量, 一个函数, 称为常微分方程
2. 定义2. 微分方程的阶: 在微分方程中, 导数或微分的最高阶数
3. 定义3. 微分方程的解: 
   已知 y 关于 x 的微分方程 \\(F(y^{(n)}, y^{(n-1)}, \dots,y', y, x)=0\\)
   若函数 \\(y=\varphi(x)\\) 满足 \\(F(y^{(n)}, y^{(n-1)}, \dots,y', y, x)=0\\)
   称 \\(y=\varphi(x)\\) 为该微分方程的解
   1. 通解: 设 \\(F(y^{(n)}, y^{(n-1)}, \dots,y', y, x)=0\\) 为 n 阶微分方程, 若该方程的解含 n 个相互独立的任意常数, 称该解为通解
      如 \\(y=C_1e^x+C_2e^{2x}\\) 为 \\(y''-3y'+2y=0\\) 的通解
   2. 特解: 不含任意常数的解, 称为特解


## 可分离变量的微分方程

1. 定义
   \\(\frac{dy}{dx}=f(x, y)\\) (\*)
   若 \\(f(x, y)=\varphi_1(x)\varphi_2(y)\\) , 称 (\*) 为可分离变量的微分方程
2. 解法
   \\(\frac{dy}{dx}=f(x, y) \rArr \frac{dy}{dx}=\varphi_1(x)\varphi_2(y) \rArr \frac{dy}{\varphi_2(y)}=\varphi_1(x)dx\\)
   \\(\int\frac{dy}{\varphi_2(y)}=\int\varphi_1(x)dx+c\\) (不定积分中我们不要求+c, 但在微分方程中要加) 

## 齐次微分方程

1. 定义
   设 \\(\frac{dy}{dx}=f(x, y)\\) (\*)
   若 \\(f(x, y)=\varphi(\frac{y}{x})\\) , 称 (\*) 为齐次微分方程
2. 解法
   \\(\frac{dy}{dx}=f(x, y) \rArr \frac{dy}{dx}=\varphi(\frac{y}{x})\\)
   令 \\(u=\frac{y}{x}\\) , 则 \\(y=ux \rArr y'=u'x+ux' \rArr \frac{dy}{dx}=x\frac{du}{dx}+u\\) 代入上面的方程 (这里把u看成是x的函数)
   \\(u+x\frac{du}{dx}=\varphi(u) \rArr x\frac{du}{dx}=\varphi(u)-u \rArr \frac{du}{\varphi(u)-u}=\frac{dx}{x} \rArr \int\frac{dx}{x}=\int\frac{du}{\varphi(u)-u}+c\\)

## 一阶线性微分方程

### 一阶齐次线性方程

1. 定义
   形如 \\(\frac{dy}{dx}+P(x)y=0\\) 的方程称为一阶齐次线性方程
2. 解法及通解公式
   \\(\frac{dy}{dx}=-P(x)y\\)
   情况1 y=0 为方程的解
   情况2 \\(y\neq0\\) 时 
   \\(\begin{aligned} \rArr \frac{1}{y}dy=-P(x)dx &\rArr \ln|y|=-\int P(x)dx+c_0 \\\ &\rArr |y|=e^{-\int P(x)dx+c_0} \\\ &\rArr y=\pm e^{c_0}\cdot e^{-\int P(x)dx} \end{aligned}\\)
   令 \\(\pm e^{c_0}=c\\)
   \\(\therefore 通解 y=ce^{-\int P(x)dx}\\)

### 一阶非齐线性微分方程

1. 定义
   形如 \\(\frac{dy}{dx}+P(x)y=Q(x)\\) 的方程称为一阶非齐线性微分方程
2. 解法
   通过常数易变法, 将上面齐次方程通解中的**常数项c换做未知函数 u(x)** , 得到
   \\(y=u(x)e^{-\int P(x)dx}\\) ,
   然后对 y 求导得
   \\(y'=\frac{dy}{dx}=u'(x)e^{-\int P(x)dx}-u(x)P(x)e^{-\int P(x)dx}\\) (注意复合函数求导法则)
   以上两式带入原方程得
   \\(\begin{aligned} &u'(x)e^{-\int P(x)dx}-u(x)P(x)e^{-\int P(x)dx}+P(x)u(x)e^{-\int P(x)dx}=Q(x) \\\ \rArr &u'(x)e^{-\int P(x)dx}=Q(x) \\\ \rArr &u'(x)=Q(x)e^{\int P(x)dx} \rArr \int u'(x)dx=\int Q(x)e^{\int P(x)dx}dx+c \\\ \rArr &u(x)=\int Q(x)e^{\int P(x)dx}dx+c \end{aligned}\\)
   求得的 u(x) 再次带入通解式得 \\(y=[\int Q(x)e^{\int P(x)dx}dx+c]e^{-\int P(x)dx}\\)

## 可降阶的高阶微分方程

1. \\(y^{(n)}=f(x)\quad(n\geqslant2)\\)
   太简单不再赘述
2. \\(f(x, y' ,y'')=0\quad(缺失y)\\)
   解法:
   令 \\(y'=p , y''=\frac{dp}{dx}\\) 代入得
   \\(f(x, p, \frac{dp}{dx})=0 \rArr p=\varphi(x, c_1)\\) , 即 \\(\frac{dy}{dx}=\varphi(x, c_1)\\)
   \\(\therefore y=\int \varphi(x, c_1)dx+c_2\\)
3. \\(f(y, y', y'')=0\quad(缺失x)\\)
   解法:
   令 \\(y'=p , y''=\frac{dp}{dx} \rArr y''=\frac{dp}{dy}\cdot\frac{dy}{dx}=\frac{dp}{dy}\cdot p\\) , 代入得 
   \\(f(y, p, \frac{dp}{dy}\cdot  p=0) \rArr p=\varphi(y, c_1)\\)
   即 \\(\frac{dy}{dx}=\varphi(y, c_1) \rArr  \frac{dy}{\varphi(y, c_1)}=dx \rArr \int\frac{dy}{\varphi(y, c_1)}=\int dx+c_2\\)

## 高阶线性微分方程

### 基本概念



### 结构

## 常系数齐次线性微分方程

## 常系数非齐次线性微分方程
