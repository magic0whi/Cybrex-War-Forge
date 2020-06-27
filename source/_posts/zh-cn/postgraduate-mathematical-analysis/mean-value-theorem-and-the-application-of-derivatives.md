---
title: mean-value-theorem-and-the-application-of-derivatives
category: postgraduate-mathematical-analysis
lang: zh-cn
date: 2020-05-22 16:56:27
tags:
toc: true
---

## 微分中值定理

### 罗尔中值定理

TODO: 补充图片

若:
1. \\(f(x)\in c[a, b]\\)
2. \\(f(x)\\) 在 \\((a, b)\\) 内可导
3. \\(f(a)=f(b)\\)
则:
\\(\exist\xi\in(a, b)\\) , 使 \\(f'(\xi)=0\\)

### 拉格朗日中值定理

TODO: 补充图片

若:
1. \\(f(x)\in c[a,b]\\)
2. \\(f(x)\\) 在 \\((a, b)\\) 内连续
则 \\(\exist\xi\in(a, b)\\) , 使 \\(f'(\xi)=\frac{f(b)-f(a)}{b-a}\\)
(ab间某个点的斜率=ab两点所成直线的斜率. 顺便一提某个点的导数就是该点上作的切线的斜率)

证明:
作虚线 \\(L_{ab}\\) 连接点 a,b
将相关参数带入直线点斜式方程可得:
\\(L_{ab}: y-f(a)=\frac{f(b)-f(a)}{b-a}(x-a) \rArr y=f(a)+\frac{f(b)-f(a)}{b-a}(x-a)\\\)
令 \\(\varphi(x)=曲-直=f(x)-y=f(x)-f(a)-\frac{f(b)-f(a)}{b-a}(x-a)\\)
\\(\varphi(x)\in c[a, b] , \varphi(x)\\) 在 \\((a, b)\\) 内可导
且 \\(\varphi(a)=\varphi(b)=0\\)
根据罗尔中值定理, \\(\exist\xi\in(a, b)\\) , 使 \\(\varphi'(\xi)=0\\)
\\(\because \varphi'(x)=f'(x)-\frac{f(b)-f(a)}{b-a}\\)
\\(\therefore \varphi'(\xi)=f'(\xi)-\frac{f(b)-f(a)}{b-a}=0 \rArr f'(\xi)=\frac{f(b)-f(a)}{b-a}\\)

### 柯西中值定理

若:
1. \\(f(x) , g(x)\in c[a, b]\\)
2. \\(f(x) , g(x)\\) 在 \\((a,b)\\) 内可导
3. \\(g'(x)\neq0 \quad(a<x<b)\\)
则 \\(\exist\xi\in(a, b)\\) , 使 \\(\frac{f'(\xi)}{g'(\xi)}=\frac{f(b)-f(a)}{g(b)-g(a)}\\)

证明:
令 \\(\varphi(x)=f(x)-f(a)-\dfrac{f(b)-f(a)}{g(b)-g(a)}[g(x)-g(a)]\\) (这式子是逆推出来的?)
\\(\varphi(x)\in c[a, b]\\) , \\(\varphi(x)\\) 在 \\((a, b)\\) 内可导
\\(\because \varphi(a)=\varphi(b)=0\\)
\\(\therefore \exist\xi\in(a,b)\\) , 使 \\(\varphi'(\xi)=0\\)
\\(\because \varphi'(x)=f'(x)-\dfrac{f(b)-f(a)}{g(b)-g(a)}g'(x) , 且 g'(\xi)=\neq0\\)
\\(\therefore \varphi'(\xi)=f'(\xi)-\dfrac{f(b)-f(a)}{g(b)-g(a)}g'(\xi)=0 \rArr \dfrac{f'(\xi)}{g'(\xi)}=\dfrac{f(b)-f(a)}{g(b)-g(a)}\\)

## 洛必达法则

问题的起源:
求 \\(\lim\limits_{x\to0}\frac{\tan x-\sin x}{x^3}\\)
解:
\\(原式=\lim\limits_{x\to0}\frac{\tan x}{x}\cdot\frac{1-\cos x}{x^2}=\frac{1}{2}\\)
\\(原式=\lim\limits_{x\to0}\frac{x-x}{x^3}=0\\) . 不行(精确度不够)
同样使用等价无限小, 却得到了不同的结果.
说明对于存在 无穷小比无穷小(\\(\frac{0}{0}\\)) 的极限 , 用**等价无穷小解极限有局限性**
(Q:具体为什么局限? A: 分子分母经过等价无穷小转化后不同阶, 导数精确度不够)

洛必达法则目标: 解 \\(\frac{0}{0} , \frac{\infty}{\infty}\\) 类型极限新方法

洛必达法则:
若:
1. f(x), g(x) 在 \\(x=a\\) 的去心领域内可导且 \\(g'(x)\neq0\\)
2. \\(\frac{0}{0}型: \lim\limits_{x\to a}f(x)=0 , \lim\limits_{x\to a}g(x)=0 ,\quad \frac{\infty}{\infty}型: \lim\limits_{x\to a}f(x)=\infty , \lim\limits_{x\to a}g(x)=\infty\\)
3. \\(\lim\limits_{x\to a}\frac{f'(x)}{g'(x)}=A\\)

则 \\(\lim\limits_{x\to a}\frac{f(x)}{g(x)}=A\\)

证明: (令 \\(f(a)=0 , g(a)=0\\))
则 \\(\frac{f'(\xi)}{g'(\xi)}=\frac{f(x)-f(a)}{g(x)-g(a)}=\frac{f(x)}{g(x)} \quad (\xi 介于 a 与 x 之间, 柯西中值定理)\\)
\\(\therefore \lim\limits_{x\to a}\frac{f(x)}{g(x)}=\lim\limits_{x\to a}\frac{f'(\xi)}{g'(\xi)}=\lim\limits_{\xi\to a}\frac{f'(\xi)}{g'(\xi)}=A\\) 
(\\(x\\)趋向于\\(a\\) , \\(\xi\\) 介于 \\(a\\) 与 \\(x\\) 之间 \\(\rArr \xi\\) 也趋向于 \\(a\\) , 且 \\(\xi\approx x\\))

Notes:
1. 若 \\(\lim\limits_{x\to a}\frac{f'(x)}{g'(x)}\\) 不存在, 只能表明洛必达法则不能使用, 不代表极限 \\(\lim\limits_{x\to a}\frac{f(x)}{g(x)}\\) 一定不存在
2. \\(\lim\limits_{x\to +\infty}\frac{\ln x}{x^a}=0 \enspace(a>0)\\)
   \\(\lim\limits_{x\to +\infty}\frac{x^a}{b^x}=0 \enspace(a>0 , b>1)\\)

## 泰勒公式

设 \\(f(x)\\) 在 \\(x=x_0\\) 邻域内 \\(n+1\\) 阶可导.
则 \\(f(x)=P_n(x)+R_n(x)\\)
\\(\begin{aligned} 其中:\enspace &P_n(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2+\text{...}+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n \\\ &R_n(x)=\circ((x-x_0)^n)=\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1} \quad (\xi 介于 x_0 与 x 之间)\end{aligned}\\)
如果 \\(x_0=0\\) , 这个式子被称为麦克劳林公式

证明:
1. \\(P_n(x)\\) 部分
   设 \\(f(x)=a_0+a_1(x-x_0)+a_2(x-x_0)^2+a_3(x-x_0)^3+\text{...}+a_n(x-x_0)^n\\)
   要使这个式子派用场, 得找到 \\(a_0, a_1, \text{...}\\) 这些系数的值, 怎么做呢?
   要得到 \\(a_0\\) , 我们可以使 \\(x=x_0\\), 这样其他项就消除了.
   那其他的 \\(a_1, a_2, a_3\\) 呢?
   我们可以不断对该式求它的一阶, 二阶, 三阶, ... 导数:
   \\(\begin{aligned} &f'(x)=a_1+2a_2(x-x_0)+3a_3(x-x_0)^2+\text{...}+na_n(x-x_0)^{n-1} \\\ &f''(x)=2a_2+3\cdot2a_3(x-x_0)^2+\text{...}+n\cdot (n-1)(x-x_0)^{n-2} \\\ &\text{...} \end{aligned}\\)
   发现规律了吗, 将 \\(x=x_0\\) 带入, 可以轻松得到对应项的系数值: \\(a_1=\frac{f'(x_0)}{1} , a_2=\frac{f''(x_0)}{1\cdot2}, a_3=\frac{f'''(x_0)}{1\cdot2\cdot3} \rArr a_n=\frac{f^{(n)}(x_0)}{n!}\\)
   然后式子就能写成 \\(f(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2+\text{...}+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n\\)
2. \\(R_n(x)\\) 部分(拉格朗日型余项)
   TODO: 最后倒数4,3步的分母变化没看懂
   令 \\(R_n(x)=f(x)-P_n(x)\\)
   \\(R_n(x)=f(x)-P_n(x)\\)
   \\(R_n(x_0)=0 , R_n'(x_0)=0,\text{...},R_n^{(n)}(x_0)=0\\)
   \\(\\)
   \\(\begin{aligned}\dfrac{R_n(x)}{(x-x_0)^{n+1}}=\dfrac{R_n(x)-R_n(x_0)}{(x-x_0)^{n+1}-(x_0-x_0)^{n+1}}&=\dfrac{R_n'(\xi_1)}{(n+1)(\xi_1+x_0)^n} \quad(\xi_1 在 x 与 x_0 内, 使用柯西中值定理) \\\ &=\dfrac{R_n'(\xi_1)-R_n'(x_0)}{(n+1)(\xi_1-x_0)^n-(n+1)(x_0-x_0)^n} \\\ &=\dfrac{R_n''(\xi_2)}{(n+1)\cdot n(\xi_2-x_0)^{n-1}} \quad(\xi_2 在 x_0 与 \xi_1 内, 再次使用柯西中值定理) \\\ &=\text{...} \\\ &=\frac{R_n^{(n)}(\xi_n)}{(n+1)\cdot n(\xi_2-x_0)^{n-1}\cdot\text{...}\cdot2(\xi_n-x_0)^1} \\\ &=\frac{R_n^{(n)}(\xi_n)-R_n^{(n)}(x_0)}{(n+1)!(\xi_n-x_0)-(n+1)!(x_0-x_0)} \\\ &=\frac{R_n^{(n+1)}(\xi)}{(n+1)!} \quad(\xi 在 x_0 与 \xi_n 内) \\\  &=\frac{f^{(n+1)}(\xi)}{(n+1)!} \\\ &\rArr R_n(x)=\frac{f^{(n+1)(\xi)}}{(n+1)!}(x-x_0)^{n+1} \end{aligned}\\)

Notes:
1. \\(e^x=1+x+\frac{x^2}{2!}+\text{...}+\frac{x^n}{n!}+\circ(x^n)\\)
2. \\(\sin x=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\text{...}+(-1)^n\frac{x^{2n+1}}{(2n+1)!}+\circ(x^{2n+1})\\)
3. \\(\cos x=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\text{...}+(-1)^n\frac{x^{2n}}{(2n)!}+\circ(x^{2n})\\)
4. \\(\ln(1+x)=x-frac{x^2}{2}+\frac{x^3}{3}-\frac{x^4}{4}+\text+(-1)^{n-1}\frac{x^n}{n}+\circ(x^n)\\)
5. \\(\frac{1}{1-x}=1+x+x^2+x^3+\text{...}+x^n+\circ(x^n)\\)
6. \\(\frac{1}{1+x}=1-x+x^2-x^3+\text{...}+(-1)^nx^n+\circ(x^n)\\)

## 导数与函数单调性和曲线凹凸性的关系

### 导数与函数单调性

导数可以判别函数的单调性: (可理解为导数就是函数变化的速度, 速度的正负代表函数变化方向)
设 \\(f(x) , x\in [a, b]\\) 且 (a, b) 内可导.
1. 若 \\(f'(x)>0 \quad(a<x<b)\\) , 则 \\(f(x)\\) 在 \\([a, b]\\) 上单调递增
2. 若 \\(f'(x)<0 \quad(a<x<b)\\) , 则 \\(f(x)\\) 在 \\([a, b]\\) 上单调递减

### 导数与曲线凹凸性

1. (不用看)曲线凹凸性的定义: TODO: 补充图片
   看 \\(\text{O}-\frac{x_1+x_2}{2}\\) 与 \\(\text{O}-\frac{f(x_1)+f(x_2)}{2}\\) 两线段围成矩形的形状
   1. 若 \\(\forall x_1 , x_2 \in D\\) 且 \\(x_1\neq x_2\\) , 有
      \\(f(\frac{x_1+x_2}{2})<\frac{f(x_1)+f(x_2)}{2}\\)
      称 \\(f(x)\\) 在 D 内为凹函数
   2. 若 \\(\forall x_1 , x_2 \in D\\) 且 \\(x_1\neq x_2\\) , 有
      \\(f(\frac{x_1+x_2}{2})>\frac{f(x_1)+f(x_2)}{2}\\)
      称 \\(f(x)\\) 在 D 内为凸函数
2. 判别法: (可理解为二阶导数就是函数变化的加速度, 加速度的变化代表函数凹凸)
   设 \\(f(x) , x\in [a, b]\\) 且 (a, b) 内二阶可导.
   1. 若 \\(f''(x)>0 \quad(a<x<b)\\) , 则 \\(y=f(x)\\) 图像在 [a, b] 上是凹的
   2. 若 \\(f''(x)<0 \quad(a<x<b)\\) , 则 \\(y=f(x)\\) 图像在 [a, b] 上是凸的

## 极值与最值

一个函数中, 极大值/最小值可以有很多, 但最大值/最小值只能有一个

### 函数的极大值与极小值

1. 定义:
   设 \\(y=f(x) \enspace(x\in D) \enspace x_0\in D\\)
   若 \\(\exist\delta>0\\) , 当 \\(0<|x-x_0|<\delta\\) 时
   1. 有 \\(f(x)>f(x_0)\\) , 称 \\(x_0\\) 为极小点, \\(f(x_0)\\) 为极小值
   2. 有 \\(f(x)<f(x_0)\\) , 称 \\(x_0\\) 为极大点, \\(f(x_0)\\) 为极大值
   与导数的关系:
   [x=a 为 f(x) 极值点] 是 [f'(a)=0 或 f'(a) 不存在] 的必要不充分条件
2. 求极值的步骤:
   1. 法一(利用目标点附近导数)
      1. 若 \\(\begin{cases} x<x_0 时 , f'(x)<0 \\\ x>x_0 时 , f'(x)>0 \end{cases} , x=x_0\\) 为极小点
      2. 若 \\(\begin{cases} x<x_0 时 , f'(x)>0 \\\ x>x_0 时 , f'(x)<0 \end{cases} , x=x_0\\) 为极大点
   2. 法二(利用二阶导数)
      设 \\(f'(x_0)=0 , f''(x_0)\begin{cases} >0 , x_0 为极小点 \\\ < 0 , x_0为极大点 \end{cases}\\)

### 最大值与最小值

设 \\(f(x)\in c[a, b] , a<x<b\\)
则极小值和极大值可在 f(a), f(b) 和其他使 f'(x)=0或不存在的点之中找到

## 函数图像描绘

### 渐近线

设函数\\(f(x)\\)
1. 水平渐近线: TODO: 补充图片
   若 \\(\lim\limits_{x\to\infty}f(x)=A\\)
   称 \\(f(x)\\) 有水平渐近线 \\(y=A\\)
2. 垂直渐近线: TODO: 补充图片
   若 \\(\lim\limits_{x\to a}f(x)=\infty\\)
   称 \\(f(x)\\) 有垂直渐近线 \\(x=a\\)
3. 斜渐近线:
   若
   1. \\(\lim\limits_{x\to\infty}\frac{f(x)}{x}=k \quad\\) (可以理解为是斜率)
   2. \\(\lim\limits_{x\to\infty}[f(x)-kx]=b\\)
   
   称 \\(f(x)\\) 有斜渐近线 \\(y=ax+b\\)

### 作图

(根据一阶和二阶导数的值描绘函数曲线)

设函数 \\(f(x) , x\in D\\)
1. 在定义域内:
   找出满足 \\(f'(x) \begin{cases} =0 \\\ 不存在 \end{cases}\\) 的所有点
   找出满足 \\(f''(x) \begin{cases} =0 \\\ 不存在 \end{cases}\\) 的所有点
4. 画渐近线
5. 作表
   <table>
   <thead>
     <tr>
       <th>x</th>
       <th>()</th>
       <th>?</th>
       <th>()</th>
       <th>?</th>
       <th>...</th>
     </tr>
   </thead>
   <tbody>
     <tr>
       <td>f'(x)</td>
       <td>+</td>
       <td></td>
       <td>-</td>
       <td></td>
       <td></td>
     </tr>
     <tr>
       <td>f''(x)</td>
       <td>+</td>
       <td></td>
       <td>+</td>
       <td></td>
       <td></td>
     </tr>
     <tr>
       <td>f(x)</td>
       <td>\(\nearrow\)</td>
       <td>极大</td>
       <td>\(\searrow\)</td>
       <td></td>
       <td></td>
     </tr>
   </tbody>
   </table>
6. 在坐标系上找到关键点, 描图.

## 弧微分与曲率

### 弧微分

前面的微分能让我们求 \(\Delta y\\) 的近似值 , 也就是从 \\(x\\) 到 \\(x_0\\) 后 y 轴的偏移量近似值
但如果我们想要求从 \\(x\\) 到 \\(x_0\\) 间这段函数曲线长度的近似值(即弧微分)呢?

弧微分的形象解释:
1. TODO 补充图片
2. TODO 补充图片

两种弧微分形式:
1. 普通函数
   \\(L: f(x)\\)
   \\(ds=\sqrt{1+(\frac{dy}{dx})^2(dx)^2}=\sqrt{1+[f'(x)]^2}dx\\)
2. 参数方程
   \\(L: \begin{cases} x=\varphi(t) \\\ y=\psi(t) \end{cases}\\)
   \\(ds=\sqrt{(dx)^2+(dy)^2}=\sqrt{(\frac{dx}{dt})^2+(\frac{dy}{dt})^2(dt)^2}=\sqrt{[\varphi'(t)]^2+[\psi'(t)]^2}dt\\)

### 曲率与曲率半径

1. 曲率的大小: (与切线夹角和切点间弧长有关)
   1. TODO: 补充图片
      \\(\Delta\alpha\\) 一定, \\(|\widehat{M_1N_1}|<|\widehat{M_2N_2}|\\) , 弯曲度: 前者>后者
      **角度一定, 弯曲度与两点间的弧长成反比**
   2. TODO: 补充图片
      \\(|\widehat{MN}|\\) 一定, \\(\Delta\alpha_1>\Delta\alpha_2\\), 弯曲度: 前者>后者
      **长度一定, 弯曲度与切线夹角成正比**
2. 曲率定义: TODO: 补充图片
   (切线夹角即切线的变化角度)
   设 \\(L: f(x) , |\widehat{MM'}|=\Delta s\\)
   平均曲率 \\(\bar{k}=\dfrac{|\Delta\alpha|}{|\Delta s|}\\)
   某点的曲率 \\(k=\lim\limits_{\Delta x\to0}|\frac{\Delta\alpha}{\Delta s}|=|\frac{d\alpha}{ds}|=\frac{|f''(x)|}{(1+[f'(x)]^2)^\frac{3}{2}}\\)
   曲率半径: \\(R=\dfrac{1}{k}\\)
   证明:
   可知 \\(\lim\limits_{\Delta x\to0}\tan\alpha=f'(x)\\) (TODO: 作个图解释)
   1. \\(ds=\sqrt{1+[f(x)']^2}dx\\)
   2. \\(\because \tan\alpha=f'(x)\\) 两边对x求导得
      \\(\therefore \sec^2\alpha\cdot\frac{d\alpha}{dx}=f''(x)\\)
      \\(\because \sec^2\alpha=1+\tan^2\alpha=1+[f'(x)]^2\\)
      \\(\therefore \frac{d\alpha}{dx}=\frac{f''(x)}{1+[f'(x)]^2} \rArr d\alpha=\frac{f''(x)}{1+[f'(x)]^2}dx\\)