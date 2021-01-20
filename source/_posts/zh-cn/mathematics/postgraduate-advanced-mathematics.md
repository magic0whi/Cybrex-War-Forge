---
title: postgraduate-advanced-mathematics
toc: true
category: mathematics
lang: zh-cn
date: 2021-01-19 09:08:57
tags:
---

同济高等数学笔记整合
基于 [wmathor/Postgraduate-Advanced-Mathematics](https://github.com/wmathor/Postgraduate-Advanced-Mathematics)
复合函数就是初等函数套初等函数
补充了级数部分

<!-- more -->

## 函数与极限

### 函数

1. 函数:
   有集合 \\(D\\) 和 \\(x\\)、\\(y\\) 两个变量. 若对任意 \\(x\in D\\) ,
   总存在唯一确定的解 \\(y\\) 与 \\(x\\) 对应, 称 \\(y\\) 为 \\(x\\) 的函数,
   记作 \\(y=f(x)\\) , \\(D\\) 为 \\(x\\) 的定义域
2. 反函数:
   \\(y=f(x)\enspace\\) (\\(x\in D\\)) 严格单调 **(单调函数必有单调反函数)**
   若 \\(y=f(x) \implies x=\varphi(y)\\)
   则 \\(\varphi(y)\\) 就是 \\(f(x)\\) 的反函数
3. 基本初等函数:
   1. \\(x^a\\)
   2. \\(a^x\\) (\\(a>0\\) 且 \\(a\ne 1\\))
   3. \\(\log_a{x}\\) (\\(a>0\\) 且 \\(a\ne 1\\))
   4. \\(\sin x,\cos x,\tan x,\cot x,\sec x,\csc x\\)
4. 初等函数: 由常数、基本初等函数经过四则运算、复合运算而成的式子

#### 初等性质

1. 奇偶性
   设 \\(y=f(x)\enspace\\) (\\(x\in D\\) , \\(D\\) 关于原点对称)
   若对于 \\(\forall x\in D\\), 有
   \\(f(-x)=-f(x)\\) , 则为奇函数;
   \\(f(-x)=f(x)\\) , 则为偶函数
2. 单调性
   设 \\(y=f(x)\enspace\\) (\\(x\in D\\))
   若 \\(\exist x_1,x_2\in D\\) 且 \\(x_1<x_2\\) 时 , 有 \\(f(x_1)<f(x_2)\\) , 称 \\(f(x)\\) 在 \\(D\\) 上严格单调递增;
   若 \\(\exist x_1,x_2\in D\\) 且 \\(x_1<x_2\\) 时 , 有 \\(f(x_1)>f(x_2)\\) , 称 \\(f(x)\\) 在 \\(D\\) 上严格单独递减
   {% asset_img 1.png %}

3. 有界性
   设 \\(y=f(x)\enspace\\) (\\(x\in D\\)) , 函数的界 \\(M\\) (即值域范围)
   若 \\(\exist M>0\\) , 对于 \\(\forall x\in D\\) , 有 \\(|f(x)|\leqslant M\\) , 称 \\(f(x)\\) 在 \\(D\\) 上有界
   {% asset_img 2.png %}

   若 \\(\forall x\in D\\) , \\(f(x)\geqslant M_1\\) , 有下界
   若 \\(\forall x\in D\\) , \\(f(x)\leqslant M_2\\) , 有上界
   如: \\(|f(x)|\leqslant 3\hArr\begin{cases} f(x)\geqslant -3 \\\ f(x)\leqslant 3 \end{cases}\\)
4. 周期性
   设 \\(y=f(x)\enspace\\) (\\(x\in D\\)) ,
   若 \\(\exist T>0\\) , 对于 \\(\forall x\in D\enspace\\) (\\(x+T\in D\\)) , 有 \\(f(x+T)=f(x)\\) , 称 \\(f(x)\\) 为周期函数

### 数列极限

1. 数列收敛定义(\\(\epsilon−N\\)):
   设数列 \\(\\{a_n\\}\\) , \\(A\\) 为极限值, 最大误差 \\(\varepsilon\\) , 数列在元素 \\(a_N\\) 后极限有效(即之后数列元素与极限值的误差进入容许范围),
   若 \\(\forall\varepsilon > 0 , \exist N > 0\\) , 当 \\(n > N\\) 时 \\(|a_n - A| < \varepsilon\\)
   称收敛于极限 \\(A\\) , 记作 \\(\lim\limits_{n\to\infty}=A\\) 或 \\(a_n\to A\enspace\\) (\\(n\to\infty\\))
   例:
   设通项公式 \\(a_n=\frac{n+1}{2n}\\), 具体值为 \\(\frac{3}{4},\frac{2}{3},\frac{5}{8},\frac{3}{5},\dots\\) , 观察得极限 \\(a_n\to\frac{1}{2}\\)
   设最大误差 \\(\varepsilon=\frac{1}{10}>0\\), 则误差值 \\(|a_n-\frac{1}{2}|=\frac{1}{2n}<\frac{1}{10}\Harr n>5\\).
   同理:
   若 \\(\varepsilon=\frac{1}{100}>0\\), 则 \\(\frac{1}{2n}<\frac{1}{100}\Harr n>50\\)
   若 \\(\varepsilon=\frac{1}{1000}>0\\), 则 \\(\frac{1}{2n}<\frac{1}{1000}\Harr n>500\\)
   由此发现该数列有极限: \\(\lim\limits_{n\to\infty}a_n=\frac{1}{2}\\)
2. 性质
   1. 唯一性: 数列有极限必唯一
      证明(反证法):
      设数列有两个极限 \\(\lim\limits_{n\to\infty}a_n=A ,\enspace \lim\limits_{n\to\infty}a_n = B \\) , 且 \\(A\neq B\\)
      不妨设 \\(A>B\\) , \\(\varepsilon=-\dfrac{A+B}{2}\\) (误差值的定义由 \\(\varepsilon + A=-\varepsilon - B\\) 解出, 目的是让下面两个\\(a_n\\)的值域没有交集)
      \\(\because\lim\limits_{n\to\infty}a_n=A\\) , \\(\therefore\exist N_1>0\\) , 当 \\(n>N_1\\) 时, \\(|a_n-A|<\varepsilon\Harr\frac{3A+B}{2}<a_n<\frac{A-B}{2}\\) (1)
      \\(\because\lim\limits_{n\to\infty}a_n=B\\) , \\(\therefore\exist N_2>0\\) , 当 \\(n>N_2\\) 时, \\(|a_n-B|<\varepsilon\Harr\frac{A-B}{2}<a_n<\frac{-A+B}{2}\\) (2)
      取 \\(N=\text{max}\\{N_1,N_2\\}\\) , 当 \\(n<N_2\\) 时, (1)、(2) 都成立, 但这两个不等式没有交集, 矛盾, 所以 \\(A>B\\) 不对, 同理 \\(B>A\\) 也不对.
      \\(\therefore A=B\\), 极限值只有一个.
   2. 有界性:
      若 \\(\lim\limits_{n\to\infty}a_n=A\\) , 则 \\(\exist M>0\\) , 使得 \\(|a_n|\leqslant M\\) , **反之不成立**.
      证明: 
      \\(\rArr\\) 设 \\(\varepsilon=1>0\\)
      \\(\because\lim\limits_{n\to\infty}a_n=A\\)
      \\(\therefore\exist N>0\\) , 当 \\(n>N\\) 时 , \\(|a_n-A|<1\\)
      \\(\because||a_n|-|A||\leqslant|a_n-A|\\) (三角不等式)
      \\(\therefore\\) 当 \\(n>N\\) 时, \\(||a_n|-|A_1||<1\rArr|a_n|<1+|A|\\) 在 \\(n>N\\) 时成立
      取 \\(M=\text{max}\\{|a_1|,|a_2|,\dots,|a_n|,1+|A|\\}\\) , 对于 \\(\forall n\\) , 有 \\(|a_n|\leqslant M\\)
      \\(\nLeftarrow\\) 设 \\(a_n=1+(-1)^n\\) , 有 \\(|a_n|\leqslant 2\\) , 但 \\(\lim\limits_{n\to\infty}a_n\\) 不存在
   3. 保号性:
      若 \\(\lim\limits_{n\to\infty}a_n=A>0(<0)\\) , 则 \\(\exist N>0\\) , 当 \\(n>N\\) 时 , \\(a_n>0(<0)\\)
      证明:
      设 \\(A>0\\) , 取 \\(\varepsilon=\frac{A}{2}>0\\)
      \\(\because\lim\limits_{n\to\infty}a_n=A\\) , \\(\therefore\exist N>0\\) , 当 \\(n>N\\) 时 , \\(|a_n-A|<\frac{A}{2}\hArr\frac{A}{2}<a_n<\frac{3A}{2}\hArr a_n>\frac{A}{2}>0\\)
      设 \\(A<0\\) , 取 \\(\varepsilon=-\frac{A}{2}>0\\)
      \\(\because\lim\limits_{n\to\infty}a_n=A\\) , \\(\therefore\exist N>0\\) , 当 \\(n>N\\) 时 , \\(|a_n-A|<-\frac{A}{2}\hArr\frac{3A}{2}<a_n<\frac{A}{2}\hArr a_n<\frac{A}{2}<0\\)

### 函数极限

1. 定义
   \\(\varepsilon-\delta\\) 语言定义法: (\\(\varepsilon\\) 为值域的误差, \\(\delta\\) 为定义域的误差)
   若 \\(\forall\varepsilon>0\\) , \\(\exist\delta>0\\) , 当 \\(0<|x-a|<\delta\\) 时 \\(|f(x)-A|<\varepsilon\\) ,
   称 \\(f(x)\\) 当 \\(x\to 0\\) 时以 \\(A\\) 为极限
   记作 \\(\lim\limits_{x\to a}f(x)=A\\) 或 \\(f(x)\to A\enspace\\) (\\(x\to a\\))

   \\(\varepsilon-X\\) 语言定义法: (\\(X\\) 为值域临界点)
   若 \\(\forall\varepsilon>0\\) , \\(\exist X>0\\) , \\(|f(x)-A|<\varepsilon\\)
   1. 当 \\(x>X\\) 时, \\(\lim\limits_{x\to+\infty}f(x)=A\\)
   2. 当 \\(x<-X\\) 时, \\(\lim\limits_{x\to-\infty}f(x)=A\\)
   3. 当 \\(|x|>X\\) 时, \\(\lim\limits_{x\to\infty}f(x)=A\\)
2. 性质
   1. 唯一性(函数有极限必唯一)
      证明: 设 \\(\lim\limits_{x\to a}f(x)=A\\) , \\(\lim\limits_{x\to a}f(x)=B\\)
      不妨设 \\(A>B\\) , 取 \\(\varepsilon=\frac{A-B}{2}>0\\) (凑出矛盾的结果)
      \\(\because\lim\limits_{x\to a}f(x)=A\\)
      \\(\therefore\exist\delta_1>0\\) , 当 \\(0<|x-a|<\delta_1\\) 时, \\(|f(x)-A|<\frac{A-B}{2}\hArr\frac{A+B}{2}<f(x)<\frac{3A-B}{2}\\) (1)
      又 \\(\because\lim\limits_{x\to a}f(x)=B\\)
      \\(\therefore\exist\delta_2>0\\) , 当 \\(0<|x-a|<\delta_2\\) 时, \\(|f(x)-B|<\frac{A-B}{2} \hArr \frac{3B-A}{2}<f(x)<\frac{A+B}{2}\\) (2)
      取 \\(\delta=\text{min}\\{\delta_1,\delta_2\\}\\) , 当 \\(0<|x-a|<\delta\\) 时 (1)(2) 皆成立, 矛盾.
      \\(\therefore A>B\\) 不对, 同理 \\(A<B\\) 也不对.
      \\(\therefore A=B\\), 极限值只有一个.
   2. 局部有界性: 设 \\(\lim\limits_{x\to a}f(x)=A\\) , \\(\exist\delta>0\\) , \\(M>0\\) , 当 \\(0<|x-a|<\delta\\) 时, \\(|f(x)|\leqslant M\\)
      证明: 证明目标是找出 \\(|f(x)|\leqslant\\) 某个确切的值
      取 \\(\varepsilon=1>0\\)
      \\(\because\lim\limits_{x\to a}f(x)=A\\)
      \\(\therefore\exist\delta>0\\) , 当 \\(0<|x-a|<\delta\\) 时, \\(|f(x)-A|<1\\)
      又 \\(\because||f(x)|-|A||\leqslant|f(x)-A|\\) (三角不等式)
      \\(\therefore\\) 当 \\(0<|x-a|<\delta\\) 时, \\(||f(x)|-|A||<1\rArr|f(x)|<1+|A|(=M)\\)
      \\(\therefore\\) 当 \\(0<|x-a|<\delta\\) 时, \\(|f(x)|\leqslant M\\)
   3. 保号性: 设 \\(\lim\limits_{x\to a}f(x)=A>0(<0)\\) , 则 \\(\exist\delta>0\\) , 当 \\(0<|x-a|<\delta\\) 时, \\(f(x)>0(<0)\\)
      证明:
      1. 若 \\(A>0\\) , 取 \\(\varepsilon=\frac{A}{2}>0\\)
         \\(\because\lim\limits_{x\to a}f(x)=A\\) ,
         \\(\therefore\exist\delta>0\\) , 当 \\(0<|x-a|<\delta\\) 时 \\(|f(x)-A|<\frac{A}{2}\rArr f(x)>\frac{A}{2}>0\\)
      2. 若 \\(A<0\\) , 取 \\(\varepsilon=-\frac{A}{2}>0\\)
         \\(\because\lim\limits_{x\to a}f(x)=A\\) ,
         \\(\therefore\exist\delta>0\\) , 当 \\(0<|x-a|<\delta\\) 时 \\(|f(x)-A|<-\frac{A}{2}\rArr f(x)>\frac{A}{2}>0\\)

Notes:
1. \\(\\{x|0<|x-a|<\delta\\}\\) 可表示为 \\(\mathring{\text{U}}(a\cdot \delta)\\) (a的取心δ邻域)
   {% asset_img 3.png %}

2. \\(x\to a\\) 时 \\(\begin{cases} x\to a^- \\\ x\to a^+ \end{cases}\\)
3. 左极限与右极限
   若 \\(\forall\varepsilon>0\\) , \\(\exist\delta>0\\)
   1. 当 \\(x\in(a-\delta,a)\\) 时 \\(|f(x)-A| < \varepsilon\\) ,
      此时 \\(A\\) 称 \\(f(x)\\) 在 \\(x=a\\) 处左极限,
      记为 \\(\lim\limits_{x\to a^-}f(x)=A\\) 或 \\(f(a-0)=A\\)
   2. 当 \\(x\in(a,a+\delta)\\) 时 \\(|f(x-B)|<\varepsilon\\) ,
      此时 \\(B\\) 称 \\(f(x)\\) 在 \\(x=a\\) 处右极限,
      记为 \\(\lim\limits_{x\to a^+}f(x)=B\\) 或 \\(f(a+0)=B\\)
4. \\(\lim\limits_{x\to a}f(x)\\) 意味着左右极限存在且相等
5. \\(\lim\limits_{x\to a}f(x)\\) 与 \\(f(a)\\) 无关(除非该点连续)
   如:
   1. 分段函数 \\(f(x)=\begin{cases} x-1 & x<0 \\\ 0 & x=0 \\\ 2x-1 & x>0 \end{cases}\\), 它的极限为 \\(\begin{cases} \lim\limits_{x\to 0^+}f(x)=-1 \\\ \lim\limits_{x\to 0^-}f(x)=-1 \end{cases}\rArr\lim\limits_{x\to 0}f(x)=-1\\) , 但 \\(f(0)=0\\)
   2. \\(\lim\limits_{x\to 2}\frac{x^2-4}{x-2}=\lim\limits_{x\to 2}(x+2)=4\\), 但 \\(f(2)\\) 时分母为零

### 无穷小与无穷大

1. 无穷小
   1. \\(\varepsilon-\delta\\) 定义: 若 \\(\forall\varepsilon>0\\) , \\(\exist\delta>0\\) , 当 \\(0<|x-x_0|<\delta\\) 时 , \\(|\alpha(x)-0|   <\varepsilon\\) , 称 \\(\alpha(x)\\) 在 \\(x\to x_0\\) 时无穷小, 记 \\(\lim\limits_{x\to x_0}\alpha(x)=0\\)
   2. 常规性质:
      1. 若 \\(\alpha\to 0\\) , \\(\beta\to 0\\) , 则 \\(\begin{cases} \alpha\pm\beta\to 0 \\\ k\alpha\to 0 \\\ \alpha\beta\to0 \end{cases}\\)
      2. 无穷小乘有界函数还是无穷小: \\(\alpha\to 0\\) , \\(|\beta|\leqslant M\\) , 则 \\(\alpha\beta\to 0\\)
      3. (重要)任意极限加无穷小还是原极限 \\(\lim\limits_{x\to x_0}f(x)=A \hArr \lim\limits_{x\to x_0}f(x)=A+\alpha\enspace\\) (\\(\alpha\to 0\\))
   
   Notes: 0 是无穷小, 但无穷小不一定为 0
2. 无穷大
   \\(\varepsilon-\delta\\) 定义: 若 \\(\forall M>0\\) , \\(\exist\delta>0\\) , 当 \\(0<|x-x_0|<\delta\\) 时, \\(|f(x)|\geqslant M\rArr\\) 称 \\(f(x)\\) 在 \\(x\to x_0\\) 时无穷大, 记 \\(\lim\limits_{x\to x_0}f(x)=\infty\\)
   \\(\varepsilon-X\\) 定义: 若 \\(\forall M>0\\) , \\(\exist X>0\\) , 当 \\(x>X\\) 时, \\(|f(x)|\geqslant M\rArr\\) 称 \\(f(x)\\) 在 \\(x\to +\infty\\) 时无穷大, 记 \\(\lim\limits_{x\to+\infty}f(x)=\infty\\)
3. 无穷小与无穷大的关系: \\(\lim\limits_{x\to x_0}f(x)=0\hArr\lim\limits_{x\to x_0}\frac{1}{f(x)}=\infty\\)

### 极限的运算法则

1. 四则求导法则
   有 \\(\lim\limits_{x\to x_0}f(x)=A\\) , \\(\lim\limits_{x\to x_0}g(x)=B\\)
   1. 加减: \\(\lim\limits_{x\to x_0}[f(x)\pm g(x)]=\lim\limits_{x\to x_0}f(x)\pm\lim\limits_{x\to x_0}g(x)=A\pm B\\)
   2. 数乘: \\(\lim\limits_{x\to x_0}kf(x)=k\lim\limits_{x\to x_0}f(x)=kA\\)
   3. 乘法: \\(\lim\limits_{x\to x_0}[f(x)g(x)]=\lim\limits_{x\to x_0}f(x)\cdot\lim\limits_{x\to x_0}g(x)=AB\\)
   4. 除法: \\(\lim\limits_{x\to x_0}\frac{f(x)}{g(x)}=\frac{\lim\limits_{x\to x_0}f(x)}{\lim\limits_{x\to x_0}g(x)}=\frac{A}{B}\\)
      极限除法的值以最高阶系数为准:
      设 \\(P(x)=a_nx^n+\dots+a_1x+a_0\\) , \\(Q(x)=b_mx^m+\dots+b_1x+b_0\\)
      则 \\(\lim\limits_{x\to\infty}\frac{P(x)}{Q(x)}=\begin{cases} \frac{a_n}{b_m} & n=m \\\ \infty & n>m \\\ 0 & n<m \end{cases}\\)
2. 复合函数极限法则: 
   设 \\(u=\varphi(x)\neq a\\) , \\(\lim\limits_{u\to a}f(u)=A\\) , \\(\lim\limits_{x\to x_0}\varphi(x)=a\\) , 则 \\(\lim\limits_{x\to x_0}f[g(x)]=A\\)

### 极限存在法则和两个重要极限

1. 极限存在准则
   1. 夹逼定理
      1. 数列型:
         设 \\(\begin{cases} a_n\leqslant b_n\leqslant c_n \\\ \lim\limits_{n\to\infty}a_n=\lim\limits_{n\to\infty}c_n=A \end{cases}\\)
         则 \\(\lim\limits_{n\to\infty}b_n=A\\)
         (证明方法: 利用 \\(\varepsilon−N\\) 定义推出 \\(A-\varepsilon<b_n<A+\varepsilon\rArr|b_n-A|<\varepsilon\\))
      2. 函数型:
         设 \\(\begin{cases} f(x)\leqslant g(x)\leqslant h(x) \\\ \lim f(x)=\lim h(x)=A \end{cases}\\)
         则 \\(\lim g(x)=A\\)
   2. 单调有界数列必有极限
      * \\(\\{a_n\\}\\) 有界 \\(\hArr\\{a_n\\}\\) 有上下界
      * 若 \\(\\{a_n\\}\\) 单调递增: \\(\begin{cases} \text{有上界}\rArr\lim\limits_{n\to\infty}a_n \text{存在} \\\ \text{无上界}\rArr\lim\limits_{n\to\infty}a_n\text{不存在} \end{cases}\\)
      * 若 \\(\\{a_n\\}\\) 单调递减: \\(\begin{cases} \text{有下界}\rArr\lim\limits_{n\to\infty}a_n \text{存在} \\\ \text{无下界}\rArr\lim\limits_{n\to\infty}a_n\text{不存在} \end{cases}\\)
2. 两个重要极限
   1. \\(\lim\limits_{x\to 0}\frac{\sin x}{x}=1\\)
      证明:
      {% asset_img 4.png %}
      
      设 \\(0<x<\frac{\pi}{2}\\)
      \\(S_{\triangle AOB}=\frac{1}{2}\sin x\\)
      \\(S_{扇形AOB}=\frac{1}{2}x\\)
      \\(S_{RT\triangle AOC}=\frac{1}{2}\tan x\\)
      \\(\therefore\\) 结合图片和三者面积公式可得 \\(\sin x<x<\tan x \rArr 1<\frac{x}{\sin x}<\frac{1}{\cos x}\\)
      \\(\because\lim\limits_{x\to0}\cos x=1\\)
      \\(\therefore\lim\limits_{x\to0}\frac{1}{\cos x}=1\\) , \\(\lim\limits_{x\to0}1=1\rArr\lim\limits_{x\to 0}\frac{x}{\sin x}=1\\) (夹逼定理) \\(\rArr\lim\limits_{x\to 0}\frac{\sin x}{x}=1\\)
   2. \\(\lim\limits_{n\to\infty}(1+\frac{1}{n})^n=e\\)

### 无穷小的比较(相除)

1. 无穷小的比较
   设 \\(\alpha\to 0\\) , \\(\beta\to 0\\)
   若 \\(\lim\frac{\beta}{\alpha}=0\\) , 称 \\(\beta\\) 为 \\(\alpha\\) 的高阶无穷小, 记 \\(\beta=\circ(\alpha)\\)
   若 \\(\lim\frac{\beta}{\alpha}=\infty\\) , 称 \\(\beta\\) 为 \\(\alpha\\) 的低阶无穷小
   若 \\(\lim\frac{\beta}{\alpha^k}=k\enspace\\) (\\(k\neq 0,\infty\\)) , 称 \\(\beta\\) 为 \\(\alpha\\) 的 \\(k\\) 阶无穷小
   若 \\(\lim\frac{\beta}{\alpha}=k\enspace\\) (\\(k\neq 0,\infty)\\) , 称 \\(\beta\\) 为 \\(\alpha\\) 的同阶无穷小, 记 \\(\beta=\bigcirc(\alpha)\\)
   若 \\(\lim\frac{\beta}{\alpha}=1\\) , 称 \\(\beta\\) 为 \\(\alpha\\) 的等价无穷小, 记 \\(\beta\sim\alpha\\)
   等价无穷小是同阶无穷小的充分不必要条件
2. 等价无穷小的性质
   设 \\(\alpha\to 0\\) , \\(\beta\to 0\\)
   1. \\(\alpha\sim\beta\hArr\beta=\alpha+\circ(\alpha)\\)
   2. 若 \\(\alpha\sim\alpha_1\\) , \\(\beta\sim\beta_1\\) , \\(\lim\frac{\beta_1}{\alpha_1}=A\\) , 则 \\(\lim\frac{\beta}{\alpha}=A\\)
3. 常用等价无穷小 (\\(x\to 0\\))
   1. \\(x\sim\sin x\\) , \\(x\sim\tan x\\) , \\(x\sim\arcsin x\\) , \\(x\sim\arctan x\\) , \\(x\sim\ln(1+x)\\) , \\(x\sim e^x-1\\)
   2. \\(1-\cos x\sim\frac{x^2}{2}\\)
   3. \\((1+x)^a-1\sim ax\\)

### 函数的连续性与间断点

连续是极限存在的充分不必要条件, 因为间断不代表极限不存在

1. 连续
   1. 函数在一点连续: \\(\lim\limits_{x\to a}f(x)=f(a)\\) 或 \\(f(a-0)=f(a+0)=f(a)\\)
      若 \\(f(a-0)=f(a)\\) , 称 \\(f(a)\\) 在 \\(x=a\\) 左连续
      若 \\(f(a+0)=f(a)\\) , 称 \\(f(a)\\) 在 \\(x=a\\) 右连续
   2. 函数在闭区间连续:
      设 \\(f(x)\\) 在 \\([a,b]\\) 上有定义, 若:
      1. \\(f(x)\\) 在 \\((a,b)\\) 内处处连续
      2. \\(f(a)=f(a+0)\\) , \\(f(b)=f(b-0)\\)
      
      则称 \\(f(x)\\) 在 \\([a,b]\\) 上连续, 记 \\(f(x)\in c[a,b]\\)
2. 间断点及分类
   1. 间断: 若 \\(\lim\limits_{x\to a}f(x)\neq f(a)\\) , 称 \\(f(x)\\) 在 \\(x=a\\) 间断
   2. 分类:
      1. 第一类间断点: \\(f(a-0)\\) , \\(f(a+0)\\) 皆存在
         * 可去间断点: \\(f(a-0)=f(a+0)\neq f(a)\\) {% asset_img 5.png %}
         * 跳跃间断点: \\(f(a-0)\neq f(a+0)\\) {% asset_img 6.png %}
      2. 第二类间断点: \\(f(a-0)\\) , \\(f(a+0)\\) 至少一个不存在
      3. \\(\lim\limits_{x\to 0^-}e^\frac{1}{x}=0\\) , \\(\lim\limits_{x\to 0^+}e^\frac{1}{x}=+\infty\\)

### 连续函数运算及初等函数连续性

1. 连续函数运算
   1. 四则运算
      设 \\(f(x)\\) , \\(g(x)\\) 在 \\(x=x_0\\) 处连续, 则
      1. \\(f(x)\pm g(x)\\) 在 \\(x=x_0\\) 处连续
      2. \\(f(x)g(x)\\) 在 \\(x=x_0\\) 处连续
      3. \\(\frac{f(x)}{g(x)}\\) 在 \\(x=x_0\\) 处连续 (\\(g(x)\neq 0\\))
      (证明思路是证明该点处极限与函数实际取该点值相等, 也就是上节讲到的函数连续定义)
   2. 复合运算
      设 \\(f(u)\\) , \\(u=\varphi(x)\neq a\\)
      若 \\(\lim\limits_{u\to a}f(u)=f(a)\\) , \\(\lim\limits_{x\to x_0}\varphi(x)=a\\) , 则 \\(\lim\limits_{x\to x_0}f[\varphi(x)]=f[\lim\limits_{x\to x_0}\varphi(x)]=f(a)\\)
2. 初等函数连续性: 基本初等函数、初等函数在其定义域内连续

### 闭区间上连续函数的性质

1. 最值定理
   设 \\(f(x)\in c[a, b]\\)
   则 \\(f(x)\\) 在 \\([a,b]\\) 上取到最小值 \\(m\\) 和最大值 \\(M\\)
   即 \\(\exist x_1,x_2\in[a,b]\\) , 使 \\(f(x_1)=m\\) , \\(f(x_2)=M\\)
2. 有界定理
   设 \\(f(x)\in c[a,b]\\)
   则 \\(\exist k>0\\) , 使 \\(\forall x\in[a,b]\\) 有 \\(|f(x)|\leqslant k\\)
3. 零点定理(高中数学中零点存在定理)
   设 \\(f(x)\in c[a,b]\\) , 若 \\(f(a)f(b)<0\\)
   则 \\(\exist c\in[a,b]\\) 使 \\(f\(c\)=0\\)
4. 界值定理
   设 \\(f(x)\in c[a, b]\\)
   则 \\(\forall\eta\in[m,M]\\) , \\(\exist\xi\in[a,b]\\) 使 \\(f(\xi)=\eta\\)
   (即介于 \\(m\\) 和 \\(M\\) 之间的 \\(f(x)\\) 皆可取到)

## 导数与微分

### 导数的概念

1. 导数定义
   设 \\(y=f(x)\enspace\\) (\\(x\in D\\)) , \\(\Delta y=f(x_0+\Delta x)-f(x_0)\enspace\\) (\\(x_0,(x_0+\Delta x)\in D\\))
   若 \\(\lim\limits_{\Delta x\to 0}\frac{\Delta y}{\Delta x}\\) 存在, 称 \\(f(x)\\) 在 \\(x=x_0\\) 处可导, 该极限称为 \\(f(x)\\) 在 \\(x=x_0\\) 处的导数, 记 \\(f^\prime(x_0)\\) 或 \\(\frac{\mathrm{d}y}{\mathrm{d}x}|_{x=x_0}\\)
2. 注意:
   1. 可导一定连续, 连续不一定可导.
      (因为连续函数在点 \\(f^\prime(x)=0\\) 处不可导, 如正弦曲线的 \\(y=1\\) 处左右导数不同)
   2. \\(f^\prime(x_0)=\lim\limits_{\Delta x\to 0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}=\lim\limits_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}\\)
      (证明可通过代入\\(\Delta x=x-x_0\\))
   3. 可导时左右导数存在且相等
      左导数: \\(\lim\limits\_{\Delta x\to 0^-}\frac{\Delta y}{\Delta x}(=\lim\limits_{x\to x_0^-}\frac{f(x)-f(x_0)}{x-x_0})=f\_-^\prime(x_0)\\)
      右导数: \\(\lim\limits\_{\Delta x\to 0^+}\frac{\Delta y}{\Delta x}(=\lim\limits_{x\to x_0^+}\frac{f(x)-f(x_0)}{x-x_0})=f\_+^\prime(x_0)\\)

