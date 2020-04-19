---
title: momentum-and-collision
lang: zh-cn
category: physics
mathjax: 'true'
date: 2020-04-09 12:21:52
tags:
---

## 动量与碰撞

### 动量

定义: 物体由于受力而具有的能量叫动量
(由此定义可得 $\exist p \larr \exist E_k$ 注:必要不充分条件)

(由下面的动量定理得到动量表达式)
动量: $p=mv$ , 单位: 千克米每秒, $\text{kg}\cdot\text{m/s}$

动量是矢量

### 动量定理

动量定理: 物体的动量变化量等于力对物体做的冲量(力与时间的乘积)

表达式(联立牛顿第二定律, 加速度定义式可得): $Ft=mv_1-mv_0 \lArr I=F\varDelta t=ma\varDelta t=m\dfrac{v_1-v_0}{\varDelta t}\varDelta t=mv_1-mv_0=\varDelta p$ , 其中 $I$ 代表冲量


动量与动能关系(将动能定义带入动量定义得到): $p=\sqrt{2mE_k} \hArr E_k=\dfrac{p^2}{2m}$

基于**受力位移**的能量计量方法----动能定理
基于**受力时间**的能量计量方法----动量定理

### 动量守恒定律

内容: 如果一个系统不受外力或者外力的矢量和为零, 这个系统的总动量保持不变, 表达式 $p_总=p_1+p_2$

逻辑关系: 机械能守恒 $\rarr$ 动量守恒 $\rarr$ 能量守恒

### 碰撞

(动能定理不适合探讨碰撞这种受力位移很小难以测量的情况, 于是就需要基于受力时间的能量计量方法----动量定理来解决)

* 弹性碰撞
  $$\begin{cases}
      p_1+p_2=p_1'+p_2' &\rArr m_1v_1+m_2v_2=m_1v_1'+m_2v_2' \\
      E_{k总}=E_{k1}+E_{k2}=E_{k1}'+E_{k2}' &\rArr \dfrac{1}{2}m_1v_1^2+\dfrac{1}{2}m_2v_2^2=\dfrac{1}{2}m_1v_1'^2+\dfrac{1}{2}m_2v_2'^2
  \end{cases}
  $$
* 非弹性碰撞(机械能不守恒)
  $$\begin{cases}
    m_1v_1+m_2v_2=m_1v_1'+m_2v_2' \\
    \varDelta E_{k总}=(\dfrac{1}{2}m_1v_1^2+\dfrac{1}{2}m_2v_2^2)-(\dfrac{1}{2}m_1v_1'^2+\dfrac{1}{2}m_2v_2'^2)
  \end{cases}
  $$
* 完全非弹性碰撞(物体1"沾"在物体2上, **碰撞后两物体速度相等**; 机械能损失最大)
  $$\begin{cases}
    m_1v_1+m_2v_2=(m_1+m_2)v \\
    \varDelta E_{k总}=(\dfrac{1}{2}m_1v_1^2+\dfrac{1}{2}m_2v_2^2)-\dfrac{1}{2}(m_1+m_2)v^2
  \end{cases}
  $$