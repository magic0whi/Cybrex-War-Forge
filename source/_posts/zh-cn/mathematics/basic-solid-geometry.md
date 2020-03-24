---
title: basic-solid-geometry
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-03-23 17:18:59
tags:
---
## 立体几何初步

### 空间几何体 

#### 柱锥台球

$$
\begin{aligned}
&圆柱: S=2\pi r^2 + 2\pi rl = 2\pi r(r+l) \qquad &V=S_底h \\
&圆锥: S=\pi r^2 + \pi rl = \pi r(r+l) \qquad &V=\frac{1}{3}S_底h \\
&圆台: S= \pi r^2 + \pi r'^2 + \frac{1}{2}(c+c')l = \pi(r^2 + r'^2 + rl + r'l) \qquad &V=\frac{1}{3}(S_{下底} + S'_{上底} + \sqrt{S_{下底}S'_{上底}})h \\
&球体: S=4\pi R^2 \qquad &V=\frac{4}{3}\pi R^2 \\
\\
&柱体: S_侧=ch \qquad &(c为底面周长)\\
&正棱锥: S_侧 = \frac{1}{2}ch' \, &(h'为斜高) \\
&台体: S_侧 = \frac{1}{2}(c' + c)h' \, &(h'为斜高)
\end{aligned}
$$

#### 三视图

#### 平行投影与中心投影

### 点线面的位置关系

#### 四大公理

1. 公理1 如果一直线上两点在一个平面内, 那么这条直线在此平面内
   推论: 判定一条直线是否在平面内
         判定点在平面内
         检验平面

2. 公理2 过不在一直线上的三点, 有且只有一个平面
   推论: 经过一条直线和这条直线上一点, 有且只有一个平面
         经过两天相交直线, 有且只有一个平面
         经过两条平行直线, 有且只有一个平面

3. 公理3 如果两个不重合的平面有一个公共点, 那么它们有且只有一条过该点的公共直线
   推论: 判断两个平面是否相交
         $判断点是否在直线上 \rArr A \in \alpha , A \in \beta, \alpha \cap \beta = l, 则 A \in l$

4. 公理4 平行与同一条直线的两条直线互相平行

#### 线面平行和垂直

定理1 空间中如果两个角的两边分别对应平行, 那么这两个角相等或互补

1. 直线\平面平行的判定
   定理2 判定定理(直线与平面): 平面外一条直线与此平面内的一条直线平行, 则该直线与此平面平行
         符号语言: $a \nsubseteq \alpha \quad b \subset \alpha \quad a \parallel b \rArr a \parallel \alpha$
   定理3 判定定理(平面与平面): 一个平面内的两条相交直线与另一个平面平行, 则这两个平面平行
         符号语言: $a \subset \alpha \quad b \subset \alpha \quad a \cap b = p \quad a \parallel \beta,\, b \parallel \beta \rArr \beta \parallel \alpha$
   定理4 性质定理(直线与平面): 一条直线与一个平面平行, 则过这条直线的任一平面与此平面的交线与该直线平行
         符号语言: $a \parallel \alpha \quad a \subset \beta \quad \alpha \cap \beta = b \rArr a \parallel b$
   定理5 性质定理(平面与平面): 如果两个平行平面同时与第三个平面相交, 那么它们的交线平行
         符号语言: $\alpha \parallel \beta \quad \alpha \cap \gamma = a \quad \beta \cap \gamma = b \rArr a \parallel b$
2. 直线\平面垂直的判定
   定理6 判定定理(直线与平面): 一条直线与另一个平面内的两条相交直线垂直, 则该直线与此平面垂直
         符号语言: $a \perp b \quad a \perp c \quad b \subset \alpha \quad c \subset \alpha \quad b \cap c = p \rArr a \perp \alpha$
   定理7 判定定理(平面与平面): 一个平面过另一个平面的垂线, 则这两个平面垂直
         符号语言: $a \perp \alpha \quad a \subset \beta \rArr \alpha \perp \beta$
   定理8 性质定理(直线与平面): 垂直于同一平面的两条直线平行
         符号语言: $a \perp \alpha \quad b \perp \alpha \rArr a \parallel b$
   定理9 性质定理(平面与平面): 两个平面垂直, 则一个平面内垂直于交线的直线与另一个平面垂直
         符号语言: $\alpha \perp \beta \quad a \subset \alpha \quad \alpha \cap \beta = b \quad a \perp b \rArr a \perp \beta$
