---
title: multiple-integral
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:03:22
tags:
---

重积分

<!-- more -->

## 二重积分的概念与性质

### 二重积分的定义

设 f(x, y) 在 xOy 面有限闭区域 D 内有界
1. D 划分为 \\(\Delta\sigma_1 , \Delta\sigma_2 , \dots , \Delta\sigma_n \\)
2. \\(\forall(\xi_i, \eta_i)\in\Delta\sigma_i\\)
   作 \\(\displaystyle\sum_{i=1}^n f(\xi_i, \eta_i)\Delta\sigma_i\\)
3. \\(\lambda\\) 为 \\(\Delta\sigma_1 , \Delta\sigma_2 , \dots , \Delta\sigma_n\\) 最大值
   若 \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n f(\xi_i , \eta_i)\Delta\sigma_i\\) 存在, 称此极限为 f(x, y) 在 D 上的二重积分, 记 \\(\iint_D f(x, y)d\sigma\\)

### 二重积分的性质

1. 设 \\(f(x, y) , g(x, y)\\) 在区域 D 上可积, 则
   \\(\iint_D[af(x, y)+bg(x, y)]d\sigma=a\iint_D f(x, y)d\sigma+b\iint_D g(x, y)d\sigma\\)
2. \\(D=D_1+D_2\\) 且 \\(D_1\cap D_2=\varnothing\\) , 则
   \\(\iint_D f(x, y)d\sigma=\iint_{D_1}f(x, y)d\sigma+\iint_{D_2}f(x, y)d\sigma\\)
3. \\(\iint_D 1d\sigma=A\\)
4. 1. 若 \\(f(x, y)\geqslant g(x, y) \enspace((x, y)\in D)\\) 则 \\(\iint_D f(x, y)d\sigma\geqslant\iint_D g(x, y)d\sigma\\)
   2. \\(f(x, y)\\) 和 \\(|f(x, y)|\\) 在 D 上可积, 则 \\(|\iint_D f(x, y)d\sigma|\leqslant\iint_D|f(x, y)|d\sigma\\)
5. 积分中值定理
   D 为有限闭区域, f(x, y) 在 D 上连续
   则 \\(\exist(\xi, \eta)\in D\\) , 使 \\(\iint_D f(x, y)d\sigma=f(\xi, \eta)A \quad\\) (A 为常数)
   证明:
   \\(\because f(x, y)\in c(D)\\)
   \\(\therefore f(x, y)\\) 在 D 上有上下界 \\(m, M\\) , 使 \\(m\leqslant f(x, y)\leqslant M\\)
   \\(\therefore mA\leqslant\iint_D f(x, y)d\sigma\leqslant MA\\)
   \\(\mskip{1em}\rArr m\leqslant\frac{1}{A}\iint f(x, y)d\sigma\leqslant M\\)
   \\(\mskip{1em}\exist(\xi, \eta)\in D\\) , 使 \\(f(\xi, \eta)=\frac{1}{A}\iint_D f(x, y)d\sigma \rArr \iint_D f(x, y)d\sigma=f(\xi, \eta)A\\)

## 二重积分的计算法

### 直角坐标法计算二重积分

1. 情况1 TODO: 补充图片
   \\(D=\\{(x, y)|a\leqslant x\leqslant b, \varphi_1(x)\leqslant y\leqslant \varphi_2(x)\\}\\)\
   则 \\(\iint_D f(x, y)d\sigma=\int_a^b dx\int_{\varphi_1(x)}^{\varphi_2(x)}f(x, y)dy\\)
2. 情况2 TODO: 补充图片
   \\(D=\\{(x, y)|c\leqslant y\leqslant d, \varphi_1(y)\leqslant x\leqslant\varphi_2(y)\\}\\)
   则 \\(\iint_D f(x, y)d\sigma=\int_c^d dx\int_{\varphi_1(y)}^{\varphi_2(y)}f(x, y)dx\\)

