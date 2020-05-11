---
title: universal-gravitation
lang: zh-cn
category: physics
mathjax: 'true'
date: 2020-04-09 12:26:12
tags:
toc: true
---

## 万有引力

### 万有引力定律

公式: \\(F=G\dfrac{m_1m_2}{r^2}\\) , 其中 \\(G\approx 6.67\times10^{-11}\\)

推导过程:
设行星椭圆轨道半长轴距离为 \\(r\\), 行星质量为 \\(m\\), 行星线速度为 \\(v\\)
1. 首先需要知道开普勒第三定律(周期定律):
   椭圆轨道半长轴的三次方与它的公转周期二次方的比值是个常数 \\(\rArr k=\dfrac{r^3}{T^2} \qquad(1)\\)
2. 圆周运动中: 线速度 \\(v=\omega r=\dfrac{2\pi}{T}r \qquad(2)\\)
3. 最后由向心力公式: \\(F=m\dfrac{v^2}{r} \enspace\underrightarrow{带入(2)式以消去v}\enspace F=\dfrac{4\pi^2mr}{T^2} \enspace\underrightarrow{带入(1)式以消去T}\enspace F=\dfrac{4\pi^2km}{r^2} \enspace\underrightarrow{讨论, 确定变量r,m. 消去常数项(4\pi^2k)} F\propto \dfrac{m}{r^2}\\)
4. 由牛顿第三定律: 行星也对太阳有吸引力 \\(F\propto\dfrac{m}{r^2} \hArr  F'\propto\dfrac{M}{r^2} \enspace\underrightarrow{F=F'}\enspace F\propto \dfrac{mM}{r^2}\\) , \\(M\\) 为太阳质量
5.  一般认为太阳的质量是常量, 有 \\(G=\dfrac{4\pi^2k}{M}\\) , 得到万有引力公式 \\(F=G\dfrac{mM}{r^2}\\)

### 第二和第三宇宙速度

无论是第一第二第三宇宙速度指的都是初始逃逸速度, 指的是发射物体射出去后不加外力, 一直做减速运动也能成功逃逸的最小速度

第一宇宙速度: \\(7.9 \enspace\text{km/s}\\) 绕地球做匀速圆周运动的最小速度. 具体推导见下面章节----环绕速度

第二宇宙速度: \\(11.2 \enspace\text{km/s}\\) 脱离地心引力所需的最小速度

第三宇宙速度: \\(16.7 \enspace\text{km/s}\\) 脱离太阳引力束缚成为自由天体

### 环绕速度

实际上, 第一宇宙速度就是卫星绕地球的最小环绕速度

思路: 万有引力作为圆周运动的向心力:
地表到地心的距离 \\(R=6.40\times 10^6\\) , 地球质量 \\(M=5.98\times10^{24}\\)
\\(G\dfrac{Mm}{R^2}=m\dfrac{v^2}{R}\rArr v=\sqrt{\dfrac{GM}{R}}=\sqrt{\dfrac{6.67 \times 10^{-11} \times 5.98\times10^{24}}{6.40\times 10^6}} \enspace \text{m/s}\\)

由上面的 \\(v=\sqrt{\dfrac{GM}{R}}\\) , 由于 \\(G\\) 和 \\(M\\) 是常量, 衍生得到速度与环绕半径为反比例关系 \\(v\propto\sqrt{\dfrac{1}{r}}\\)

### 经典时空观/相对论时空观

经典时空观: 也叫绝对时空观, 时空测量虽然是在参照系中进行的，但时空测量的结果在不同的参照系中却是相同的; 即时间和空间独立于不同的参照系之间, 是绝对的.

相对论时空观: 时间与空间也是相对的, 在不同参照系中时间与空间也不同. 唯有光速是绝对的.
