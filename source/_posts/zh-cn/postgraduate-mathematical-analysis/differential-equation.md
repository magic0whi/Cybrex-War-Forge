---
title: differential-equation
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:00:04
tags:
toc: true
---

微分方程

<!-- more -->

微分方程求解即根据已知的微分条件求目标函数

## 微分方程的基本概念

1. 微分方程: 含有导数或微分的方程
   常微分方程: 只含一个自变量, 一个函数的微分方程, 如 \\(f'(x)+7f(x)=0\\)
   (我们探讨的范围仅限于常微分方程)
2. 微分方程的阶: 在微分方程中, 导数或微分的最高阶数
3. 微分方程的解: 
   已知 y 关于 x 的微分方程 \\(F(y^{(n)},y^{(n-1)},\dots,y',y,x)=0\\)
   若代入函数 \\(y=\varphi(x)\\) 能够满足 \\(F(y^{(n)},y^{(n-1)},\dots,y',y,x)=0\\)
   称 \\(y=\varphi(x)\\) 为该微分方程的解
   1. 通解: 设 \\(F(y^{(n)},y^{(n-1)},\dots,y',y,x)=0\\) 为 n 阶微分方程, 若该方程的解含 n 个相互独立的任意常数, 称该解为通解
      如 \\(y=C_1e^x+C_2e^{2x}\\) 为 \\(y''-3y'+2y=0\\) 的通解
   2. 特解: 不含任意常数的解


## 可分离变量微分方程

1. 定义
   形如 \\(\frac{dy}{dx}=\varphi_1(x)\varphi_2(y)\\) 的方程
2. 解法
   \\(\frac{dy}{dx}=\varphi_1(x)\varphi_2(y)\rArr\frac{dy}{\varphi_2(y)}=\varphi_1(x)dx\\)
   两边积分得:
   \\(\int\frac{dy}{\varphi_2(y)}=\int\varphi_1(x)dx+C\\) (不定积分中可以省略常数 C, 但在微分方程中自变量一端要加)

## 齐次微分方程

1. 定义
   形如 \\(\frac{dy}{dx}=\varphi(\frac{y}{x})\\) 的方程
2. 解法
   换元法, 设 \\(u=\frac{y}{x}\\) , 则 \\(y=ux\rArr y'=u'x+ux'\rArr\frac{dy}{dx}=x\frac{du}{dx}+u\\)
   将上式代入方程得到 \\(x\frac{du}{dx}+u=\varphi(u)\\)
   然后就可以套用分离变量的方法, 最后两边积分: 
   \\(\frac{dx}{x}=\frac{du}{\varphi(u)-u}\rArr\int\frac{dx}{x}=\int\frac{du}{\varphi(u)-u}+c\\)

## 一阶线性微分方程

### 一阶齐次线性方程

1. 定义
   形如 \\(\frac{dy}{dx}+P(x)y=0\\) 的方程称为一阶齐次线性方程
2. 解法及通解公式
   \\(\frac{dy}{dx}=-P(x)y\\)
   1. 情况1 \\(y=0\\) 为方程的解
   2. 情况2 \\(y\neq0\\) 时, 先分离变量, 然后两边积分, 再套用积分公式求解
      \\(\begin{aligned} \frac{1}{y}dy=-P(x)dx & \rArr\int\frac{1}{y}dy=\int -P(x)dx \\\ & \rArr\ln|y|=-\int P(x)dx+C_0 \\\ & \rArr|y|=e^{-\int P(x)dx+C_0} \\\ & \rArr y=\pm e^{C_0}\cdot e^{-\int P(x)dx} \end{aligned}\\)
      令 \\(\pm e^{C_0}=C\\)
      \\(\therefore 通解 y=Ce^{-\int P(x)dx}\\)

### 一阶非齐线性微分方程

1. 定义
   形如 \\(\frac{dy}{dx}+P(x)y=Q(x)\\) 的方程称为一阶非齐线性微分方程
2. 解法
   通过常数易变法, 将上面齐次方程通解中的**常数项 C 换做未知函数 u(x)** , 得到
   \\(y=u(x)e^{-\int P(x)dx}\\) ,
   然后对 y 求导得
   \\(y'=\frac{dy}{dx}=u'(x)e^{-\int P(x)dx}-u(x)P(x)e^{-\int P(x)dx}\\) (这里注意复合函数求导法则, 且对积分求导的结果是原函数)
   以上两式带入一阶非齐线性微分方程得
   \\(\begin{aligned} &u'(x)e^{-\int P(x)dx}-u(x)P(x)e^{-\int P(x)dx}+P(x)u(x)e^{-\int P(x)dx}=Q(x) \\\ \rArr &u'(x)e^{-\int P(x)dx}=Q(x) \\\ \rArr &u'(x)=Q(x)e^{\int P(x)dx} \rArr \int u'(x)dx=\int Q(x)e^{\int P(x)dx}dx+C \\\ \rArr &u(x)=\int Q(x)e^{\int P(x)dx}dx+C \end{aligned}\\)
   求得的 u(x) 再次带入通解式得 \\(y=[\int Q(x)e^{\int P(x)dx}dx+C]e^{-\int P(x)dx}\\)

## 可降阶的高阶微分方程

1. \\(y^{(n)}=f(x)\quad(n\geqslant2)\\)
   太简单不再赘述
2. \\(f(x, y' ,y'')=0\quad(缺失y)\\)
   解法:
   令 \\(y'=p , y''=\frac{dp}{dx}\\) 代入得
   \\(f(x, p, \frac{dp}{dx})=0 \rArr p=\varphi(x, c_1)\\) , 即 \\(\frac{dy}{dx}=\varphi(x, c_1)\\)
   \\(\therefore y=\int \varphi(x, c_1)dx+c_2\\)
3. \\(f(y, y', y'')=0\quad(缺失x)\\)
   解法:
   令 \\(y'=p , y''=\frac{dp}{dx} \rArr y''=\frac{dp}{dy}\cdot\frac{dy}{dx}=\frac{dp}{dy}\cdot p\\) , 代入得 
   \\(f(y, p, \frac{dp}{dy}\cdot  p=0) \rArr p=\varphi(y, c_1)\\)
   即 \\(\frac{dy}{dx}=\varphi(y, c_1) \rArr  \frac{dy}{\varphi(y, c_1)}=dx \rArr \int\frac{dy}{\varphi(y, c_1)}=\int dx+c_2\\)

## 高阶线性微分方程

### 基本概念

1. 二阶齐次线性微分方程: \\(y''+a(x)y'+b(x)y=0\\)
   二阶非齐线性微分方程: \\(y''+a(x)y'+b(x)y=c(x)\\)
2. n阶齐次线性微分方程: \\(y^{(n)}+a_1(x)y^{(n-1)}+\dots+a_{n-1}y'+a_n(x)y=0\\)
   n阶非齐线性微分方程: \\(y^{(n)}+a_1(x)y{(n-1)}+\dots+a_{n-1}y'+a_n(x)y=f(x)\\)
3. 设 \\(\varphi_1(x) , \varphi_2(x)\\) 为两个函数
   1. 若 \\(\varphi_1(x) , \varphi_2(x)\\) 不成比例, 称 \\(\varphi_1(x) , \varphi_2(x)\\) 线性无关
   2. 若 \\(\varphi_1(x) , \varphi_2(x)\\) 成比例, 称 \\(\varphi_1(x) , \varphi_2(x)\\) 线性相关
   
   如 \\(x^2 , \sin x\\) 线性无关, \\(x^2 , 3x^2\\) 线性相关

### 结构

设:
(1) \\(y''+a(x)y'+b(x)y=0\\)
(2) \\(y''+a(x)y'+b(x)y=c(x)\\)
(3) \\(y''+a(x)y'+b(x)y=f(x)\\)
若 \\(f(x)=f_1(x)+f_2(x)\\) 则
(3)'\\(\enspace y''+a(x)y'+b(x)y=f_1(x)\\)
(3)''\\(\enspace y''+a(x)y'+b(x)y=f_2(x)\\)

1. 若 \\(\varphi_1(x) , \varphi_2(x)\\) 为 (1) 的解, 则 \\(y=c_1\varphi_1(x)+c_2\varphi_2(x)\\) (线性组合)仍为 (1) 的解
2. 若 \\(\varphi_1(x) , \varphi_2(x)\\) 分别为 (1), (2) 的解, 则 \\(y=\varphi_1(x)+\varphi_2(x)\\) 为 (2) 的解
3. 若 \\(\varphi_1(x) , \varphi_2(x)\\) 为 (2) 的解, 则 \\(y=\varphi_2(x)-\varphi_1(x)\\) 为 (1) 的解
4. 若 \\(\varphi_1(x) , \varphi_2(x)\\) 为 (3)', (3)'' 的解, 则 \\(y=\varphi_1(x)+\varphi_2(x)\\) 为 (3) 的解
5. 1. 设 \\(\varphi_1(x) , \varphi_2(x)\\) 为 (1) 的两个线性无关解
      则 (1) 通解为 \\(y=c_1\varphi_1(x)+c_2\varphi_2(x)\\)
   1. 设 \\(\varphi_1(x) , \varphi_2(x)\\) 为 (1) 的两个线性无关解, \\(\varphi_0(x)\\) 为 (2) 的一个特解
      则 (2) 的通解为
      \\(y=c_1\varphi_1(x)+c_2\varphi_2(x)+\varphi_0(x)\\)

证明: 
1. \\(\begin{cases} \varphi_1''+a(x)\varphi_1'+b(x)\varphi_1=0 \\\ \varphi_2''+a(x)\varphi_2'+b(x)\varphi_2=0 \end{cases}\\)
   将 \\(y=c_1\varphi_1(x)+c_2\varphi_2(x)\\) 代入 (1) 得
   \\(\begin{aligned} &(c_1\varphi_1+c_2\varphi_2)''+a(x)(c_1\varphi_1+c_2\varphi_2)'+b(x)(c_1\varphi_1+c_2\varphi_2) \\\ =&c_1(\varphi_1''+a(x)\varphi_1'+b(x)\varphi_1)+c_2(\varphi_2''+a(x)\varphi_2'+b(x)\varphi_2) \\\ =&c_1\cdot0+c_2\cdot0=0 \end{aligned}\\)
   \\(\therefore y=c_1\varphi_1(x)+c_2\varphi_2(x)\\) 为 (1) 的解
2. \\(\begin{cases} \varphi_1''+a(x)\varphi_1'+b(x)\varphi_1=0 \\\ \varphi_2''+a(x)\varphi_2'+b(x)\varphi_2=c(x) \end{cases}\\)
   将 \\(y=\varphi_1(x)+\varphi_2(x)\\) 代入 (2) 得
   \\(\begin{aligned} (\varphi_1+\varphi_2)''+a(x)(\varphi_1+\varphi_2)'+b(x)(\varphi_1+\varphi_2)&=c(x) \\\ \rArr (\varphi_1''+a(x)\varphi_1'+b(x)\varphi_1)+(\varphi_2''+a(x)\varphi_2'+b(x)\varphi_2)&=c(x) \\\ 0+c(x)&=c(x)\end{aligned}\\)
   \\(\therefore y=\varphi_1(x)+\varphi_2(x)\\) 为 (2) 的解
3. \\(\begin{cases} \varphi_1''+a(x)\varphi_1'+b(x)\varphi_1=c(x) \\\ \varphi_2''+a(x)\varphi_2'+b(x)\varphi_2=c(x) \end{cases}\\)
   将 \\(y=\varphi_2(x)-\varphi_1(x)\\) 代入 (2) 得
   \\(\begin{aligned} &(\varphi_2-\varphi_1)''+a(x)(\varphi_2-\varphi_1)'+b(x)(\varphi_2-\varphi_1) \\\ =&(\varphi_2''+a(x)\varphi_2'+b(x)\varphi_2)-(\varphi_1''+a(x)\varphi_1'+b(x)\varphi_1) \\\ =&c(x)-c(x)=0 \end{aligned}\\)
   \\(\therefore y=\varphi_2(x)-\varphi_1(x)\\) 为 (1) 的解
4. \\(\begin{cases} \varphi_1''+a(x)\varphi_1'+b(x)\varphi_1(x)=f_1(x) \\\ \varphi_2''+a(x)\varphi_2'+b(x)\varphi_2(x)=f_2(x) \end{cases}\\)
   将 \\(y=\varphi_1(x)+\varphi_2(x)\\) 代入 (3) 得
   \\(\begin{aligned} (\varphi_1+\varphi_2)''+a(x)(\varphi_1+\varphi_2)'+b(x)(\varphi_1+\varphi_2)&=f(x) \\\ \rArr (\varphi_1''+a(x)\varphi_1'+b(x)\varphi_1)+(\varphi_1''+a(x)\varphi_2'+b(x)\varphi_2)&=f(x) \\\ \rArr f_1(x)+f_2(x)&=f(x) \end{aligned}\\)
   \\(\therefore y=\varphi_1(x)+\varphi_2(x)\\) 为 (3) 的解

## 常系数齐次线性微分方程

\\(y''+py'+qy=0\\) (\*)
其中 p, q 为常数, 则称 (\*) 为二阶常系数齐次线性微分方程

猜测: (\*) 解的形式? \\(\begin{cases} e^{\lambda x} \\\ \sin\beta x\cdot\cos\beta x \end{cases}\\)
令 \\(y=e^{\lambda x}\\) 为 (\*) 的解, 代入得
\\(\lambda^2e^{\lambda x}+p\lambda e^{\lambda x}+qe^{\lambda x}=0 \rArr \lambda^2+p\lambda+q=0\\) , 称其为 (\*) 的特征方程

1. 情况1 \\(\Delta=p^2-4q>0 , \lambda^2+p\lambda+q=0\\) 有两个不同实根 \\(\lambda_1 , \lambda_2\\)
   \\(y_1=e^{\lambda_1x} , y_2=e^{\lambda_2x}\\) 为 (\*) 的解
   \\(\because \lambda_1\neq\lambda_2 \therefore y_1 与 y_2 线性无关\\)
   \\(\therefore (\*) 的通解为 y=c_1e^{\lambda_1x}+c_2e^{\lambda_2x}\\)
2. 情况2 \\(\Delta=p^2-4q=0 , \lambda^2+p\lambda+q=0\\) 有两个相等的实根 \\(\lambda_1=\lambda_2\\)
   \\(y_1=e^{\lambda_1x}\\) 为 (\*) 的解
   令 \\(\frac{y_2}{y_1}=u(x) \enspace(\neq c)\\) 且 \\(y_2\\) 为 (\*) 的解, 得到
   \\(y_2=u(x)y_1=ue^{\lambda_1x}\\)
   \\(y_2'=u'e^{\lambda_1x}+\lambda_1ue^{\lambda_1x}\\)
   \\(y_2''=u''e^{\lambda_1x}+2\lambda_1u'e^{\lambda_1x}+\lambda_1^2ue^{\lambda_1x}\\)
   以上三式代入 \\(y''+py'+qy=0\\) 得
   \\(\begin{aligned} &u''e^{\lambda_1x}+2\lambda_1u'e^{\lambda_1x}+\lambda_1^2ue^{\lambda_1x}+pu'e^{\lambda_1x}+p\lambda_1ue^{\lambda_1x}+que^{\lambda_1x}=0 \\\ \rArr &u''+2\lambda_1u'+\lambda_1^2u+pu'+p\lambda_1u+qu=0 \\\ \rArr &u''+(2\lambda_1+p)u'+(\lambda_1^2+p\lambda_1+q)u=0 \end{aligned}\\)
   \\(\because \begin{cases} \lambda_1^2+p\lambda_1+q=0 \\\ \lambda_1+\lambda_2=-p \rArr 2\lambda_1+p=0 \end{cases}\\) TODO 下面式子没弄懂
   \\(\therefore u''=0\\)
   取 u(x)=x
   \\(\therefore y_2=xe^{\lambda_1x}\\)
   则通解 \\(y=c_1e^{\lambda_1x}+c_2xe^{\lambda_1x}=(c_1+c_2x)e^{\lambda_1x}\\)
3. 情况3 \\(\Delta=p^2-4q<0\\)
   \\(\lambda^2+p\lambda+q=0 \rArr \lambda_{1,2}=\alpha\pm i\beta\\)
   \\(y_1=e^{(\alpha+\beta i)x}\\) 与 \\(y_2=e^{(\alpha-\beta i)x}\\) 为两个解
   \\(y_1=e^{\alpha x+\beta xi}=e^{\alpha x}\cdot e^{\beta xi}=e^{\alpha x}\cdot(\cos\beta x+i\sin\beta x)\\)
   \\(y_2=e^{\alpha x-\beta xi}=e^{\alpha x}\cdot e^{-\beta xi}=e^{\alpha x}\cdot(\cos\beta x-i\sin\beta x)\\)
   \\(Y_1=\frac{1}{2}y_1+\frac{1}{2}y_2=e^{\alpha x}\cos\beta x\\)
   \\(Y_2=\frac{1}{2i}y_1+(-\frac{1}{2i})y_2=\frac{1}{2i}(y_1-y_2)=e^{\alpha x}\sin\beta x\\)
   \\(\therefore\\) (\*) 的通解为 \\(y=c_1e^{\alpha x}\cos\beta x+c_2e^{\alpha x}\sin\beta x=e^{\alpha x}(c_1\cos\beta x+c_2\sin\beta x)\\)

总结: \\(y''+py'+qy=0\\) (\*)
1. 特征方程: \\(\lambda^2+p\lambda+q=0\\)
2. 1. \\(\Delta>0 , y=c_1c^{\lambda_1x}+c_2e^{\lambda_2x}\\)
   2. \\(\Delta=0 , y=(c_1+c_2x)e^{\lambda_1x}\\)
   3. \\(\Delta<0 , y=e^{\alpha x}(c_1\cos\beta x+c_2\sin\beta x)\\)

### 高阶常系数齐次线性微分方程

\\(y'''+py''+qy'+\Gamma y=0\\)
1. \\(\lambda^3+p\lambda^2+q\lambda+\Gamma=0\\) - 特征方程
2. 1. \\(\lambda_1 , \lambda_2 , \lambda_3\\) 实, 单值
      \\(y=c_1e^{\lambda_1x}+c_2e^{\lambda_2x}+c_3e^{\lambda_3x}\\)
   2. \\(\lambda_1 , \lambda_2 , \lambda_3\\) 实且 \\(\lambda_1=\lambda_2\neq\lambda_3\\)
      \\(y=(c_1+c_2x)e^{\lambda_1x}+c_3e^{\lambda_3x}\\)
   3. \\(\lambda_1 , \lambda_2 , \lambda_3\\) 实且 \\(\lambda_1=\lambda_2=\lambda_3\\)
      \\(y=(c_1+c_2x+c_3x^2)e^{\lambda_1x}\\)
   4. \\(\lambda_1\in R , \lambda_{2,3}=\alpha\pm i\beta\\)
      \\(y=c_1e^{\lambda_1x}+e^{\alpha x}(c_2\cos\beta x+c_3\sin\beta x)\\)

## 常系数非齐次线性微分方程

\\(y''+py'+qy=f(x)\\) (\*\*)
(\*\*) 通解:
1. \\(y''+py'+qy=0\\) 通解
2. \\(y''+py'+qy=f(x)\\) 的一个特解 \\(y_0(x)\\)?

3. \\(f(x)=P_n(x)e^{kx}\\)
4. \\(f(x)=e^\alpha x\\) [\\(多项式\cdot\cos\beta x + 多项式\cdot\sin\beta x\\)]