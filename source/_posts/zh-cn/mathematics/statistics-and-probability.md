---
title: statistics-and-probability
lang: zh-cn
category: mathematics
mathjax: 'true'
date: 2020-03-19 16:18:34
tags:
---

## 统计

### 随机抽样

1. <u>简单随机抽样</u>: 设一个总体含有<u>N个</u>个体, 从中<u>逐个不放回地抽取</u>n个个体为样本. 如果每次抽取时总体上各个个体被抽到的<u>机会相等</u>. 就把这种抽样方法叫做简单随机抽样.

   常用的简单随机抽样法有两种: 抽签法 和 随机数法

   抽签法: 把总体中的N个个体编号, 把号码写在号签上, 将号签放在一个不透明容器中, 搅拌均匀后, 每次从中抽取一个号签. 连续抽取n次, 就得到一个容量为n的样本.

2. <u>分层抽样</u>: 在抽样时, 将总体分成互不相交的层, 然后按照一定的比例, 从各层独立地抽取一定数量的个体, 将各层取出的个体合在一起作为样本, 这种抽样方法是一种分层抽样.

3. <u>系统抽样</u>: 又叫做等距抽样法. 先分段(分组), 起始段用简单随机抽样再在各段相同位置取得样本

   极差: 一组数据最大值与最小值
   组数: $\frac{极差}{组距}$

### 样本分析

#### 频率分布直方图

组距=$\frac{全距}{组数}$
纵轴: $\frac{频率}{组距}$
横轴: 按照组距分成若干段
**每个矩形的面积恰好是该组的频率**

频率分布折线图: 将频率分布直方图中各个矩形的上底边的中点连结起来, 就成了频率分布折线图

#### 茎叶图
用于对比两组数据, 也可用于记录单组数据

"茎": 中间的一列数, 从上到下由小到大, 一般取数据中十位上的数
"叶": 两边分别记录两个组的数据, 由外到内数越来越小, 一般去数据中个位上的数

#### 标准差

$S = \sqrt{\frac{1}{n}\sum_{i = 1}^n (x_i - \bar{x})^2} \quad n为样本中数据个数$
$方差=S^2$

### 变量相关性

#### 散点图

1. 散点图: 将变量所对应的点在直角坐标系中标出
2. 正相关和负相关: 依据点的散步方式, 斜杠"/"方向是正相关, 反斜杠"\"方向是负相关

<span id="linear_regression__equation"></span>
#### 回归直线方程

1. 最小平方法: 如果有n个样本点 $(x_1, y_1), (x_2), (y_2), ..., (x_n, y_n)$ , 若要求一条最能拟合这些点的直线 $\hat{y} = bx + a$, 可通过下面的表达式:
   $$[y_1 - (a + bx_1)]^2 + [y_2 - (a + bx_2)]^2 + ... + [y_n - (a + bx_n)]^2$$
   若上述表达式能取得最小值, 将得到的 a, b 的值带入 $\hat{y} = bx + a$ 就是我要所要的最拟合直线. 这种方法也叫**最小二乘法**.
2. 线性回归方程: 将上面那条表达式使用配方法化简, 我们就得到了
   $$\begin{cases}
       \hat{b} = \frac{\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^n (x_i - \bar{x})^2} = \frac{\sum_{i=1}^n x_i y_i - n\bar{x}\bar{y}}{\sum_{i=1}^n x_i^2 - n\bar{x}^2} \\
       \hat{a} = \bar{y} - \hat{b}\bar{x}
   \end{cases}$$
   带入即可得目标式 $\hat{y} = \hat{b}x + \hat{a}$.
   此方程恒经过样本的$(\bar{x}, \bar{y})$, 即**样本中心点**

### 计数原理

#### 分类加法和分布乘法计数

1. 分类加法计数原理: 举个例子, 完成一件事可以有两类不同的方法, 在方案一有 m 种不同的方法, 在方案二有 n 种不同的方法. 那么完成这件事只有 N = m + n 种不同方法.

2. 分布乘法计数原理: 举个例子, 完成一件事需要两个步骤, 做第一步有m种不同的方法, 做第二步有 n 种不同的方法. 那么完成这件事共有 N = mn 种不同的方法.

#### 排列与组合

1. 排列: 从n个不同元素中取出 $m \quad (m \geqslant n)$, 按照一定的顺序排成一列, 叫做从n 个不同元素中取出 m 个元素的一个排列 (互异性 有异性)
2. 排列数: $A_n^m = n(n-1)(n-2)...(n-m+1) = \frac{n!}{(n-m)!} \qquad (m \leqslant n, m,n \in N^+)$
   将n个不同元素全部取出的一个排列, 叫做n个元素的一个排列, 记作$A_n^n = n! \quad (规定 0! = 1)$

3. 组合: 从n个不同的元素中取出 $m \quad (m \leqslant n)$ 个元素合成一组, 叫做从n个不同元素中取出 m 个元素的一个组合 (与顺序无关, 只取不排)
4. 组合数: $C_n^m = \frac{A_n^m}{A_m^m} = \frac{n(n-1)(n-2)...(n-m+1)}{m!} = \frac{n!}{m!(n-m)!} \qquad (m \leqslant n, m,n \in N^+)$
   $组合式性质公式 \begin{cases}
      C_n^m = C_n^{n-m} \\
      C_{n+1}^m = C_n^m + C_n^{m-1}
   \end{cases}$

