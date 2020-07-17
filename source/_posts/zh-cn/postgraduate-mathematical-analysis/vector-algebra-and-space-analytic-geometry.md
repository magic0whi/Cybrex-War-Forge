---
title: vector-algebra-and-space-analytic-geometry
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:01:57
tags:
toc: true
---

向量代数和几何分析

<!-- more -->

## 向量及其线性运算

1. 定义
   1. 向量: 有大小, 有方向
      Note: 向量由大小(长度)及方向唯一确定
   2. 向量相等: 若 \\(\vec{a} , \vec{b}\\) 方向相同且长度相同, 称 \\(\vec{a} , \vec{b}\\) 相等, 记 \\(\vec{a}, \vec{b}\\)
   3. 向量的模:
      设 \\(\vec{a}\\) 为一个向量, 其长度记为 \\(|\vec{a}|\\)
      * 若 \\(|\vec{a}|=0\\) , 称 \\(\vec{a}\\) 为零向量, 记 \\(\vec{a}=\vec{0}\\) (零向量的方向不确定)
      * 若 \\(|\vec{a}|=1\\) , 称 \\(\vec{a}\\) 为单位向量
   4. 向量的夹角:
      设 \\(\vec{a} , \vec{b}\\) 为两个向量, 如图 TODO: 补充图片
      \\(\vec{a} , \vec{b}\\) 夹角为 \\(\theta\\) , 记 \\((\widehat{\vec{a} , \vec{b}})=0 \enspace (0\leqslant\theta\leqslant\pi)\\)
2. 向量的线性运算
   1. \\(\vec{a}+\vec{b}\\) :
      平行四边形法则 TODO: 补充图片
      \\(\begin{cases} \vec{a}+\vec{b}=\vec{b}+\vec{a} \\\ \vec{a}+(\vec{b}+\vec{c})=(\vec{a}+\vec{b})+\vec{c} \end{cases}\\)
   2. \\(\vec{a}-\vec{b}\\) : TODO: 补充图片
      \\(\vec{a}-\vec{b}=\vec{a}+(-\vec{b})\\)
   3. 向量数乘 \\(k\vec{a}\\) (k为常数):
      1. \\(k>0 , k\vec{a}\\) 与 \\(\vec{a}\\) 方向相同
      2. \\(k=0 , k\vec{a}=\vec{0}\\)
      3. \\(k<0 , k\vec{a}\\) 与 \\(\vec{a}\\) 方向反向
3. 空间直角坐标系
   TODO: 补充图片, x, y, z 顺序无所谓, 但必须<u>逆时针排列</u>
   | z>0      | z<0      | x-y平面 |
   |----------|----------|---------|
   | 第一卦限 | 第五卦限 | x>0 y>0 |
   | 第二卦限 | 第六卦限 | x<0 y>0 |
   | 第三卦限 | 第七卦限 | x<0 y<0 |
   | 第四卦限 | 第八卦限 | x>0 y<0 |
   空间向量的正交分解:
   设 \\(\vec{r}=\overrightarrow{OM}=\\{a, b, c\\}\\)
   \\(\vec{i}\\) 为 x 轴正方向的单位向量 \\(\overrightarrow{OA}=a\vec{i}\\)
   \\(\vec{j}\\) 为 y 轴正方向的单位向量 \\(\overrightarrow{OB}=b\vec{j}\\)
   \\(\vec{k}\\) 为 x 轴正反向的单位向量 \\(\overrightarrow{OC}=c\vec{k}\\)
   \\(\because \vec{r}=\overrightarrow{OM}=\overrightarrow{OA}+\overrightarrow{OB}+\overrightarrow{OC}\\) (根据平行四边形法则)
   \\(\therefore \\{a, b, c\\}=a\vec{i}+b\vec{j}+c\vec{k}\\)
4. 向量线性运算的代数描述
   设 \\(\vec{a}=\\{a_1, b_1, c_1\\}\\) , \\(\vec{b}=\\{a_2, b_2, c_2\\}\\)
   1. \\(\vec{a}+\vec{b}=\\{a_1+a_2, b_1+b_2, c_1+c_2\\}\\)
   2. \\(\vec{a}-\vec{b}=\\{a_1-a_2, b_1-b_2, c_1-c_2\\}\\)
   3. \\(k\vec{a}=\\{ka_1, kb_1, kc_1\\}\\)
