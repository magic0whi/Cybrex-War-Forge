---
title: function-and-limit
category: postgraduate-mathematical-analysis
lang: zh-cn
date: 2020-05-22 16:54:13
tags:
toc: true
---

## 前置知识
全称量词:
\\(\forall\\) ------ 任意的, 所有的
\\(\exist\\) ------ 存在
\\(\exist 1\\) ---- 存在且唯一

函数:
\\(\text{max}\\{N_1, N_2\\}\\) ---- 返回两者中较大者

## 函数

1. **函数**:
有 集合D 和 x, y 两个变量. 若对任意 \\(x \in D\\) ,
总存在唯一确定的解 y 与 x 对应.
称 y 为 x 的函数,
记 \\(y=f(x)\\) , D 为 x 的定义域

2. **反函数**:
\\(y=f(x) \quad(x\in D)\\) 严格单调 **(单调函数是反函数的充分条件)**
若 \\(y=f(x) \implies x=\varphi(y)\\)
则 \\(\varphi(y)\\) 就是 \\(f(x)\\) 的反函数

1. **基本初等函数**:
<div>
$$
\begin{aligned}
    &1. x^\alpha \\
    &2. a^x \mskip{5.6em}(a>0且a\ne 1) \\
    &3. \log_a{x} \mskip{4em}(a>0且a\ne 1) \\
    &4. \sin x, \cos x, \tan x, \cot x, \sec x, \csc x
\end{aligned}
$$
</div>

4. **初等函数**: 由 常数\基本初等函数, 经过 四则运算\复合运算 而成的式子

### 初等性质

1. 奇偶性
   有 \\(y=f(x) \quad(x\in D,  D 关于原点对称)\\)
   若对于 \\(\forall x \in D\\),
   \\(\begin{aligned}&f(-x)=&-f(x) \enspace, &则为奇函数; \\\ &f(-x)=&f(x) \enspace, &则为偶函数\end{aligned}\\)
2. 单调性(TODO: 补充图片)
   有 \\(y=f(x) \quad(x\in D)\\)
   1. 若 \\(\exist x_1, x_2 \in D\\) 且 \\(x_1 < x_2\\) 时 , 有 \\(f(x_1)<f(x_2)\\)
      称 \\(f(x)\\) 在 D 上严格单调递增.
   2. 若 \\(\exist x_1, x_2 \in D\\) 且 \\(x_1<x_2>\\) 时 , 有 \\(f(x_1)>f(x_2)\\)
      称 \\(f(x)\\) 在 D 上严格单独递减
3. 有界性(TODO: 补充图片)
   有 \\(y=f(x) \quad(x\in D)\\), 函数之界 M (即值域的范围)
   若 \\(\exist M>0\\) , 对于 \\(\forall x\in D\\) , 有 \\(|f(x)|\leqslant M\\) , 称 \\(f(x)\\) 在 \\(D\\) 上有界
4. 周期性
   有 \\(y=f(x) \quad(x\in D)\\) ,
   若 \\(\exist T>0\\) , 使 \\(\forall x\in D \quad(x+T\in D)\\)
   有 \\(f(x+T)=f(x)\\) , 称 f(x) 为周期函数

## 数列极限

1. 数列收敛定义(ε−N):
   **(建议先看例子)**
   设 \\({a_n}\\) 为数列, A为极限值, 最大误差\\(\varepsilon\\), \\(a_N\\)后极限有效(即之后的数列元素与极限值的误差进入容许范围),
   若 \\(\forall\varepsilon > 0 , \exist N > 0\\) ,
   且当 \\(n > N\\) 时. \\(|a_n - A| < \varepsilon\\)

   由此发现数列收敛于极限A, 用 \\(\lim\limits_{n\to\infty} = A\\) 或 \\(a_n \to A \quad(n\to\infty)\\) 表示

   举个例子:
   如有通项公式 \\(a_n=\dfrac{n+1}{2n}\\), 具体值为 \\(\dfrac{3}{4}, \dfrac{2}{3}, \dfrac{5}{8}, \dfrac{3}{5}, \text{...}\\) , 观察得极限 \\(a_n\to\dfrac{1}{2}\\)

   设最大容许误差 \\(\varepsilon = \dfrac{1}{10} > 0\\), 则误差值 \\(|a_n - \dfrac{1}{2}| = \dfrac{1}{2n} < \dfrac{1}{10} \Harr n > 5\\).
   同理:
   \\(\varepsilon= \frac{1}{100} > 0\\), 则 \\(\frac{1}{2n} < \frac{1}{100} \Harr n > 50\\)
   \\(\varepsilon= \frac{1}{1000} > 0\\), 则 \\(\frac{1}{2n} < \frac{1}{1000} \Harr n > 500\\)
   
   由此发现该数列有极限: \\(n\to\infty , a_n\to\dfrac{1}{2}\\)