### 极坐标法计算二重积分

1. 特征:
   1. 区域 D 的边界含 \\(x^2+y^2\\)
   2. \\(f(x, y)\\) 含 \\(x^2+y^2\\)
2. 变换: TODO; 补充图片
   \\(\begin{cases} x=r\cos\theta \\\ y=r\sin\theta \end{cases} \alpha\leqslant\theta\leqslant\beta , r_1(\theta)\leqslant r\leqslant r_2(\theta)\\)
3. \\(d\sigma\\)
   取 \\([\theta, \theta+d\theta]\\)
   取 \\([r, r+dx]\\)
   \\(d\sigma=rdrd\theta\\)
   \\(\therefore \iint_D f(x, y)d\sigma=\int_\alpha^\beta d\theta\int_{r_1(\theta)}^{r_2(\theta)}r\cdot f(r\cos\theta, r\sin\theta)dr\\)

## 三重积分

### 三重积分的定义

设 \\(\Omega\\) 为空间有限几何体, \\(f(x, y, z)\\) 在 \\(\Omega\\) 上有界

\\(\Omega\\) 划分为 \\(\Delta V_1, \Delta V_2, \dots, \Delta V_n\\)
\\(\forall(\xi_i, \eta_i, \zeta_i)\in\Delta V_i\\) , 作 \\(\displaystyle\sum_{i=1}^n f(\xi_i, \eta_i, \zeta_i)\Delta V_i\\)

\\(\lambda\\) 为 \\(\Delta V_1, \Delta V_2, \dots, \Delta V_n\\) 直径最大值
若 \\(\lim\limits_{a\to0}\displaystyle\sum_{i=1}^n f(\xi_i, n_i, \zeta_i)\Delta V_i\\)
称此极限为 \\(f(x, y, z)\\) 在 \\(\Omega\\) 上的三重积分
记 \\(\iiint_{\Omega}f(x, y, z)dV\\)
即 \\(\iiint_{\Omega}f(x, y, z)dV=\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n f(\xi_1, \eta_i, \zeta_i)\Delta V_i\\)

### 三重积分的性质

1. \\(\iiint_{\Omega} 1dV=V\\)
2. \\(\Omega\\) 为有限闭区域, \\(f(x, y, z)\\) 在 \\(\Omega\\) 上连续, 则 \\(\exist(\xi, \eta, \zeta)\in\Omega\\) , 使 \\(\iiint_\Omega f(x, y, z)dV=f(\xi, \eta, \zeta)V\\)

### 三重积分的计算方法

1. 直角坐标法
   1. 铅直投影法 TODO: 补充图片
      \\(\Omega=\\{(x, y, z)|(x, y)\in Dxy , \varphi_1(x, y)\leqslant z\leqslant\varphi_2(x, y)\\}\\)
      \\(\iiint_\Omega f(x, y, z)dv=\iint_{Dxy}dxdy\int_{\varphi_1(x, y)}^{\varphi_2(x, y)}f(x, y, z)dz\\)
   2. 切片法 TODO: 补充图片
      \\(\Omega=\\{(x, y, z)|(x, y)\in Dz, c\leqslant z\leqslant d\\}\\)
      \\(\iiint_\Omega f(x, y, z)dv=\int_c^d dz\iint_{Dz} f(x, y, z)dxdy\\)