5. 向量的模, 方向角, 方向余弦. 在坐标轴上的投影
   1. 向量的模
      设 \\(\vec{a}=\\{a_1, b_1, c_1\\}\\), 则 \\(|\vec{a}|=\sqrt{a_1^2+b_1^2+c_1^2}\\) (空间勾股定理)
   2. 对应单位向量
      设 \\(\vec{a}=\\{a_1, b_1, c_1\\}\neq\vec{0}\\) , \\(\vec{a}\\) 对应的单位向量记为 \\(\vec{a}^0\\) <!-- 还没找到更好的表示对应单位向量的方法 -->
      \\(\begin{aligned} \vec{a}^0=\frac{1}{|\vec{a}|}\cdot\vec{a}&=\frac{1}{\sqrt{a_1^2+b_1^2+c_1^2}}\cdot\\{a_1, b_1, c_1\\} \\\ &=\\{\frac{a_1}{\sqrt{a_1^2+b_1^2+c_1^2}}, \frac{b_1}{\sqrt{a_1^2+b_1^2+c_1^2}}, \frac{c_1}{\sqrt{a_1^2+b_1^2+c_1^2}}\\} \enspace(向量数乘) \end{aligned}\\)
   3. 方向角和方向余弦
      设 \\(\vec{a}=\\{a_1, b_1, c_1\\}\neq\vec{0}\\) , \\(\vec{a}\\) 与 x, y, z 轴正方向的夹角称为方向角, 记 \\(\alpha, \beta, \gamma\\)
      称 \\(\cos\alpha, \cos\beta, \cos\gamma\\) 为 \\(\vec{a}\\) 的方向余弦
      \\(\because \cos\alpha=\frac{a_1}{|\vec{a}|}=\frac{a_1}{\sqrt{a_1^2+b_1^2+c_1^2}} , \cos\beta=\frac{b_1}{|\vec{a}|}=\frac{b_1}{\sqrt{a_1^2+b_1^2+c_1^2}} , \cos\gamma=\frac{c_1}{|\vec{a}|}=\frac{c_1}{\sqrt{a_1^2+b_1^2+c_1^2}} \enspace\\) (想象平面坐标系下的情况)
      \\(\therefore \\{\cos\alpha, \cos\beta, \cos\gamma\\}=\vec{a}^0=\frac{\vec{a}}{|\vec{a}|}\\)
      推论:
      1. \\(\cos^2\alpha+\cos^2\beta+\cos^2\gamma=1\\)
      2. \\(\\{\cos\alpha, \cos\beta, \cos\gamma\\}=\vec{a}^0\\)
   4. 向量在坐标轴上的投影 TODO: 补充图片
      1. \\(\overrightarrow{A_1B_1}\\) 称为 \\(\overrightarrow{AB}\\) 在 u 轴上的**投影向量**
         \\(\overrightarrow{A_1B_1}=(x_2-x_1)\vec{e}\\)
      2. \\(A_1B_1=x_2-x_1\\) 称为 \\(\overrightarrow{AB}\\) 在 u 轴上的**投影**
         记 \\(Pr j_u\overrightarrow{AB}\\)
      3. 设 \\(\overrightarrow{AB}\\) 与 u 轴夹角为 \\(\theta\\) , 则
         \\(Pr j_u\overrightarrow{AB}=|\overrightarrow{AB}|\cdot\cos\theta\\)

## 向量的数量积与向量积

### 向量的数量积

1. 产生的背景: 做功 TODO: 补充图片
   \\(W=|\vec{F}|\cdot\cos\theta\cdot|\overrightarrow{AB}|=|\vec{F}|\cdot|\overrightarrow{AB}|\cdot\cos(\widehat{\overrightarrow{AB}, \vec{F}}) \rArr \vec{F}\cdot\overrightarrow{AB}\\)
2. 向量的数量积定义(几何)
   \\(\vec{a}\cdot\vec{b}\\) 称为 \\(\vec{a}, \vec{b}\\) 的数量积
   \\(\vec{a}\cdot\vec{b}=|\vec{a}|\cdot|\vec{b}|\cdot\cos(\widehat{\vec{a}, \vec{b}})\\)
3. 性质
   1. \\(\vec{a}\cdot\vec{b}=\vec{b}\cdot\vec{a}\\)
   2. \\(\vec{a}\cdot\vec{a}=|\vec{a}|^2\\)
      若 \\(\vec{a}\cdot\vec{a}=0 \hArr \vec{a}=\vec{0}\\)
   3. \\(\vec{a}\cdot\vec{b}=0 \hArr \vec{a}\perp\vec{b}\\)