2. 性质
   1. 唯一性: 数列有极限必唯一(极限值只有一个)
      证(反证法):
      设数列有两个极限 \\(\lim\limits_{n\to\infty}a_n=A ,\enspace \lim\limits_{n\to\infty}a_n = B \\) , 且 \\(A\neq B\\)
      不妨设 \\(A>B\\) , \\(\varepsilon=-\dfrac{A+B}{2}\\) (误差值的定义由 \\(\varepsilon + A=-\varepsilon - B\\) 解出, 目的是让下面两个\\(a_n\\)的值域没有交集)
      \\(\because\lim\limits_{n\to\infty}a_n=A,\enspace \therefore \exist N_1 > 0\\) , 当 \\(n>N_1\\) 时, \\(|a_n-A|<\varepsilon \quad\Harr\quad \frac{3A+B}{2}<a_n<\frac{A-B}{2}\\) (\*)
      \\(\because\lim\limits_{n\to\infty}a_n=B,\enspace \therefore \exist N_2 > 0\\) , 当 \\(n>N_2\\) 时, \\(|a_n-B|<\varepsilon \quad\Harr\quad \frac{A-B}{2}<a_n<\frac{-A+B}{2}\\) (\*\*)
      取 \\(N=\text{max}\\{N_1 , N_2\\}\\) , 当 \\(n < N_2\\) 时, (\*) (\*\*) 都成立, 但这两个不等式没有交集, 矛盾, 所以 \\(A>B\\) 不对, 同理 \\(B>A\\) 也不对.
      \\(\therefore A=B\\), 极限值只有一个.
   2. 有界性:
      若 \\(\lim\limits_{n\to\infty}a_n = A\\) , 则 \\(\exist M > 0\\) , 使得 \\(|a_n| \leqslant M\\) , **反之不成立**.
      证明: 
      <div>
      $$
      \begin{aligned}
         & "\rArr" \enspace 取 \varepsilon = 1 > 0 \\
         &\because \lim\limits_{n\to\infty}a_n=A \\
         &\therefore \exist N > 0,\enspace 当 n > N 时 , |a_n - A | < 1 \\
         &\because ||a_n|-|A|| \leqslant |a_n-A| \\
         &\therefore 当 n > N 时,\enspace ||a_n| - |A_1|| < 1 \rArr |a_n| < 1 + |A| 在 n>N 时成立 \\
         &取 \text{M} = \text{max}\{|a_1| ,\enspace |a_2| ,\enspace \text{...} ,\enspace |a_n| ,\enspace 1+|A|\} \\
         &\forall n ,\enspace 有 |a_n| \leqslant M \\
         &"\nLeftarrow" \enspace a_n = 1+ (-1)^n \enspace |a_n| \leqslant 2 ,\enspace 但 \lim\limits_{n\to\infty}a_n 不存在
      \end{aligned}
      $$
      </div>

   3. 保号性:
      若 \\(\lim\limits_{n\to\infty}a_n = A \begin{cases} >0 \\\ <0 \end{cases}\\) , 则 \\(\exist N > 0\\) , 当 \\(n > N\\) 时 , \\(a_n\begin{cases} >0 \\\ <0  \end{cases}\\)
      **极限正, 分界线往后就正; 极限负, 分界线往后就负**
      证明:
      <div>
      $$
      \begin{aligned}
         &设 A > 0 ,\enspace 取 \varepsilon = \frac{A}{2} > 0 \\
         &\because \lim\limits_{n\to\infty}a_n=A ,\enspace \therefore \exist N > 0 ,\enspace 当 n>N 时 ,\enspace |a_n - A| < \frac{A}{2} \rArr \frac{A}{2} < a_n < \frac{3A}{2} \quad\rArr\quad a_n > \frac{A}{2} > 0 \\
         &设 A < 0 , 取 \varepsilon = -\frac{A}{2} > 0 \\
         &\because \lim\limits{n\to\infty}a_n=A ,\enspace \therefore \exist N > 0 ,\enspace 当 n>N 时 ,\enspace |a_n - A| < -\frac{A}{2} \hArr \frac{3A}{2} < a_n < \frac{A}{2} \quad\rArr\quad a_n < \frac{A}{2} < 0
      \end{aligned}
      $$
      </div>

