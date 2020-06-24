---
title: derivatives-and-differentiation
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 16:54:47
tags:
toc: true
---

## 导数的概念

### 导数定义

设 \\(y=f(x) \quad (x\in D)\\) , \\(\quad \Delta y=f(x_0+\Delta x)-f(x_0) \quad x_0\in D , (x_0 + \Delta x)\in D\\)
若 \\(\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta x}\\) 存在, 称 \\(f(x)\\) 在 \\(x=x_0\\) 处可导, 该极限称为 \\(f(x)\\) 在 \\(x=x_0\\) 处的导数, 记 \\(f'(x_0)\\) 或 \\(\frac{dy}{dx}|_{x=x_0}\\)

Notes:
1. 可导是函数连续的充分不必要条件, 因为连续的函数在f'(x)=0处不可导(如正弦曲线y=1处, 左右导数不同)
2. \\(f'(x_0)=\lim\limits_{\Delta x\to0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}\boxed{=\lim\limits_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}}\\) <- 导数等价定义
   (证明: \\(\Delta x=x-x_0\\))
3. 可导时左右导数存在且相等
   左导数: \\(\lim\limits_{\Delta x\to0^-}\frac{\Delta y}{\Delta x}(=\lim\limits_{x\to x_0^-}\frac{f(x)-f(x_0)}{x-x_0})=f'_-(x_0)\\)

   右导数: \\(\lim\limits_{\Delta x\to0^+}\frac{\Delta y}{\Delta x}(=\lim\limits_{x\to x_0^+}\frac{f(x)-f(x_0)}{x-x_0})=f'_+(x_0)\\)

### 常见初等函数的导函数(积累公式)

1. \\(f(x)=C ,\quad f(x)'=0\\)
2. \\(f(x)=x^n ,\quad f'(x)=nx^{n-1}\\)
3. \\(f(x)=a^x ,\quad f'(x)=a^x\ln a\\)

4. \\((\sin x)'=\cos x\\)
   \\((\cos x)'=-\sin x\\)
   \\((\tan x)'=\sec^2x\\)
   \\((\cot x)'=-\csc^2x\\)
   \\((\sec x)'=\sec x\tan x\\)
   \\((\csc x)'=-\csc x\cot x\\)

5. \\((\arcsin x)'=\frac{1}{\sqrt{1-x^2}}\\)
   \\((\arccos x)'=-\frac{1}{\sqrt{1-x^2}}\\)
   \\((\arctan x)'=\frac{1}{1+x^2}\\)
   \\((\text{arccot } x)'=-\frac{1}{1+x^2}\\) <!-- katex好像没有\arccot -->

6. \\((\sin x)^{(n)}=\sin(x+\frac{nx}{2})\\)
   \\((\cos x)^{(n)}=\cos(x+\frac{nx}{2})\\)
   \\((\frac{1}{ax+b})^{(n)}=(-1)^n n! \frac{a^n}{(ax+b)^{n+1}}\\)

推导:
首先是套路 \\(f'(x)=\lim\limits_{\Delta x\to0}\frac{f(x+\Delta x)-f(x)}{\Delta x}\\)
1. \\(=\lim\limits_{\Delta x\to0}\frac{c-c}{\Delta x}=0 \rArr \(c\)'=0\\)
2. \\(=\lim\limits_{\Delta x\to0}\frac{(x+\Delta x)^n-x^n}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{(C_n^0x^n+C_n^1x^{n-1}\Delta x+\text{...}+C_n^n\Delta x^n)-x^n}{\Delta x}=\lim\limits_{\Delta x\to0}[C_n^1x^{n-1}+\frac{C_n^2x^{n-2}\Delta x^2+\text{...}+C_n^n\Delta x^{n}}{\Delta x})]=nx^{n-1} \rArr (x^n)'=nx^{n-1}\\)
   (你不会忘了二项式展开式了吧)
3. \\(=\lim\limits_{\Delta x\to0}\frac{a^{x+\Delta x}-a^x}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{a^x(a^{\Delta x}-1)}{\Delta x}=\underbrace{\lim\limits_{\Delta x\to0}\frac{a^x(e^{\Delta x\ln a}-1)}{\Delta x}}_{\normalsize a^{\Delta x}=e^{\ln a^{\Delta x}}=e^{\Delta x\ln a}}=\underbrace{\lim\limits\_{\Delta x\to0}\frac{a^x(\Delta x\ln a)}{\Delta x}=a^x\ln a}\_{\large\text{常用等价无穷小}x\text{\textasciitilde}(e^x-1)} \rArr (a^x)'=a^x\ln a\\) <!-- 这边katex和markdown兼容问题一些"_"前面加了"\" -->
   \*特别地 \\((e^x)'=e^x\\)

4. \\(=\lim\limits_{\Delta x\to0}\frac{\sin(x+\Delta x)-\sin x}{\Delta x}=\underbrace{\lim\limits_{\Delta x\to0}\frac{\sin x\cos\Delta x+\cos x\sin\Delta x-\sin x}{\Delta x}}_{和差角公式}=\lim\limits\_{\Delta x\to0}\frac{\sin x(\cos\Delta x-1)}{\Delta x}+\cos x\lim\limits\_{\Delta x\to0}\underbrace{\frac{\sin\Delta x}{\Delta x}}\_{等价无穷小}=\cos x \\) <!-- 这边katex和markdown兼容问题一些"_"前面加了"\" -->
   \\((\cos x)'\\) 的推导也同理
   后面的都是将其化为\\(\sin x\\) 和 \\(\cos x\\)的形式然后利用求导的四则运算法则推导 (提示: \\(\sec x=\frac{1}{\cos x} \quad\csc x=\frac{1}{\sin x}\\))
5. (参考求导法则-反函数求导法则)
   这里只证明 \\(\arcsin x\\)
   \\(f(x): y=\arcsin x \quad \varphi(y): x=\sin y\\)
   \\(f'(x)=\frac{1}{\varphi'(y)} \rArr (\arcsin x)'=\dfrac{1}{\cos y}=\underbrace{\frac{1}{\sqrt{1-\sin^2 y}}}_{平方关系式}=\underbrace{\frac{1}{\sqrt{1-x^2}}}\_{带入 x=\sin y}\\)
6. 使用[高阶导数-归纳法](#induction_method)
   1. \\(f(x)=\sin x\\)
      \\(f'(x)=\cos x=\sin(x+\frac{\pi}{2})\\)
      \\(f''(x)=-\sin x=\sin(x+\frac{2\pi}{2})\\)
      \\(f'''(x)=-\cos x=\sin\(x+\frac{3\pi}{2}\\)
      \\(f^{(4)}(x)=\sin x=\sin\(x+\frac{4\pi}{2}\\)
      \\(\therefore f^{(n)}(x)=\sin(x+\frac{nx}{2})\\)
      同理 \\((\cos x)^{(n)}=\cos(x+\frac{nx}{2})\\)
   2. \\(f(x)=(2x+1)^{-1}\\)
      \\(f'(x)=(-1)(2x+1)^{-2}\times 2\\)
      \\(f''(x)=(-1)(-2)(2x+1)^{-3}\times 2^2\\)
      \\(\therefore f^{(n)}(x)=(-1)^n\times n! \times 2^n \times (2x+1)^{-(n+1)}\\)

## 求导法则

### 四则法则

设 \\(u(x) , v(x)\\) 可导, 则
1. 加减: \\([u(x)\pm v(x)]'=u'(x)\pm v'(x)\\)
2. 乘: \\([u(x)v(x)]'=u'(x)v(x)+u(x)v'(x)\\)
3. 除: \\([\frac{u(x)}{v(x)}]'=\frac{u'(x)v(x)-u(x)v'(x)}{v^2(x)} \quad (v(x)\neq0)\\)

证明:
1. 令 \\(\varphi(x)=u(x)+v(x)\\)
   则 \\(\Delta\varphi=\varphi(x+\Delta x)-\varphi(x)=u(x+\Delta x)+v(x+\Delta x)-u(x)-v(x)=\Delta u+\Delta v\\)
   进而 \\(\lim\limits_{\Delta x\to0}\frac{\Delta\varphi}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{\Delta u}{\Delta x}+\lim\limits_{\Delta x\to0}\frac{\Delta v}{\Delta x}=u'(x) + v'(x)\\)
2. 令 \\(\varphi(x)=u(x)v(x)\\)\
   \\(\begin{aligned} \Delta\varphi&=\varphi(x+\Delta x)-\varphi(x) \\\ &=u(x+\Delta x)v(x+\Delta x)-u(x)v(x) \\\ &=u(x+\Delta x)v(x+\Delta x)-u(x)v(x+\Delta x)+u(x)v(x+\Delta x)-u(x)v(x) \quad (提示: 加一个[u(x)v(x+\Delta x)-u(x)v(x+\Delta x)]) \\\ &=\Delta u\cdot v(x+\Delta x)+u(x)\Delta v \end{aligned}\\) 
   进而 \\(\lim\limits_{\Delta x\to0}\frac{\Delta\varphi}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{\Delta u}{\Delta x}\cdot\lim\limits_{\Delta x\to0}v(x+\Delta x)+u(x)\cdot\lim\limits_{\Delta x\to0}\frac{\Delta v}{\Delta x}=u'(x)v(x)+u(x)v'(x) \quad (提示: \lim\limits_{\Delta x\to0}v(x+\Delta x)=v(x))\\)
3. 令 \\(\varphi(x)=\dfrac{u(x)}{v(x)} \quad (v(x)\neq0)\\)
   \\(\begin{aligned} \Delta\varphi=\varphi(x+\Delta x)-\varphi(x)&=\frac{u(x+\Delta x)}{v(x+\Delta x)}-\frac{u(x)}{v(x)} \\\ &=\frac{u(x+\Delta x)v(x)-v(x+\Delta x)u(x)}{v(x+\Delta x)v(x)} \\\ &=\frac{[u(x+\Delta x)v(x)-u(x)v(x)]-[u(x)v(x+\Delta x)-u(x)v(x)]}{v(x+\Delta x)v(x)} \quad (提示: 加一个[u(x)v(x)-u(x)v(x)]) \\\ &=\frac{\Delta u\cdot v(x)-u(x)\Delta v}{v(x+\Delta x)v(x)} \end{aligned}\\)
   进而 \\(\lim\limits_{\Delta x\to0}\frac{\Delta\varphi}{\Delta x}=\frac{\lim\limits_{\Delta x\to0}\frac{\Delta u}{\Delta x}\cdot v(x)-u(x)\cdot\lim\limits_{\Delta x\to0}\frac{\Delta v}{\Delta x}}{v(x)\lim\limits_{\Delta x\to0}v(x+\Delta x)}=\frac{u'(x)v(x)-u(x)v'(x)}{v^2(x)} \quad (提示: \lim\limits_{\Delta x\to0}v(x+\Delta x)=v(x))\\)

推论:
1. \\((ku)'=ku'\\) (k是常数)
2. \\((uvw)'=u'vw+uv'w+uvw'\\)

## 反函数求导法则

\\(y=f(x)\\) 严格单调, 反函数 \\(x=\varphi(y)\\)

设 \\(y=f(x)\\) 可导且 \\(f(x)'\neq0\\) , \\(x=\varphi(y)\\) 为反函数
则 \\(x=\varphi(y)\\) 可导且 \\(\varphi'(y)=\frac{1}{f'(x)}\\)

证明:
\\(\varphi'(y)=\lim\limits_{\Delta y\to0}\frac{\Delta x}{\Delta y}=\lim\limits_{\Delta y\to0}\frac{1}{\frac{\Delta y}{\Delta x}}=\underbrace{\lim\limits_{\Delta x\to0}}\_{(1)}\frac{1}{\frac{\Delta y}{\Delta x}}=\frac{1}{f'(x)}\\)
(1) \\(\lim\limits_{\Delta x\to0}\lim\limits\_{\Delta x\to0}\frac{\Delta y}{\Delta x}\neq 0 \rArr \Delta y=\bigcirc(\Delta x)\\) 同阶无穷小

## 复合函数求导法则

(如何判断复合函数: 自变量项外面是否还有初等函数)

\\(y=f(u\\) 可导, \\(u=\varphi(x)\\) 可导且 \\(\varphi'(x)\neq0\\) , 则 \\(y=f(\varphi(x)\\) 可导
且 \\(\frac{dy}{dx}=\frac{dy}{du}\cdot\frac{du}{dx}=f'(u)\cdot\varphi'(x)=f'[\varphi(x)]\varphi'(x)\\)

证明:
\\(\dfrac{dy}{dx}=\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta x}=\lim\limits_{\Delta x\to0}(\frac{\Delta y}{\Delta u}\cdot\frac{\Delta u}{\Delta x})=\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta u}\cdot\lim\limits_{\Delta x\to0}\frac{\Delta u}{\Delta x}=\underbrace{\lim\limits_{\Delta u\to0}}\_{(1)}\frac{\Delta y}{\Delta u}\cdot\lim\limits_{\Delta x\to0}\frac{\Delta u}{\Delta x}=f'(u)\cdot\varphi'(x)\\)
(1) \\(\varphi'(x)=\lim\limits_{\Delta x}\frac{\Delta u}{\Delta x}\neq0 \rArr \boxed{\Delta u=\bigcirc(\Delta x)}\\) 同阶

## 高阶导数

二阶及以上的导数称为高阶导数.
对导数再求导一次就是二阶导数:
\\([f'(x)]'=f''(x)=\dfrac{d(\frac{dy}{dx})}{dx}=\dfrac{d^2y}{dx^2}\\)
同理三阶导数 \\(\dfrac{d^3y}{dx^3}\\) , n阶导数 \\(f^{(n)}=\dfrac{d^ny}{dx^n}\\)

高阶导数求导方法:
<span id="induction_method"></span>
1. 归纳法
2. 公式法
   如:
   \\((uv)'=u'v+uv' \rArr (uv)''=(u'v)'+(uv')'=u''v+2u'v'+uv''\\) <!-- 这边 '' 渲染错误 -->
   莱布尼茨公式(请记住)
   \\((uv)^{(n)}=C_n^0 u^{(n)}v + C_n^1 u^{(n-1)}v' + C_n^2 u^{(n-2)}v'' + \text{...} + C_n^n uv^{(n)}\\)

## 隐函数及由参数方程确定的函数求导

### 隐函数求导

### 参数方程确定的函数求导

## 微分