4. 向量数量积的代数描述
   设 \\(\begin{aligned} &\vec{a}=\\{a_1, b_1, c_1\\}=a_1\vec{i}+b_1\vec{j}+c_1\vec{k} \\\ &\vec{b}=\\{a_2, b_2, c_2\\}=a_2\vec{i}+b_2\vec{j}+c_2\vec{k} \end{aligned}\\)
   则
   \\(\vec{a}\cdot\vec{b}=(a_1\vec{i}+b_1\vec{j}+c_1\vec{k})\cdot(a_2\vec{i}+b_2\vec{j}+c_2\vec{k})=a_1a_2+b_1b_2+c_1c_2 \enspace\\) (提示: \\(\vec{i}, \vec{j}, \vec{k}\\) 三个向量为正交单位向量)
   推论: \\(\vec{a}\cdot\vec{b}=0 \hArr \vec{a}\perp\vec{b} \hArr a_1a_2+b_1b_2+c_1c_2=0\\)

### 向量的向量积

(参与运算的是向量, 结果还是向量)

1. 产生的背景: 法向量(垂直于某一平面的向量) TODO: 补充图片
2. 向量的向量积定义
   \\(\vec{a}\times\vec{b}\\) 称为 \\(\vec{a}, \vec{b}\\) 的向量积
   1. 几何刻划:
      \\(\vec{a}\times\vec{b}\begin{cases} 方向: 右手准则(拇指食指中指分别对应\vec{a}, \vec{b}, \vec{c}) \\\ 大小: |\vec{a}\times\vec{b}|=|\vec{a}|\cdot|\vec{b}|\cdot\sin(\widehat{\vec{a}, \vec{b}}) \end{cases}\\)
   2. 代数刻划:
      设 \\(\begin{aligned} &\vec{a}=\\{a_1, b_1, c_1\\}=a_1\vec{i}+b_1\vec{j}+c_1\vec{k} \\\ &\vec{b}=\\{a_2, b_2, c_2\\}=a_2\vec{i}+b_2\vec{j}+c_2\vec{k} \end{aligned}\\)
      则
      \\(\begin{aligned} \vec{a}\times\vec{b}=&(a_1\vec{i}+b_1\vec{j}+c_1\vec{k})\times(a_2\vec{i}+b_2\vec{j}+c_2\vec{k}) \\\ =&\mskip{1.2em}a_1a_2\vec{i}\times\vec{i}+a_1b_2\vec{i}\times\vec{j}+a_1c_2\vec{i}\times\vec{k} \\\ &+b_1a_2\vec{j}\times\vec{i}+b_1b_2\vec{j}\times\vec{j}+b_1c_2\vec{j}\times\vec{k} \\\ &+c_1a_2\vec{k}\times\vec{i}+c_1b_2\vec{k}\times\vec{j}+c_1c_2\vec{k}\times\vec{k} \\\ =&a_1b_2\vec{i}\times\vec{j}+a_1c_2\vec{i}\times\vec{k}+b_1a_2\vec{j}\times\vec{i}+b_1c_2\vec{j}\times\vec{k}+c_1a_2\vec{k}\times\vec{i}+c_1b_2\vec{k}\times\vec{j} \enspace(平行或相同向量的向量积为无意义的零向量, 舍去) \\\ =&a_1b_2\vec{k}-a_1c_2\vec{j}-b_1a_2\vec{k}+b_1c_2\vec{i}+c_1a_2\vec{j}-c_1b_2\vec{i} \enspace(提示: 右手准则用起来) \\\ =&(a_1b_2-b_1a_2)\vec{k}+(c_1a_2-a_1c_2)\vec{j}+(b_1c_2-c_1b_2)\vec{i} \\\ =&\\{b_1c_2-b_2c_1, -(a_1c_2-a_2c_1), a_1b_2-a_2b_1\\} \end{aligned}\\)
      即 \\(\vec{a}\times\vec{b}=\\{b_1c_2-b_2c_1, -(a_1c_2-a_2c_1), a_1b_2-a_2b_1\\}\\)
