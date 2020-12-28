---
title: mathematics
toc: true
category: senior-high-schoool
lang: zh-cn
date: 2020-12-28 17:15:02
tags:
---

高中数学的内容
省略了不重要的东西(比如集合、函数的一些谁都懂的概念)

<!-- more -->

## 函数

### 基本初等函数

1. 指数函数 Exponential function 
   形如: \\(y=a^x\enspace\\) (\\(a>0\\) 且 \\(a\neq 1\\))
   性质:
   * 指数函数恒过定点 (0, 1)
   * \\(\begin{cases} 0 < a < 1 & \text{为减函数} \\\ a > 1 & \text{为增函数} \end{cases}\\)
   
   注意: 比较两个数(带有次数)可利用 \\(a^0=1\\) 的特殊性
   例: \\(1.7^{0.3}\\) , \\(0.9^{3.1}\\)
   \\(\because 1.7^{0.3}>1.7^0=1, 0.9^{3.1} < 0.9^0 = 1 \\\ \therefore 1.7^{0.3} > 0.9^{3.1}\\)
2. 对数函数 Logarithmic function 
   形如 \\(y=\log_ax\enspace\\) (\\(a > 0\\) , 且 \\(a\neq 1\\))
   其中 \\(y\\) 叫做以 \\(a\\) 为底的对数, \\(x\\) 叫做真数
   性质:
   * 对数函数横过定点 (1, 0)
   * 对数函数公式: (\\(a > 0\\) 且 \\(a \neq 1\\) , \\(M > 0\\) , \\(N > 0\\)) TODO: 补充这些公式的推导过程
     \\(a^{\log_ab}=b\\)
     \\(\log_ab\cdot\log_ba=1\\)
     \\(log_{a^n}b^n=\log_ab\\)
     \\(\log_a(M\cdot N)=\log_aM+\log_aN\\)
     \\(\log_a(\frac M N)=\log_aM-\log_aN\\)
     \\(\log_aM^n=n\log_aM\enspace\\) (\\(n\in R\\))
     \\(\log_ab=\frac{\log_cb}{\log_ca}\enspace\\) (\\(c > 0\\) 且 \\(c\neq 1\\)) (换底公式, 是重点)
     \\(\log_{a^N}b^M=\frac{M}{N}\log_ab\\)
   * \\(\begin{cases} 0 < a < 1 & \text{为减函数} \\\ a > 1 & \text{为增函数} \end{cases}\\)
3. 反函数: 关于直线y=x对称的两个函数
   > 对数函数 \\(y=\log_ax\enspace\\) (\\(a>0\\) 且 \\(a\neq 1\\))
     和指数函数 \\(y=a^x\enspace\\) (\\(a>0\\) 且 \\(a\neq 1\\))
     互为反函数
4. 幂函数 Power function
   幂函数: \\(y=x^a\enspace\\) (\\(x\\) 为自变量, \\(a\\) 为常数)
   (一般只讨论 \\(a=1,2,3,4,\frac{1}{2},-1\\) 时的情形)
   性质:
   * 在第一象限内:
     当 \\(a>0\\) 时, 单调增
     当 \\(a<0\\) 时, 单调减

### 函数与方程

1. 二次函数 Quadratic function
   形如 \\(y=ax^2+bx+c\enspace\\) (\\(a \neq 0\\))
   性质: TODO 补充 \\(\Delta\\) 的推导过程
   * 顶点坐标: \\((-\frac{b}{2a},\frac{4ac-b^2}{4a})\\)
   * 方程根: \\((\frac{-b - \sqrt{\Delta}}{2a}, 0)和(\frac{-b + \sqrt{\Delta}}{2a}, 0)\\)
   * \\(\Delta=b^2-4ac\\)
     若 \\(\Delta>0\\) , 函数与 \\(x\\) 轴交于两点
     若 \\(\Delta=0\\) , 函数与 \\(x\\) 轴交于一点
     若 \\(\Delta<0\\) , 函数与 \\(x\\) 轴无公共点
2. 零点与方程根的关系 Realtionship between zero point and equation root
   函数 \\(y＝f(x)\\) 有零点 \\(\lrArr\\) 方程 \\(f(x)＝0\\) 有实数根 \\(\lrArr\\) 函数 \\(y＝f(x)\\) 的图象与 \\(x\\) 轴有交点
3. 二分法 Dichotomy
   对于区间 \\([a,b]\\) 上连续不断且 \\(f(a)\cdot f(b)<0\\) 的函数 \\(y=f(x)\\) ,
   通过不断地把函数 \\(f(x)\\) 的零点所在的区间一分为二,
   使区间的两个端点逐步逼近零点, 进而得到零点近似值的方法叫二分法

### 三九函数

