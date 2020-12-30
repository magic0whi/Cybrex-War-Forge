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

1. 指数函数 (Exponential function) 
   形如: \\(y=a^x\enspace\\) (\\(a>0\\) 且 \\(a\neq 1\\))
   性质:
   * 指数函数恒过定点 (0, 1)
   * \\(\begin{cases} 0 < a < 1 & \text{为减函数} \\\ a > 1 & \text{为增函数} \end{cases}\\)
   
   注意: 比较两个数(带有次数)可利用 \\(a^0=1\\) 的特殊性
   例: \\(1.7^{0.3}\\) , \\(0.9^{3.1}\\)
   \\(\because 1.7^{0.3}>1.7^0=1, 0.9^{3.1} < 0.9^0 = 1 \\\ \therefore 1.7^{0.3} > 0.9^{3.1}\\)
2. 对数函数 (Logarithmic function) 
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
4. 幂函数 (Power function)
   幂函数: \\(y=x^a\enspace\\) (\\(x\\) 为自变量, \\(a\\) 为常数)
   (一般只讨论 \\(a=1,2,3,4,\frac{1}{2},-1\\) 时的情形)
   性质:
   * 在第一象限内:
     当 \\(a>0\\) 时, 单调增
     当 \\(a<0\\) 时, 单调减

### 函数与方程

1. 二次函数 (Quadratic function)
   形如 \\(y=ax^2+bx+c\enspace\\) (\\(a \neq 0\\))
   性质: TODO 补充 \\(\Delta\\) 的推导过程
   * 顶点坐标: \\((-\frac{b}{2a},\frac{4ac-b^2}{4a})\\)
   * 方程根: \\((\frac{-b - \sqrt{\Delta}}{2a}, 0)和(\frac{-b + \sqrt{\Delta}}{2a}, 0)\\)
   * \\(\Delta=b^2-4ac\\)
     若 \\(\Delta>0\\) , 函数与 \\(x\\) 轴交于两点
     若 \\(\Delta=0\\) , 函数与 \\(x\\) 轴交于一点
     若 \\(\Delta<0\\) , 函数与 \\(x\\) 轴无公共点
2. 零点与方程根的关系 (Realtionship between zero point and equation root)
   函数 \\(y＝f(x)\\) 有零点 \\(\lrArr\\) 方程 \\(f(x)＝0\\) 有实数根 \\(\lrArr\\) 函数 \\(y＝f(x)\\) 的图象与 \\(x\\) 轴有交点
3. 二分法 (Dichotomy)
   对于区间 \\([a,b]\\) 上连续不断且 \\(f(a)\cdot f(b)<0\\) 的函数 \\(y=f(x)\\) ,
   通过不断地把函数 \\(f(x)\\) 的零点所在的区间一分为二,
   使区间的两个端点逐步逼近零点, 进而得到零点近似值的方法叫二分法

### 三角函数

1. 诱导公式 (Induction formula)
   **"奇变偶不变, 符号看象限"**
   * \\(\begin{cases} \sin(2k\pi+\alpha)=\sin\alpha & (k\in Z) \\\ \cos(2k\pi+\alpha)=\cos\alpha & (k\in Z) \\\ \tan(2k\pi+\alpha)=\tan\alpha & (k\in Z) \end{cases}\\)
   * \\(\begin{cases} \sin(\pi+\alpha)=-\sin\alpha \\\ \cos(\pi+\alpha)=-\cos\alpha \\\ \tan(\pi+\alpha)=\tan\alpha \end{cases}\\)
   * \\(\begin{cases} \sin(-\alpha)=-\sin\alpha \\\ \cos(-\alpha)=\cos\alpha \\\ \tan(-\alpha)=-\tan\alpha \end{cases}\\)
   * \\(\begin{cases} \sin(\pi-\alpha)=\sin\alpha \\\ \cos(\pi-\alpha) =-\cos\alpha \\\ \tan(\pi-\alpha)=-\tan\alpha \end{cases}\\)
   * \\(\begin{cases} \sin(\frac{\pi}{2}-\alpha)=\cos\alpha \\\ \cos(\frac{\pi}{2}-\alpha)=\sin\alpha \\\ \tan(\frac{\pi}{2}-\alpha)=\cot\alpha \end{cases}\\)
   * \\(\begin{cases} \sin(\frac{\pi}{2}+\alpha)=\cos\alpha \\\ \cos(\frac{\pi}{2}+\alpha)=-\sin\alpha \\\ \tan(\frac{\pi}{2}+\alpha)=-\cot\alpha \end{cases}\\)