#### 常见初等函数的导函数

1. \\(C^\prime=0\\)
2. \\((x^n)^\prime=nx^{n-1}\\)
3. \\((a^x)^\prime=a^x\ln a\\)
4. \\((\log_a x)^\prime=\frac{1}{x\ln a}\\)
5. \\((\sin x)^\prime=\cos x\\)
   \\((\cos x)^\prime=-\sin x\\)
   \\((\tan x)^\prime=\sec^2x\\)
   \\((\cot x)^\prime=-\csc^2x\\)
   \\((\sec x)^\prime=\sec x\tan x\\)
   \\((\csc x)^\prime=-\csc x\cot x\\)
6. \\((\arcsin x)^\prime=\frac{1}{\sqrt{1-x^2}}\\)
   \\((\arccos x)^\prime=-\frac{1}{\sqrt{1-x^2}}\\)
   \\((\arctan x)^\prime=\frac{1}{1+x^2}\\)
   \\((\text{arccot }x)^\prime=-\frac{1}{1+x^2}\\) <!-- katex好像没有\arccot -->
7. \\((\sin x)^{(n)}=\sin(x+\frac{nx}{2})\\)
   \\((\cos x)^{(n)}=\cos(x+\frac{nx}{2})\\)
   \\((\frac{1}{ax+b})^{(n)}=(-1)^n n!\frac{a^n}{(ax+b)^{n+1}}\\)

