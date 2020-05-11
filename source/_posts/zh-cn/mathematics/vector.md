---
title: vector
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-03-24 18:37:30
tags:
toc: true
---

## 平面向量

### 向量的线性运算

#### 加减

三角形法则及平行四边形法则、其满足的运算规律有交换率和结合率

#### 数乘

规定实数 \\(\lambda\\) 与 \\(\vec{a}\\) 的积是一个向量, 这种运算叫做向量的数乘. 记作 \\(\lambda\vec{a}\\)

设 \\(\lambda,\,\vec{a}\\) 为实数. 则有:
\\(\\)\begin{aligned}
&结合律: \lambda(\mu\vec{a}) = (\lambda\mu)\vec{a} \\
&分配律: (\lambda + \mu)\vec{a} = \lambda\vec{a} + \mu\vec{a} \\
&分配律: \lambda(\vec{a} + \vec{b}) = \lambda\vec{a} + \lambda\vec{b} \\
&分配律:\lambda(\vec{a} - \vec{b}) = \lambda\vec{a} - \lambda\vec{b} \\
&乘负数时反向(-\lambda)\vec{a} = -(\lambda\vec{a}) = \lambda(-\vec{a})
\end{aligned}
\\(\\)

### 坐标表示和基本定理

已知 \\(\vec{a} = (x_1, y_1) \quad \vec{b} = (x_2, y_2)\\)
则
\\(\\)\begin{aligned}
    &\vec{a} + \vec{b} = (x_1 + x_2, y_1 + y_2) \\
    &\vec{a} - \vec{b} = (x_1 - x_2, y_1 - y_2) \\
    &\lambda\vec{a} = (\lambda x_1, \lambda y_1)
\end{aligned}\\(\\)

一个向量的坐标表示一条从原点到此坐标的有向线段(若始点坐标非零则是终点坐标减去始点坐标)

两向量平行或垂直的性质
设
\\(\\)\begin{aligned}
\vec{a} = (x_1, y_1) \quad \vec{b} = (x_2, y_2). \, &若 \vec{a} \parallel \vec{b} \quad (\vec{b} \neq \vec{0}) \hArr \frac{x_1}{x_2} = \frac{y_1}{y_2} \, (内向积等于外向积) \hArr x_1y_2 - x_2y_1 = 0 \\
&若 \vec{a} \perp \vec{b} \hArr \vec{a} \cdot \vec{b} = 0 \hArr x_1x_2 + y_1y_2 = 0
\end{aligned}
\\(\\)

#### 正交分解

把一个向量分解成两个相互垂直的向量, 叫做把向量正交分解
\\((x_i, y_i) \rArr (x_i, 0), \, (0, y_i)\\)

#### 向量共线基本定理

向量共线基本定理: \\(\vec{a}\\) 与 \\(\vec{b}\\) 共线 \\((\vec{a} \parallel \vec{b} \quad \vec{b} \neq 0)\\) \\(\hArr\\) 当且仅当有唯一一个实数 \\(\lambda\\), 使 \\(\vec{b} = \lambda\vec{a}\\)

### 数量积

\\(\vec{a} \cdot \vec{b} = |\vec{a}||\vec{b}|\cos{\theta}\\), 其中 \\(\theta\\) 是 \\(\vec{a}\\) 与 \\(\vec{b}\\) 的夹角

点乘满足交换律 \\(\vec{a} \cdot \vec{b} = \vec{b} \cdot \vec{a}\\)

\\(|\vec{a}|\cos{\theta}\\) 叫向量 \\(\vec{a}\\) 在 \\(\vec{b}\\) 方向上的投影
\\(|\vec{b}|\cos{\theta}\\) 叫向量 \\(\vec{b}\\) 在 \\(\vec{a}\\) 方向上的投影

## 空间向量

### 空间向量及其运算

向量共线定理推论: 若 \\(A, B, P\\) 三点共线. 对空间任意一点O. 都有 \\(\vec{OP} = \vec{OA} + \lambda\vec{AB} = \lambda\vec{OB} + (1-\lambda)\vec{OA}\\)

