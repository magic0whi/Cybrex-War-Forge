---
title: definite-integral
category: postgraduate-mathematical-analysis
lang: zh-cn
date: 2020-05-22 16:58:48
tags:
toc: true
---

## 定积分的概念与性质

### 定积分定义

设 f(x) 在 [a, b] 上有界(弱, 见Notes.2) , \\(x_1, x_2, \dots, x_n\\) 为[a ,b]间的分段点
1. \\(a=x_0<x_1<x_2<\dots<x_n=b \quad\Delta x_i=x_i-x_{i-1} \quad(1\leqslant i \leqslant n)\\)
2. \\(\exist s_i\in[x_{i-1}, x_i]\\) , 作 \\(\displaystyle\sum_{i=1}^n f(\xi_i)\Delta x_i\\)
3. \\(\lambda=\text{max}\\{\Delta x_1, \Delta x_2, \dots, \Delta x_n\\}\\)

若 \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n f(\xi_i)\Delta x_i\\) 存在, 称 f(x) 在 [a, b] 上可积
极限值称为 f(x) 在 [a, b] 上的定积分, 记 \\(\int_a^b f(x)dx\\)
即 \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n f(\xi_1)\Delta x_i = \int_a^b f(x)dx\\)

Notes:
1. \\(L: y=f(x)\geqslant0 \quad(a\leqslant x\leqslant b)\\)
   则 \\(A=\int_a^b f(x)dx\\)
   设 \\(v=V(t) \quad(a\leqslant t\leqslant b \quad\\) (v 为速度, t 为时间)
   则 \\(S=\int_a^b V(t)dt\\)
2. \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n f(\xi_1)\Delta x_i\\) 与 [a, b] 分法及 \\(\xi_i\\) 取法无关
3. f(x) 在 [a, b] 上有界不一定可积
   如 \\(f(x)=\begin{cases} 1 , x\in Q \\\ 0 , x\in R,Q \end{cases}\\)
4. 若 \\(f(x)\in c[a, b]\\) , 则 f(x) 在 [a, b] 上可积
   若 f(x) 在 [a, b] 上只有有限个第一类间断点, 则 f(x) 在 [a, b] 上可积

### 定积分的一般性质

0. \\(\int_a^a f(x)dx=0\\)
   \\(\int_a^b f(x)dx=-\int_b^a f(x)dx\\)
1. \\(\int_a^b[f(x)\pm g(x)]dx=\int_a^b f(x)dx\pm\int_a^b g(x)dx\\)
2. \\(\int_a^b kf(x)dx=k\int_a^b f(x)dx\\)
3. 设 a<b , 则 \\(\int_a^b f(x)dx=\int_a^c f(x)dx+\int_c^b f(x)dx\\)
   (证明思路: 即使c<a<b也成立, 因为 \\(\int_a^c\\) 是负的, 正好减去了 \\(\int_c^b\\) 多出来的)
4. \\(\int_a^b 1dx=b-a\\)
5. 定积分间的比较
   1. \\(f(x)\geqslant0 (a\leqslant x\leqslant b)\\) , 则 \\(\int_a^b f(x)dx\geqslant0\\)
   2. \\(f(x)\geqslant g(x) (a\leqslant x\leqslant b)\\) , 则 \\(\int_a^b f(x)dx\geqslant\int_a^b g(x)dx\\)
   3. \\(f(x) , |f(x)|\\) 在 [a, b] 上可积, 则 \\(|\int_a^b f(x)dx|\leqslant\int_a^b|f(x)|dx\\)
6. 积分中值定理
   TODO: 补充图片
   设 \\(f(x)\in c[a, b]\\) , 则 \\(\exist\xi\in[a, b]\\) , 使 \\(\underbrace{\int_a^b f(x)dx}\_{曲边梯形面积}=\underbrace{f(\xi)(b-a)}_{矩形面积}\\)
   证明:
   \\(\because f(x)\in c[a, b]\\)
   \\(\therefore \exist m,M\in[a, b]\\)
   使 \\(m(b-a)\leqslant\int_a^b f(x)dx\leqslant M(b-a)\\)
   \\(\rArr m\leqslant\underbrace{\frac{1}{b-a}\int_a^b f(x)dx}\_{可理解为: 面积\div底边=高}\leqslant M\\)
   \\(\therefore \exist\xi\in[a, b]\\) , 使 \\(f(\xi)=\frac{1}{b-a}\int_a^b f(x)dx \rArr \int_a^b f(x)dx=(b-a)f(\xi)\\)
   (Note: 若 \\(f(x)\in c[a, b] \rArr \exist m,M,\forall\eta\in[m, M], \exist\xi\in[a, b]\\) , 使 \\(f(\xi)=\eta\\))