3. 性质
   1. \\(\vec{a}\times\vec{b}=\vec{0} \hArr \vec{a}\parallel\vec{b}\\)
   2. \\(\vec{a}\times\vec{b}\perp\vec{a}, \vec{b}\\)
   3. 向量积不适用乘法交换律 \\(\vec{a}\times\vec{b}=-\vec{b}\times\vec{a}\\) TODO: 补充图片
   4. \\(|\vec{a}\times\vec{b}|=2S_\Delta\\) TODO: 补充图片
      证明:
      \\(\begin{aligned} S_\Delta&=\frac{1}{2}|\vec{a}|\cdot|\vec{b}|\cdot\sin(\widehat{\vec{a}, \vec{b}}) \\\ &=\frac{1}{2}|\vec{a}\times\vec{b}| \end{aligned}\\)

## 向量应用

### 平面及其方程

#### 空间曲面

(概念, 了解一下就好)
设 \\(F(x, y, z)=0\\) 为一个三元方程, \\(\Sigma\\) 为曲面
若 \\(F(x, y, z)=0\\) 的任意解 \\((x_0, y_0, z_0)\\) 对应的点 \\(M_0(x_0, y_0, z_0)\\) 在曲面上
或者反之, 曲面上任一点 \\(M(x_0, y_0, z_0)\\) 有 \\(F(x_0, y_0, z_0)=0\\)
称 \\(F(x, y, z)=0\\) 为曲面 \\(\Sigma\\) 方程, \\(\Sigma\\) 为方程 \\(F(x, y, z)=0\\) 对应的曲面
记 \\(\Sigma: F(x, y, z)=0\\)

#### 曲面的特殊情形 -- 平面

1. 平面的点法式方程 TODO: 补充图片
   设 \\(M_0(x_0, y_0, z_0)\in\pi \enspace,\enspace 法向量 \vec{n}=\\{A, B, C\\}\perp\pi\\)
   \\(\forall M(x, y, z)\\) , 有 \\(M(x, y, z)\in\pi \rArr \vec{n}\perp\overrightarrow{M_0M} \rArr \vec{n}\cdot\overrightarrow{M_0M}=0\\)
   而 \\(\overrightarrow{M_0M}=\\{x-x_0, y-y_0, z-z_0\\}\\)
   \\(\therefore \pi: A(x-x_0)+B(y-y_0)+C(z-z_0)=0\\)
2. 截距式方程 TODO: 补充图片
   \\(\overrightarrow{AB}=\\{-a, b, 0\\} \enspace,\enspace \overrightarrow{AC}=\\{-a, 0, c\\}\\)
   法向量 \\(\vec{n}=\overrightarrow{AB}\times\overrightarrow{AC}=\\{bc, ac, ab\\}\\)
   平面:
   \\(\begin{aligned} \pi: bc(x-a)+ac(y-0)+an(z-0)=0 \rArr bc(x-a)+acy+abz&=0 \\\ bcx+acy+abz&=abc \\\ \frac{x}{a}+\frac{y}{b}+\frac{z}{c}&=1 \end{aligned}\\)
   即 \\(pi: \frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1\\)
3. 一般式方程
   平面 \\(\pi: Ax+By+Cz+D=0\\)
   且 \\(\vec{n}=\\{A, B, C\\}\\)

#### 两个平面夹角

TODO: 补充图片
平面 \\(\pi_1: A_1x+B_1y+C_1z+D_1=0\\)
平面 \\(\pi_2: A_2X+B_2y+C_2z+D_2=0\\)
\\(\vec{n_1}=\\{A_1, B_1, C_1\\}\\)
\\(\vec{n_2}=\\{A_2, B_2, C_2\\}\\)

(取决于你从哪个面判断夹角 \\((\widehat{\vec{n_1}, \vec{n_2}})\\), 但是平面夹角必须是锐角)
1. \\((\widehat{\vec{n_1}, \vec{n_2}})\in[0, \frac{\pi}{2}]\\) , 则 \\(\theta=(\widehat{\vec{n_1}, \vec{n_2}})\\)
   \\(\cos\theta=\cos(\widehat{\vec{n_1}, \vec{n_2}})=\frac{\vec{n_1}\cdot\vec{n_2}}{|\vec{n_1}|\cdot|\vec{n_2}|}\\)
2. \\((\widehat{\vec{n_1}, \vec{n_2}})\in[\frac{\pi}{2}, \pi]\\) , 则 \\(\theta=\pi-(\widehat{\vec{n_1}, \vec{n_2}})\\)
   \\(\cos\theta=\cos(\pi-(\widehat{\vec{n_1}, \vec{n_2}}))=-\cos(\widehat{\vec{n_1}, \vec{n_2}})=-\frac{\vec{n_1}\cdot\vec{n_2}}{|\vec{n_1}|\cdot|\vec{n_2}|}\\)