#### 二项式定理

二项式定理: $(a+b)^n = C_n^0 a^n + C_n^1 a^{n-1}b + C_n^2 a^{n-2}b^2 + ... + C_n^nb^n$

##### 二项式系数的性质

结合"杨辉三角"研究推出

二项式系数: $C_n^k (k \in 1, 2, 3, ..., n) \qquad (a+b)^n共有 n+1 项$

1. 对称性: 与首末两端"等距离"的两个二项式系式相等.
   直线 $r = \frac{n}{2}$ 为对称轴将二项式系数所表示出的图像分成对称的两部分

2. 增减性与最大值: 
   $\begin{aligned}
   &k < \frac{n+1}{2} \rArr 二项式系数为增 \\
   &k > \frac{n+1}{2} \rArr 二项式系数为减 \\
   &n 为偶数时, 其最大的二项式系数为 C_n^{\frac{n}{2}} \\
   &n 为奇数时, 其最大的二项式系数为 C_n^{\frac{n-1}{n}}, C_n^{\frac{n+1}{2}}
\end{aligned}$

1. 各二项式系数的和 $2^n = C_n^0 + C_n^1 + C_n^2 + ... + C_n^n$

### 统计案例

#### 独立性检验

独立性检验的基本方法:
一般地, 对于两个研究对象I和II, I 有两类取值, 即类 A 和类 B; II 也有两类取值, 即类 1 和 类. 得到如下列联表所示的抽样数据:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-baqh{text-align:center;vertical-align:top}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-c3ow" colspan="2" rowspan="2"></th>
    <th class="tg-c3ow" colspan="2">II</th>
    <th class="tg-c3ow"></th>
  </tr>
  <tr>
    <td class="tg-c3ow">类1</td>
    <td class="tg-c3ow">类2</td>
    <td class="tg-c3ow">合计</td>
  </tr>
  <tr>
    <td class="tg-c3ow" rowspan="2">I</td>
    <td class="tg-c3ow">类A</td>
    <td class="tg-c3ow">a</td>
    <td class="tg-c3ow">b</td>
    <td class="tg-c3ow">a+b</td>
  </tr>
  <tr>
    <td class="tg-c3ow">类B</td>
    <td class="tg-c3ow">c</td>
    <td class="tg-c3ow">d</td>
    <td class="tg-c3ow">c+d</td>
  </tr>
  <tr>
    <td class="tg-baqh" colspan="2">合计</td>
    <td class="tg-baqh">a+c</td>
    <td class="tg-baqh">b+d</td>
    <td class="tg-baqh">a+b+c+d</td>
  </tr>
</table>

要推断"I和II"没有关系, 可按下面步骤进行
1. 第一步提出假设$H_0$: "I和II没有关系"
2. 第二步根据2x2列联表计算统计量$X^2 = \frac{n(ad-bc)^2}{(a+b)(c+d)(a+c)(b+d)} \qquad (n=a+b+c+d)$
3. 第三步对照下面的临界值表, 作出判断:
   | $P(X^2 \geqslant x_0)$ | 0.50 | 0.40 | 0.25 | 0.15 | 0.10 | 0.05 | 0.025 | 0.010 | 0.005 | 0.001 |
   | ------------------ | ---- | ---- | ---- | ---- | ---- | ---- | ----- | ----- | ----- | ----- |
   | $x_0$ | 0.455 | 0.708 | 1.323 | 2.072 | 2.706 | 3.841 | 5.024 | 6.635 | 7.879 | 10.828 |
   若$X^2 > 10.828$, 则有 99.9% 的把握认为"I 与 II 有关系"
   若$X^2 > 6.635$, 则有 99% 的把握认为"I 与 II 有关系"
   若$X^2 > 2.706$, 则有 90% 的把握认为"I 与 II 有关系"
   若$X^2 \leqslant 2.706$, 则认为没有充分的证据显示"I 与 II 有关系", **但也不能作出结论$H_0$成立, 即 I 与 II 没有关系, 只能说有$\geqslant 10\%$的把握认为"I 与 II 无关系"**

#### 回归分析

