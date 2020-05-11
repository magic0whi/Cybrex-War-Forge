---
title: derivatives
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-03-17 18:01:07
tags:
toc: true
---

## 导数的概念及其几何意义 The concept of derivative and its geometric meaning

平均变化率: 函数\\(y=f(x)\\)从\\(x_1\\)到\\(x_2\\)的平均变化率表示为\\(\frac{f(x_2) - f(x_1)}{x_2 - x_1} = \frac{\vartriangle{y}}{\vartriangle{x}}\\)

瞬时变化率: 函数\\(y=f(x)\\)在\\(x=x_0\\)处的瞬时变化率是\\(f'(x_0) = \lim\limits_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0}\\)

## 导数的计算

导数公式:

\\(\\)\begin{cases}
    1. (c)' = 0 \quad c为常数 \\
    2. (x^\alpha)' = \alpha x^{\alpha - 1} \quad \alpha \in Q^* \\
    3. (\sin{x})' = \cos{x} \\
    4. (\cos{x})' = -\sin{x} \\
    5. (a^x)' = a^x\ln{a} \\
    6. (\log_ax)' = \frac{1}{x\ln{a}} = \frac{1}{x}\log_ae \\
    7. (e^x)' = e^x \\
    8. \ln{x} = \frac{1}{x}
\end{cases}
\\(\\)

导数运算法则:

\\(\\)\begin{cases}
    [f(x) \pm g(x)]' = f'(x) \pm g'(x) \\
    [f(x)g(x)]' = f'(x)g(x) + f(x)g'(x) \\
    [\frac{f(x)}{g(x)}]' = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2} \quad (g(x) \neq 0)
\end{cases}
\\(\\)

复合函数: 一般地, 对于两个函数 \\(y = f(u)\\) 和 \\(u = g(x)\\) . 如果通过变量\\(u, y\\)可以表示成x的函数, 那么称这个函数 \\(f(g(x))\\) 为 \\(y = f(u)\\) 和 \\(u = g(x)\\)的复合函数. 记作\\(y = f(g(x))\\)

复合函数的求导: \\(f'(g(x)) = f'(u) \cdot g'(x)\\)

## 导数在研究函数中的作用

函数的单调性与其导函数的正负有如下关系:
\\(\\)\begin{aligned}
\exist函数 y = f(x), 在某个区间 (a, b) 内, &如果f'(x) > 0, 那么函数在这个区间内单调递增 \\
&如果f'(x) < 0, 那么函数在这个区间内单调递减
\end{aligned}
\\(\\)

利用导数找函数极值点和极值:
\\(\\)\begin{aligned}
&首先\exist f'(a) = 0 \\
&极小值点: 若在点 x = a 附近, 左侧 f'(x) < 0, 右侧 f'(x) > 0. 则点 a 叫做函数的极小值点 \\
&极大值点: 若在点 x = a 附近, 左侧 f'(x) > 0, 右侧 f'(x) < 0. 则点 a 叫做函数的极大值点
\end{aligned}
\\(\\)

<u>注意: 求出的各个单调区间用"和" ", "连接</u>

求函数 \\(y = f(x)\\) 在 \\([a, b]\\) 上的最大值与最小值的步骤如下
(1) 求函数\\(y = f(x)\\) 在 \\((a, b)\\) 内的极值
(2) 将函数\\(y = f(x)\\) 的各极值与端点处的函数值\\(f(a), f(b)\\) 比较. 其中最大的一个是最大值; 最小的一个是最小值

## 定积分与微积分基本定理

先来看看微分的概念
微分本身定义 \\(dx = \lim\limits_{\varDelta x \to 0}\varDelta x\\)

结合导数的定义, 有 \\(f'(x)=\dfrac{dy}{dx} \rArr dy=f'(x)dx\\)

将 \\(y=f(x)\\) 带入上式
就有关于微分的公式:
1. \\(df(x) = f'(x)dx\\)
2. \\(d(ax + b) = adx\\)

## 定积分

定积分四部曲:
1. 分割
2. 近似代替
3. 求和
4. 取极限

定积分概念: 
\\(\\)\begin{aligned}
    &\int_a^b f(x)dx = \lim\limits_{n \to \infty} \sum_{i = 1}^n \frac{b - a}{n} f(\xi_i) \\
    &a 与 b 分别叫做积分下限和积分上限, 区间 [a, b] 叫做积分区间 \\
    &函数 f(x) 叫做被积函数, x 叫做积分变量 \\
    &f(x)dx 叫做被积式 \\
    &上式中\enspace dx \enspace与\enspace \frac{b - a}{n} \enspace对应
\end{aligned}\\(\\)

定积分公式:
\\(\\)\begin{aligned}
&(1) \int_a^b kf(x)dx = k\int_a^b f(x)dx \quad 表现了线性性质\\
&(2) \int_a^b [f_1(x) \pm f_2(x)]dx = \int_a^b f_1(x)dx \pm \int_a^b f_2(x)dx \quad 表现了线性性质\\
&(3) \int_a^b f(x)dx = \int_a^c f(x)dx + \int_c^b f(x)dx \quad (其中a < c < b) \quad 表现了积分区间的可加性 \\
&(4) 无论a <b 还是 a > b, -\int_a^b f(x)dx = \int_b^a f(x)dx
\end{aligned}\\(\\)

定积分性质:
1. 函数值域大于等于零时, 积分大于零; 函数值域小于等于零时, 积分小于零
\\(f(x) \geqslant 0 \rArr \int_a^bf(x)dx > 0 \qquad f(x) \leqslant 0 \rArr \int_a^b f(x)dx < 0\\)


2. 若\\(f(x)\\)是奇函数, 则\\(\int_{-a}^a f(x)dx = 0 \qquad\\) (因为奇函数沿原点对称)
   若\\(f(x)\\)是偶函数, 则\\(\int_{-a}^a f(x)dx = 2\int_0^a f(x)dx \qquad\\) (因为偶函数沿y轴对称)

## 微积分基本定理

一般地, 如果 \\(f(x)\\) 是区间 \\([a, b]\\) 上的连续函数. 并且\\(\exist F'(x) = f(x)\\), 那么
\\(\\)\int_a^b f(x)dx = F(b) - F(a) = F(x)|_a^b = [F(x) + c]|_a^b\\(\\)
这个结论叫做微积分基本定理, 也称 牛顿 ⋅ 莱布尼茨公式.
