---
title: derivatives-and-differentiation
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 16:54:47
tags:
---

## 导数的概念

### 导数定义

设 \\(y=f(x) \quad (x\in D)\\) , \\(\quad \Delta y=f(x_0+\Delta x)-f(x_0) \quad x_0\in D , (x_0 + \Delta x)\in D\\)
若 \\(\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta x}\\) 存在, 称 \\(f(x)\\) 在 \\(x=x_0\\) 处可导, 该极限称为 \\(f(x)\\) 在 \\(x=x_0\\) 处的导数, 记 \\(f'(x_0)\\) 或 \\(\frac{dy}{dx}|_{x=x_0}\\)

Notes:
1. 可导是函数连续的充分不必要条件
2. \\(f'(x_0)=\lim\limits_{\Delta x\to0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}\boxed{=\lim\limits_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}}\\) <- 导数等价定义
   (证明: \\(\Delta x=x-x_0\\))
3. 可导时左右导数存在且相等
   左导数: \\(\lim\limits_{\Delta x\to0^-}\frac{\Delta y}{\Delta x}(=\lim\limits_{x\to x_0^-}\frac{f(x)-f(x_0)}{x-x_0})=f'_-(x_0)\\)

   右导数: \\(\lim\limits_{\Delta x\to0^+}\frac{\Delta y}{\Delta x}(=\lim\limits_{x\to x_0^+}\frac{f(x)-f(x_0)}{x-x_0})=f'_+(x_0)\\)

### 常见初等函数的导函数(积累公式)

1. \\(f(x)=C ,\quad f(x)'=0\\)
2. \\(f(x)=x^n ,\quad f'(x)=nx^{n-1}\\)
3. \\(f(x)=a^x ,\quad f'(x)=a^x\ln a\\)

推导:
首先是套路 \\(f'(x)=\lim\limits_{\Delta x\to0}\frac{f(x+\Delta x)-f(x)}{\Delta x}\\)
1. \\(=\lim\limits_{\Delta x\to0}\frac{c-c}{\Delta x}=0 \rArr \(c\)'=0\\)
2. \\(=\lim\limits_{\Delta x\to0}\frac{(x+\Delta x)^n-x^n}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{(C_n^0x^n+C_n^1x^{n-1}\Delta x+\text{...}+C_n^n\Delta x^n)-x^n}{\Delta x}=\lim\limits_{\Delta x\to0}[C_n^1x^{n-1}+\frac{C_n^2x^{n-2}\Delta x^2+\text{...}+C_n^n\Delta x^{n}}{\Delta x})]=nx^{n-1} \rArr (x^n)'=nx^{n-1}\\)
   (你不会忘了二项式展开式了吧)
3. \\(=\lim\limits_{\Delta x\to0}\frac{a^{x+\Delta x}-a^x}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{a^x(a^{\Delta x}-1)}{\Delta x}=\underbrace{\lim\limits_{\Delta x\to0}\frac{a^x(e^{\Delta x\ln a}-1)}{\Delta x}}_{\normalsize a^{\Delta x}=e^{\ln a^{\Delta x}}=e^{\Delta x\ln a}}=\underbrace{\lim\limits\_{\Delta x\to0}\frac{a^x(\Delta x\ln a)}{\Delta x}=a^x\ln a}\_{\large\text{常用等价无穷小}x\text{\textasciitilde}(e^x-1)} \rArr (a^x)'=a^x\ln a\\)<!-- 这边katex和markdown兼容问题一些"_"前面加了"\" -->
   \*特别地 \\((e^x)'=e^x\\)

## 求导法则

## 高阶导数

## 隐函数及由参数方程确定的函数求导

## 微分