2. 周期性和单调性 (Periodic and monotonic)
   周期函数: 对于函数 \\(f(x)\\), 如果 \\(\exist T\enspace\\) (\\(T\neq 0\\)), 使得 \\(\forall x\in\\) 定义域, 都有 \\(f(x+T)=f(x)\\) , 那么函数 \\(f(x)\\) 就是一个周期函数
   最小正周期: \\(f(x)\\) 的所有周期长度(\\(T,2T,3T,\dots\\)) 中的最小正数 \\(T\\) 叫做函数 \\(f(x)\\) 的最小正周期
3. 简谐运动 (Simple harmonic motion)
   形如 \\(y=A\sin(wx+\varphi)+k\\) 的函数
   (画这类函数的图像可用**五点法**)
   TODO: 图像
   \\(A\\) 为这个简谐运动的振幅(影响函数的值域), \\(k\\) 为基准(影响函数初始高度)
   (\\(w\\) 影响函数的周期长度)这个简谐运动的周期为 \\(T=\frac{2\pi}{w}\\) , 所以频率 \\(f=\frac{1}{T}=\frac{w}{2\pi}\\)
   \\(wx+\varphi\\) 称为相位, \\(x=0\\) 时的相位 \\(\varphi\\) 称为初相(影响函数左右平移)
   性质
   * \\(A=\frac{y(\text{max}-\text{min})}{2}\\) (函数值域长度的一半就是波动的幅度)
     \\(k=\frac{y(\text{max}+\text{min})}{2}\\) (函数值域的中点就是基准点)
4. 同角三角函数基本关系式
   平方关系: \\(\sin^2\alpha+\cos^2\alpha=1\\)
   商关系: \\(\frac{\sin\alpha}{\cos\alpha}=\tan\alpha\enspace\\) (\\(\alpha\neq k\pi+\frac{\pi}{2}\\) , \\(k \in Z\\))
5. 三角恒等变换
   和差角公式:
   \\(\sin(\alpha\pm\beta)=\sin\alpha\cos\beta\pm\cos\alpha\sin\beta\\)
   \\(\cos(\alpha\pm\beta)=\cos\alpha\cos\beta\mp\sin\alpha\sin\beta\\)
   \\(\tan(\alpha\pm\beta)=\frac{\tan\alpha\pm\tan\beta}{1\mp\tan\alpha\cdot\tan\beta}\\)
   二倍角公式:
   \\(\sin2\alpha=2\sin\alpha\cos\alpha\\)
   \\(\cos2\alpha=\cos^2\alpha-\sin^2\alpha=1-2\sin^2\alpha=2\cos^2\alpha-1\\)
   辅助角公式:
   \\(a\sin{x}+b\cos{x}=\sqrt{a^2+b^2}\sin(x+\varphi)=\sqrt{a^2+b^2}\cos(x-\varphi)\\)
   \\(\tan\varphi=\frac{b}{a}\\) , \\(\varphi\\) 为辅助角