2. 柱面坐标变换法
   1. 特征: TODO: 补充图片
      1. 区域 \\(\Omega\\) 的边界含 \\(x^2+y^2\\)
      2. \\(f(x, y, z)\\) 含 \\(x^2+y^2\\)
   2. 变换: TODO: 补充图片
      \\(\Omega=\\{(x, y, z)|(x, y)\in Dxy , \varphi_1(x, y)\leqslant z\leqslant\varphi_2(x, y)\\}\\)
      令 \\(\begin{cases} x=r\cos\theta \\\ y=r\sin\theta \\\ z=z \end{cases} \quad \begin{aligned} &\alpha\leqslant\theta\leqslant\beta \\\ &r_1(\theta)\leqslant r\leqslant r_2(\theta) \\\ &\varphi_1(r\cos\theta, r\sin\theta)\leqslant z\leqslant\varphi_2(r\cos\theta, r\sin\theta) \end{aligned}\\)
   3. \\(dV=r dr d\theta dz\\) TODO: 补充图片
      \\(\iiint_{\Omega}f(x, y, z)dV=\int_\alpha^\beta d\theta\int_{r_1(\theta)}^{r_2(\theta)}dr\int_{\varphi_1(r\cos\theta, r\sin\theta)}^{\varphi_2(r\cos\theta, r\sin\theta)}rf(r\cos\theta, r\sin\theta, z)dz\\)
3. 球面坐标变换法
   1. 特征:
      1. \\(\Omega\\) 的表面含 \\(x^2+y^2+z^2\\)
      2. \\(f(x, y, z)\\) 含 \\(x^2+y^2+z^2\\)
   2. 变换
      \\(\begin{cases} x=r\cos\theta\sin\varphi \\\ y=r\sin\theta\sin\varphi \\\ z=r\cos\varphi \end{cases}\\)
   3. \\(dV=r^2\sin\varphi dr d\theta d\varphi\\)

## 重积分的应用

### 几何应用

1. 面积
   1. D 为 xOy 面内有限闭区域, 则 D 的面积为 \\(A=\iint_D 1d\sigma\\)
   2. 空间曲面的面积 TODO: 补充图片
      1. \\(\forall d\sigma\subset D\\)
      2. \\(\vec{n}=\\{-f_x^', -f_y^', 1\\}\\)
         \\(\cos r=\frac{1}{\sqrt{1+f_x^2'+f_y^2'}}\\)
         \\(\because ds\cos r=d\sigma\\)
         \\(\therefore ds=\sqrt{1+f_x^2'+f_y^2'}d\sigma\\)
      3. \\(A=\iint_D ds=\iint_D\sqrt{1+f_x^2'+f_y^2'}d\sigma\\)

### 物理应用

1. 质心
   1. 二维 TODO: 补充图片
      \\(m=\iint_D \rho(x, y)d\sigma\\)
      \\(\bar{x}=\frac{\iint_D x\rho(x, y)d\sigma}{\iint_D\rho(x, y)d\sigma} , \bar{y}=\frac{\iint_D y\rho(x, y)d\sigma}{\iint_D \rho(x, y)d\sigma}\\)
   2. 三维 TODO: 补充图片
      \\(m=\iiint_\Omega \rho(x, y, z)dV\\)
      \\(\bar{x}=\frac{\iiint_\Omega x\rho(x, y, z)dV}{\iiint_\Omega \rho(x, y, z)dV} , \bar{y}=\frac{\iiint_\Omega y\rho(x, y, z)dV}{\iiint_\Omega \rho(x, y, z)dV} , \bar{z}=\frac{\iiint_\Omega z\rho(x, y, z)dV}{\iiint_\Omega \rho(x, y, z)dV}\\)
2. 转动惯量
   1. 二维 TODO: 补充图片
      \\(I_L=\iint_D d^2\rho(x, y)d\sigma\\)
      \\(I_x=\iint_D y^2\rho(x, y)d\sigma\\)
      \\(I_y=\iint_D x^2\rho(x, y)d\sigma\\)
      \\(I_0=\iint_D(x^2+y^2)\rho(x, y)d\sigma\\)
   2. 三维 TODO: 补充图片
      \\(I_x=\iint_\Omega(y^2+z^2)\rho(x, y, z)dV\\)
      \\(I_y=\iint_\Omega(x^2+z^2)\rho(x, y, z)dV\\)
      \\(I_z=\iint_\Omega(x^2+y^2)\rho(x, y, z)dV\\)