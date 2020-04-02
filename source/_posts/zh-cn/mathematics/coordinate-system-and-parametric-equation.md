---
title: coordinate-system-and-parametric-equation
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-03-31 15:55:11
tags:
---

## 坐标系

### 伸缩变换

<u>伸缩变换</u>: 设点 $P(x, y)$ 是平面直角坐标系中的任意一点, 在变换
$$\varphi\begin{cases}
    x'= \lambda\cdot x \qquad &(\lambda < 0) \\
    y = \mu\cdot y &(\mu > 0)
\end{cases}
$$
的作用下, 点 $P(x, y)$ 对应到点 $P'(x', y')$ 称<u> $\varphi$ 为平面直角坐标系中的坐标伸缩变换</u>, 简称伸缩变换

经过伸缩变换后得到一条关于 $x', y'$ 的曲线方程, 最后要将 $x', y'$ 分别转化为具有普遍意义的 $x, y$, 得到一条关于 $x, y$ 的全新的曲线方程.

### 极坐标

<u>极坐标</u>: 在平面内取一个定点O, 叫做<u>极点</u>, 自极点O引一条射线OX, 叫做<u>极轴</u>, 再确定单位长度\角度单位. 及其正方向. 这样就建立了一个极坐标系.

一般地, 极坐标 $(P, \theta)$ 与 $(P, \theta + 2k\pi)(k \in Z)$ 表示同一个点. 特别地, 极点 O 的坐标为 $(0, \theta) (\theta \in R)$. 和直角坐标系不同, 平面内一个点的极坐标有无数种表示

1. 极坐标与直角坐标的互允公式
   1. 互化公式的应用条件:
   1. 极点与直角坐标系的原点重合
   2. 极轴与直角坐标系的x轴正半轴重合
   3. 两个坐标系的单位长度相同

2. 极坐标化为直角坐标 $\begin{cases}
    x=\rho\cos\theta \\
    y=\rho\sin\theta
\end{cases}$
   直角坐标化为极坐标: $\begin{cases}
       \rho^2=x^2 + y^2 \\
       \tan\theta=\frac{y}{x}
   \end{cases}$

极坐标内两点的距离公式: $\begin{aligned}
    &若 A(\rho_1, \theta_1) \quad B(\rho_2, \theta_2),\, 则 \\
    &|AB|=\sqrt{\rho_1^2+\rho_2^2=2\rho_1\rho_2\cos(\theta_1-\theta_2)}
\end{aligned}$

求某些题目给出相关信息求极坐标方程可用直角三角形中三边的函数关系进行求解. 取要求的曲线上任一点设为 $M(\rho, \theta)$. 结合题意表示出关于变量 $\rho, \theta$ 的极坐标方程, 即为题目所求的极坐标方程.

圆心为 $(\rho_0, \theta_0)$ 半径为 $r$.
则圆的极坐标方程为 $\rho^2+\rho_0^2-2\rho_0\rho\cos(\theta-\theta_0)=r^2$

过点 $P(\rho_1, \theta_1)$ 且与极轴所成的角为 $\alpha$ 的直线的极坐标方程为 $\rho\sin(\alpha-\theta)=\rho_1\sin(\alpha-\theta_1)$

### 柱坐标/球坐标

柱坐标: 在极坐标的基础上增加垂直于此平面的$Oz$轴, 类似一条圈起来的纸带,某一点P坐标为$(\rho, \theta, z) z为点P在z轴高度$

球坐标: 类似于地球经纬度, 某点P坐标$(r, \theta, \varphi)$, 其中$r$为矢径, $\theta$ 为纬度, $\varphi$为经度. xOz中, 一般极轴Oz朝上, Ox水平

## 参数方程

参数方程的求法:
1. 建系, 设点 $(x, y)$
2. 选取参数
3. 求出 $x, y$ 与参数之间的表达式
4. 结论