## 函数极限

1. 定义
   TODO: 补充图片
   如: \\(y = x^2 + 1\\) , 它的极限为: \\(x^2 + 1 \to 2 \qquad(x\to 1)\\)
   又如: \\(y=\frac{x^2 - 1}{x - 1}\\) , 它的极限为: \\(\frac{x^2 - 1}{x - 1} \qquad(x\to 1)\\)
   
   ε-δ语言定义法:
   (ε为值域的误差, δ为定义域的误差)
   TODO: 补充图片
   若 \\(\forall\varepsilon > 0 ,\enspace \exist\delta >0\\) , 当 \\(0 < |x - a| < \delta\\) 时
   \\(|f(x) - A| < \varepsilon\\) , 称 f(x) 当 \\(x\to 0\\) 时以A为极限
   记作 \\(\lim\limits_{x\to a}f(x) = A\\) 或 \\(f(x)\to A \qquad(x\to a)\\)

   ε-X语言定义法:
   (X为值域临界点)
   若 \\(\forall\varepsilon > 0 , \exist X > 0 ,\enspace |f(x)-A|<\varepsilon\\)
   情况1. 当 \\(x>X\\) 时, \\(\lim\limits_{x\to \infty}f(x)=A\\)
   情况2. 当 \\(x<-X\\) 时, \\(\lim\limits_{x\to -\infty}f(x)=A\\)
   情况3. 当 \\(|x|>X\\) 时, \\(\lim\limits_{x\to \infty}f(x)=A\\)
2. 性质
   1. 唯一性(函数有极限必唯一)
      证明: 设 \\(\lim\limits_{x\to a}f(x)=A \enspace,\enspace \lim\limits_{x\to a}f(x)=B\\)
      不妨设 A > B , 取 \\(\varepsilon=\frac{A-B}{2}>0\\) (凑出矛盾的结果)
      \\(\because \lim\limits_{x\to a}f(x)=A\\)
      \\(\therefore \exist\delta_1>0\\) , 当 \\(0<|x-a|<\delta_1\\) 时,
      \\(\mskip{1em}|f(x)-A|<\frac{A-B}{2} \hArr \frac{A+B}{2}<f(x)<\frac{3A-B}{2}\\) (\*)
      又 \\(\because \lim\limits_{x\to a}f(x)=B\\)
      \\(\therefore \exist\delta_2>0\\) , 当 \\(0<|x-a|<\delta_2\\) 时.
      \\(\mskip{1em}|f(x)-B|<\frac{A-B}{2} \hArr \frac{3B-A}{2}<f(x)<\frac{A+B}{2}\\) (\*\*)
      取 \\(\delta=\text{min}\\{\delta_1 , \delta_2\\}\\) , 当 \\(0<|x-a|<\delta\\) 时 (**)(*) 皆成立, 矛盾.
      \\(\therefore A>B\\) 不对, 同理 \\(A<B\\) 也不对.
      \\(\therefore A=B\\), 极限值只有一个.
   2. 局部有界性: 设 \\(\lim\limits_{x\to a}f(x)=A\\) , 则 \\(\exist\delta>0 ,\enspace M>0\\) , 当 \\(0<|x-a|<\delta\\) 时, \\(|f(x)|\leqslant M\\)
      证明: 证明目标是找出 \\(|f(x)|\leqslant\\) 某个确切的值
      取 \\(\varepsilon=1>0\\)
      \\(\because \lim\limits_{x\to a}f(x)=A\\)
      \\(\therefore \exist\delta>0\\) , 当 \\(0<|x-a|<\delta\\) 时. \\(\mskip{1em} |f(x)-A|<1\\)
      又 \\(\because ||f(x)|-|A||\leqslant|f(x)-A|\\) (不等式公式)
      \\(\therefore 当 0<|x-a|<\delta 时 \enspace,\enspace ||f(x)|-|A||<1 \rArr |f(x)|<1+|A|=M\\)
      即, \\(当 0<\|x-a|<\delta 时 \enspace,\enspace |f(x)|\leqslant M\\)
   3. (废话)保号性: 设 \\(\lim\limits_{x\to a}f(x)=A \begin{cases} >0 \\\ <0 \end{cases}\\) , 则 \\(\exist\delta>0\\) , 当 \\(0<|x-a|<\delta\\) 时, \\(f(x) \begin{cases} >0 \\\ <0 \end{cases}\\)
      证明:
      1. 若 A>0 , 取 \\(\varepsilon=\frac{A}{2}>0\\)
         \\(\because \lim\limits_{x\to a}f(x)=A\\)
         \\(\therefore \exist\delta>0\\)
         当 \\(0<|x-a|<\delta\\) 时, \\(|f(x)-A|<\frac{A}{2} \rArr f(x)>\frac{A}{2}>0\\)
      2. 若 A<0 , 取 \\(\varepsilon=-\frac{A}{2}>0\\)
         \\(\because \lim\limits_{x\to a}f(x)=A\\)
         \\(\therefore \exist\delta>0\\)
         当 \\(0<|x-a|<\delta\\) 时, \\(|f(x)-A|<-\frac{A}{2} \rArr f(x)>\frac{A}{2}>0\\)