推导:
直接代入 \\(f^\prime(x)=\lim\limits_{\Delta x\to0}\frac{f(x+\Delta x)-f(x)}{\Delta x}\\)
1. \\((x^n)^\prime=nx^{n-1}\\) : 二项式展开可推导
2. \\((a^x)^\prime=a^x\ln a\\) : 直接代入即可, 期间会用到 \\(x=e^{\ln x}\\) 和 \\(x\sim(e^x-1)\\)
   \*特别地 \\((e^x)^\prime=e^x\\)
3. 用微分代替极限表示以显得简洁
   <div>
   $$
   f^\prime(x)=\dfrac{\mathrm{d}y}{\mathrm{d}x}
   =\overbrace{\dfrac{\log_a(x+\mathrm{d}x)-\log_a x}{\mathrm{d}x}=\dfrac{\log_a(\frac{x+\mathrm{d}x}{x})}{\mathrm{d}x}}^{\log_a \frac{M}{N}
   =\log_a M-\log_a N}=\dfrac{\log_a(1+\frac{\mathrm{d}x}{x})}{\mathrm{d}x}
   =\overbrace{\dfrac{\frac{\ln(1+\frac{\mathrm{d}x}{x})}{\ln a}}{\mathrm{d}x}}^{\log_a N=\frac{\log_b N}{\log_b a}}
   =\overbrace{\dfrac{\frac{\frac{\mathrm{d}x}{x}}{\ln a}}{\mathrm{d}x}}^{x\sim\ln(1+x)}=\dfrac{1}{x\ln a}
   $$
   </div>
