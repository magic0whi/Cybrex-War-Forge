---
title: function-and-limit
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 16:54:13
tags:
---

## 前置知识
全称量词:
\\(\forall\\) ------ 任意的, 所有的
\\(\exist\\) ------ 存在
\\(\exist 1\\) ---- 存在且唯一

## 函数

1. **函数**:
有 集合D 和 x, y 两个变量. 若对任意 \\(x \in D\\) ,
总存在唯一确定的解 y 与 x 对应.
称 y 为 x 的函数,
记 \\(y=f(x)\\) , D 为 x 的定义域

2. **反函数**:
\\(y=f(x) \quad(x\in D)\\) 严格单调 **(单调函数是反函数的充分条件)**
若 \\(y=f(x) \implies x=\varphi(y)\\)
则 \\(\varphi(y)\\) 就是 \\(f(x)\\) 的反函数

1. **基本初等函数**:
<div>
$$
\begin{aligned}
    &1. x^\alpha \\
    &2. a^x \mskip{5.6em}(a>0且a\ne 1) \\
    &3. \log_a{x} \mskip{4em}(a>0且a\ne 1) \\
    &4. \sin x, \cos x, \tan x, \cot x, \sec x, \csc x
\end{aligned}
$$
</div>

4. **初等函数**: 由 常数\基本初等函数, 经过 四则运算\复合运算 而成的式子

## 初等性质

1. 奇偶性
   有 \\(y=f(x) \quad(x\in D,  D 关于原点对称)\\)
   若对于 \\(\forall x \in D\\),
   \\(\begin{aligned}&f(-x)=&-f(x) \enspace, &则为奇函数; \\\ &f(-x)=&f(x) \enspace, &则为偶函数\end{aligned}\\)
2. 单调性(TODO: 补充图片)
   有 \\(y=f(x) \quad(x\in D)\\)
   1. 若 \\(\exist x_1, x_2 \in D\\) 且 \\(x_1 < x_2\\) 时 , 有 \\(f(x_1)<f(x_2)\\)
      称 \\(f(x)\\) 在 D 上严格单调递增.
   2. 若 \\(\exist x_1, x_2 \in D\\) 且 \\(x_1<x_2>\\) 时 , 有 \\(f(x_1)>f(x_2)\\)
      称 \\(f(x)\\) 在 D 上严格单独递减
3. 有界性(TODO: 补充图片)
   有 \\(y=f(x) \quad(x\in D)\\), 函数之界 M (即值域的范围)
   若 \\(\exist M>0\\) , 对于 \\(\forall x\in D\\) , 有 \\(|f(x)|\leqslant M\\) , 称 \\(f(x)\\) 在 \\(D\\) 上有界
4. 周期性
   有 \\(y=f(x) \quad(x\in D)\\) ,
   若 \\(\exist T>0\\) , 使 \\(\forall x\in D \quad(x+T\in D)\\)
   有 \\(f(x+T)=f(x)\\) , 称 f(x) 为周期函数
