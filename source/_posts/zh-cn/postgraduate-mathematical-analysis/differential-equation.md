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
   \\(u+x\frac{du}{dx}=\varphi(u) \rArr x\frac{du}{dx}=\varphi(u)-u \rArr \int\frac{dx}{x}=\frac{du}{\varphi(u)-u}+c\\)

## 一阶线性微分方程

## 可降阶的高阶微分方程

## 高阶线性微分方程

## 常系数齐次线性微分方程

## 常系数非齐次线性微分方程