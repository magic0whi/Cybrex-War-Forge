---
title: multiple-integral
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:03:22
tags:
---

## 二重积分的概念与性质

### 二重积分的定义

设 f(x, y) 在 xOy 面有限闭区域 D 内有界
1. D 划分为 \\(\Delta\sigma_1 , \Delta\sigma_2 , \dots , \Delta\sigma_n \\)
2. \\(\forall(\xi_i, \eta_i)\in\Delta\sigma_i\\)
   作 \\(\displaystyle\sum_{i=1}^n f(\xi_i, \eta_i)\Delta\sigma_i\\)
3. \\(\lambda\\) 为 \\(\Delta\sigma_1 , \Delta\sigma_2 , \dots , \Delta\sigma_n\\) 最大值
   若 \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n f(\xi_i , \eta_i)\Delta\sigma_i\\) 存在, 称此极限为 f(x, y) 在 D 上的二重积分, 记 \\(\iint_D f(x, y)d\sigma\\)

### 二重积分的性质

1. 设 \\(f(x, y) , g(x, y)\\) 在区域 D 上可积, 则
   \\(\iint_D[af(x, y)+bg(x, y)]d\sigma=a\iint_D f(x, y)d\sigma+b\iint_D g(x, y)d\sigma\\)
2. \\(D=D_1+D_2\\) 且 \\(D_1\cap D_2=\varnothing\\) , 则
   \\(\iint_D f(x, y)d\sigma=\iint_{D_1}f(x, y)d\sigma+\iint_{D_2}f(x, y)d\sigma\\)
3. \\(\iint_D 1d\sigma=A\\)
4. 1. 若 \\(f(x, y)\geqslant g(x, y) \enspace((x, y)\in D)\\) 则 \\(\iint_D f(x, y)d\sigma\geqslant\iint_D g(x, y)d\sigma\\)
   2. \\(f(x, y)\\) 和 \\(|f(x, y)|\\) 在 D 上可积, 则 \\(|\iint_D f(x, y)d\sigma|\leqslant\iint_D|f(x, y)|d\sigma\\)
5. 积分中值定理
   D 为有限闭区域, f(x, y) 在 D 上连续
   则 \\(\exist(\xi, \eta)\in D\\) , 使 \\(\iint_D f(x, y)d\sigma=f(\xi, \eta)A \quad\\) (A 为常数)
   证明:
   \\(\because f(x, y)\in c(D)\\)
   \\(\therefore f(x, y)\\) 在 D 上有上下界 \\(m, M\\) , 使 \\(m\leqslant f(x, y)\leqslant M\\)
   \\(\therefore mA\leqslant\iint_D f(x, y)d\sigma\leqslant MA\\)
   \\(\mskip{1em}\rArr m\leqslant\frac{1}{A}\iint f(x, y)d\sigma\leqslant M\\)
   \\(\mskip{1em}\exist(\xi, \eta)\in D\\) , 使 \\(f(\xi, \eta)=\frac{1}{A}\iint_D f(x, y)d\sigma \rArr \iint_D f(x, y)d\sigma=f(\xi, \eta)A\\)

## 二重积分的计算法

## 三重积分

## 重积分的应用