## 积分基本公式

### 积分基本定理

积分上限函数及其与目标函数的关系:
设 \\(f(x)\in c[a, b]\\) 令 \\(\varPhi(x)=\int_a^x f(t)dt\\) , 则 \\(\varPhi'(x)=\frac{d}{dx}\int_a^x f(t)dt=f(x)\\)
推论
\\(\frac{d}{dx}\int_a^{\varphi(x)} f(t)dt=f[\varphi(x)]\cdot\varphi'(x)\\)

证明:
1. 定积分与不定积分的比较:
   \\(\int f(x)\neq\int f(t)\quad\\) (x 与 t 可能本身是不同的函数, 值域不同, 所以相等)
   \\(\int_a^b f(x)dx=\int_a^b f(t)dt\quad\\) (x 与 t 可能不同, 但值域被限制在[a, b] , 所以相等)
   因此: 定积分由 \\(\begin{cases} 上下限 \\\ 函数关系 \end{cases}\\) 确定, 与积分变量无关
   即:
   存在积分上限函数 \\(\varPhi(x)=\int_a^x f(x)dx=\int_a^x f(t)dt\quad\\) (自变量的x与积分上限的x不同) 
2. 设 \\(\Delta\varPhi=\varPhi(x+\Delta x)-\varPhi(x)=\int_a^{x+\Delta x}f(t)dt-\int_a^x f(t)dt=\int_x^{x+\Delta x}f(t)dt\\)
   \\(\because f(x)\in c[a, b] \rArr f(x)\in c[x, x+\Delta x]\\)
   \\(\begin{aligned} \therefore \exist\xi\in [x, x+\Delta x] , 使 f(\xi)\Delta x=\int_x^{x+\Delta x}f(t)dt=\Delta\varPhi &\rArr \frac{\Delta\varPhi}{\Delta x}=f(\xi) \\\ &\rArr \lim\limits_{\Delta x\to0}\frac{\Delta\varPhi}{\Delta x}=\lim\limits_{\Delta x\to0}f(\xi)=\lim\limits_{\xi\to x}f(\xi)=f(x) \\\ &\rArr \varPhi'(x)=f(x) \end{aligned}\\)

### 积分基本定理 - 牛顿莱布尼茨公式

\\(f(x)\in c[a, b]\\) , F(x) 为 f(x) 的一个原函数, 则 \\(\int_a^b f(x)dx=F(b)-F(a)\\)

证明:
\\(F'(x)=f(x)\\)
\\(\varphi(x)=\int_a^x f(t)dt , \varPhi'(x)=f(x)\\)
(F(x) 与 Φ(x) 皆为 f(x) 的原函数)

(牛顿莱布尼茨公式可用于证明积分中值定理)

## 定积分的换元积分法与分部积分法

### 换元积分法

\\(f(x)\in c[a, b] , x=\varphi(t)\\) 满足:
1. \\(\varphi(t)\\) 为单调函数且 \\(\varphi(\alpha)=a , \varphi(\beta)=b\\)
2. \\(x=\varphi(t)\\) 连续可导

则 \\(\int_a^b f(x)dx=\int_\alpha^\beta f[\varphi(t)]\varphi'(t)dt\\)

证明:
令 F(x) 为 f(x) 的原函数
\\(\int_a^b f(x)dx=F(x)|\_a^b=F(b)-F(a) \quad\\) 
\\(\because (F[\varphi(t)])'=F'[\varphi(t)]\cdot\varphi'(t)=f[\varphi(t)]\cdot\varphi'(t) , \\)
\\(\therefore \int_\alpha^\beta f[\varphi(t)]\varphi'(t)dt=F[\varphi(t)]|_\alpha^\beta=F[\varphi(\beta)]-F[\varphi(\alpha)]=F(b)-F(a)=\int\_a^b f(x)dx\\) (牛顿莱布尼茨公式)

### 分部积分法

\\(\int_a^b udv=uv|_a^b-\int_a^b vdu\\)

Notes:
\\(I_n=\int_0^{\frac{\pi}{2}}\sin^n xdx=\int_0^{\frac{\pi}{2}}\cos^n xdx=\frac{n-1}{n}I_{n-2}\\)
\\(I_0=\frac{\pi}{2} , I_1=1\\)

## 反常积分

正常积分标准:
1. 区间有限
2. f(x) 在区间上连续或第一类间断点(即有限个间断点)

### 积分区间无限

1. \\(f(x)\in c[a, +\infty]\\)
   1. \\(\lim\limits_{b\to+\infty}[F(b)-F(a)]\\) 与 \\(\int_a^{+\infty} f(x)dx\\) 相同
   2. 若 \\(\lim\limits_{b\to+\infty}[F(b)-F(a)]\\) 存在, 称 \\(\int_a^{+\infty} f(x)dx\\) 收敛
      有 \\(\lim\limits_{b\to+\infty}[F(b)-F(a)]=\int_a^{+\infty} f(x)dx=A\\)
   3. 若 \\(\lim\limits_{b\to+\infty}[F(b)-F(a)]\\) 不存在, 沉 \\(\int_a^{+\infty} f(x)dx\\) 发散
2. \\(f(x)\in c(-\infty, a]\\)
   1. \\(\lim\limits_{b\to-\infty}[F(a)-F(b)]\\) 与 \\(\int_{-\infty}^a f(x)dx\\) 相同
   2. \\(\lim\limits_{b\to-\infty}[F(a)-F(b)]\\) 存在, 称 \\(\int_{-\infty}^a f(x)dx\\) 收敛
      有 \\(\lim\limits_{b\to-\infty}[F(a)-F(b)]=\int_{-\infty}^a f(x)dx=A\\)
   3. \\(\lim\limits_{b\to-\infty}[F(a)-F(b)]\\) 不存在, 称 \\(\int_{-\infty}^a f(x)dx\\) 发散
3. \\(f(x)\in c(-\infty, +\infty\\)
   \\(若 \int_{-\infty}^{+\infty}f(x)dx 收敛 \hArr \int_{-\infty}^{a}f(x)dx 与 \int_{a}^{+\infty}f(x)dx 收敛\\)
   且 \\(\int_{-\infty}^{+\infty}f(x)dx=\int_{-\infty}^a f(x)dx+\int_a^{+\infty}f(x)dx\\)

Notes:
\\(\Gamma\\) 函数
1. 定义:
   形如 \\(\int_0^{+\infty}x^{\alpha-1}\cdot e^{-x}dx=\Gamma(\alpha)\\)
   如 \\(\int_0^{+\infty}x^5e^{-x}dx=\Gamma(6)\\)
   又如 \\(\int_0^{+\infty}x^\frac{1}{2}e^{-x}dx=\Gamma(\frac{3}{2})\\)
2. 特性:
   1. \\(\Gamma(\alpha+1)=\alpha\Gamma(\alpha)\\)
   2. \\(\Gamma(n+1)=n! \quad(n\in Z\\)
   3. \\(\Gamma(\frac{1}{2})=\sqrt{\pi}\\)

### 无界函数反常积分

1. 左无界: \\(f(x)\in c(a, b]\\) 且 \\(f(a+0)=\infty \quad\\) (a 被称作瑕点)
   1. \\(\forall\varepsilon>0 ,\enspace \lim\limits_{\varepsilon\to0^+}[F(b)-F(a+\varepsilon)]=\int_{a+\varepsilon}^b f(x)dx\\) 相同
   2. 若 \\(\lim\limits_{\epsilon\to0^+}[F(b)-F(a+\varepsilon)]\\) 存在, 称 \\(\int_a^b f(x)dx\\) 收敛
      若极限是有限实数, 则 \\(\lim\limits_{\varepsilon\to0^+}[F(b)-F(a+\varepsilon)]=\int_a^b f(x)dx=A\\)
   3. 若 \\(\lim\limits_{\varepsilon\to0^+}[F(b)-F(a+\varepsilon)]\\) 不存在, 称 \\(\int_a^b f(x)dx\\) 发散
2. 右无界: \\(f(x)\in c[a, b)\\) 且 \\(f(b-0)=\infty \quad\\)
   1. \\(\forall\varepsilon>0 ,\enspace F(b-\varepsilon)-F(a)=\int_a^{b-\varepsilon} f(x)dx\\\)
   2. 若 \\(\lim\limits_{\epsilon\to0^+}[F(b-\varepsilon)-F(a)]\\) 存在, 称 \\(\int_a^b f(x)dx\\) 收敛
      若极限是有限实数, 则 \\(\lim\limits_{\varepsilon\to0^+}[F(b-\varepsilon)-F(a)]=\int_a^b f(x)dx=A\\)
   3. 若 \\(\lim\limits_{\epsilon\to0^+}[F(b-\varepsilon)-F(a)]\\) 不存在, 称 \\(\int_a^b f(x)dx\\) 发散
3. 中无界: \\(f(x)\in c[a, c)\cup(c, b]\\) 且 \\(\lim\limits_{x\to c}f(x)=\infty\\)
   \\(若 \int_a^b f(x)dx 收敛 \hArr \int_a^c f(x)dx 与 \int_c^b f(x)dx 收敛\\)
   且 \\(\int_a^b f(x)dx=\int_a^c f(x)dx+\int_c^b f(x)dx\\)