Notes:
1. \\(\\{x|0<|x-a|<\delta\\}\\) 可用 \\(\mathring{\text{U}}(a\cdot \delta)\\) 表示, 读作 a的取心δ邻域.
   TODO: 补充图片
2. \\(x\to a\\) 时 \\(\begin{cases} x\to a^- \\\ x\to a^+ \end{cases}\\)
3. 左极限与右极限
   若 \\(\forall\varepsilon>0 ,\enspace \exist\delta > 0\\) ,
   1. 当 \\(x\in (a-\delta, a)\\) 时 \\(|f(x)-A| < \varepsilon\\) ,
      此时A称为 f(x) 在 x=a 处左极限,
      记 \\(\lim\limits_{x\to a^-}f(x)=A\\) 或 \\(f(a-0)=A\\)
   2. 当 \\(x\in (a , a+\delta)\\) 时 \\(|f(x-B)| < \varepsilon\\) ,
      此时B称为 f(x) 在 x=a出右极限,
      记 \\(\lim\limits_{x\to a^+}f(x)=B\\) 或 \\(f(a+0)=B\\)
4. \\(\lim\limits_{x\to a}f(x)\\) 左右极限存在且相等
5. \\(\lim\limits_{x\to a}f(x)\\) 与 \\(f(a)\\) 无关
   1. 如 \\(f(x)=\begin{cases} x-1 \qquad &x<0 \\\ 0 \qquad &x=0 \\\ 2x-1 \qquad &x>0 \end{cases}\\), 它的极限为 \\(\begin{cases} \lim\limits_{x\to 0^+}f(x)=-1 \\\ \lim\limits_{x\to 0^-}f(x)=-1 \end{cases} \rArr \lim\limits_{x\to 0}f(x)=-1\\) , 但真正x取到f(a)处却为0, 所以极限与f(a)无关.
   2. 如 \\(\lim\limits_{x\to 2}\frac{x^2-4}{x-2}=\lim\limits_{x\to 2}(x+2)=4\\), 这里f(2)时分母为零, 也就是f(a)压根就不存在了

## 无穷小与无穷大

### 无穷小

