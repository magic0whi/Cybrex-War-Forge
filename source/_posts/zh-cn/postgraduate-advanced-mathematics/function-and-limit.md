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

函数:
\\(\text{max}\\{N_1, N_2\\}\\) ---- 返回两者中较大者

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

### 初等性质

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

## 数列极限

1. 数列收敛定义(ε−N):
   **(建议先看例子)**
   设 \\({a_n}\\) 为数列, A为极限值, 最大误差\\(\varepsilon\\), \\(a_N\\)后极限有效(即之后的数列元素与极限值的误差进入容许范围),
   若 \\(\forall\varepsilon > 0 , \exist N > 0\\) ,
   且当 \\(n > N\\) 时. \\(|a_n - A| < \varepsilon\\)

   由此发现数列收敛于极限A, 用 \\(\lim\limits_{n\to\infty} = A\\) 或 \\(a_n \to A \quad(n\to\infty)\\) 表示

   举个例子:
   如有通项公式 \\(a_n=\dfrac{n+1}{2n}\\), 具体值为 \\(\dfrac{3}{4}, \dfrac{2}{3}, \dfrac{5}{8}, \dfrac{3}{5}, \text{...}\\) , 观察得极限 \\(a_n\to\dfrac{1}{2}\\)

   设最大容许误差 \\(\varepsilon = \dfrac{1}{10} > 0\\), 则误差值 \\(|a_n - \dfrac{1}{2}| = \dfrac{1}{2n} < \dfrac{1}{10} \Harr n > 5\\).
   同理:
   \\(\varepsilon= \frac{1}{100} > 0\\), 则 \\(\frac{1}{2n} < \frac{1}{100} \Harr n > 50\\)
   \\(\varepsilon= \frac{1}{1000} > 0\\), 则 \\(\frac{1}{2n} < \frac{1}{1000} \Harr n > 500\\)
   
   由此发现该数列有极限: \\(n\to\infty , a_n\to\dfrac{1}{2}\\)
2. 性质
   1. 唯一性: 数列有极限必唯一(极限值只有一个)
      证(反证法):
      设数列有两个极限 \\(\lim\limits_{n\to\infty}a_n=A ,\enspace \lim\limits_{n\to\infty}a_n = B \\) , 且 \\(A\neq B\\)
      再设 \\(A>B\\) , \\(\varepsilon=-\dfrac{A+B}{2}\\) (误差值的定义由 \\(\varepsilon + A=-\varepsilon - B\\) 解出, 目的是让下面两个\\(a_n\\)的值域没有交集)
      \\(\because\lim\limits_{n\to\infty}a_n=A,\enspace \therefore \exist N_1 > 0\\) , 当 \\(n>N_1\\) 时, \\(|a_n-A|<\varepsilon \quad\Harr\quad \frac{3A+B}{2}<a_n<\frac{A-B}{2}\\) (\*)
      \\(\because\lim\limits_{n\to\infty}a_n=B,\enspace \therefore \exist N_2 > 0\\) , 当 \\(n>N_2\\) 时, \\(|a_n-B|<\varepsilon \quad\Harr\quad \frac{A-B}{2}<a_n<\frac{-A+B}{2}\\) (\*\*)
      取 \\(N=\text{max}\\{N_1 , N_2\\}\\) , 当 \\(n < N_2\\) 时, (\*) (\*\*) 都成立, 但这两个不等式没有交集, 矛盾, 所以 \\(A>B\\) 不对, 同理 \\(B>A\\) 也不对.
      \\(\therefore A=B\\), 极限值只有一个.
   2. 有界性:
      若 \\(\lim\limits_{n\to\infty}a_n = A\\) , 则 \\(\exist M > 0\\) , 使得 \\(|a_n| \leqslant M\\) , **反之不成立**.
      证明: 
      <div>
      $$
      \begin{aligned}
         & "\rArr" \enspace 取 \varepsilon = 1 > 0 \\
         &\because \lim\limits_{n\to\infty}a_n=A \\
         &\therefore \exist N > 0,\enspace 当 n > N 时 , |a_n - A | < 1 \\
         &\because ||a_n|-|A|| \leqslant |a_n-A| \\
         &\therefore 当 n > N 时,\enspace ||a_n| - |A_1|| < 1 \rArr |a_n| < 1 + |A| 在 n>N 时成立 \\
         &取 \text{M} = \text{max}\{|a_1| ,\enspace |a_2| ,\enspace \text{...} ,\enspace |a_n| ,\enspace 1+|A|\} \\
         &\forall n ,\enspace 有 |a_n| \leqslant M \\
         &"\nLeftarrow" \enspace a_n = 1+ (-1)^n \enspace |a_n| \leqslant 2 ,\enspace 但 \lim\limits_{n\to\infty}a_n 不存在
      \end{aligned}
      $$
      </div>

   3. 保号性:
      若 \\(\lim\limits_{n\to\infty}a_n = A \begin{cases} >0 \\\ <0 \end{cases}\\) , 则 \\(\exist N > 0\\) , 当 \\(n > N\\) 时 , \\(a_n\begin{cases} >0 \\\ <0  \end{cases}\\)
      **极限正, 分界线往后就正; 极限负, 分界线往后就负**
      证明:
      <div>
      $$
      \begin{aligned}
         &设 A > 0 ,\enspace 取 \varepsilon = \frac{A}{2} > 0 \\
         &\because \lim\limits_{n\to\infty}a_n=A ,\enspace \therefore \exist N > 0 ,\enspace 当 n>N 时 ,\enspace |a_n - A| < \frac{A}{2} \rArr \frac{A}{2} < a_n < \frac{3A}{2} \quad\rArr\quad a_n > \frac{A}{2} > 0 \\
         &设 A < 0 , 取 \varepsilon = -\frac{A}{2} > 0 \\
         &\because \lim\limits{n\to\infty}a_n=A ,\enspace \therefore \exist N > 0 ,\enspace 当 n>N 时 ,\enspace |a_n - A| < -\frac{A}{2} \hArr \frac{3A}{2} < a_n < \frac{A}{2} \quad\rArr\quad a_n < \frac{A}{2} < 0
      \end{aligned}
      $$
      </div>

## 函数极限

## 无穷小与无穷大

## 极限的运算法则

## 极限存在法则 两个重要极限

## 无穷小的比较

## 函数的连续性与间断点

## 连续函数运算及初等函数连续性

## 闭区间上连续函数的性质