4. <div>
   $$
   \lim\limits_{\Delta x\to 0}\frac{\sin(x+\Delta x)-\sin x}{\Delta x}
   =\underbrace{\lim\limits_{\Delta x\to 0}\frac{\sin x\cos\Delta x+\cos x\sin\Delta x-\sin x}{\Delta x}}_{\text{和差角公式}}
   =\lim\limits_{\Delta x\to 0}\frac{\sin x(\cos\Delta x-1)}{\Delta x}+\cos x\lim\limits_{\Delta x\to 0}\underbrace{\frac{\sin\Delta x}{\Delta x}}_{x\sim\sin x}=\cos x 
   $$
   </div>
   
   \\((\cos x)'\\) 的推导也同理
   后面的都是将其化为\\(\sin x\\) 和 \\(\cos x\\)的形式然后利用求导的四则运算法则推导 (如 \\(\sec x=\frac{1}{\cos x}\\)、\\(\csc x=\frac{1}{\sin x}\\))
5. 使用[反函数求导法则](#反函数求导法则):
   这里只证明 \\(\arcsin x\\)
   \\(f(x):y=\arcsin x\\) , \\(\varphi(y):x=\sin y\\)
   \\(f^\prime(x)=\frac{1}{\varphi^\prime(y)}\rArr(\arcsin x)^\prime=\dfrac{1}{\cos y}=\underbrace{\frac{1}{\sqrt{1-\sin^2 y}}}_{平方关系式}=\underbrace{\frac{1}{\sqrt{1-x^2}}}\_{带入 x=\sin y}\\)
6. 使用高阶导数归纳法 <span id="induction_method"></span>
   1. \\(f(x)=\sin x\\)
      \\(f^\prime(x)=\cos x=\sin(x+\frac{\pi}{2})\\)
      \\(f^{\prime\prime}(x)=-\sin x=\sin(x+\frac{2\pi}{2})\\)
      \\(f^{\prime\prime\prime}(x)=-\cos x=\sin\(x+\frac{3\pi}{2})\\)
      \\(f^{(4)}(x)=\sin x=\sin\(x+\frac{4\pi}{2})\\)
      \\(\therefore f^{(n)}(x)=\sin(x+\frac{nx}{2})\\)
      同理 \\((\cos x)^{(n)}=\cos(x+\frac{nx}{2})\\)
   2. \\(f(x)=(2x+1)^{-1}\\)
      \\(f^\prime(x)=(-1)(2x+1)^{-2}\times 2\\)
      \\(f^{\prime\prime}(x)=(-1)(-2)(2x+1)^{-3}\times 2^2\\)
      \\(\therefore f^{(n)}(x)=(-1)^n\times n! \times 2^n \times (2x+1)^{-(n+1)}\\)

### 求导法则

1. 四则法则
   设 \\(u(x) , v(x)\\) 可导, 则
   1. 加减: \\([u(x)\pm v(x)]^\prime=u^\prime(x)\pm v^\prime(x)\\)
   2. 数乘: \\((ku)^\prime=ku^\prime\\)
   3. 乘: \\([u(x)v(x)]^\prime=u^\prime(x)v(x)+u(x)v^\prime(x)\\)
   4. 除: \\([\frac{u(x)}{v(x)}]^\prime=\frac{u^\prime(x)v(x)-u(x)v^\prime(x)}{v^2(x)}\enspace\\) (\\(v(x)\neq 0\\))
      推论: \\((uvw)^\prime=u^\prime vw+uv^\prime w+uvw^\prime\\)
2. 四则法则证明:
   1. 令 \\(\varphi(x)=u(x)+v(x)\\)
      则 \\(\Delta\varphi=\varphi(x+\Delta x)-\varphi(x)=u(x+\Delta x)+v(x+\Delta x)-u(x)-v(x)=\Delta u+\Delta v\\)
      进而 \\(\lim\limits_{\Delta x\to0}\frac{\Delta\varphi}{\Delta x}=\lim\limits_{\Delta x\to0}\frac{\Delta u}{\Delta x}+\lim\limits_{\Delta x\to0}\frac{\Delta v}{\Delta x}=u'(x) + v'(x)\\)
   2. 令 \\(\varphi(x)=u(x)v(x)\\)
      <div>
      $$
      \begin{aligned}
       \Delta\varphi & =\varphi(x+\Delta x)-\varphi(x) \\
       & =u(x+\Delta x)v(x+\Delta x)-u(x)v(x) \\
       & =u(x+\Delta x)v(x+\Delta x)-u(x)v(x+\Delta x)+u(x)v(x+\Delta x)-u(x)v(x) \\
       & =\Delta uv(x+\Delta x)+u(x)\Delta v
      \end{aligned}
      $$
      </div>
      进而
      
      \\(\lim\limits_{\Delta x\to 0}\frac{\Delta\varphi}{\Delta x}=\lim\limits_{\Delta x\to 0}\frac{\Delta u}{\Delta x}\cdot\lim\limits_{\Delta x\to 0}v(x+\Delta x)+u(x)\lim\limits_{\Delta x\to0}\frac{\Delta v}{\Delta x}=u'(x)v(x)+u(x)v'(x)\\)
      提示: \\(\lim\limits_{\Delta x\to0}v(x+\Delta x)=v(x)\\)
   3. 令 \\(\varphi(x)=\dfrac{u(x)}{v(x)}\enspace\\) (\\(v(x)\neq 0\\))
      <div>
      $$
      \begin{aligned}
       \Delta\varphi=\varphi(x+\Delta x)-\varphi(x) & =\frac{u(x+\Delta x)}{v(x+\Delta x)}-\frac{u(x)}{v(x)} \\
       & =\frac{u(x+\Delta x)v(x)-v(x+\Delta x)u(x)}{v(x+\Delta x)v(x)} \\
       & =\frac{[u(x+\Delta x)v(x)-u(x)v(x)]-[u(x)v(x+\Delta x)-u(x)v(x)]}{v(x+\Delta x)v(x)} \\
       & =\frac{\Delta uv(x)-u(x)\Delta v}{v(x+\Delta x)v(x)}
      \end{aligned}
      $$
      </div>
      进而

      \\(\lim\limits_{\Delta x\to 0}\frac{\Delta\varphi}{\Delta x}=\frac{\lim\limits_{\Delta x\to 0}\frac{\Delta u}{\Delta x}\cdot v(x)-u(x)\cdot\lim\limits_{\Delta x\to0}\frac{\Delta v}{\Delta x}}{v(x)\lim\limits_{\Delta x\to0}v(x+\Delta x)}=\frac{u'(x)v(x)-u(x)v'(x)}{v^2(x)}\\)
      提示: \\(\lim\limits_{\Delta x\to 0}v(x+\Delta x)=v(x)\\)
3. 反函数求导法则
   设 \\(y=f(x)\\) 可导且 \\(f(x)^\prime\neq 0\\) (导数不为零意味着严格单调),
   则反函数 \\(x=\varphi(y)\\) 可导且 \\(\varphi^\prime(y)=\frac{1}{f^\prime(x)}\\)
   证明:
   \\(\varphi^\prime(y)=\lim\limits_{\Delta y\to 0}\frac{\Delta x}{\Delta y}=\lim\limits_{\Delta y\to 0}\frac{1}{\frac{\Delta y}{\Delta x}}=\underbrace{\lim\limits_{\Delta x\to 0}}\_{(1)}\frac{1}{\frac{\Delta y}{\Delta x}}=\frac{1}{f^\prime(x)}\\)
   (1) \\(\lim\limits_{\Delta x\to0}\frac{\Delta y}{\Delta x}\neq 0 \rArr \Delta y=\bigcirc(\Delta x)\\) 同阶无穷小
4. 复合函数求导法则
   (如何判断复合函数: 观察有几个初等函数)
   1. 复合函数求导法则:
      设 \\(y=f(u)\\) 可导, \\(u=\varphi(x)\\) 可导且 \\(\varphi^\prime(x)\neq 0\\) , 则 \\(y=f(\varphi(x))\\) 可导
      有 \\(f^\prime(\varphi(x))=f^\prime[\varphi(x)]\varphi^\prime(x)\\)
   3. 证明:
      1. 用极限:
         <div>
         $$
         f^\prime(\varphi(x))=\lim\limits_{\Delta x\to 0}\frac{\Delta y}{\Delta x}
         =\lim\limits_{\Delta x\to 0}(\frac{\Delta y}{\Delta u}\cdot\frac{\Delta u}{\Delta x})
         =\lim\limits_{\Delta x\to 0}\frac{\Delta y}{\Delta u}\cdot\lim\limits_{\Delta x\to 0}\frac{\Delta u}{\Delta x}
         =\underbrace{\lim\limits_{\Delta u\to 0}}_{(1)}\frac{\Delta y}{\Delta u}\cdot\lim\limits_{\Delta x\to 0}\frac{\Delta u}{\Delta x}
         =f^\prime(u)\cdot\varphi^\prime(x)
         $$
         </div>
         
         (1) \\(\varphi'(x)=\lim\limits_{\Delta x\to 0}\frac{\Delta u}{\Delta x}\neq 0\rArr\Delta u=\bigcirc(\Delta x)\\) 同阶无穷小
      2. 用微分: \\(f^\prime(\varphi(x))=\frac{\\mathrm{d}y}{\mathrm{d}x}=\frac{\mathrm{d}y}{\mathrm{d}u}\cdot\frac{\mathrm{d}u}{dx}=f^\prime(u)\cdot\varphi^\prime(x)=f^\prime[\varphi(x)]\varphi^\prime(x)\\)

### 高阶导数

二阶及以上的导数称为高阶导数.

1. 二阶导数: 对导数再求导一次就是二阶导数
   \\(f^{\prime\prime}(x)=[f^\prime(x)]^\prime=\frac{\mathrm{d}(\frac{\mathrm{d}y}{\mathrm{d}x})}{\mathrm{d}x}=\frac{\mathrm{d}^2y}{\mathrm{d}x^2}\\)
   同理三阶导数 \\(\frac{\mathrm{d}^3y}{\mathrm{d}x^3}\\) , \\(n\\) 阶导数 \\(f^{(n)}=\frac{\mathrm{d}^ny}{\mathrm{d}x^n}\\)
2. 高阶导数求导方法:
   1. [归纳法](#induction_method)
   2. 公式法:
      \\((uv)^\prime=u^\prime v+uv^\prime\rArr(uv)^{\prime\prime}=(u^\prime v)^\prime+(uv^\prime)^\prime=u^{\prime\prime}v+2u^\prime v^\prime+uv^{\prime\prime}\\)
      莱布尼茨公式(请记住)
      \\((uv)^{(n)}=C_n^0 u^{(n)}v+C_n^1 u^{(n-1)}v^\prime+C_n^2 u^{(n-2)}v^{\prime\prime}+\dots+C_n^n uv^{(n)}\\)

### 隐函数及由参数方程确定的函数求导

1. 隐函数求导
   * 显函数: \\(y=f(x)\\)
   * 隐函数: \\(F(x,y)=0\enspace\underrightarrow{\text{显式化}}\enspace y=f(x)\\)
   * 方法:
     有 \\(F(x,y)=0\\) , 确定 \\(y\\) 为 \\(x\\) 的函数.
     两边对 \\(x\\) 求导. 求导时 \\(y^\prime=f^\prime(x)=\frac{\mathrm{d}y}{\mathrm{d}x}\\) , 最终将一边化为 \\(\frac{\mathrm{d}y}{\mathrm{d}x}\\)
   * 例: \\(e^{x+y}=x^2+y+1\\) 确定 \\(y\\) 为 \\(x\\) 的函数, 求 \\(\frac{\mathrm{d}y}{\mathrm{d}x}\\)
     解: 两边对 \\(x\\) 求导得
     <div>
     $$
     \begin{aligned}
      & e^{x+y}(1+\frac{\mathrm{d}y}{\mathrm{d}x})=2x+\frac{\mathrm{d}y}{\mathrm{d}x} \\
      \hArr & (e^{x+y}-1)\frac{\mathrm{d}y}{\mathrm{d}x}=2x-e^{x+y} \\
      \hArr & \frac{\mathrm{d}y}{\mathrm{d}x}=\frac{2x-e^{x+y}}{e^{x+y}-1}
     \end{aligned}
     $$
     </div>
2. 参数方程确定的函数求导
   设 \\(\begin{cases} x=\varphi(t) \\\ y=\psi(t) \end{cases}\\) , 其中 \\(\varphi(t) , \psi(t)\\) 可导, 则 \\(\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\psi^\prime(t)}{\varphi^\prime(t)}\enspace\\) (\\(\varphi(t)\neq 0\\))
   证明: \\(\frac{\psi^\prime(t)}{\varphi^\prime(t)}=\frac{\frac{\mathrm{d}y}{\mathrm{d}t}}{\frac{\mathrm{d}x}{\mathrm{d}t}}=\frac{\mathrm{d}y}{\mathrm{d}x}\\)

### 微分

1. 微分定义
   1. 什么是微分
      设 \\(y=f(x)\enspace\\) (\\(x\in D\\)) , \\(\Delta y=f(x_0+\Delta x)-f(x_0)\enspace\\) (\\(x_0,(x_0+\Delta x)\in D\\))
      若 \\(\Delta y\\) 和 \\(\Delta x\\) 能化为线性形式: \\(\Delta y=A\Delta x+\circ(\Delta x)\\)
      则该函数在点 \\(x=x_0\\) 可微, 记作 \\(\mathrm{d}y|_{x=x_0}=A\Delta x=A\mathrm{d}x\\)
   2. 结合导数定义 \\(f^\prime(x)=\frac{\mathrm{d}y}{\mathrm{d}x}\\) 可得:
      * \\(\mathrm{d}y=f^\prime(x)\mathrm{d}x\approx \lim\limits_{\Delta x\to 0}\Delta y\\)
      * \\(\mathrm{d}x=\lim\limits_{\Delta x\to 0}\Delta x\\)
      
      可以发现: 可导 \\(\hArr\\) 可微
      (一般情况下都是先有导数后求微分, 微分的主要应用是在知道导数的情况下求 \\(\Delta y\\) 的近似值 \\(\mathrm{d}y\\))
2. 近似计算:
   若要求 \\(f(x)\\) 的值, 可以找离 \\(x\\) 较近的点 \\(x_0\\) , 它们的距离是 \\(\Delta x\\), 且 \\(f(x_0)\\) 的值已知
   则 \\(f(x)=f(x_0+\Delta x)=f(x_0)+\Delta y\approx f(x_0)+f^\prime(x_0)\Delta x\\)
   * 求近似值还可利用 0 的特殊性, 即 \\(x\to 0\\) 时, \\(f(x)=f(0+x)\approx f(0)+f^\prime(0)x\\)
     1. \\(\sqrt[n]{1+x}\approx 1+\frac{x}{n}\\)
     2. \\(e^x\approx 1+x\\)
     3. \\(\ln(1+x)\approx x\\)
3. 微分公式
   1. \\(\mathrm{d}\(c\)=c'\mathrm{d}x=0\\)
   2. \\(\mathrm{d}(x^a)=ax^{a-1}\mathrm{d}x\\)
   3. \\(\mathrm{d}(a^x)=a^x\ln a\mathrm{d}x\\)
   4. \\(\mathrm{d}(\log_a x)=\frac{1}{x\ln a}\mathrm{d}x\\)
   5. \\(\mathrm{d}(\sin x)=\cos x\mathrm{d}x\\)
      \\(\mathrm{d}(\cos x)=-\sin x\mathrm{d}x\\)
      \\(\mathrm{d}(\tan x)=\sec^2 x\mathrm{d}x\\)
      \\(\mathrm{d}(\cot x)=-csc^2 x\mathrm{d}x\\)
      \\(\mathrm{d}(\sec x)=\sec x\tan x\mathrm{d}x\\)
      \\(\mathrm{d}(\csc x)=-\csc x\cot x\mathrm{d}x\\)
   6. \\(\mathrm{d}(\arcsin x)=\frac{1}{\sqrt{1-x^2}}\mathrm{d}x\\)
      \\(\mathrm{d}(\arccos x)=-\frac{1}{\sqrt{1-x^2}}\mathrm{d}x\\)
      \\(\mathrm{d}(\arctan x)=\frac{1}{1+x^2}\mathrm{d}x\\)
      \\(\mathrm{d}(\text{arccot } x)=-\frac{1}{1+x^2}\mathrm{d}x\\)
4. 微分四则运算
   设函数 \\(u\\)、\\(v\\)
   1. 加减: \\(\mathrm{d}(u\pm v)=\mathrm{d}u\pm\mathrm{d}v\\)
   2. 乘: \\(\mathrm{d}(uv)=\mathrm{d}u\cdot v+u\cdot\mathrm{d}v\\)
   3. 除: \\(\mathrm{d}(\frac{u}{v})=\frac{\mathrm{d}u\cdot v-u\cdot \mathrm{d}v}{v^2}\\)
5. 复合函数求微分
   设 \\(y=f(u)\\) , \\(u=\varphi(x)\\)
   则 \\(\mathrm{d}y=f^\prime[\varphi(x)]\varphi^\prime(x)\mathrm{d}x=f^\prime[\varphi(x)]\mathrm{d}\varphi(x)=f^\prime(u)\mathrm{d}u\\)