1. 定义: 若 \\(\lim\limits_{x\to x_0}\alpha(x)=0\\) , 称 \\(\alpha(x)\\) 在 \\(x\to x_0\\) 时无穷小
   ε-δ语言定义: 若 \\(\forall\varepsilon>0 \enspace,\enspace \exist\delta>0\\) , 当 \\(0<|x-x_0|<\delta\\) 时 , \\(|\alpha(x)-0|<\varepsilon\\) , 即 \\(\lim\limits_{x\to x_0}\alpha(x)=0\\)
2. 常规性质:
   1. 若 \\(\alpha\to0 , \beta\to0\\) , 则 \\(\begin{cases} \alpha\pm\beta\to0 \\\ k\alpha\to0 \quad (k为任意常数) \\\ \alpha\beta\to0 \end{cases}\\)
   2. 无穷小乘以有界函数还是无穷小: \\(\alpha\to0\\) , \\(|\beta|\leqslant M\\) , 则 \\(\alpha\beta\to0\\)
   3. (重要) \\(\lim\limits_{x\to x_0}f(x)=A \hArr \lim\limits_{x\to x_0}f(x)=A+\alpha \quad (\alpha\to 0)\\)

Notes:
1. 0是无穷小的充分但不必要条件x_0

### 无穷大

1. 定义:
   ε-δ语言定义: 若 \\(\forall M>0 \enspace,\enspace \exist\delta>0\\) , 当 \\(0<|x-x_0|<\delta\\) 时, \\(|f(x)|\geqslant M \thickspace \rArr\\) 称 f(x) 在 \\(x\to x_0\\) 时无穷大, 记 \\(\lim\limits_{x\to x_0}f(x)=\infty\\)
   ε-X语言定义: 若 \\(\forall M>0 \enspace,\enspace \exist X>0\\) , 当 \\(x>X\\) 时, \\(|f(x)|\geqslant M \rArr\\) 称 f(x) 在 \\(x\to +\infty\\) 时无穷大, 记 \\(\lim\limits_{x\to +\infty}f(x)=\infty\\)

### 无穷小与无穷大的关系

性质: \\(\lim\limits_{x\to x_0}f(x)=0 \hArr \lim\limits_{x\to x_0}\frac{1}{f(x)}=\infty\\)

## 极限的运算法则

### 四则求导法则

有 \\(\lim\limits_{x\to x_0}f(x)=A \enspace,\enspace \lim\limits_{x\to x_0}g(x)=B\\)

1. 加减: \\(\lim\limits_{x\to x_0}[f(x)\pm g(x)]=\lim\limits_f(x)\pm \lim\limits_{x\to x_0}g(x)=A\pm B\\)
2. 乘(常数): \\(\lim\limits_{x\to x_0}kf(x)=k\lim\limits_{x\to x_0}f(x)=kA\\)
3. 乘(另一极限): \\(\lim\limits_{x\to x_0}[f(x)g(x)]=\lim\limits_{x\to x_0}f(x)+\lim\limits_{x\to x_0}g(x)=AB\\)
4. 除: \\(\lim\limits_{x\to x_0}\frac{f(x)}{g(x)}=\frac{\lim\limits_{x\to x_0}f(x)}{\lim\limits_{x\to x_0}g(x)}=\frac{A}{B}\\)

Notes:
\\(P(x)=a_nx^n + \text{...} + a_1x + a_0\\)
\\(Q(x)=b_mx^m + \text{...} + b_1x + b_0\\)
\\(\lim\limits_{x\to \infty}\frac{P(x)}{Q(x)}=\begin{cases} \frac{a_n}{b_m} , &n=m \\\ \infty , &n>m \\\ 0 , &n<m \end{cases}\\)

### 复合函数极限法则

有 \\(u=\varphi(x) \enspace,\enspace \varphi(x)\neq a\\)
若 \\(\lim\limits_{u\to a}f(u)=A \enspace,\enspace \lim\limits_{x\to x_0}\varphi(x)=a \enspace,\enspace 则 \lim\limits_{x\to x_0}f[g(x)]=A\\)

## 极限存在法则 两个重要极限

### 极限存在准则

