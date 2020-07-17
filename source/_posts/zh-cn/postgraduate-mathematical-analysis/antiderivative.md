---
title: antiderivative
category: postgraduate-mathematical-analysis
lang: zh-cn
date: 2020-05-22 16:57:48
tags:
toc: true
---

不定积分

<!-- more -->

## 不定积分的概念与性质

### 不定积分的概念

1. 原函数:
   设 \\(f(x) , F(x) \enspace(x\in I)\\)
   若 \\(\forall x\in I\\) , 有 \\(F'(x)=f(x) , 称 F(x)\\) 为 \\(f(x)\\) 的**一个**原函数

   注意:
   1. 一个函数若有原函数, 那一定有无数个原函数
      推导:
      设 \\(F'(x)=f(x)\\)
      则 \\((F(x)+c)\\) 为 \\(f(x)\\) 的一切原函数
   2. 一个函数的的任意两个原函数之差\\(\in C\\) 
      (基于前一条可推导)
2. 不定积分
   设 \\(F(x)+c\\) 为 \\(f(x)\\) 的所有原函数
   则 \\(F(x)+c\\) 就是 \\(f(x)\\) 的不定积分, 记 \\(\int f(x)dx\\)

### 不定积分工具(积累公式)

1. \\(\int kdx=kx+c\\)
2. 1. \\(a\neq-1\\) 时 \\(\int a^a dx=\frac{1}{a+1}x^{a+1}+c\\)
   1. \\(a=-1\\) 时 \\(\begin{cases}\int\frac{1}{x}dx=\ln(-x)+c , &x<0 \\\ \int\frac{1}{x}dx=\ln(x)+c , &x>0 \end{cases} \therefore\int\frac{1}{x}dx=\ln|x|+c\\)
3. \\(\int a^xdx=\frac{a^x}{\ln a}+c\\)
4. 1. \\(\int\sin xdx=-\cos x+c\\)
   2. \\(\int\cos xdx=\sin x+c\\)
   3. \\(\int\tan xdx=-\ln|\cos x|+c\\)
   4. \\(\int\cot xdx=\ln|\sin x|+c\\)
   5. \\(\int\csc xdx=\ln|\tan\frac{x}{2}|+c=\ln|\csc x-\cot x|+c\\)
   6. \\(\int\sec xdx=\ln|\sec x+\tan x|+c\\)
   7. \\(\int\sec^2xdx=\tan x+c\\)
   8. \\(\int\csc^2xdx=-\cot x+c\\)
   9. \\(\int\sec x\tan xdx=\sec x+c\\)
   10. \\(\int\csc x\cot xdx=-\csc x+c\\)
5. 1. \\(\int\frac{1}{\sqrt{1-x^2}}dx=\arcsin x+c\\)
   2. \\(\int\frac{1}{\sqrt{a^2-x^2}}dx=\arcsin\frac{x}{a}+c\\)
   3. \\(\int\frac{1}{1+x^2}dx=\arctan x+c\\)
   4. \\(\int\frac{1}{a^2+x^2}dx=\frac{1}{a}\arctan\frac{x}{a}+c\\)
   5. \\(\int\frac{1}{x^2-a^2}dx=\frac{1}{2a}\ln|\frac{x-a}{x+a}|+c\\)
   6. \\(\int\frac{1}{\sqrt{x^2+a^2}}dx=\ln(x+\sqrt{x^2+a^2}+c\\) TODO: 补充图片(在第二类积分方法-平方和差)
   7. \\(\int\frac{1}{\sqrt{x^2-a^2}}dx=\ln|x+\sqrt{x^2-a^2}|+c\\)
   8. \\(\int\frac{1}{\sqrt{a^2-x^2}}dx=\frac{a^2}{2}\arcsin\frac{x}{a}+\frac{1}{2}x\sqrt{a^2-x^2}+c\\)

推导:
1. \\(\int\tan xdx=\int\frac{\sin x}{\cos x}dx=-\int\frac{1}{\cos x}d(\cos x)=-\ln|\cos x|+c\\)
2. \\(\int\cot xdx=\int\frac{\cos x}{\sin x}dx=\int\frac{1}{\sin x}d(\sin x)=\ln|\sin x|+c\\)

### 不定积分性质

1. \\(\int[f(x)\pm g(x)]dx=\int f(x)dx+\int g(x)dx\\)
2. \\(\int af(x)dx=a\int f(x)dx\\)

## 积分方法

### 换元积分法

1. 第一类换元积分法
   \\(f(u)\\) 存在原函数, \\(\varphi(x)\\) 可导, \\(F(u)\\) 为 \\(f(u)\\) 的原函数, 则
   \\(\int f[\varphi(x)]\underbrace{\varphi'(x)dx}_{f'(x)dx=df(x)}=\int\underbrace{f[\varphi(x)]d\varphi(x)}\_{设 \varphi(x)=t}=\int f(t)dt=F(t)+c=F[\varphi(x)]+c\\)
2. 第二类换元积分法
   \\(x=\psi(t)\\) 可导且 \\(\psi'(t)\neq0\\)
   \\(\int f(x)dx=\int f[\psi(t)]\psi'(t)dt=\int g(t)dt=G(t)+c=G[\psi^{-1}(x)]+c \quad (t=反函数\psi^{-1}(x))\\)

### 分部积分法

分部积分公式: \\(\int udv=uv-\int vdu\\)

推导:
结合导数四则运算和不定积分性质可得 \\(\int(uv)'dx=\int u'vdx+\int uv'dx\\)
结合第一类换元积分法进一步变换得 \\(\underbrace{uv}_{\int(uv)'dx}=\int vdu+\int udv\\)