1, 2综合得: \\(\cos\theta=\frac{|\vec{n_1}\vec{n_2}|}{|\vec{n_1}|\cdot|\vec{n_2}|}\\)

### 空间直线

1. 点向式方程 TODO: 补充图片
   直线上一点 \\(M_0(x_0, y_0, z_0)\in L\\)
   有向量 \\(\vec{S}=\\{m, n, p\\}\parallel L\\)
   \\(\forall M(x, y, z)\\)
   若 \\(M\in L\\), 则 \\(\overrightarrow{M_0M}\parallel\vec{S}\qquad \overrightarrow{M_0M}=\\{x-x_0, y-y_0, z-z_0\\}\\)
   \\(\because \overrightarrow{M_0M}\parallel\vec{S} \hArr \frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}\\)
   \\(\therefore L: \frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}\\)
2. 参数式方程
   设 \\(M_0(x_0, y_0, z_0) \qquad \vec{S}=\\{m, n, p\\}\parallel L\\)
   \\(L=\frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}\\)
   令 \\(\frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}=t\\)
   则 L 的参数方程为
   \\(L: \begin{cases} x=x_0+mt \\\ y=y_0+nt \\\ z=z_0+pt \end{cases}\\)
3. 一般式方程
   (两平面相交得到一条直线)
   \\(L: \begin{cases} A_1x+B_1y+C_1z+D_1=0 \\\ A_2x+B_2y+C_2z+D_2=0 \end{cases}\\)
