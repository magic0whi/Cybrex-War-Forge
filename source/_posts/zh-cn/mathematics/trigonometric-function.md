---
title: trigonometric-function
lang: zh-cn
category: mathematics
date: 2020-03-16 16:14:18
tags:
---

## 诱导公式 Induction formula

口诀: **"奇变偶不变, 符号看象限"**

$$公式一\begin{cases}
\sin(2k\pi + \alpha)= \sin\alpha \quad (k \in Z) \\
\cos(2k\pi + \alpha) = \cos\alpha \quad (k \in Z) \\
\tan(2k\pi + \alpha) = \tan\alpha \quad (k \in Z) \\
\end{cases}$$

$$公式二\begin{cases}
\sin(\pi + \alpha)= -\sin\alpha \\
\cos(\pi + \alpha) = -\cos\alpha \\
\tan(\pi + \alpha) = \tan\alpha \\
\end{cases}$$

$$公式三\begin{cases}
\sin(-\alpha)= -\sin\alpha \\
\cos(-\alpha) = \cos\alpha \\
\tan(-\alpha) = -\tan\alpha \\
\end{cases}$$

$$公式四\begin{cases}
\sin(\pi - \alpha)= \sin\alpha \\
\cos(\pi - \alpha) = -\cos\alpha \\
\tan(\pi - \alpha) = -\tan\alpha \\
\end{cases}$$

$$公式五\begin{cases}
\sin(\frac{\pi}{2} - \alpha)= \cos\alpha \\
\cos(\frac{\pi}{2} - \alpha) = \sin\alpha \\
\tan(\frac{\pi}{2} - \alpha) = \cot\alpha \\
\end{cases}$$

$$公式六\begin{cases}
\sin(\frac{\pi}{2} + \alpha)= \cos\alpha \\
\cos(\frac{\pi}{2} + \alpha) = -\sin\alpha \\
\tan(\frac{\pi}{2} + \alpha) = -\cot\alpha \\
\end{cases}$$

## 周期性和单调性 Periodic and monotonic

周期函数: $对于函数f(x), 如果存在一个非零常数T, 使得当x取定义域的每一个值时. 都有f(x+T)=f(x). 那么函数f(x)就是一个周期函数$

最小正周期: 如果在周期函数f(x)的所有周期长度中存在一个最小正数, 那么这个最小正数就叫做f(x)的最小正周期

### 简谐运动 Simple harmonic motion

$y=A\sin(wx + \varphi) + k$ 的函数图像 (画该函数图像可用五点法)

$A$ 影响值域, $w$ 影响函数的周期性
$\varphi$ 影响函数左右平移, $k$ 影响上下平移

A为这个简谐运动的振幅.

这个简谐运动的周期为$T = \frac{2\pi}{w}$. 频率为$f = \frac{1}{T} = \frac{w}{2\pi}$

$wx + \varphi$ 称为相位, $x = 0$ 时的相位 $\varphi$ 称为初相

$\bigstar A = \frac{y(max - min)}{2} \quad k = \frac{y(max+min)}{2}$

## 同角三角函数基本关系式

平方关系: $\sin^2\alpha + \cos^2\alpha = 1$

商关系: $\frac{\sin\alpha}{\cos\alpha} = \tan\alpha \quad (\alpha \neq k\pi + \frac{\pi}{2}, k \in Z)$


## 三角恒等变换

和差角公式:

$$\begin{aligned}
&\sin(\alpha \pm \beta) = \sin\alpha\cos\beta \pm \cos\alpha\sin\beta \\
&\cos(\alpha \pm \beta) = \cos\alpha\cos\beta \mp \sin\alpha\sin\beta \\
&\tan(\alpha \pm \beta) = \frac{\tan\alpha \pm \tan\beta}{1 \mp \tan\alpha \cdot \tan\beta}
\end{aligned}$$

二倍角公式:

$$\begin{aligned}
&\sin{2\alpha} = 2\sin{\alpha}\cos{\alpha} \\
&\cos{2\alpha} = \cos^2{\alpha} - \sin^2{\alpha} = 1 - 2\sin^2{\alpha} = 2\cos^2{\alpha} - 1
\end{aligned}$$

辅助角公式:

$$\begin{aligned}
y = a\sin{x} + b\cos{x} &= \sqrt{a^2 + b^2}\sin(x + \varphi) \\
&= \sqrt{a^2 + b^2}\cos(x - \varphi)
\end{aligned}$$

## 解三角形

正选定理: $2R = \frac{a}{\sin{A}} = \frac{b}{\sin{B}} = \frac{c}{\sin{C}}$

余弦定理: $\begin{cases}
a^2 = b^2 + c^2 - 2bc\cos{A} \\ b^2 = a^2 + c^2 - 2ac\cos{B} \\ c^2 = a^2 + b^2 - 2ab\cos{C}
\end{cases}$

三角形面积公式 $S = \frac{1}{2}bc\sin{A} = \frac{1}{2}ac\sin{B} = \frac{1}{2}ab\sin{C}$

解三角形记得判断求出的该角能否为钝(锐)角 (大角对大边, 小角对小边)

正弦定理推论: $2R = \frac{a + b + c}{\sin{A} + \sin{B} + \sin{C}} \quad (\frac{a}{\sin{A}})^2 = \frac{bc}{\sin{B}\sin{C}} \quad (\frac{a}{\sin{A}})^3 = \frac{abc}{\sin{A}\sin{B}\sin{C}}$

余弦定理推论: $\cos{A} = \frac{b^2 + c^2 - a^2}{2bc} \quad \cos{B} = \frac{a^2 + c^2 - b^2}{2ac} \quad \cos{C} = \frac{a^2 + b^2 - c^2}{2ab}$