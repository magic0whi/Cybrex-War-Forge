---
title: arithmetic-progression-and-geometric-progression
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-04-02 15:15:35
tags:
---

## 数列

### 等差数列 (Arithmetic progression)

等差数列: $a_n=a_1+(n-1)d$
设 $a_n$ 的前 $n$ 项和为 $S_n$, 则 $S_n=na_1+\frac{(n-1)n}{2}d=\frac{(a_1+a_n)n}{2}$

若 $A, B, C$ 成等差数列. 则 $B$ 为等差中项. 有 $B=\frac{A+C}{2}$

性质: 
1. $m+n=p+q \quad (m, n, p, q \in N^*) \rArr a_m+a_n=a_p+a_q$
2. 数列的前n项和 $S_n$ 和 $a_n$ 的关系 $a_n=\begin{cases}
    S_1 \quad &n=1 \\
    S_n-S_{n-1} &n\geqslant 2
\end{cases}$

<u>等差数列前n项和性质</u>: 等差数列 $\{a_n\}$ 中, 其前 $n$ 项和为 $S_n$, 则 $\{a_n\}$ 中连续的 $n$ 项之和构成的数列 $S_n, S_{2n}-S_n, S_{3n}-S_{2n}, S_{4n}-S_{3n}, ...$ 构成等差为 $n^d$ 的等差数列

### 等比数列 (Geometric progression)

等比数列: $a_n=a_1q^{n-1}$
设 $a_n$ 的前 $n$ 项和为 $S_n$, 则 $S_n=\frac{a_1(1-q^n)}{1-q}=\frac{a_1-a_nq}{1-q} \quad (q\neq 1)$

若 $A, B, C$ 成等比数列. 则 $B$ 为等比中项. 有 $B^2=AC$

性质:
$k+l=m+n \quad (k, l, m, n \in N^*) \rArr a_k \cdot a_l = a_m \cdot a_n$

若 $\{a_n\}, \{b_n\}$ 是项数相同的等比数列, 且公比分别是 $p$ 和 $q$
则 $\begin{aligned}
    &\{\lambda a_n\} 的公比为 p, \{\frac{1}{a_n}\} 的公比为 \frac{1}{p} \\
    &\{a_n^2\} 的公比为 p^2, \{a_nb_n\} 的公比为 pq \\
    &\{\frac{a_n}{b_n}\} 的公比为 \frac{p}{q}
\end{aligned}$

<u>等比数列前n项和性质</u>: 在公比不等于 $-1$ 的等比数列 $\{a_n\}$ 中, 连续相同橡树也成等比数列, 即 $S_n, S_{2n}-S_n, S_{3n}-S_{2n}, S_{4n}-S_{3n}, ...$ 构成公比为 $q^n$ 的等比数列

在等比数列中. 当项数为 $2n$ 时, 比时有 $\frac{S_偶}{S_奇}=q$

### 其他

并项求和: 如 $\begin{aligned}
    &S=-1+2-3+4-5+6+(-1)^n \\
    &1. 当 n 为偶 S_n=\frac{n}{2}, 2. 当 n 为奇 S_n=\frac{n-1}{2}-n
\end{aligned}$