6. 解三角形
   正弦定理: \\(2R=\frac{a}{\sin A}=\frac{b}{\sin B}=\frac{c}{\sin C}\\)
   正弦定理推论: \\(2R=\frac{a+b+c}{\sin A+\sin B+\sin C}\\) , \\((\frac{a}{\sin A})^2=\frac{bc}{\sin B\sin C}\\) , \\((\frac{a}{\sin A})^3=\frac{abc}{\sin A\sin B\sin C}\\)
   余弦定理: \\(\begin{cases} a^2=b^2+c^2-2bc\cos A \\\ b^2=a^2+c^2-2ac\cos B \\\ c^2=a^2+b^2-2ab\cos C \end{cases}\\)
   余弦定理推论: \\(\cos{A} = \frac{b^2 + c^2 - a^2}{2bc}\\) , \\(\cos{B} = \frac{a^2 + c^2 - b^2}{2ac}\\) , \\(\cos{C} = \frac{a^2 + b^2 - c^2}{2ab}\\)
   三角形面积公式: \\(S_\triangle=\frac{1}{2}bc\sin A=\frac{1}{2}ac\sin B=\frac{1}{2}ab\sin C\\)
   解三角形记得判断求出的该角能否为钝(锐)角 (大角对大边, 小角对小边)

### 导数及其应用