1. 夹逼定理
   1. 数列型:
      有 \\(\begin{cases} a_n \leqslant b_n \leqslant c_n \\\ \lim\limits_{n\to\infty}a_n=\lim\limits_{n\to\infty}c_n=A \end{cases}\\)
      则 \\(\lim\limits_{n\to\infty}b_n=A\\)
      (证明方法: 利用ε−N语言推出 \\(A-\varepsilon<b_n<A+\varepsilon \rArr |b_n-A|<\varepsilon\\))
   2. 函数型:
      有 \\(\begin{cases} f(x)\leqslant g(x)\leqslant h(x) \\\ \lim f(x)=\lim h(x)=A \end{cases}\\)
      则 \\(\lim g(x)=A\\)
2. 单调有界数列必有极限
   Notes:
   * \\(\\{a_n\\}\\) 有界 \\(\hArr \\{a_n\\}\\) 有上下界
   * 若 \\(\\{a_n\\}\\) 单调递增: \\(\begin{cases} 有上界 \rArr \lim\limits_{n\to\infty}a_n 存在 \\\ 无上界 \rArr \lim\limits_{n\to\infty}a_n 不存在\end{cases}\\)
   * 若 \\(\\{a_n\\}\\) 单调递减: \\(\begin{cases} 有下界 \rArr \lim\limits_{n\to\infty}a_n 存在 \\\ 无下界 \rArr \lim\limits_{n\to\infty}a_n 不存在\end{cases}\\)

### 两个重要极限

1. \\(\lim\limits_{x\to0}\frac{\sin x}{x}=1\\)
   证明:
   {% asset_img 1.png [title] %}
   
   设 \\(0<x<\frac{\pi}{2}\\)
   \\(S_{\triangle AOB}=\frac{1}{2}\sin x\\)
   \\(S_{扇形AOB}=\frac{1}{2}x\\)
   \\(S_{RT\triangle AOC}=\frac{1}{2}\tan x\\)
   \\(\therefore \sin x<x<\tan x \rArr 1<\frac{x}{\sin x}<\frac{1}{\cos x}\\)
   \\(\because \lim\limits_{x\to0}cos x=1\\)
   \\(\therefore \lim\limits_{x\to0}\frac{1}{\cos x}=1 , \lim\limits_{x\to0}1=1 \rArr \lim\limits_{x\to0}\frac{x}{\sin x}=1\\) (夹逼定理) \\(\rArr \lim\limits_{x\to0}\frac{\sin x}{x}=1\\)
2. \\(\lim\limits_{n\to\infty}(1+\frac{1}{n})^n=e\\)

## 无穷小的比较(相除)

### 无穷小的比较

有 \\(\alpha\to0 , \beta\to0\\)
1. \\(\lim\frac{\beta}{\alpha}=0\\) , 称 \\(\beta\\) 为 \\(\alpha\\) 的高阶无穷小, 记 \\(\beta=\circ(\alpha)\\)
   \\(\lim\frac{\beta}{\alpha}=\infty\\) , 称 \\(beta\\) 为 \\(\alpha\\) 的低阶无穷小
   \\(\lim\frac{\beta}{\alpha^k}=k \quad (k\neq0,\infty)\\) , 称 \\(\beta\\) 为 \\(\alpha\\) 的 k 阶无穷小
   \\(\lim\frac{\beta}{\alpha}=k \quad (k\neq0,\infty)\\) , 称 \\(\beta\\) 为 \\(\alpha\\) 的同阶无穷小, 记 \\(\beta=\bigcirc(\alpha)\\)
   \\(\lim\frac{\beta}{\alpha}=1\\) , 称 \\(\beta\\) 为 \\(\alpha\\) 的等价无穷小, 记 \\(\beta\sim\alpha\\)
   等价无穷小是同阶无穷小的充分不必要条件

### 等价无穷小的性质及常用等价无穷小

1. 等价无穷小的性质
   有 \\(\alpha\to0\\) , \\(\beta\to0\\)
   1. \\(\alpha\sim\beta \hArr \beta=\alpha+\circ(\alpha)\\)
   2. 若 \\(\begin{cases} \alpha\sim\alpha_1 , \beta\sim\beta_1 \\\ \lim\frac{\beta_1}{\alpha_1}=A \end{cases}\\)
      则 \\(\lim\frac{\beta}{\alpha}=A\\)
