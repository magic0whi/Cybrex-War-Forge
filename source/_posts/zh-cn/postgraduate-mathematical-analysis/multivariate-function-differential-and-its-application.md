---
title: multivariate-function-differential-and-its-application
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:00:56
tags:
toc: true
---

## 多元函数的基本概念

### 平面点集

平面点集中的:
1. 邻域 TODO: 补充图片
   \\(M_0(x_0, y_0)\in D\\) , 取 \\(\delta>0\\)
   1. 领域:
      称 \\(\\{(x, y)|\sqrt{(x-x_0)^2+(y-y_0)^2}<\delta\\}\\) 为 \\(M_0\\) 的 \\(\delta\\) 邻域
      记 \\(U(M_0, \delta)\\)
   2. 去心邻域:
      称 \\(\\{(x, y)|0<\sqrt{(x-x_0)^2+(y-y_0)^2}<\delta\\}\\) 为 \\(M_0\\) 的去心 \\(\delta\\) 邻域
      记 \\(\mathring{U}(M_0, \delta)\\)
2. 开集
   设 D 为 xOy 面上的点集,
   \\(\forall M_0(x_0, y_0)\in D\\) ,
   有 \\(\exist\delta>0\\) , 使 \\(U(M_0, \delta) \subset D\\) , 称 D 为开集
   若能取到边界上, 则称 D 为闭集
3. 区域: 连通的开集称为区域(开区域)
   闭区域: 开区域连同边界称为闭区域(或者说连通的闭集)

### 多元函数的概念

(空间中的一个曲面)
D 为区域, x, y, z 为变量, 若 \\(\forall(x, y)\in D\\)
\\(\exist z\\) 与 (x, y) 对应, 称 z 为 (x, y) 的函数, 记 \\(z=f(x, y)\\)
D 为定义域, 值域 \\(R=\\{z|z=f(x, y), (x, y)\in D\\}\\)

### 多元函数的极限

回顾一下一元函数极限定义:
\\(y=f(x) , (x\in D)\\) ,
若 \\(\forall\varepsilon>0\\) ,
\\(\exist\delta>0\\) , 当 \\(0<|x-x_0|<\delta\\) 时, 有 \\(|f(x)-A|<\varepsilon\\)
称 A 为 f(x) 当 \\(x\to x_0\\) 的极限, 记 \\(\lim\limits_{x\to x_0}f(x)=A\\)

二元函数极限定义:
设 \\(z=f(x, y) , ((x, y)\in D)\\) , \\(M_0(x_0, y_0)\\) ,
若 \\(\forall\varepsilon>0\\) ,
\\(\exist\delta>0\\) , 当 \\(0<\sqrt{(x-x_0)^2-(y-y_0)^2}<\delta\\) 时, 有 \\(|f(x, y)-A|<\varepsilon\\)
称 A 为 \\(f(x, y)\\) 当 \\((x, y)\to(x_0, y_0)\\) 的极限, 记 \\(\lim\limits_{\substack{x\to x_0 \\\ y\to y_0}}f(x, y)=A\\)

### 多元函数连续性与性质