4. 杂知识点
   1. 夹角
      1. 两向量的夹角:
         设 \\(\vec{a}=\\{a_1, b_1, c_1\\}, \vec{b}=\\{a_2, b_2, c_2\\}\\) 为两个向量, \\((\widehat{\vec{a}, \vec{b}})=\theta \enspace(0\leqslant\theta\leqslant\pi)\\)
         由 \\(\vec{a}\cdot\vec{b}=|\vec{a}|\cdot|\vec{b}|\cdot\cos\theta\\)
         得 \\(\cos\theta=\frac{\vec{a}\cdot\vec{b}}{|\vec{a}||\vec{b}|}=\frac{a_1a_2+b_1b_2+c_1c_2}{\sqrt{a_1^2+b_1^2+c_1^2}\sqrt{a_2^2+b_2^2+c_2^2}}\\)
      2. [两平面夹角](#两个平面夹角)
      3. 两直线夹角: 同 [两平面夹角](#两个平面夹角)
      4. 直线与平面夹角: TODO: 补充图片(提示, 图二作得不好, 三角形外切角)
         设平面法向量 \\(\vec{n}\\), 直线对应向量 \\(\vec{s}\\)
         1. \\((\widehat{\vec{n}, \vec{s}})\in[0, \frac{\pi}{2}]\\) 时
            \\(\varphi+(\widehat{\vec{n}, \vec{s}})=\frac{\pi}{2} \rArr \varphi=\frac{\pi}{2}-(\widehat{\vec{n}, \vec{s}})\\)
            \\(\sin\varphi=\cos(\widehat{\vec{n}, \vec{s}})\\)
         2. \\((\widehat{\vec{n}, \vec{s}})\in[\frac{\pi}{2}, \pi]\\) 时
            \\((\widehat{\vec{n}, \vec{s}})=\frac{\pi}{2}+\varphi\\)
            \\(\sin\varphi=-\cos(\vec{n}, \vec{s})\\)
            \\(\therefore 综合1, 2 得 \sin\varphi=|\cos(\vec{n}, \vec{s})|=\frac{|\vec{n}\cdot\vec{s}|}{|\vec{n}|\cdot|\vec{s}|}\\)
   2. 距离
      1. 两点距离:
         设 \\(A(x_1, y_1, z_1) , B(x_2, y_2, z_2)\\)
         则 AB 距离 \\(d=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2+(z_2+z_1)^2}\\)
      2. 点到平面距离 TODO: 补充图片
         设平面 \\(\pi: Ax+By+Cz+D=0\\) , 点 \\(M_0(x_0, y_0, z_0)\notin\pi\\)
         \\(\forall M_1(x_1, y_1, z_1)\in\pi\\)
         \\(\overrightarrow{M_0M_1}=\\{x_1-x_0, y_1-y_0, z_1-z_0\\}\\)
         \\(\begin{aligned} Prj_{\vec{n}}\overrightarrow{M_0M_1}=\frac{\vec{n}\cdot\overrightarrow{M_0M_1}}{|\vec{n}|}&=\frac{A(x_1-x_0)+B(y_1-y_0)+c(z_1-z_0)}{\sqrt{A^2+B^2+C^2}} \\\ &=\frac{(Ax_1+By_1+Cz_1)-(Ax_0+By_0+Cz_0)}{\sqrt{A^2+B^2+C^2}} \end{aligned}\\)
         \\(\because M_1\in\pi\\)
         \\(\therefore 代入平面\pi得 Ax_1+By_1+Cz_1=-D\\)
         \\(\therefore Prj_{\vec{n}}\overrightarrow{M_0M_1}=-\frac{Ax_0+By_0+Cz_0+D}{\sqrt{A^2+B^2+C^2}}\\)
   3. 平面束
      L 为直线, 经过 L 的所有平面称为平面束
      设 \\(L: \begin{cases} A_1x+B_1y+C_1z+D_1=0 \\\ A_2x+B_2y+C_2z+D_2=0 \end{cases}\\)
      过 L 的平面束为 \\(\pi: A_1x+B_1y+C_1z+D_1+\lambda(A_2x+B_2y+C_2z+D_2)=0\\)
      即 \\(\pi: (A_1+A_2\lambda)x+(B_1+B_2\lambda)y+(C_1+C_2\lambda)z+(D_1+D_2\lambda)=0\\)

## 空间曲面及方程

\\(\Sigma: F(x, y, z)=0\\)

### 柱面

方程: \\(x^2+y^2=4\\)
二维: 半径为2的圆
三维: 到z轴的距离为2的点形成的曲面
推导:
TODO: 补充图片
设 \\(\forall M(x, y, z)\in\Sigma ,\enspace T(0, 0, z)\\)
\\(|MT|=2 \rArr \sqrt{(x-0)^2+(y-0)^2+(z-z)^2}=2 \rArr x^2+y^2=4\\)
\\(\therefore \Sigma: x^2+y^2=4\\)

1. \\(\Sigma: F(x, y)=0\\) 为母线平行于 z 轴的柱面
2. \\(\Sigma: G(y, z)=0\\) 为母线平行于 x 轴的柱面
3. \\(\Sigma: H(x, z)=0\\) 为母线平行于 y 轴的柱面

### 旋转曲面

设: \\(L:\begin{cases} F(x, y)=0 \\\ z=0 \end{cases}\\)
1. TODO: 补充图片
   设 L 绕 x 轴旋转一周形成的曲面为 \\(\Sigma_x\\)
   设 \\(\forall M(x, y, z)\in\Sigma_x ,\enspace M_0(x, y_0, 0)\in L,\enspace T(x, 0, 0)\\)
   由 \\(|M_0T|=|MT|\\) 得
   \\(\sqrt{y_0^2}=\sqrt{y^2+z^2}\\)
   \\(y_0=\pm\sqrt{y^2+z^2}\\)
   \\(\because M_0(x, y_0, 0)\in L\\)
   \\(\therefore f(x, y_0)=0\\)
   \\(\therefore \Sigma_x: f(x, \pm\sqrt{y^2+z^2})=0\\)
2. 设 L 绕 y 轴旋转一周形成的曲面为 \\(\Sigma_y\\)
   (和绕 x 轴同理)
   \\(\Sigma_y: f(\pm\sqrt{x^2+z^2}, y)=0\\)

## 空间曲线及方程

### 空间曲线的形式

1. 一般形式 TODO: 补充图片
   \\(L: \begin{cases} F(x, y, z)=0 \\\ G(x, y, z)=0 \end{cases}\\\)
2. 参数式
   \\(L: \begin{cases} x=\varphi(t) \\\ y=\psi(t) \\\ z=\omega(t) \end{cases}\\)

### 曲线的特殊情形 -- 直线

参见 [空间直线](#空间直线)

### 投影直线

TODO: 补充图片(视频中还有阴影, 笔记上没画)
设 \\(L: \begin{cases} F(x, y, z)=0 \\\ G(x, y, z)=0 \end{cases}\\)
L向 xOy 面铅直投影得到投影曲线 \\(L_0\\)

由 \\(\begin{cases} F(x, y, z)=0 \\\ G(x, y, z)=0 \end{cases} \xRightarrow{消\large z} H(x, y)=0\\)
\\(L_0 \begin{cases} H(x, y)=0 \\\ z=0 \end{cases}\\)