1. 导数的概念及其几何意义
   平均变化率: 函数 \\(y=f(x)\\) 从 \\(x_1\\) 到 \\(x_2\\) 的平均变化率为 \\(\frac{f(x_2)-f(x_1)}{x_2-x_1}=\frac{\vartriangle{y}}{\vartriangle{x}}\\)
   瞬时变化率: 函数 \\(y=f(x)\\) 在 \\(x=x_0\\) 处的瞬时变化率是 \\(f'(x_0)=\lim\limits_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}\\)
   几何意义: 导数是函数曲线随 \\(x\\) 轴变化的速度
2. 导数的计算
   导数公式:
   1. \\(\(c\)'=0\enspace\\) (\\(c\\) 为常数)
   2. \\((x^a)' = ax^{a-1}\enspace\\) (\\(a\in Q^*\\))
   3. \\((\sin x)'=\cos x\\)
   4. \\((\cos x)'=-\sin x\\)
   5. \\((a^x)'=a^x\ln a\\)
   6. \\((\log_a x)'=\frac{1}{x\ln a}=\frac{1}{x}\log_a e\\)
   7. \\((e^x)'=e^x\\)
   8. \\(\ln x=\frac{1}{x}\\)
   
   导数运算法则:
   \\([f(x)\pm g(x)]'=f'(x)\pm g'(x)\\)
   \\([f(x)g(x)]'=f'(x)g(x)+f(x)g'(x)\\)
   \\([\frac{f(x)}{g(x)}]'=\frac{f'(x)g(x)-f(x)g'(x)}{[g(x)]^2}\enspace\\) (\\(g(x)\neq 0\\))
   复合函数: 一般地, 对于两个函数 \\(y=f(u)\\) 和 \\(u=g(x)\\) . 如果通过变量 \\(u\\)、\\(y\\)可以表示成一个关于 \\(x\\) 的函数, 那么称这个函数 \\(f(g(x))\\) 为 \\(y=f(u)\\) 和 \\(u=g(x)\\) 的复合函数. 记作\\(y=f(g(x))\\)
   复合函数的求导: \\(f'(g(x))=f'(u)\cdot g'(x)\\)
3. 导数在研究函数中的作用
   * 函数的单调性与其导函数的正负有如下关系:
     存在函数 \\(y=f(x)\\) , 在某个区间 \\((a,b)\\) 内,
     如果 \\(f'(x)>0\\) , 则该函数在这个区间内单调递增
     如果 \\(f'(x)<0\\) , 则该函数在这个区间内单调递减
   * 利用导数找函数极值点和极值:
     首先得 \\(\exist f'(a)=0\\)
     极小值点: 若在点 \\(x=a\\) 附近, 左侧 \\(f'(x)<0\\) , 右侧 \\(f'(x)>0\\) . 则点 \\(a\\) 叫做函数的极小值点
     极大值点: 若在点 \\(x=a\\) 附近, 左侧 \\(f'(x)>0\\) , 右侧 \\(f'(x)<0\\) . 则点 \\(a\\) 叫做函数的极大值点
   
   求函数 \\(y=f(x)\\) 在区间 \\([a,b]\\) 的最大值与最小值的步骤如下
   1. 求函数 \\(y=f(x)\\) 在 \\((a,b)\\) 内的极值
   2. 将求到的各极值连同端点处的函数值 \\(f(a)\\)、\\(f(b)\\) 比较. 其中最大的是最大值; 最小的是最小值
4. 定积分与微积分基本定理
   1. 微分
      先来看看微分的概念 \\(dx=\lim\limits_{\varDelta x\to 0}\varDelta x\\)
      结合导数的定义, 有 \\(f'(x)=\dfrac{dy}{dx}\rArr dy=f'(x)dx\\)
      关于微分的公式:
      1. \\(df(x)=f'(x)dx\\)
      2. \\(d(ax+b)=adx\\)
   2. 定积分
      定积分四部曲: 分割->近似代替->求和->取极限
      定积分概念: 
      \\(\int_a^b f(x)dx=\lim\limits_{n\to\infty}\displaystyle\sum_{i = 1}^n\frac{b-a}{n}f(\xi_i)\\)
      \\(a\\) 与 \\(b\\) 分别叫做积分下限和积分上限, 组成的区间 \\([a,b]\\) 叫做积分区间
      函数 \\(f(x)\\) 叫做被积函数, \\(x\\) 叫做积分变量, \\(f(x)dx\\) 叫做被积式
      上式中 \\(dx\\) 与 \\(\frac{b-a}{n}\\) 对应, 几何意义为被无穷分割的区间 \\([a,b]\\) 中的一小段, \\(\xi_i\\) 表示这一小段对应的位置
      定积分性质:
      1. (线性性质)
         \\(\int_a^b kf(x)dx=k\int_a^b f(x)dx\\)
         \\(\int_a^b[f_1(x)\pm f_2(x)]dx=\int_a^b f_1(x)dx\pm\int_a^b f_2(x)dx\\)
      2. (积分区间的可加性) \\(\int_a^b f(x)dx=\int_a^c f(x)dx+\int_c^b f(x)dx\enspace\\) (\\(a<c<b\\))
      3. \\(\int_a^b f(x)dx=-\int_b^a f(x)dx\\)
      4. 函数值大于等于零时, 积分大于零; 函数值小于等于零时, 积分小于零
         \\(f(x)\geqslant 0\rArr\int_a^bf(x)dx>0\\) , \\(f(x)\leqslant 0\rArr\int_a^b f(x)dx<0\\)
      5. 若 \\(f(x)\\) 是奇函数, 则 \\(\int_{-a}^a f(x)dx=0\\) (奇函数沿原点对称, 正好抵消)
         若 \\(f(x)\\) 是偶函数, 则 \\(\int_{-a}^a f(x)dx=2\int_0^a f(x)dx\\) (偶函数沿 \\(y\\) 轴对称)
   3. 微积分基本定理
      一般地, 如果 \\(f(x)\\) 是区间 \\([a, b]\\) 上的连续函数. 并且 \\(\exist F'(x)=f(x)\\), 那么
      \\(\int_a^b f(x)dx=F(b)-F(a)=F(x)|_a^b=[F(x)+c]|_a^b\\)
      这个结论叫做微积分基本定理, 也称牛顿⋅莱布尼茨公式.


## 数列

1. 等差数列 (Arithmetic progression)
   通项公式: \\(a_n=a_1+(n-1)d\\)
   前 \\(n\\) 项和: \\(S_n=na_1+\frac{(n-1)n}{2}d=\frac{(a_1+a_n)n}{2}\\)
   性质:
   1. 设等差数列 \\(A,B,C\\) , 若 \\(B\\) 为等差中项, 则有 \\(B=\frac{A+C}{2}\\)
   2. \\(m+n=p+q\rArr a_m+a_n=a_p+a_q\enspace\\) (\\(m,n,p,q\in N^*\\))
   3. 数列的前 \\(n\\) 项和 \\(S_n\\) 和 \\(a_n\\) 的关系
      \\(a_n=\begin{cases} S_1 & n=1 \\\ S_n-S_{n-1} & n\geqslant 2 \end{cases}\\)
   4. 等差数列前 \\(n\\) 项和性质: 等差数列 \\(\\{a_n\\}\\) 中, 连续的 \\(n\\) 项之和构成的数列(\\(S_n,S_{2n}-S_n,S_{3n}-S_{2n},S_{4n}-S_{3n},\dots\\))构成等差为 \\(n^d\\) 的等差数列
2. 等比数列 (Geometric progression)
   通项公式: \\(a_n=a_1q^{n-1}\\)
   前 \\(n\\) 项和: \\(S_n=\frac{a_1(1-q^n)}{1-q}=\frac{a_1-a_nq}{1-q} \quad (q\neq 1)\\)
   性质:
   1. 设等比数列 \\(A,B,C\\) , 若 \\(B\\) 为等比中项, 则有 \\(B^2=AC\\)
   2. \\(k+l=m+n\rArr a_k\cdot a_l=a_m\cdot a_n\enspace\\) (\\(k,l,m,n\in N^*\\))
   3. 若 \\(\\{a_n\\} , \\{b_n\\}\\) 是项数相同的等比数列, 且公比分别是 \\(p\\) 和 \\(q\\)
      则
      \\(\\{\lambda a_n\\}\\) 的公比为 \\(p\\) , \\(\\{\frac{1}{a_n}\\}\\) 的公比为 \\(\frac{1}{p}\\)
      \\(\\{a_n^2\\}\\) 的公比为 \\(p^2\\) , \\(\\{a_nb_n\\}\\) 的公比为 \\(pq\\)
      \\(\\{\frac{a_n}{b_n}\\}\\) 的公比为 \\(\frac{p}{q}\\)
   4. 等比数列前 \\(n\\) 项和性质: 在公比不等于 \\(-1\\) 的等比数列 \\(\\{a_n\\}\\) 中, 连续的 \\(n\\) 项之和构成的数列(\\(S_n,S_{2n}-S_n,S_{3n}-S_{2n},S_{4n}-S_{3n},\dots\\))构成公比为 \\(q^n\\) 的等比数列
   5. 在等比数列中, 当项数为偶数时, 比时有 \\(\dfrac{S_偶}{S_奇}=q\\) (全部偶数项除以全部奇数项)
3. 其他
   并项求和: 如 \\(S=-1+2-3+4-5+6+(-1)^n\\)
   1. 当 \\(n\\) 为偶 \\(S_n=\frac{n}{2}\\)
   2. 当 \\(n\\) 为奇 \\(S_n=S_{n-1}-n=\frac{n-1}{2}-n\\)

## 复数

1. 复数的概念
   \\(复数域\begin{cases} 实数 \begin{cases} 有理数 \\\ 无理数 \end{cases} \\\ 虚数 \begin{cases} 纯虚数 \\\ 非纯虚数 \end{cases} \end{cases}\\)

   形如 \\(a+bi\enspace\\) (\\(a,b\in R\\)) 的数叫做复数, \\(i\\) 叫做复数单位
   当 \\(a=0\\) 且 \\(b\neq0\\) 时. 叫做纯虚数.

   虚数 \\(i\\) 的周期性(虚数的周期为 4): 
   \\(i^{4n+1}=i\\)
   \\(i^{4n+2}=-1\\)
   \\(i^{4n+3}=-i\\)
   \\(i^{4n}=1\\)

   共轭复数: 一般地, 当两个复数的实部相等, 虚部互为相反数时, 这两个复数互为共轭复数(虚部不等于 0 的两个共轭复数也叫做共轭虚数)

2. 复数的四则运算
   复数的乘法运算 \\((a+bi)(c+di)=ac+adi+bci+bdi^2=(ac-bd)+(ad+bc)i\\)
   复数的除法运算 \\((a+bi)\div(c+di)=\frac{a+bi}{c+di}=\frac{(a+bi)(c-di)}{(c+di)(c-di)}=\frac{ac+bd}{c^2-d^2}+\frac{bc-ad}{c^2-d^2}i\\)

   有复数 \\(Z=a+bi\enspace\\) (\\(a,b\in R\\)) 对应复平面上的点 \\(Z\\) , 则 \\(Z(a, b)\\) 到原点距离为 \\(\sqrt{a^2+b^2}\\)

## 逻辑

1. 常用逻辑用语
   1. 命题及其关系
      四种命题:
      1. 原命题: 若 \\(a\\) , 则 \\(b\\)
      2. 逆命题: 若 \\(b\\) , 则 \\(a\\)
      3. 否命题: 若非 \\(a\\) , 则非 \\(b\\)
      4. 逆否命题: 若非 \\(b\\) , 则非 \\(a\\)

      原命题和逆否命题同真同假, 否命题和逆命题同真同假
      命题关系: 互逆, 互否, 互为逆否

      充分条件: 若 \\(p\\) 能推出 \\(q\\), 则 \\(p\\) 是 \\(q\\) 的充分但不必要条件; 表达式 \\(p\rArr q\\) , 且 \\(p\nLeftarrow p\\)
      必要条件: 若 \\(q\\) 的结果必定有 \\(p\\) , 则 \\(p\\) 是 \\(q\\) 的必要但不充分条件; 表达式 \\(p\lArr q\\) , 且 \\(p\nRightarrow p\\)
   2. 逻辑连结词或\且\非
      1. 或: 符号 \\(p \lor q\\) , \\(p\\) 或 \\(q\\) 其中任意一个成立, 结果为真
      2. 且: 符号 \\(p \land q\\) , \\(p\\) 和 \\(q\\) 全部成立, 结果才为真
      3. 非: 符号 \\(\lnot p\\), 若 \\(p\\) 不成立, 结果为真
   3. 全称量词与存在量词
      全称量词: 符号 \\(\forall\\) . 如 \\(\forall x\in M\\) , \\(f(x)\\) 表示"对于函数的任意值(都满足某种条件)"
      存在量词: 符号 \\(\exist\\) . 如 \\(\exist x\in M\\) , \\(f(x)\\) 表示"函数存在某个值(满足某种条件)"
2. 推理与证明
   1. 合情推理与演绎推理
      * 合情推理(结论不一定可靠)
        * 归纳推理: 由某类事物的部分对象具有某些特征, 推出该类事物的全部对象都具有这些特征的推理, 或者由个别事实概括出一般结论的推理 (部分到整体, 个别到一致)
        * 类比推理: 由两类对象具有某些类似特征和其中一类对象的某些已知特征, 推出另一类对象也具有这些特征的推理(特殊到特殊)
      * 演绎推理
        * 从一般到特殊
        * 在大, 小前提及推理形式都正确的情况下, 结论必正确
        
        "三段论"是演绎推理的一般模式, 包括
        1. 大前提(已知的一般原理)
        2. 小前提(所研究的特殊情况)
        3. 结论(根据一般原理, 对特殊情况做出的判断)
        
        例子:
        ```
        大前提: M是P
        小前提: S是M
        结论:   S是P
        ```
   2. 直接证明与间接证明
      * 直接证明
        1. 综合法
           利用已知条件和某些数学定义、公理、定理等, 经过一系列的推理论证, 最后推导出所要证明的结论成立.
           特点: 由因导果(顺推)
           
           用 \\(P\\) 表示已知条件、已有的定义、公理、定理等, \\(Q\\) 表示所要证明的结论:
           \\(P\rArr Q_1\rarr Q_1\rArr Q_2\rarr Q_2\rArr Q_3\rarr\dots\rarr Q_n\rArr Q\\)
        2. 分析法
           从要证明的结论出发, 逐步寻求使它成立的充分条件, 直至最后, 把要证明的结论归结为判定一个明显成立的条件(已知条件、定义、公理、定理等)为止.
           特点: 由果导因(逆推)
           用 \\(Q\\) 表示要证明的结论:
           \\(Q\lArr P_1\rarr P_1\lArr P_2\rarr P_2\lArr P_3\rarr\dots\rarr\\) \[一个明显成立的条件\] 
      * 间接证明
        1. 反证法
           假设原命题不成立(即在原命题条件下, 结论不成立), 经过正确的推理, 最后得出矛盾. 因此说明假设错误, 从而证明了原命题成立.
           三个步骤: 反设->归谬->存真
3. 数学归纳法
   用于证明一个与正整数 \\(n\\) 有关的命题
   1. (归纳奠基)证明当 \\(n\\) 取第一个值 \\(n_0\enspace\\) (\\(n_0\in N^+\\)) 时命题成立
   2. (归纳递推)假设 \\(n=k\enspace\\) (\\(k\geqslant n_0\\) , \\(k\in N^+\\)) 时命题成立. 证明当 \\(n=k+1\\) 时命题也成立

## 算法初步

1. 辗转相除法(求最大公约数)
   例: 求 8251 与 6105 的最大公约数
   \\(8251=6105\times 1+2146\\) (6105 与 2146 的公约数也是 8251 与 6105 的公约数)
   \\(6105=2146\times 2+1813\\)
   \\(2146=1813\times 1+333\\)
   \\(1813=333\times 5+148\\)
   \\(333=148\times 2+37\\)
   \\(148=37\times 4\\)
   \\(\therefore\\) 37 是 148 与 37 的最大公约数, 也是 8251 与 6105 的最大公约数
2. 更相减损术(求最大公约数)
   方法:
   1. 任意给定两个正整数, 判断它们是否都是偶数. 若是, 用 2 约简; 若不是, 执行第二步
   2. 以较大的数减去较小的数, 接着把所得的差与较小的数比较, 并以大数减小数.
      继续这个操作, 直到所得的数相等为止.
   
   例: 求 98 与 63 的最大公约数
   因为 63 不是偶数, 执行第二步
   \\(98-63=35\\)
   \\(63-35=28\\)
   \\(35-28=7\\)
   \\(28-7=21\\)
   \\(21-7=14\\)
   \\(14-7=7\\)
   \\(\therefore\\) 98 和 63 的最大公约数为 7
3. 秦九韶算法
   把 \\(f(x)=a_nx^n+a_{n-1}x^{n-1}+\dots+a_1x+a_0\\) 改写成如下形式
   \\(\begin{aligned} f(x) & =a_nx^n+a_{n-1}x^{n-1}+\dots+a_1x+a_0 \\\ & =(a_nx^{n-1}+a_{n-1}x^{n-2}+\dots+a_1)x+a_0 \\\ & =((a_nx^{n-2}+a_{n-1}x^{n-3}+\dots+a_2)x+a_1)x+a_0 \\\ & =\dots \\\ & =(\dots((a_nx+a_{n-1})x+a_{n-2})x+\dots+a_1)x+a_0 \end{aligned}\\)
   求多项式的值时, 首先计算内层内一次多项式的值
   \\(v_1=a_nx+a_{n-1}\\)
   \\(v_2=v_1x+a_{n-2}\\)
   \\(v_3=v_2x+a_{n-3}\\)
   \\(\dots\\)
   \\(v_n=v_{n-1}x+a_0\\)
   \\(v_n\\) 即为该式的值, 这种算法可以减少大量的幂计算
4. 进位制: 约定满二进一, 就是二进制.
   二转十通过按位权展开
   十转二通过除二取余法