定义
\\(z=f(x, y) \enspace((x, y)\in D\\) , \\(M_0(x_0, y_0)\in D\\)
若 \\(\lim\limits_{\substack{x\to x_0 \\\ y\to y_0}}f(x, y)=f(x_0, y_0)\\) , 称 \\(f(x, y)\\) 在 \\((x_0, y_0)\\) 处连续

### 多元函数在有界闭区域上的性质

设 D 为 闭区域 , 若 \\(\exist R>0\\) ,
使 \\(D=\\{(x, y)|x^2+y^2<R\\}\\)
称 D 为有界闭区域

1. 最值定理
   设 D 为有界闭区域, f(x, y) 在 D 上连续
   则 f(x, y) 在 D 上取到最小值 m 和最大值 M
2. 有界定理
   设 D 为有界闭区域, f(x, y) 在 D 上连续
   则 \\(\exist k>0 , \forall(x, y)\in D\\) , 有 \\(|f(x, y)|\leqslant k\\)
3. 界值定理
   f(x, y) 在 D 上连续, 
   则 \\(\exist下界m和上界M , \forall\delta\in[m, M]\\) ,
   \\(\exist(\xi, n)\in D\\) 使 \\(f(\xi, n)=\delta\\)

## 偏导数

### 定义

\\(z=f(x, y) \enspace((x, y)\in D), M_0(x_0, y_0)\in D\\)

1. 偏增量
   * f(x, y) 在 \\(M_0\\) 处关于 x 的偏增量 \\(\Delta z_x=f(x_0+\Delta x, y_0)-f(x_0, y_0) \enspace(=f(x, y_0)-f(x_0, y_0))\\)
   * f(x, y) 在 \\(M_0\\) 处关于 y 的偏增量 \\(\Delta z_y=f(x_0, y_0+\Delta y)-f(x_0, y_0) \enspace(=f(x_0, y)-f(x_0, y_0))\\)
   * f(x, y) 在 \\(M_0\\) 处的全增量 \\(\Delta z=f(x_0+\Delta x, y_0+\Delta y)-f(x_0, y_0) \enspace(=f(x, y)-f(x_0, y_0))\\)
2. 偏导数
   * 若 \\(\lim\limits_{\Delta x\to0}\frac{\Delta z_x}{\Delta x}\\) 存在
     称 f(x, y) 在 \\(M_0\\) 处关于 x 可偏导, 
     该极限称为 f(x, y) 在 \\(M_0\\) 处关于 x 的偏导数, 记 \\(f_x^'(x_0, y_0)\\) 或 \\(\frac{\partial z}{\partial x}|_{(x_0, y_0)}\\)
   * 若 \\(\lim\limits_{\Delta y\to0}\frac{\Delta z_y}{\Delta y}\\) 存在
     称 f(x, y) 在 \\(M_0\\) 处关于 y 可偏导,
     该极限称为 f(x, y) 在 \\(M_0\\) 处关于 y 的偏导数, 记 \\(f_y^'(x_0, y_0)\\) 或 \\(\frac{\partial z}{\partial y}|_{(x_0, y_0)}\\)
   * 若 \\(\forall(x, y)\in D\\) , f(x, y) 对 x, y 皆可偏导, 称 \\(f_x^'(x, y) , f_y^'(x, y)\\) 为 f(x, y) 对 x, y 的偏导数

(求偏导数时, 其余参数视为常数)

### 高阶偏导数

定义:
设\\(z=f(x, y)\\) 在 D 内对 x, y 可偏导,
\\(\frac{\partial z}{\partial x}=f_x^'(x, y)\\) 为 f(x, y) 对 x 偏导数,
\\(\frac{\partial z}{\partial y}=f_y^'(x, y)\\) 为 f(x, y) 对 y 偏导数.
1. * 若 \\(f_x^'(x, y)\\) 对 x 可偏导, 其对 x 的偏导数称为 f(x, y) 对 x 的二阶偏导数, 记 \\(f_{xx}^{''}\\) 或 \\(\frac{\partial^2z}{\partial x^2}\\)
   * 若 \\(f_y^'(x, y)\\) 对 y 可偏导, 其对 y 的偏导数称为 f(x, y) 对 y 的二阶偏导数, 记 \\(f_{yy}^{''}\\) 或 \\(\frac{\partial^2z}{\partial y^2}\\)
2. * 若 \\(f_x^'(x, y)\\) 对 y 可偏导, 其对 y 的偏导数称为 f(x, y) 对先x后y的二阶混合偏导数, 记 \\(f_{xy}^{''}(x, y)\\) 或 \\(\frac{\partial^2z}{\partial x\partial y}\\)
   * 若 \\(f_y^'(x, y)\\) 对 x 可偏导, 其对 x 的偏导数称为 f(x, y) 对先y后x的二阶混合偏导数, 记 \\(f_{yx}^{''}(x, y)\\) 或 \\(\frac{\partial^2z}{\partial y\partial x}\\)

定理:
若 z=f(x, y) 的二阶混合偏导数 \\(\frac{\partial^2z}{\partial x\partial y} , \frac{\partial^2z}{\partial y\partial x}\\) 皆连续,
则 \\(\frac{\partial^2z}{\partial x\partial y}=\frac{\partial^2z}{\partial y\partial x}\\) ,
即 \\(f_{xy}^{''}=f_{yx}^{''}\\)

## 全微分

### 二元函数全微分定义

设 \\(z=f(x, y) \enspace((x, y)\in D)\\) , \\(M_0(x_0, y_0)\in D\\)
全增量 \\(\Delta z=f(x_0+\Delta x, y_0+\Delta y)-f(x_0, y_0) \enspace(=f(x, y)-f(x_0, y_0))\\)
若 \\(\Delta z=A\Delta x+B\Delta y+\circ(\rho)\\) , \\(\rho=\sqrt{(\Delta x)^2+(\Delta y)^2}\\)
称 f(x, y) 在 \\((x_0, y_0)\\) 处可全微
称 \\(A\Delta x+B\Delta y\\) 为 f(x, y) 在 \\(x_0, y_0\\) 处的全微分, 记 \\(dz|_{(x_0, y_0)}=Adx+Bdy\\)

结合偏导数:
\\(dz|_{(x_0, y_0)}=f_x^'(x_0, y_0)dx+f_y^'(x_0, y_0)dy\\)
\\(dz=\frac{\partial z}{\partial x}dx+\frac{\partial z}{\partial y}dy\\)

### 结论

设 \\(z=f(x, y) \enspace((x, y)\in D)\\) , \\(M_0(x_0, y_0)\in D\\)
1. 若 f(x, y) 在 \\(M_0\\) 处可微, 则 f(x, y) 在 \\(M_0\\) 连续, 反之不对
2. 若 f(x, y) 在 \\(M_0\\) 处可微, 则 f(x, y) 在 \\(M_0\\) 可偏导, 反之不对
3. (可微充分条件) 若 z=f(x, y) 的偏导数 \\(\frac{\partial z}{\partial x}\\) , \\(\frac{\partial z}{\partial y}\\) 连续(或连续可偏导) , 则 f(x, y) 可微

## 多元复合函数求导法则

1. 情形一: \\(z=f(u, v) \enspace\begin{cases} u=\varphi(t) \\\ v=\psi(t) \end{cases} \rArr z=f[\varphi(t), \psi(t)]\\)
   z=f(u, v) 关于 u,v 连续可偏导, \\(\varphi(t) , \psi(t)\\) 可导
   则 \\(z=f[\varphi(t), \psi(t)]\\) 可导,
   且 \\(\frac{dz}{dt}=\frac{\partial f}{\partial u}\cdot\frac{du}{dt}+\frac{\partial f}{\partial v}\cdot\frac{dv}{dt}=f_{u}'\cdot\varphi(t)'+f_{v}'\cdot\psi'(t)\\)
   证明:
   \\(\Delta u=\varphi(t+\Delta t)-\varphi(t)\\)
   \\(\Delta v=\psi(t+\Delta t)-\psi(t)\\)
   \\(\because z=f(u, v)\\) 关于 u,v 连续可偏导
   \\(\therefore z=f(u, v)\\) 可微
   \\(\Delta z=\frac{\partial f}{\partial u}\Delta u+\frac{\partial f}{\partial v}\Delta v+\circ(\rho)\\) , \\(\rho=\sqrt{(\Delta u)^2+(\Delta v)^2}\\)
   \\(\rArr \frac{\Delta z}{\Delta t}=\frac{\partial f}{\partial u}\frac{\Delta u}{\Delta t}+\frac{\partial f}{\partial v}\frac{\Delta v}{\Delta t}+\frac{\circ(\rho)}{\Delta t}\\)
   \\(\rArr \frac{dz}{dt}=\frac{\partial f}{\partial u}\cdot\frac{du}{dt}+\frac{\partial f}{\partial v}\cdot\frac{dv}{dt}\\)
2. 情形二: \\(z=f(u, v) \enspace\begin{cases} u=\varphi(x, y) \\\ v=\psi(x, y) \end{cases} \rArr z=f[\varphi(x, y), \psi(x,  y)]\\)
   z=f(u, v) 关于 u,v 连续可偏导, \\(\begin{cases} u=\varphi(x, y) \\\ v=\psi(x, y) \end{cases}\\) 对 (x, y) 可偏导
   则 \\(z=f[\varphi(x, y), \psi(x, y)]\\) 关于 x, y 可偏导,
   且
   \\(\frac{\partial z}{\partial x}=\frac{\partial f}{\partial u}\cdot\frac{\partial u}{\partial x}+\frac{\partial f}{\partial v}\cdot\frac{\partial v}{\partial x}\\) ,
   \\(\frac{\partial z}{\partial y}=\frac{\partial f}{\partial u}\cdot\frac{\partial u}{\partial y}+\frac{\partial f}{\partial v}\cdot\frac{\partial v}{\partial y}\\)

## 隐函数求导法则

### 一个约束条件的情形

隐函数: f(x, y)=0
隐函数显式化 \\(f(x, y)=0 \rArr y=\varphi(x)\\)

1. 定理一:
   设 \\(F(x, y)\\) 在点 \\(M_0(x_0, y_0)\\) 邻域内连续可偏导且 \\(F(x_0, y_0)=0\\) ,
   若 \\(F_y^'(x_0, y_0)\neq0 \enspace\\) (表示y方向上连续),
   则由 \\(F(x, y)=0\\) 在 \\(M_0\\) 邻域内确定唯一连续可导函数 \\(y=f(x)\\) ,
   使 \\(y_0=f(x_0) , \dfrac{dy}{dx}=-\dfrac{F_x'}{F_y'}\\)
   证明:
   \\(F(x, y)=0\\) , 把 y 看成 x 的函数 \\(\varphi(x)\\) , 则 \\(F(x, \varphi(x))=0\\)
   两边对 x 求导, \\(F_x^'+F_y^'\frac{dy}{dx}=0 \rArr \frac{dy}{dx}=-\frac{F_x'}{F_y'}\\)
2. 定理二:
   设 \\(F(x, y, z)\\) 在 \\(M_0(x_0, y_0, z_0)\\) 邻域内连续可偏导且 \\(F(x_0, y_0, z_0)=0\\)
   若 \\(F_z^'(x_0, y_0, z_0)\neq0 \enspace\\) (表示z方向上连续),
   则由 \\(F(x, y, z)=0\\) 在 \\(M_0\\) 邻域内确定唯一连续可偏导函数 \\(z=\varphi(x, y)\\) ,
   使 \\(z_0=\varphi(x_0, y_0)\\) , \\(\dfrac{\partial z}{\partial x}=-\dfrac{F_x'}{F_z'}\\) , \\(\dfrac{\partial z}{\partial y}=-\dfrac{F_y'}{F_z'}\\)
   证明:
   \\(F(x, y, z)=0 \rArr z=\varphi(x, y)\\) , 把 z 看成 x 的函数 \\(\varphi(x)\\) , 则 \\(F(x, y, \varphi(x))=0\\)
   两边对 x 求偏导, \\(F_x'+F_z'\frac{\partial z}{\partial x}=0 \rArr \frac{\partial z}{\partial x}=-\frac{F_x'}{F_z'} \enspace\\)
   两边对 y 求偏导, \\(F_y'+F_z'\frac{\partial z}{\partial y}=0 \rArr \frac{\partial z}{\partial y}=-\frac{F_y'}{F_z'}\\)

## 多元函数微分学的几何应用

### 空间曲线

(空间曲线有切线和法平面)

\\(M_0(x_0, y_0, z_0)\in L\\)
\\(M(x_0+\Delta x, y_0+\Delta y, z_0+\Delta z)\in L\\)
\\(\overrightarrow{M_0M}=\\{\Delta x, \Delta y, \Delta z\\}\\)
直线 \\(\overline{M_0M}: \frac{x-x_0}{\Delta x}=\frac{y-y_0}{\Delta y}=\frac{z-z_0}{\Delta z}\\)

1. 情况一 \\(L: \begin{cases} x=\varphi(t) \\\ y=\psi(t) \\\ z=\omega(t) \end{cases} , t=t_0 \rArr M_0(x_0, y_0, z_0)\in L\\)
   \\(t=t_0+\Delta t \rArr M(x_0+\Delta x, y_0+\Delta y, z_0+\Delta z)\in L\\)
   \\(\overline{M_0M}=\frac{x-x_0}{\Delta x}=\frac{y-y_0}{\Delta y}=\frac{z-z_0}{\Delta z} \hArr \frac{x-x_0}{\frac{\Delta x}{\Delta t}}=\frac{y-y_0}{\frac{\Delta y}{\Delta t}}=\frac{z-z_0}{\frac{\Delta z}{\Delta t}}\\)
   当 \\(\Delta t\to0\\) 时, \\(\overline{M_0M}\\) 即为切线
   \\(\therefore 切线: \frac{x-x_0}{\varphi'(t_0)}=\frac{y-y_0}{\psi'(t_0)}=\frac{z-z_0}{\omega'(t_0)}\\)
2. 情况二 \\(L: \begin{cases} F(x, y, z)=0 \\\ G(x, y, z)=0 \end{cases} , M_0(x_0, y_0, z_0)\in L\\)
   \\(\vec{T}=\\{F_y'G_z'-F_z'G_y', F_z'G_x'-F_x'G_z', F_x'G_y'-F_y'G_x'\\}\\)
   若将 \\(M_0\\) 代入 \\(\vec{T}=\\{a, b, c\\}\\) , 则
   切线 \\(\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}\\)
   法平面 \\(a(x-x_0)+b(y-y_0)+c(z-z_0) \enspace\\) (平面的点法式方程, 法平面指在该点垂直于切线的平面)

### 空间曲面

(曲面有切平面和法线)

求空间曲面上某一点的法向量:
曲面 \\(\Sigma: F(x, y, z)=0 \enspace M_0(x_0, y_0, z_0)\in\Sigma\\)
在 \\(\Sigma\\) 内过 \\(M_0\\) 任取一曲线 L
\\(L: \begin{cases} x=\varphi(t) \\\ y=\psi(t) \\\ z=\omega(t) \end{cases} \enspace M_0 \harr t=t_0\\)
\\(\because L\subset\Sigma\\)
\\(\therefore F[\varphi(t), \psi(t), \omega(t)]=0\\)
两边对 t 求导得 \\(F_x'[\varphi(t), \psi(t), \omega(t)]\cdot\varphi'(t)+F_y'[\varphi(t), \psi(t), \omega(t)]\psi'(t)+F_z'[\varphi(t), \psi(t), \omega(t)]\omega'(t)=0 \enspace\\) (使用多元复合函数求导情形一)
将 \\(t=t_0\\) 代入
\\(F_x'(x_0, y_0, z_0)\varphi'(t_0)+F_y'(x_0, y_0, z_0)\psi'(t_0)+F_z'(x_0, y_0, z_0)\omega'(t_0)=0\\)
可化为两个向量点乘 \\(\\{F_x', F_y', F_z'\\}_{M_0}\cdot\\{\varphi'(t_0), \psi'(t_0), \omega'(t_0)\\}=0\\)

因此法向量 \\(\vec{n}=\\{F_x', F_y', F_z'\\}_{M_0}\\)

## 方向导数与梯度

### 方向导数

1. 定义
   1. 二元函数
      TODO: 补充图片
      设 \\(z=f(x, y) \enspace((x, y)\in D)\\) , \\(M_0(x_0, y_0)\in D\\)
      在 xOy 面内过 \\(M_0\\) 作射线 L,
      取 \\(M(x_0+\Delta x, y_0+\Delta y)\in L\\) , \\(\rho=\sqrt{(\Delta x)^2+(\Delta y)^2}\\)
      \\(\Delta z=f(x_0+\Delta x, y_0+\Delta y)-f(x_0, y_0)\\)
      若 \\(\lim\limits_{\rho\to0}\frac{\Delta z}{\rho}\\) 存在,
      称此极限为函数 \\(z=f(x, y)\\) 在 \\(M_0\\) 处沿射线 L 的方向导数, 记 \\(\dfrac{\partial z}{\partial L}|_{M_0}\\)
   2. 三元函数
      设 \\(u=f(x, y, z) \enspace((x, y, z)\in\Omega)\\) , \\(M_0(x_0, y_0, z_0)\in\Omega\\)
      过 \\(M_0\\) 作射线 L,
      取 \\(M(x_0+\Delta x, y_0+\Delta y, z_0+\Delta z)\in L\\) , \\(\rho=\sqrt{(\Delta x)^2+(\Delta y)^2+(\Delta z)^2}\\)
      \\(\Delta u=f(x_0+\Delta x, y_0+\Delta y, z_0+\Delta z)-f(x_0, y_0, z_0)\\)
      若 \\(\lim\limits_{\rho\to0}\frac{\Delta u}{p}\\) 存在, 称此极限为 \\(u=f(x, y, z)\\) 在 \\(M_0\\) 处沿射线 L 的方向导数, 记 \\(\frac{\partial u}{\partial L}|_{M_0}\\)
2. 方向导数计算方法
   1. \\(z=f(x, y)\\) 在 \\(M_0(x_0, y_0)\\) 可微,
      TODO:补充图片
      在 xOy 面内过 \\(M_0\\) 作射线 L , 方向角为 \\(\alpha, \beta\\) ,
      则 \\(\frac{\partial z}{\partial L}|_{M_0}=f_x'(x_0, y_0)\cdot\cos\alpha+f_y'(x_0, y_0)\cos\beta\\)
      
      证明:
      xOy 面内直线 L 的方向向量为 \\(\\{\cos\alpha, \cos\beta\\} \enspace\\) (向量的方向余弦)
      可得直线 L 的参数方程 \\(L: \begin{cases} x=t\cos\alpha \\\ y=t\cos\beta \end{cases}\\)
      代入 f(x, y) 关于 t 求导得 \\(\frac{\partial z}{\partial L}=f_L'(t\cos\alpha, t\cos\beta)=f_{x}'\cdot(t\cos\alpha)'+f_{y}\cdot(t\cos\beta)'=f_x'\cdot\cos\alpha+f_y'\cdot\cos\beta\\)
   2. \\(u=f(x, y, z\\) 在 \\(M_0(x_0, y_0, z_0)\\) 可微,
      过 \\(M_0\\) 作射线 L , 方向角为 \\(\alpha, \beta, \gamma\\) ,
      则 \\(\frac{\partial u}{\partial L}|\_{M\_0}=\frac{\partial u}{\partial x}|\_{M\_0}\cos\alpha+\frac{\partial u}{\partial y}|\_{M\_0}\cos\beta+\frac{\partial u}{\partial z}|\_{M\_0}\cos\gamma\\)

### 梯度

\\(u=f(x, y, z)\\) , \\(M_0(x_0, y_0, z_0)\in\Omega\\) , 过 \\(M_0\\) 作射线 L, 方向角为 \\(\alpha, \beta, \gamma\\)
\\(\frac{\partial u}{\partial L}|\_{M\_0}=\frac{\partial u}{\partial x}|\_{M\_0}\cos\alpha+\frac{\partial u}{\partial y}|\_{M\_0}\cos\beta+\frac{\partial u}{\partial z}|\_{M\_0}\cos\gamma\\)
上式可分离为两个向量点乘:
\\(\frac{\partial u}{\partial L}|\_{M\_0}=\\{\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial u}{\partial z}\\}|\_{M\_0}\cdot\\{\cos\alpha, \cos\beta, \cos\gamma\\}\\)

这两个向量中前者称作梯度, 即函数u的梯度:
\\(\text{grad}u=\\{\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial u}{\partial z}\\}|\_{M\_0}\\)

后者是与 L 同向的单位向量, 设其为 \\(\vec{e}\\)
则 \\(\frac{\partial u}{\partial L}|\_{M\_0}=\text{grad}u\cdot\vec{e}=\sqrt{(\frac{\partial u}{\partial x})^2+(\frac{\partial u}{\partial y})^2+(\frac{\partial u}{\partial z})^2}\cdot1\cdot\cos\theta \enspace\\) (\\(\theta\\) 为梯度u 与 \\(\vec{e}\\) 间的夹角)
由该式可知当 \\(\cos\theta=1\\) , 即 \\(\theta=0\\) 时, \\(\frac{\partial u}{\partial L}|\_{M\_0}\\) 取最大值, 即这个点方向导数取最大值
因此**梯度的方向即函数增大速度最快的方向, 或方向导数取最大值的方向**


## 代数应用 -- 多元函数的极值