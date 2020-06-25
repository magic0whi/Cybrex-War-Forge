---
title: mean-value-theorem-and-the-application-of-derivatives
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 16:56:27
tags:
---

## 微分中值定理

### 罗尔中值定理

TODO: 补充图片

若:
1. \\(f(x)\in c[a, b]\\)
2. \\(f(x)\\) 在 \\((a, b)\\) 内可导
3. \\(f(a)=f(b)\\)
则:
\\(\exist\xi\in(a, b)\\) , 使 \\(f'(\xi)=0\\)

### 拉格朗日中值定理

TODO: 补充图片

若:
1. \\(f(x)\in c[a,b]\\)
2. \\(f(x)\\) 在 \\((a, b)\\) 内连续
则 \\(\exist\xi\in(a, b)\\) , 使 \\(f'(\xi)=\frac{f(b)-f(a)}{b-a}\\)
(ab间某个点的斜率=ab两点所成直线的斜率. 顺便一提某个点的导数就是该点上作的切线的斜率)

证明:
作虚线 \\(L_{ab}\\) 连接点 a,b
将相关参数带入直线点斜式方程可得:
\\(L_{ab}: y-f(a)=\frac{f(b)-f(a)}{b-a}(x-a) \rArr y=f(a)+\frac{f(b)-f(a)}{b-a}(x-a)\\\)
令 \\(\varphi(x)=曲-直=f(x)-y=f(x)-f(a)-\frac{f(b)-f(a)}{b-a}(x-a)\\)
\\(\varphi(x)\in c[a, b] , \varphi(x)\\) 在 \\((a, b)\\) 内可导
且 \\(\varphi(a)=\varphi(b)=0\\)
根据罗尔中值定理, \\(\exist\xi\in(a, b)\\) , 使 \\(\varphi'(\xi)=0\\)
\\(\because \varphi'(x)=f'(x)-\frac{f(b)-f(a)}{b-a}\\)
\\(\therefore \varphi'(\xi)=f'(\xi)-\frac{f(b)-f(a)}{b-a}=0 \rArr f'(\xi)=\frac{f(b)-f(a)}{b-a}\\)

### 柯西中值定理

若:
1. \\(f(x) , g(x)\in c[a, b]\\)
2. \\(f(x) , g(x)\\) 在 \\((a,b)\\) 内可导
3. \\(g'(x)\neq0 \quad(a<x<b)\\)
则 \\(\exist\xi\in(a, b)\\) , 使 \\(\frac{f'(\xi)}{g'(\xi)}=\frac{f(b)-f(a)}{g(b)-g(a)}\\)

证明:
令 \\(\varphi(x)=f(x)-f(a)-\dfrac{f(b)-f(a)}{g(b)-g(a)}[g(x)-g(a)]\\) (这式子是逆推出来的?)
\\(\varphi(x)\in c[a, b]\\) , \\(\varphi(x)\\) 在 \\((a, b)\\) 内可导
\\(\because \varphi(a)=\varphi(b)=0\\)
\\(\therefore \exist\xi\in(a,b)\\) , 使 \\(\varphi'(\xi)=0\\)
\\(\because \varphi'(x)=f'(x)-\dfrac{f(b)-f(a)}{g(b)-g(a)}g'(x) , 且 g'(\xi)=\neq0\\)
\\(\therefore \varphi'(\xi)=f'(\xi)-\dfrac{f(b)-f(a)}{g(b)-g(a)}g'(\xi)=0 \rArr \dfrac{f'(\xi)}{g'(\xi)}=\dfrac{f(b)-f(a)}{g(b)-g(a)}\\)

## 洛必达法则

问题的起源:
求 \\(\lim\limits_{x\to0}\frac{\tan x-\sin x}{x^3}\\)
解:
\\(原式=\lim\limits_{x\to0}\frac{\tan x}{x}\cdot\frac{1-\cos x}{x^2}=\frac{1}{2}\\)
\\(原式=\lim\limits_{x\to0}\frac{x-x}{x^3}=0\\) . 不行(精确度不够)
同样使用等价无限小, 却得到了不同的结果.
说明对于存在 无穷小比无穷小(\\(\frac{0}{0}\\)) 的极限 , 用**等价无穷小解极限有局限性**

洛必达法则目标: 解 \\(\frac{0}{0} , \frac{\infty}{\infty}\\) 类型极限新方法

1. 解 \\(\frac{0}{0}\\) 型极限
2. 若 xxxxxxxxxxxxxxxxxxxx

## 泰勒公式

## 函数单调性与曲线凹凸性

## 极值与最值

## 函数图像描绘

## 弧微分与曲率