如果三个变量不共面, 那么对空间任一向量 \\(\vec{p}\\), 存在有序实数组 \\({x, y, z}\\) 使得 \\(\vec{p} = x\vec{a} + y\vec{b} + z\vec{c}\\)
我们把 \\({\vec{a}, \vec{b}, \vec{c}}\\) 叫做空间的一个基底. \\(\vec{a}, \vec{b}, \vec{c}\\) 都叫做基向量

向量共面定理: 若两个向量 \\(\vec{a}, \, \vec{b}\\) 不共线. 向量 \\(\vec{p}\\) 与向量 \\(\vec{a}, \, \vec{b}\\) 共面 \\(\hArr\\) 存在唯一的有序实数对 \\((x, y)\\). 使 \\(\vec{p} = x\vec{a} + y\vec{b}\\)
推论: 
1. P, A, B, C 四点共面 \\(\hArr\\) 存在有序实数对 \\((x, y)\\). 使 \\(\vec{P} = x\vec{a} + y\vec{b}\\)
2. P, A, B, C 四点共面 \\(\hArr\\) 存在有序实数对 \\((x, y)\\). 使 \\(\vec{OP} = \vec{OA} + x\vec{AB} + y\vec{AC}\\)
3. P, A, B, C 四点共面 \\(\hArr\\) 存在 \\(x, y, z \in R\\). 使 \\(\vec{OP} = x\vec{OA} + y\vec{OB} + z\vec{OC} \quad (x + y + z = 1)\\)

模长公式: 
1. 若 \\(\vec{a} = (x, y, z)\\) 则 \\(|\vec{a} = \sqrt{x^2 + y^2 + z^2}|\\)
2. 若 \\(\vec{a} = (x_1, y_1, z_1), \vec{b} = (x_2, y_2, z_2)\\) 则 \\(\cos{<\vec{a}, \vec{b}>} = \frac{\vec{a}\cdot\vec{b}}{|\vec{a}||\vec{b}|} = \frac{x_1x_2+y_1y_2+z_1z_2}{\sqrt{x_1^2+y_1^2+z_1^2}+\sqrt{x_2^2+y_2^2+z_2^2}}\\)

### 空间向量的应用

#### 直线的方向向量

设 \\(\vec{a}, \, \vec{b}\\) 分别是直线 \\(l, m\\) 的方向向量
1. \\(\vec{a} = \lambda\vec{b} \hArr \vec{a} \parallel \vec{b} \hArr l \parallel m\\)
2. \\(\vec{a} \cdot \vec{b} = 0 \hArr \vec{a} \perp \vec{b} \hArr l \perp m\\)

#### 平面的法向量

如果表示非零向量 n 的有向线段所在直线垂直于平面 \\(\alpha\\), 那么称向量 n 垂直于平面 \\(\alpha\\), 记作 \\(n \perp \alpha\\). 此时, 我们把向量 n 叫做平面 \\(\alpha\\) 的法向量

应用:
直线与平面
设 \\(\vec{a}\\) 是 \\(l\\) 的方向向量, \\(\vec{n}\\) 是 \\(\alpha\\) 的法向量
1. \\(\vec{a} = \lambda\vec{n} \hArr \vec{a} \parallel \vec{n} \hArr l \perp \alpha\\)
2. \\(\vec{a} \cdot \vec{n} = 0 \hArr \vec{a} \perp \vec{n} \hArr l \parallel \alpha\\)

平面与平面
设 \\(\vec{u}, \vec{n}\\) 分别为 \\(\alpha, \beta\\) 的法向量
1. \\(\vec{u} = \lambda\vec{n} \hArr \vec{u} \parallel \vec{n} \hArr \alpha \parallel \beta\\)
2. \\(\vec{u} \cdot \vec{n} = 0 \hArr \vec{u} \perp \vec{n} \hArr \alpha \perp \beta\\)

#### 三垂线定理

在平面内的一条直线, 如果和这个平面的一条斜线的射影垂直, 那么它也和这条斜线垂直
符号语言: \\(PO \perp \alpha \quad l \subset \alpha \quad OA是PA在\alpha内的射影, l \perp OA \rArr l \perp PA\\)