2. 常用等价无穷小
   (\\(x\to0\\))
   1. \\(x\sim\sin x \enspace,\enspace x\sim\tan x \enspace,\enspace x\sim\arcsin x \enspace,\enspace x\sim\arctan x \enspace,\enspace x\sim\ln(1+x) \enspace,\enspace x \enspace\sim\enspace e^x-1\\)
   2. \\(1-\cos x \enspace\sim\enspace \frac{x^2}{2}\\)
   3. \\((1+x)^a-1 \enspace\sim\enspace ax\\)

## 函数的连续性与间断点

连续是极限存在的充分不必要条件, 因为间断不代表极限不存在

### 连续

1. 函数在一点连续: 
   若 \\(\lim\limits_{x\to a}f(x)=f(a)\\) 或 \\(f(a-0)=f(a+0)=f(a)\\)
2. f(x) 在闭区间上连续:
   设 f(x) 在 [a, b] 上有定义, 若:
   1. f(x) 在 (a, b) 内处处连续
   2. f(a)=f(a+0), f(b)=f(b-0)
   则称 f(x) 在 [a, b] 上连续, 记 \\(f(x)\in c[a,b]\\)

Note:
若 f(a-0)=f(a) , 称f(a)在x=a左连续
若 f(a+0)=f(a) , 称f(a)在x=a右连续

### 间断点及分类

1. 间断: 若 \\(\lim\limits_{x\to a}f(x)\neq f(a)\\) , 称 f(x) 在 x=a 间断
2. 分类:
   1. 第一类间断点: f(a-0) , f(a+0) 皆存在
      * 可去间断点: f(a-0)=f(a+0)
      * 跳跃间断点: f(a-0)≠f(a+0)
   2. 第二类间断点: f(a-0) , f(a+0) 至少一个不存在

Note:
\\(\lim\limits_{x\to0^-}e^\frac{1}{x}=0\\) , \\(\lim\limits_{x\to0^+}e^\frac{1}{x}=+\infty\\)

## 连续函数运算及初等函数连续性

### 连续函数运算

1. 四则运算
   设f(x) , g(x) 在 \\(x=x_0\\) 处连续, 则
   1. \\(f(x)\pm g(x)\\) 在 \\(x=x_0\\) 处连续
   2. \\(f(x)g(x)\\) 在 \\(x=x_0\\) 处连续
   3. \\(\frac{f(x)}{g(x)}\\) 在 \\(x=x_0\\) 处连续 (\\(g(x)\neq0\\))
   (证明思路是证明该点处极限与函数实际取该点值相等, 也就是上节讲到的函数连续定义)
2. 复合运算
   设 \\(f(u) , u=\varphi(x) , \varphi(x)\neq a\\)
   若 \\(\lim\limits_{u\to a}f(u)=f(a) , \lim\limits_{x\to x_0}\varphi(x)=a\\) , 则 \\(\lim\limits_{x\to x_0}f[\varphi(x)]=f[\lim\limits_{x\to x_0}\varphi(x)]=f(a)\\)

### 初等函数连续性

基本初等函数/初等函数在其定义域内连续

## 闭区间上连续函数的性质

(基本就是废话)

1. 最值定理
   设 \\(f(x)\in c[a, b]\\)
   则 f(x) 在 [a, b] 上取到 最小值m 和 最大值M
   即 \\(\exist x_1, x_2 \in[a, b]\\) , 使 \\(f(x_1)=m , f(x_2)=M\\)
2. 有界定理
   设 \\(f(x)\in c[a, b]\\)
   则 \\(\exist k>0\\) , 使 \\(\forall x\in[a, b]\\) , 有 \\(|f(x)|\leqslant k\\)
3. 零点定理
   设 \\(f(x)\in c[a, b]\\)
   若 \\(f(a)f(b)<0\\) , 则 \\(\exist c\in[a, b]\\) , 使 \\(f\(c\)=0\\)
   (高中的零点存在定理)
4. 界值定理
   设 \\(f(x)\in c[a, b]\\)
   则 \\(\forall\eta\in[m, M] , \exist\xi\in[a, b]\\) , 使 \\(f(\xi)=\eta\\)
   (即介于 m 和 M 之间的 f(x) 皆可取到)