1. 诱导公式 Induction formula
   **"奇变偶不变, 符号看象限"**
   * \\(\begin{cases} \sin(2k\pi+\alpha)=\sin\alpha & (k\in Z) \\\ \cos(2k\pi+\alpha)=\cos\alpha & (k\in Z) \\\ \tan(2k\pi+\alpha)=\tan\alpha & (k\in Z) \end{cases}\\)
   * \\(\begin{cases} \sin(\pi+\alpha)=-\sin\alpha \\\ \cos(\pi+\alpha)=-\cos\alpha \\\ \tan(\pi+\alpha)=\tan\alpha \end{cases}\\)
   * \\(\begin{cases} \sin(-\alpha)=-\sin\alpha \\\ \cos(-\alpha)=\cos\alpha \\\ \tan(-\alpha)=-\tan\alpha \end{cases}\\)
   * \\(\begin{cases} \sin(\pi-\alpha)=\sin\alpha \\\ \cos(\pi-\alpha) =-\cos\alpha \\\ \tan(\pi-\alpha)=-\tan\alpha \end{cases}\\)
   * \\(\begin{cases} \sin(\frac{\pi}{2}-\alpha)=\cos\alpha \\\ \cos(\frac{\pi}{2}-\alpha)=\sin\alpha \\\ \tan(\frac{\pi}{2}-\alpha)=\cot\alpha \end{cases}\\)
   * \\(\begin{cases} \sin(\frac{\pi}{2}+\alpha)=\cos\alpha \\\ \cos(\frac{\pi}{2}+\alpha)=-\sin\alpha \\\ \tan(\frac{\pi}{2}+\alpha)=-\cot\alpha \end{cases}\\)
2. 周期性和单调性 Periodic and monotonic
   周期函数: 对于函数 \\(f(x)\\), 如果 \\(\exist T\enspace\\) (\\(T\neq 0\\)), 使得 \\(\forall x\in\\) 定义域, 都有 \\(f(x+T)=f(x)\\) , 那么函数 \\(f(x)\\) 就是一个周期函数
   最小正周期: \\(f(x)\\) 的所有周期长度(\\(T,2T,3T,\dots\\)) 中的最小正数 \\(T\\) 叫做函数 \\(f(x)\\) 的最小正周期
3. 简谐运动 Simple harmonic motion
   形如 \\(y=A\sin(wx+\varphi)+k\\) 的函数
   (画这类函数的图像可用**五点法**)
   TODO: 图像
   \\(A\\) 为这个简谐运动的振幅(影响函数的值域), \\(k\\) 为基准(影响函数初始高度)
   (\\(w\\) 影响函数的周期长度)这个简谐运动的周期为 \\(T=\frac{2\pi}{w}\\) , 所以频率 \\(f=\frac{1}{T}=\frac{w}{2\pi}\\)
   \\(wx+\varphi\\) 称为相位, \\(x=0\\) 时的相位 \\(\varphi\\) 称为初相(影响函数左右平移)

   性质
   * \\(A=\frac{y(\text{max}-\text{min})}{2}\\) (函数值域长度的一半就是波动的幅度)
     \\(k=\frac{y(\text{max}+\text{min})}{2}\\) (函数值域的中点就是基准点)

## 同角三角函数基本关系式

平方关系: \\(\sin^2\alpha + \cos^2\alpha = 1\\)

商关系: \\(\frac{\sin\alpha}{\cos\alpha} = \tan\alpha \quad (\alpha \neq k\pi + \frac{\pi}{2}, k \in Z)\\)


## 三角恒等变换

和差角公式:

\\(\begin{aligned} &\sin(\alpha \pm \beta) = \sin\alpha\cos\beta \pm \cos\alpha\sin\beta \\\ &\cos(\alpha \pm \beta) = \cos\alpha\cos\beta \mp \sin\alpha\sin\beta \\\ &\tan(\alpha \pm \beta) = \frac{\tan\alpha \pm \tan\beta}{1 \mp \tan\alpha \cdot \tan\beta} \end{aligned}\\)

二倍角公式:

\\(\begin{aligned} &\sin{2\alpha} = 2\sin{\alpha}\cos{\alpha} \\\ &\cos{2\alpha} = \cos^2{\alpha} - \sin^2{\alpha} = 1 - 2\sin^2{\alpha} = 2\cos^2{\alpha} - 1 \end{aligned}\\)

辅助角公式:

\\(\begin{aligned} y = a\sin{x} + b\cos{x} &= \sqrt{a^2 + b^2}\sin(x + \varphi) \\\ &= \sqrt{a^2 + b^2}\cos(x - \varphi) \end{aligned}\\)

## 解三角形

正选定理: \\(2R = \frac{a}{\sin{A}} = \frac{b}{\sin{B}} = \frac{c}{\sin{C}}\\)

余弦定理: \\(\begin{cases} a^2 = b^2 + c^2 - 2bc\cos{A} \\\ b^2 = a^2 + c^2 - 2ac\cos{B} \\\ c^2 = a^2 + b^2 - 2ab\cos{C} \end{cases}\\)

三角形面积公式 \\(S = \frac{1}{2}bc\sin{A} = \frac{1}{2}ac\sin{B} = \frac{1}{2}ab\sin{C}\\)

解三角形记得判断求出的该角能否为钝(锐)角 (大角对大边, 小角对小边)

正弦定理推论: \\(2R = \frac{a + b + c}{\sin{A} + \sin{B} + \sin{C}} \quad (\frac{a}{\sin{A}})^2 = \frac{bc}{\sin{B}\sin{C}} \quad (\frac{a}{\sin{A}})^3 = \frac{abc}{\sin{A}\sin{B}\sin{C}}\\)

余弦定理推论: \\(\cos{A} = \frac{b^2 + c^2 - a^2}{2bc} \quad \cos{B} = \frac{a^2 + c^2 - b^2}{2ac} \quad \cos{C} = \frac{a^2 + b^2 - c^2}{2ab}\\)