1. 回归方程见前面[回归直线方程](#linear_regression__equation)
2. 相关指数
   $r = \frac{\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^n} (x_i - \bar{x})^2 \sum_{i = 1}^n (y_i - \bar{y})^2} = \frac{\sum_{i=1}^n x_iy_i - n\bar{x}\bar{y}}{\sqrt{(\sum_{i=1}^n x_i^2-n(\bar{x}^2)(\sum_{i=1}^n y_i^2 -n(\bar{y})^2)}}$
   r的性质
     $|r| \leqslant 1;$
     $|r| 越接近1, x, y的线性相关程度越强;$
     $|r| 越接近0, x, y的线性相关程度越弱.$

## 概率I

### 事件与概率

#### 随机事件

在条件S下可能发生也可能不发生的事件

#### 互斥事件

互斥: 若 $A\cap B$ 为不可能事件($A\cap B = \varnothing$), 则称事件A与事件B<u>互斥</u>. 其含义是: 事件A与事件B不会同时发生.

对立: 若$A\cap B$ 为不可能事件但 $A\cup B$ 为必然事件, 那么称事件A与事件B<u>互为对立事件</u>. 其含义是: 事件A与事件B在任何一次试验中有且仅有一个发生.

互斥和对立区别:
互斥: $P(A\cup B) = P(A) + P(B) \leqslant 1$
对立: $P(A\cup B) = P(A) + P(B) = 1$

### 古典概型

基本事件: 在1次实验中可能出现的每一个基本结果
基本事件的特点:
1. 任何两个事件是互斥的
2. 任何事件(除不可能事件)都可以表示成某个或某些基本事件的和

古典概型的两个特点:
1. 所有的基本事件只有有限个
2. 每个基本事件出现的可能性相等

古典概型公式: $P(A) = \frac{事件A包含的基本事件的个数}{基本事件的总数}$

### 几何概型

随机数:

几何概型公式: $P(A) = \frac{构成事件A的区域长度(面积或体积)}{试验的全部结果所构成的区域长度(面积或体积)}$

## 概率II

### 离散型随机变量

随机变量, 如果随机试验的结果可以用一个变量来表示, 那么这样的变量叫做随机变量. 常用字母表示: $X, Y, \xi, \eta$

离散型随机变量: 所有取值可以一一列出的随机变量

#### 超几何分布

超几何分布: 一般地, 在含有M件次品的N件产品中, 任取n件, 其中恰有x件次品.
$则 P(x=r) = \frac{C_M^k C_{N-M}^{n-k}}{C_N^n} \qquad (r = 1, 2, 3, ..., n)$
不合格数量X的概率分布表如下表所示:
| X | 0 | 1 | 2 | ... | $l$ |
| - | - | - | - | - | - |
| P | $\frac{C_M^0 C_{N-M}^n}{C_N^n}$ | $\frac{C_M^1 C_{N-M}^{n-1}}{C_N^n}$ | $\frac{C_M^2 C_{N-M}^{n-2}}{C_N^n}$ | ... | $\frac{C_M^l C_{N-M}^{n-l}}{C_N^n}$ |
$其中l = min(M, n). 且 n \leqslant N, M \leqslant N, n、m、N \in N^+$
此时称随机变量X服从参数为n, M, N的二项分布; 记作$X\text{\textasciitilde}H(n, M, N)$

### n次重复试验(伯努利试验)

由n次试验构成, 且每次试验相互独立完成, 每次试验的结果仅有两种对立的状态,
即 $P(A)=p > 0$. 我们将这样的试验称为n次独立重复试验, 也称为伯努利试验

#### 二项分布

在n次独立重复试验中, 用X表示事件A发生的次数. 设每次试验中事件A发生的概率为p, 
即 $P(A)=p, \, P(\bar{A})=1-p=q, \, p+q=1$. 则
$P(X=k)=C_n^k p^k q^{n-k} \qquad (k=0, 1, 2, ..., n)$
此时称随机变量X<u>服从</u>参数为n、p的二项分布; 记作$X\text{\textasciitilde}B(n,p)$

#### 离散均值和离散方差

一般地若离散型随机变量X的概率分布为
| X | $x_1$ | $x_2$ | ... | $x_n$ |
| - | ----- | ----- | --- | ----- |
| P | $p_1$ | $p_2$ | ... | $p_n$ |

期望: $\mu = E(X) = x_1p_1 + x_2p_2 + ... + x_np_n$ 为随机变量的均值或数学期望
期望的性质:
1. $E(aX + b) = aE(X+b)$
2. $E(X_1 + X_2) = E(X_1) + E(X_2)$
3. 若$X_1,X_2$相互独立, 则$E(X_1\cdot X_2) = E(X_1)\cdot E(X_2)$
4. 两点分布期望$E(X)=p$
5. 超几何分布期望$E(X)=\frac{nM}{N}$
6. 二项分布期望$E(X)=np$

离散方差: $\sigma^2 = V(X) = (x_1-\mu)^2p_1 + (x_2-\mu)^2p_2 + ... + (x_n-\mu)^2p_n$
离散方差的性质:
1. $V(aX+b)=a^2V(X)$
2. $V(X)=E(X^2)-[E(X)]^2$
3. 两点分布方差$V(X)=p(1-p)$
4. 超几何分布$V(X)=\frac{nM(N-M)(N-n)}{N^2(N-1)}$
5. 二项分布$V(X)=np(1-p)$

### 条件概率

事件B发生下A发生的概率: $P(A|B) = \frac{P(AB)}{P(B)}$

### 事件独立性

若$P(A|B) = P(A)$, 则称事件 A, B 独立
事件独立性性质:
1. $P(A|B) = \frac{P(AB)}{P(B)} \lrArr 事件 A, B 相互独立$
2. $事件A, B相互独立\lrArr \bar{A}与B, A与\bar{B}, \bar{A}与\bar{B}也都相互独立$