参数方程化为普通方程: 要把参数消去, 还要注意 $x, y$ 的取值范围, 即在消去参数的过程中一定要注意普通方程与参数方程的等价性.
常用的消参技巧: 带入消元, 加减消元, 平方和差消元, 三角恒等式消元等
常用消参公式: $\sin^2\alpha+\cos^2\alpha=1 \qquad (t+\frac{1}{t})^2-(t-\frac{1}{t})^2=4$

### 直线的参数方程

经过点 $P_0(\rho_0, \theta_0)$, 且倾斜角为 $\alpha$ 的直线的标准参数方程为 $\begin{cases}
    x=x_0+t\cos\alpha \quad  (t为参数)\\
    y=y_0+t\sin\alpha
\end{cases}$
其中, 参数t的几何意义是在有向线段 $P_0P$的位置下标. 即 $|t|=P_0P$

另一种
直线过 $(x_0, y_0),\, \begin{cases}
    x=x_0+at \quad (t为参数) \quad &当 a^2+b^2=1 时.\, t=|M_0M| \\
    y=y_0+bt &当 a^2+b^2\neq1 时.\, t无明确意义
\end{cases}$

### 圆的参数方程

圆心坐标为 $M(a, b)$, 半径 $r_0$. 以圆心为顶点且与x轴同向的射线按逆时针方向旋转到与圆上一点所在半径成的角 $\alpha$ 为参数的圆
的参数方程为:
$$\begin{cases}
    x=a+r\cos\alpha \quad (\alpha为参数,\, \alpha \in [0, x]) \\
    y=b+r\sin\alpha
\end{cases}
$$

### 圆锥曲线的参数方程

#### 椭圆

$$
\begin{aligned}
    &\frac{x^2}{a^2}+\frac{y^2}{b^2}=1 \quad (a>b>0) \, 的一个参数方程为
    \begin{cases}
        x=a\cos\varphi \quad &(\varphi为参数) \, (a>b>0) \\
        y=b\sin\varphi &焦点在x轴
    \end{cases} \\ 
    &\frac{x^2}{b^2}+\frac{y^2}{a^2}=1 \quad (a>b>0) \, 的一个参数方程为
    \begin{cases}
        x=b\cos\varphi \quad &(\varphi为参数) \, (a>b>0) \\
        y=a\sin\varphi &焦点在y轴
    \end{cases}
\end{aligned}
$$

#### 双曲线

$$
\begin{aligned}
    &\frac{x^2}{a^2}-\frac{y^2}{b^2}=1 \quad (a,b>0) \, 的一个参数方程为
    \begin{cases}
        x=a\sec\varphi \quad &(\varphi为参数) \, (a,b>0) \quad \rArr x=\frac{a}{\cos\varphi} \\
        y=b\tan\varphi &焦点在x轴
    \end{cases} \\
    &\frac{x}{a^2}-\frac{y}{b^2}=1 \quad (a,b>0) \, 的一个参数方程为
    \begin{cases}
        x=b\tan\varphi \quad &(\varphi为参数) \, (a,b>0) \\
        y=a\sec\varphi &焦点在y轴 \quad \rArr y=\frac{a}{\cos\varphi}
    \end{cases}
\end{aligned}
$$

#### 抛物线

$$
y^2=2px \, 的一个参数方程
\begin{cases}
    x=2pt^2 \quad (t为参数) \\
    y=2pt
\end{cases}
$$

### 平摆线\渐开线

平摆线: 某一个车轮上的一点P因车轮滚动而绘制的轨迹(或称旋轮线)
车轮周上一点P的轨迹的参数方程是 $\begin{cases}
    x=r(\theta-\sin\theta) \\
    y=r(1-\cos\theta)
\end{cases}$

渐开线: 一条动直线(发生线)沿着一个固定的圆(基圆)作纯滚动时，此动直线上一点的轨迹
参数方程为$\begin{cases}
    x=r(\cos\theta+\theta\sin\theta) \\
    y=r(\sin\theta-\theta\cos\theta)
\end{cases}$