---
title: postgraduate-advanced-mathematics-2
toc: true
category: mathematics
lang: zh-cn
date: 2021-01-23 15:05:53
tags:
---

同济高等数学笔记整合(下)
基于 [wmathor/Postgraduate-Advanced-Mathematics](https://github.com/wmathor/Postgraduate-Advanced-Mathematics)
建议先看一看线性代数的行列式
补充了级数部分

<!-- more -->

## 向量代数与空间解析几何

### 向量及其线性运算

1. 定义
   1. 向量: 有大小, 有方向. 向量由大小(长度)及方向唯一确定, 与位置无关的向量称为自由向量
   2. 向量相等: 若 \\(\vec{a}\\)、\\(\vec{b}\\) 方向相同且长度相同, 称 \\(\vec{a}\\)、\\(\vec{b}\\) 相等, 记 \\(\vec{a}\\)、\\(\vec{b}\\)
   3. 向量的模:
      设 \\(\vec{a}\\) 为一个向量, 其长度记为 \\(|\vec{a}|\\)
      * 若 \\(|\vec{a}|=0\\) , 称 \\(\vec{a}\\) 为零向量, 记 \\(\vec{a}=\vec{0}\\) (零向量的方向不确定)
      * 若 \\(|\vec{a}|=1\\) , 称 \\(\vec{a}\\) 为单位向量
   4. 向量的夹角:
      设 \\(\vec{a}\\)、\\(\vec{b}\\) , 如图
      \\(\vec{a}\\)、\\(\vec{b}\\) 夹角为 \\(\theta\\) , 记 \\((\widehat{\vec{a},\vec{b}})=\theta\enspace\\) (\\(0\leqslant\theta\leqslant\pi\\))
      
      {% asset_img 1.png %}
2. 向量的线性运算
   1. 加法:
      \\(\vec{a}+\vec{b}=\vec{b}+\vec{a}\\)
      \\(\vec{a}+(\vec{b}+\vec{c})=(\vec{a}+\vec{b})+\vec{c}\\)
      * 平行四边形法则和三角形法则:
        
        {% asset_img 2.png %}
   2. 减法: \\(\vec{a}-\vec{b}=\vec{a}+(-\vec{b})\\)
      
      {% asset_img 3.png %}
3. 空间直角坐标系
   \\(x\\)、\\(y\\)、\\(z\\) 顺序无所谓, 但必须**逆时针排列** {% asset_img 4.png %}
   | \\(z>0\\) | \\(z<0\\) | \\(x-y\\) 平面 |
   |----------|----------|---------|
   | 第一卦限 | 第五卦限 | \\(x>0\\) , \\(y>0\\) |
   | 第二卦限 | 第六卦限 | \\(x<0\\) , \\(y>0\\) |
   | 第三卦限 | 第七卦限 | \\(x<0\\) , \\(y<0\\) |
   | 第四卦限 | 第八卦限 | \\(x>0\\) , \\(y<0\\) |
   空间向量的正交分解:

   {% asset_img 5.png %}
   则有 \\(\overrightarrow{OM}=\\{a,b,c\\}=a\vec{i}+b\vec{j}+c\vec{k}\\)
   \\(\vec{i}\\) 为 \\(x\\) 轴正方向的单位向量 \\(\overrightarrow{OA}=a\vec{i}\\)
   \\(\vec{j}\\) 为 \\(y\\) 轴正方向的单位向量 \\(\overrightarrow{OB}=b\vec{j}\\)
   \\(\vec{k}\\) 为 \\(z\\) 轴正反向的单位向量 \\(\overrightarrow{OC}=c\vec{k}\\)
4. 向量线性运算的代数描述
   设 \\(\vec{a}=\\{a_1,b_1,c_1\\}\\) , \\(\vec{b}=\\{a_2,b_2,c_2\\}\\)
   1. \\(\vec{a}+\vec{b}=\\{a_1+a_2,b_1+b_2,c_1+c_2\\}\\)
   2. \\(\vec{a}-\vec{b}=\\{a_1-a_2,b_1-b_2,c_1-c_2\\}\\)
   3. \\(k\vec{a}=\\{ka_1,kb_1,kc_1\\}\\)
5. 向量的模, 方向角, 方向余弦. 在坐标轴上的投影
   1. 向量的模
      设 \\(\vec{a}=\\{a_1,b_1,c_1\\}\\), 则 \\(\vec{a}\\) 的模 \\(|\vec{a}|=\sqrt{a_1^2+b_1^2+c_1^2}\\) (空间勾股定理)
   2. 对应单位向量
      设 \\(\vec{a}=\\{a_1,b_1,c_1\\}\neq\vec{0}\\) , \\(\vec{a}\\) 对应的单位向量记为 \\(\vec{a}^0\\)
      \\(\vec{a}^0=\frac{1}{|\vec{a}|}\cdot\vec{a}=\frac{1}{\sqrt{a_1^2+b_1^2+c_1^2}}\cdot\\{a_1,b_1,c_1\\}=\\{\frac{a_1}{\sqrt{a_1^2+b_1^2+c_1^2}},\frac{b_1}{\sqrt{a_1^2+b_1^2+c_1^2}},\frac{c_1}{\sqrt{a_1^2+b_1^2+c_1^2}}\\}\\)
   3. 方向角和方向余弦
      设 \\(\vec{a}=\\{a_1,b_1,c_1\\}\neq\vec{0}\\) , \\(\vec{a}\\) 与 \\(x\\)、\\(y\\)、\\(z\\) 轴正方向的夹角称为方向角, 记 \\(\alpha\\)、\\(\beta\\)、\\(\gamma\\)
      称 \\(\cos\alpha\\)、\\(\cos\beta\\)、\\(\cos\gamma\\) 为 \\(\vec{a}\\) 的方向余弦
      \\(\because\cos\alpha=\frac{a_1}{|\vec{a}|}=\frac{a_1}{\sqrt{a_1^2+b_1^2+c_1^2}},\cos\beta=\frac{b_1}{|\vec{a}|}=\frac{b_1}{\sqrt{a_1^2+b_1^2+c_1^2}},\cos\gamma=\frac{c_1}{|\vec{a}|}=\frac{c_1}{\sqrt{a_1^2+b_1^2+c_1^2}}\\)
      \\(\therefore\\{\cos\alpha,\cos\beta,\cos\gamma\\}=\vec{a}^0=\frac{\vec{a}}{|\vec{a}|}\\)
      推论: \\(\cos^2\alpha+\cos^2\beta+\cos^2\gamma=1\\)
   4. 向量在坐标轴上的投影
      
      {% asset_img 6.png %}
      1. \\(\overrightarrow{A_1B_1}\\) 称为 \\(\overrightarrow{AB}\\) 在 \\(u\\) 轴上的**投影向量**, \\(\overrightarrow{A_1B_1}=(x_2-x_1)\vec{e}\\)
      2. \\(A_1B_1=x_2-x_1\\) 称为 \\(\overrightarrow{AB}\\) 在 \\(u\\) 轴上的**投影**, 记 \\(Pr j_u\overrightarrow{AB}\\)
      3. 设 \\(\overrightarrow{AB}\\) 与 \\(u\\) 轴夹角为 \\(\theta\\) , 则 \\(Pr j_u\overrightarrow{AB}=|\overrightarrow{AB}|\cdot\cos\theta\\)

### 向量的数量积与向量积

1. 向量的数量积(参与运算的是向量, 结果是数)
   1. 产生的背景: 做功
      
      {% asset_img 7.png %}
      \\(W=|\vec{F}|\cdot\cos\theta\cdot|\overrightarrow{AB}|=|\vec{F}|\cdot|\overrightarrow{AB}|\cdot\cos(\widehat{\overrightarrow{AB},\vec{F}})\hArr\vec{F}\cdot\overrightarrow{AB}\\)
   2. 向量的数量积定义(几何)
      \\(\vec{a}\cdot\vec{b}\\) 称为 \\(\vec{a}\\) 与 \\(\vec{b}\\) 的数量积
      \\(\vec{a}\cdot\vec{b}=|\vec{a}|\cdot|\vec{b}|\cdot\cos(\widehat{\vec{a},\vec{b}})\\)
   3. 性质
      1. \\(\vec{a}\cdot\vec{b}=\vec{b}\cdot\vec{a}\\)
      2. \\(\vec{a}\cdot\vec{a}=|\vec{a}|^2\\)
      3. \\(\vec{a}\cdot\vec{b}=0\hArr\vec{a}\perp\vec{b}\\)
      4. \\(\vec{a}\cdot\vec{a}=0\hArr\vec{a}=\vec{0}\\)
   4. 向量数量积的代数描述
      设
      \\(\vec{a}=\\{a_1,b_1,c_1\\}=a_1\vec{i}+b_1\vec{j}+c_1\vec{k}\\)
      \\(\vec{b}=\\{a_2,b_2,c_2\\}=a_2\vec{i}+b_2\vec{j}+c_2\vec{k}\\)
      则 \\(\vec{a}\cdot\vec{b}=(a_1\vec{i}+b_1\vec{j}+c_1\vec{k})\cdot(a_2\vec{i}+b_2\vec{j}+c_2\vec{k})=a_1a_2+b_1b_2+c_1c_2\\)
      (推导思路: \\(\vec{i}\\)、\\(\vec{j}\\)、\\(\vec{k}\\) 三个向量为正交单位向量, 互相乘的值为零)
      推论: \\(\vec{a}\cdot\vec{b}=0\hArr\vec{a}\perp\vec{b}\hArr a_1a_2+b_1b_2+c_1c_2=0\\)
2. 向量的向量积(参与运算的是向量, 结果还是向量)
   1. 产生的背景: 法向量(垂直于某一平面的向量)
      
      {% asset_img 8.png %}
   2. 向量的向量积定义
      \\(\vec{a}\times\vec{b}\\) 称为 \\(\vec{a}\\)、\\(\vec{b}\\) 的向量积
      1. 几何刻划:
         \\(\vec{a}\times\vec{b}\begin{cases} \text{方向:右手准则(拇指食指中指分别对应}\vec{a},\vec{b},\vec{c}) \\\ \text{大小:}|\vec{a}\times\vec{b}|=|\vec{a}|\cdot|\vec{b}|\cdot\sin(\widehat{\vec{a},\vec{b}}) \end{cases}\\)
      2. 代数刻划:
         设
         \\(\vec{a}=\\{a_1,b_1,c_1\\}=a_1\vec{i}+b_1\vec{j}+c_1\vec{k}\\)
         \\(\vec{b}=\\{a_2,b_2,c_2\\}=a_2\vec{i}+b_2\vec{j}+c_2\vec{k}\\)
         则
         <div>
         $$
         \vec{a}\times\vec{b}=\{b_1c_2-b_2c_1,a_2c_1-a_1c_2,a_1b_2-a_2b_1\}=\{
         \begin{vmatrix}
          b_1 & c_1 \\
          b_2 & c_2
         \end{vmatrix}
         ,\begin{vmatrix}
          c_1 & a_1 \\
          c_2 & a_2
         \end{vmatrix}
         ,\begin{vmatrix}
          a_1 & b_1 \\
          a_2 & b_2
         \end{vmatrix}\}
         $$
         </div>
         推导:
         <div>
         $$
         \begin{aligned}
          \vec{a}\times\vec{b} & =(a_1\vec{i}+b_1\vec{j}+c_1\vec{k})\times(a_2\vec{i}+b_2\vec{j}+c_2\vec{k}) \\
          & =\mskip{1.2em}a_1a_2\vec{i}\times\vec{i}+a_1b_2\vec{i}\times\vec{j}+a_1c_2\vec{i}\times\vec{k} \\
          & \mskip{1.2em}+b_1a_2\vec{j}\times\vec{i}+b_1b_2\vec{j}\times\vec{j}+b_1c_2\vec{j}\times\vec{k} \\
          & \mskip{1.2em}+c_1a_2\vec{k}\times\vec{i}+c_1b_2\vec{k}\times\vec{j}+c_1c_2\vec{k}\times\vec{k} \\
          & =\mskip{1.2em}a_1b_2\vec{i}\times\vec{j}+a_1c_2\vec{i}\times\vec{k} \\
          & \mskip{1.2em}+b_1a_2\vec{j}\times\vec{i}+b_1c_2\vec{j}\times\vec{k} \\
          & \mskip{1.2em}+c_1a_2\vec{k}\times\vec{i}+c_1b_2\vec{k}\times\vec{j} \\
          & =a_1b_2\vec{k}-a_1c_2\vec{j}-b_1a_2\vec{k}+b_1c_2\vec{i}+c_1a_2\vec{j}-c_1b_2\vec{i} \enspace(\text{结合下面性质3和4}) \\
          & =(a_1b_2-b_1a_2)\vec{k}+(c_1a_2-a_1c_2)\vec{j}+(b_1c_2-c_1b_2)\vec{i} \\
          & =\{b_1c_2-b_2c_1,a_2c_1-a_1c_2,a_1b_2-a_2b_1\}
         \end{aligned}
         $$
         </div>
   3. 性质
      1. \\(\vec{a}\times\vec{b}=\vec{0}\hArr\vec{a}\parallel\vec{b}\\)
      2. \\(\vec{a}\times\vec{b}\perp\vec{a},\vec{b}\\)
      3. \\(\vec{a}\times\vec{b}=-\vec{b}\times\vec{a}\\)
      4. \\(\begin{cases} \vec{i}\times\vec{i}=\vec{0},\vec{j}\times\vec{j}=\vec{k}\times\vec{k}=\vec{0} \\\ \vec{i}\times\vec{j}=\vec{k},\vec{k}\times\vec{i}=\vec{j},\vec{j}\times\vec{k}=\vec{i} \end{cases}\\)
      5. \\(|\vec{a}\times\vec{b}|=2S_\Delta\\)
         
         {% asset_img 9.png %}
         推导:
         \\(\begin{aligned} S_\Delta & =\frac{1}{2}|\vec{a}|\cdot|\vec{b}|\cdot\sin(\widehat{\vec{a},\vec{b}}) \\\ & =\frac{1}{2}|\vec{a}\times\vec{b}| \end{aligned}\\)

### 空间曲面及方程

1. 空间曲面
   设 \\(F(x,y,z)=0\\) 为一个三元方程, \\(\Sigma\\) 为曲面
   若 \\(F(x,y,z)=0\\) 的任一解 \\((x_0,y_0,z_0)\\) 对应的点 \\(M_0(x_0,y_0,z_0)\\) 在曲面 \\(\Sigma\\) 上
   或者说曲面 \\(\Sigma\\) 上存在点 \\(M(x_0, y_0, z_0)\\) 使得 \\(F(x_0,y_0,z_0)=0\\)
   称 \\(F(x,y,z)=0\\) 为曲面 \\(\Sigma\\) 的方程, \\(\Sigma\\) 为方程 \\(F(x,y,z)=0\\) 对应的曲面
   记 \\(\Sigma:F(x,y,z)=0\\)
2. 柱面
   1. \\(\Sigma:F(x,y)=0\\) 为母线平行于 \\(z\\) 轴的柱面
   2. \\(\Sigma:G(y,z)=0\\) 为母线平行于 \\(x\\) 轴的柱面
   3. \\(\Sigma:H(x,z)=0\\) 为母线平行于 \\(y\\) 轴的柱面
   
   * 例: 同一个方程 \\(x^2+y^2=4\\) , 在二维坐标系中是一个半径为 2 的圆(称作母线); 在三维坐标系中在 \\(z\\) 轴无限延申, 成为了到 \\(z\\) 轴的距离为 2 的点形成的曲面

     {% asset_img 10.png %}
     设 \\(T(0,0,z)\\) 为 \\(z\\) 轴上一点, \\(\forall M(x,y,z)\in\Sigma\\)
     有 \\(|MT|=2\rArr\sqrt{(x-0)^2+(y-0)^2+(z-z)^2}=2\rArr x^2+y^2=4\\)
     \\(\therefore\Sigma:x^2+y^2=4\\)

   * 柱面 \\(\Sigma:F(x,y)=0\\) 在 \\(xOy\\) 面内的投影曲线为
     \\(L:\begin{cases} F(x,y)=0 \\\ z=0 \end{cases}\\)

     {% asset_img 11.png %}
3. 旋转曲面
   设 \\(L:\begin{cases} F(x,y)=0 \\\ z=0 \end{cases}\\)
   1. 设 \\(L\\) 绕 \\(x\\) 轴旋转一周形成的曲面为 \\(\Sigma_x\\)

      {% asset_img 12.png %}
      \\(\forall M(x,y,z)\in\Sigma_x\\) , \\(M_0(x,y_0,0)\in L\\) , \\(T(x, 0, 0)\\)
      由 \\(|M_0T|=|MT|\\) 得
      \\(\sqrt{(x-x)^2+(y_0-0)^2+(0-0)^2}=\sqrt{(x-x)^2+(y-0)^2+(z-0)^2}\\)
      \\(\hArr\sqrt{y_0^2}=\sqrt{y^2+z^2}\\)
      \\(\hArr y_0=\pm\sqrt{y^2+z^2}\\)
      \\(\because M_0\in L\\)
      \\(\therefore F(x,y_0)=0\\)
      \\(\therefore\Sigma_x:F(x,\pm\sqrt{y^2+z^2})=0\\)
   2. 设 \\(L\\) 绕 \\(y\\) 轴旋转一周形成的曲面为 \\(\Sigma_y\\)
      \\(\Sigma_y:f(\pm\sqrt{x^2+z^2},y)=0\\) (参考绕 \\(x\\) 轴)
4. 空间平面(空间曲面的特殊情形)
   1. 平面的点法式方程
      
      {% asset_img 13.png %}
      设曲面某点 \\(M_0(x_0,y_0,z_0)\in\pi\\) , 法向量 \\(\vec{n}=\\{A,B,C\\}\perp\pi\\)
      \\(\forall M(x,y,z)\in\pi\rArr\vec{n}\perp\overrightarrow{M_0M}\rArr\vec{n}\cdot\overrightarrow{M_0M}=0\\)
      代入 \\(\overrightarrow{M_0M}=\\{x-x_0,y-y_0,z-z_0\\}\\)
      得到 \\(\pi:A(x-x_0)+B(y-y_0)+C(z-z_0)=0\\)
   2. 截距式方程
      
      {% asset_img 14.png %}
      \\(\overrightarrow{AB}=\\{-a,b,0\\}\\) , \\(\overrightarrow{AC}=\\{-a,0,c\\}\\)
      平面 \\(ABC\\) 的法向量 \\(\vec{n}=\overrightarrow{AB}\times\overrightarrow{AC}=\\{bc,ac,ab\\}\\)
      将点 \\(C\\) 代入点法式方程:
      \\(\pi:bc(x-a)+ac(y-0)+an(z-0)=0\rArr bc(x-a)+acy+abz=0\\)
      \\(\hArr bcx+acy+abz=abc\hArr\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1\\)
      即 \\(\pi:\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1\\)
   3. 一般式方程 \\(\pi:Ax+By+Cz+D=0\\) , 法向量 \\(\vec{n}=\\{A,B,C\\}\\)
5. 两个平面夹角
   
   {% asset_img 15.png %}
   \\(\pi_1:A_1x+B_1y+C_1z+D_1=0\\) , \\(\vec{n_1}=\\{A_1,B_1,C_1\\}\\)
   \\(\pi_2:A_2x+B_2y+C_2z+D_2=0\\) , \\(\vec{n_2}=\\{A_2,B_2,C_2\\}\\)
   1. 若 \\((\widehat{\vec{n_1},\vec{n_2}})\in[0,\frac{\pi}{2}]\\) , 则平面夹角 \\(\theta=(\widehat{\vec{n_1},\vec{n_2}})\\)
      有 \\(\cos\theta=\cos(\widehat{\vec{n_1},\vec{n_2}})=\frac{\vec{n_1}\cdot\vec{n_2}}{|\vec{n_1}|\cdot|\vec{n_2}|}\\)

      {% asset_img 16.png %}
   2. 若 \\((\widehat{\vec{n_1},\vec{n_2}})\in(\frac{\pi}{2},\pi]\\) , 则平面夹角 \\(\theta=\pi-(\widehat{\vec{n_1},\vec{n_2}})\\)
      有 \\(\cos\theta=\cos(\pi-(\widehat{\vec{n_1},\vec{n_2}}))=-\cos(\widehat{\vec{n_1},\vec{n_2}})=-\frac{\vec{n_1}\cdot\vec{n_2}}{|\vec{n_1}|\cdot|\vec{n_2}|}\\)

      {% asset_img 17.png %}
   
   平面夹脚应是锐角, 因此综合 1、2 得: \\(\cos\theta=|\frac{\vec{n_1}\vec{n_2}}{|\vec{n_1}|\cdot|\vec{n_2}|}|\\)

### 空间曲线及方程

1. 空间曲线的形式
   1. 一般形式
      
      {% asset_img 18.png %}
      (两个空间曲面的交点集合是一条空间曲线)
      \\(L:\begin{cases} F(x,y,z)=0 \\\ G(x,y,z)=0 \end{cases}\\)
   2. 参数式
      \\(L:\begin{cases} x=\varphi(t) \\\ y=\psi(t) \\\ z=\omega(t) \end{cases}\\)
      如:
      \\(L:\begin{cases} x^2+y^2=1 \\\ x+y-z-2=0 \end{cases}\rArr\\) 化为参数式 \\(L:\begin{cases} x=\cos t \\\ y=\sin t \\\ z=\sin t+\cos t-2 \end{cases}\\)

      {% asset_img 19.png %}
2. 空间直线(空间曲线的特殊情形)
   1. 点向式(对称式)方程: \\(L:\frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}\\)
         
      {% asset_img 20.png %}
      设 \\(M_0(x_0,y_0,z_0)\in L\\) , \\(\vec{S}=\\{m,n,p\\}\parallel L\\)
      \\(\forall M(x,y,z)\in L\\), 有 \\(\overrightarrow{M_0M}=\\{x-x_0,y-y_0,z-z_0\\}\\) 且 \\(\overrightarrow{M_0M}\parallel\vec{S}\\)
      \\(\because\overrightarrow{M_0M}\parallel\vec{S}\hArr\frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}\\)
      \\(\therefore L:\frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}\\)
   2. 参数式方程: 若 \\(\frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}=t\\) 则 \\(L:\begin{cases} x=mt+x_0 \\\ y=nt+y_0 \\\ z=pt+z_0 \end{cases}\\)
   3. 一般式
      \\(L:\begin{cases} A_1x+B_1y+C_1z+D_1=0 \\\ A_2x+B_2y+C_2z+D_2=0 \end{cases}\\)
      
      {% asset_img 21.png %}
      (两平面相交得到一条直线)
3. 投影曲线
   
   {% asset_img 22.png %}
   设 \\(L:\begin{cases} F(x,y,z)=0 \\\ G(x,y,z)=0 \end{cases}\\)
   曲线 \\(L\\) 向 \\(xOy\\) 面铅直投影得到投影曲线 \\(L_0\\)
   由 \\(\begin{cases} F(x,y,z)=0 \\\ G(x,y,z)=0 \end{cases}\xRightarrow{\text{消}\large z}H(x,y)=0\\)
   得到 \\(L_0:\begin{cases} H(x,y)=0 \\\ z=0 \end{cases}\\)

### 杂知识点

1. 夹角
   1. 两向量的夹角:
      设向量 \\(\vec{a}=\\{a_1,b_1,c_1\\}\\) , \\(\vec{b}=\\{a_2,b_2,c_2\\}\\) , \\((\widehat{\vec{a},\vec{b}})=\theta \enspace\\) (\\(0\leqslant\theta\leqslant\pi\\))
      由 \\(\vec{a}\cdot\vec{b}=|\vec{a}|\cdot|\vec{b}|\cdot\cos\theta\\)
      得 \\(\cos\theta=\frac{\vec{a}\cdot\vec{b}}{|\vec{a}||\vec{b}|}=\frac{a_1a_2+b_1b_2+c_1c_2}{\sqrt{a_1^2+b_1^2+c_1^2}\sqrt{a_2^2+b_2^2+c_2^2}}\\)
   2. 两平面夹角:
      
      {% asset_img 23.png %}
      \\(\pi_1:A_1x+B_1y+C_1z+D_1=0\\)
      \\(\pi_2:A_2x+B_2y+C_2z+D_2=0\\)
      设 \\(\pi_1\\) , \\(\pi_2\\) 夹角为 \\(\theta\\)
      1. \\((\widehat{\vec{n_1},\vec{n_2}})\in[0,\frac{\pi}{2}]\\) 时 \\(\theta=(\widehat{\vec{n_1},\vec{n_2}})\\)
      2. \\((\widehat{\vec{n_1},\vec{n_2}})\in(\frac{\pi}{2},\pi]\\) 时 \\(\theta=\pi-(\widehat{\vec{n_1},\vec{n_2}})\\)
      
      综合得 \\(\cos\theta=|\cos(\widehat{\vec{n_1},\vec{n_2}})|=\frac{|\vec{n_1}\cdot\vec{n_2}|}{|\vec{n_1}||\vec{n_2}|}=\frac{|A_1A_2+B_1B_2+C_1C_2|}{\sqrt{A_1^2+B_1^2+C_1^2}\sqrt{A_2^2+B_2^2+C_2^2}}\\)
   3. 两直线夹角:
      
      {% asset_img 24.png %}
      \\(L_1:\frac{x-x_1}{m_1}=\frac{y-y_1}{n_1}=\frac{z-z_1}{p_1}\\)
      \\(L_2:\frac{x-x_2}{m_2}=\frac{y-y_2}{n_2}=\frac{z-z_1}{p_2}\\)
      设 \\(L_1\\) , \\(L_2\\) 夹脚为 \\(\theta\enspace\\) (\\(0\leqslant\theta\leqslant\frac{\pi}{2}\\))
      1. \\((\widehat{\vec{s_1},\vec{s_2}})\in[0,\frac{\pi}{2}]\\) , 则 \\(\theta=(\widehat{\vec{s_1},\vec{s_2}})\\)
      2. \\((\widehat{\vec{s_1},\vec{s_2}})\in(\frac{\pi}{2},\pi]\\) , 则 \\(\theta=\pi-(\widehat{\vec{s_1},\vec{s_2}})\\)
      
      综合得 \\(\cos\theta=|\cos(\widehat{\vec{s_1},\vec{s_2}})|=\frac{|\vec{s_1}\cdot\vec{s_2}|}{|\vec{s_1}||\vec{s_2}|}=\frac{|m_1m_2+n_1n_2+p_1p_2|}{\sqrt{m_1^2+n_1^2+p_1^2}\sqrt{m_2^2+n_2^2+p_2^2}}\\)
   4. 直线与平面夹角:
      
      {% asset_img 25.png %}
      \\(L:\frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}\\) , \\(\vec{s}=\\{m,n,p\\}\parallel L\\)
      \\(\pi:Ax+By+Cz+D=0\\) , \\(\vec{n}=\\{A,B,C\\}\\)
      1. 若 \\((\widehat{\vec{n},\vec{s}})\in[0,\frac{\pi}{2}]\\)
         则 \\(\varphi+(\widehat{\vec{n},\vec{s}})=\frac{\pi}{2}\rArr\varphi=\frac{\pi}{2}-(\widehat{\vec{n},\vec{s}})\\)
         \\(\therefore\sin\varphi=\cos(\widehat{\vec{n},\vec{s}})\\)

         {% asset_img 26.png %}
      2. 若 \\((\widehat{\vec{n},\vec{s}})\in(\frac{\pi}{2},\pi]\\)
         则 \\((\widehat{\vec{n},\vec{s}})=\frac{\pi}{2}+\varphi\rArr\varphi=-(\frac{\pi}{2}-(\widehat{\vec{n},\vec{s}}))\\)
         \\(\therefore\sin\varphi=-\cos(\widehat{\vec{n},\vec{s}})\\)

         {% asset_img 27.png %}
      
      综合 1、2 得 \\(\sin\varphi=|\cos(\vec{n},\vec{s})|=\frac{|\vec{n}\cdot\vec{s}|}{|\vec{n}|\cdot|\vec{s}|}\\)
2. 距离
   1. 两点距离:
      设 \\(A(x_1,y_1,z_1)\\) , \\(B(x_2,y_2,z_2)\\)
      则 \\(AB\\) 距离 \\(d=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2+(z_2+z_1)^2}\\)
   2. 点到平面距离
      
      {% asset_img 28.png %}
      设 \\(\pi:Ax+By+Cz+D=0\\) , \\(M_0(x_0,y_0,z_0)\notin\pi\\) , \\(\forall M_1(x_1, y_1, z_1)\in\pi\\)
      有 \\(\overrightarrow{M_0M_1}=\\{x_1-x_0, y_1-y_0, z_1-z_0\\}\\)
      <div>
      $$
      \begin{aligned}
       Prj_{\vec{n}}\overrightarrow{M_0M_1}=\frac{\vec{n}\cdot\overrightarrow{M_0M_1}}{|\vec{n}|} & =\frac{A(x_1-x_0)+B(y_1-y_0)+C(z_1-z_0)}{\sqrt{A^2+B^2+C^2}} \\
       & =\frac{(Ax_1+By_1+Cz_1)-(Ax_0+By_0+Cz_0)}{\sqrt{A^2+B^2+C^2}}
      \end{aligned}
      $$
      </div>

      将 \\(M_1\\) 代入平面 \\(\pi\\) 得 \\(Ax_1+By_1+Cz_1=-D\\)
      \\(\therefore Prj_{\vec{n}}\overrightarrow{M_0M_1}=-\frac{Ax_0+By_0+Cz_0+D}{\sqrt{A^2+B^2+C^2}}\\)
      \\(\therefore d=|Prj_{\vec{n}}\overrightarrow{M_0M_1}|=\frac{|Ax_0+By_0+Cz_0+D|}{\sqrt{A^2+B^2+C^2}}\\)
3. 平面束
   \\(L\\) 为直线, 经过 \\(L\\) 的所有平面称为平面束
   设 \\(L:\begin{cases} A_1x+B_1y+C_1z+D_1=0 \\\ A_2x+B_2y+C_2z+D_2=0 \end{cases}\\)
   过 \\(L\\) 的平面束为 \\(\pi:A_1x+B_1y+C_1z+D_1+\lambda(A_2x+B_2y+C_2z+D_2)=0\\)
   \\(\hArr\pi:(A_1+A_2\lambda)x+(B_1+B_2\lambda)y+(C_1+C_2\lambda)z+(D_1+D_2\lambda)=0\\)
   例: 求直线 \\(\begin{cases} x+y-z-1=0 \\\ x-y+z+1=0 \end{cases}\\) 在平面 \\(x+y+z=0\\) 上的投影直线
   解:

   {% asset_img 29.png %}
   1. 过直线 \\(L\\) 的平面束为
      \\(\pi:x+y-z-1+\lambda(x-y+z+1)=0\\)
      即 \\(\pi:(\lambda+1)x+(1-\lambda)y+(\lambda-1)z+\lambda-1=0\\)
   2. 在平面束 \\(\pi\\) 中找一个平面 \\(\pi_0\\) , 使其与平面 \\(x+y+z=0\\) 垂直, \\(\pi_0\\) 与 \\(x+y+z=0\\) 相交的直线即为 \\(L\\) 的投影直线
      \\(\\{(\lambda+1),(1-\lambda),(\lambda-1)\\}\cdot\\{1,1,1\\}=0\rArr \lambda=-1\\)
      投影直线 \\(L_0:\begin{cases} 2y-2z-2=0 \\\ x+y+z=0 \end{cases}\\)

## 多元函数微分学及应用

### 多元函数的基本概念

1. 平面点集
   1. 邻域: 设 \\(M_0(x_0, y_0)\in D\\) , \\(\delta>0\\)
      * 称 \\(\\{(x, y)|\sqrt{(x-x_0)^2+(y-y_0)^2}<\delta\\}\\) 为 \\(M_0\\) 的 \\(\delta\\) 邻域, 记 \\(\bigcup(M_0, \delta)\\)
        
        {% asset_img 30.png %}
      * 称 \\(\\{(x, y)|0<\sqrt{(x-x_0)^2+(y-y_0)^2}<\delta\\}\\) 为 \\(M_0\\) 的去心 \\(\delta\\) 邻域, 记 \\(\mathring{\bigcup}(M_0, \delta)\\)
        
        {% asset_img 31.png %}
   2. 开集: 设 \\(D\\) 为 \\(xOy\\) 面上的点集,
      若 \\(\forall M_0(x_0,y_0)\in D\\) , \\(\exist\delta>0\\) 使 \\(\bigcup(M_0,\delta)\subset D\\) , 称 \\(D\\) 为开集
   3. 区域: 连通的开集称为区域(开区域)
   4. 闭区域: 开区域连同边界称为闭区域
2. 多元函数的概念(空间中的一个曲面)
   设 \\(D\\) 为区域, \\(x,y,z\\) 为变量,
   若 \\(\forall(x,y)\in D\\) , \\(\exist z\\) 与 \\((x,y)\\) 对应, 称 \\(z\\) 为 \\((x,y)\\) 的函数, 记 \\(z=f(x,y)\\)
   \\(D\\) 为定义域, 值域 \\(R=\\{z|z=f(x,y),(x,y)\in D\\}\\)
3. 多元函数的极限
   回顾一元函数极限定义:
   设 \\(y=f(x)\enspace\\) (\\(x\in D\\))
   若 \\(\forall\varepsilon>0\\) , \\(\exist\delta>0\\) , 当 \\(0<|x-x_0|<\delta\\) 时, 有 \\(|f(x)-A|<\varepsilon\\)
   称 \\(A\\) 为 \\(f(x)\\) 当 \\(x\to x_0\\) 的极限, 记 \\(\lim\limits_{x\to x_0}f(x)=A\\)
   二元函数极限定义:
   设 \\(z=f(x,y)\enspace\\) (\\((x,y)\in D\\)) , \\(M_0(x_0,y_0)\in D\\)
   若 \\(\forall\varepsilon>0\\) , \\(\exist\delta>0\\) , 当 \\(0<\sqrt{(x-x_0)^2-(y-y_0)^2}<\delta\\) 时, 有 \\(|f(x, y)-A|<\varepsilon\\)
   称 \\(A\\) 为 \\(f(x,y)\\) 当 \\((x,y)\to(x_0,y_0)\\) 的极限, 记 \\(\lim\limits_{\substack{x\to x_0 \\\ y\to y_0}}f(x,y)=A\\)
4. 多元函数连续性与性质
   设 \\(z=f(x,y)\enspace\\) (\\((x,y)\in D\\)) , \\(M_0(x_0,y_0)\in D\\)
   若 \\(\lim\limits_{\substack{x\to x_0 \\\ y\to y_0}}f(x,y)=f(x_0,y_0)\\) , 称 \\(f(x,y)\\) 在 \\((x_0,y_0)\\) 处连续
5. 多元函数在有界闭区域上的性质
   1. 最值定理
      设 \\(D\\) 为有界闭区域, \\(f(x,y)\\) 在 \\(D\\) 上连续
      则 \\(f(x,y)\\) 在 \\(D\\) 上取到最小值 \\(m\\) 和最大值 \\(M\\)
   2. 有界定理
      设 \\(D\\) 为有界闭区域, \\(f(x,y)\\) 在 \\(D\\) 上连续
      则 \\(\exist k>0,\forall(x,y)\in D\\) , 有 \\(|f(x,y)|\leqslant k\\)
   3. 介值定理
      设 \\(D\\) 为有界闭区域, \\(f(x,y)\\) 在 \\(D\\) 上连续
      则 \\(\forall\delta\in[m,M]\\) , \\(\exist(\xi,\eta)\in D\\) 使 \\(f(\xi,\eta)=\delta\\)

### 偏导数

1. 定义
   设 \\(z=f(x,y)\enspace\\) (\\((x,y)\in D)\\) , \\(M_0(x_0,y_0)\in D\\)
   1. 偏增量
      * \\(f(x,y)\\) 在 \\(M_0\\) 处关于 \\(x\\) 的偏增量: \\(\Delta z_x=f(x_0+\Delta x,y_0)-f(x_0,y_0)=f(x,y_0)-f(x_0,y_0)\\)
      * \\(f(x,y)\\) 在 \\(M_0\\) 处关于 \\(y\\) 的偏增量: \\(\Delta z_y=f(x_0, y_0+\Delta y)-f(x_0, y_0)=f(x_0,y)-f(x_0,y_0)\\)
      * \\(f(x,y)\\) 在 \\(M_0\\) 处的全增量: \\(\Delta z=f(x_0+\Delta x,y_0+\Delta y)-f(x_0,y_0)=f(x,y)-f(x_0,y_0)\\)
   2. 偏导数
      * 若 \\(\lim\limits_{\Delta x\to 0}\frac{\Delta z_x}{\Delta x}\\) 存在, 称 \\(f(x,y)\\) 在 \\(M_0\\) 处关于 \\(x\\) 可偏导,
        该极限称为 \\(f(x,y)\\) 在 \\(M_0\\) 处关于 \\(x\\) 的偏导数, 记 \\(f_x^\prime(x_0,y_0)\\) 或 \\(\frac{\partial z}{\partial x}|_{(x_0,y_0)}\\)
      * 若 \\(\lim\limits_{\Delta y\to 0}\frac{\Delta z_y}{\Delta y}\\) 存在, 称 \\(f(x,y)\\) 在 \\(M_0\\) 处关于 \\(y\\) 可偏导,
        该极限称为 \\(f(x,y)\\) 在 \\(M_0\\) 处关于 \\(y\\) 的偏导数, 记 \\(f_y^\prime(x_0,y_0)\\) 或 \\(\frac{\partial z}{\partial y}|_{(x_0,y_0)}\\)
      * 若 \\(\forall(x,y)\in D\\) , \\(f(x,y)\\) 对 \\(x\\)、\\(y\\) 皆可偏导, 称 \\(f_x^\prime(x,y)\\)、\\(f_y^\prime(x,y)\\) 为 \\(f(x,y)\\) 对 \\(x\\)、\\(y\\) 的偏导数
2. 高阶偏导数
   设 \\(z=f(x,y)\\) 在 \\(D\\) 内对 \\(x\\)、\\(y\\) 可偏导,
   \\(f_x^\prime(x,y)=\frac{\partial z}{\partial x}\\) 为 \\(f(x,y)\\) 对 \\(x\\) 偏导数,
   \\(f_y^\prime(x,y)=\frac{\partial z}{\partial y}\\) 为 \\(f(x,y)\\) 对 \\(y\\) 偏导数.
   1. 若 \\(f_x^\prime(x,y)\\) 对 \\(x\\) 可偏导, 其对 \\(x\\) 的偏导数称为 \\(f(x,y)\\) 对 \\(x\\) 的二阶偏导数, 记 \\(f_{xx}^{\prime\prime}\\) 或 \\(\frac{\partial^2z}{\partial x^2}\\)
      若 \\(f_y^\prime(x,y)\\) 对 \\(y\\) 可偏导, 其对 \\(y\\) 的偏导数称为 \\(f(x,y)\\) 对 \\(y\\) 的二阶偏导数, 记 \\(f_{yy}^{\prime\prime}\\) 或 \\(\frac{\partial^2z}{\partial y^2}\\)
   2. 若 \\(f_x^\prime(x,y)\\) 对 \\(y\\) 可偏导, 其对 \\(y\\) 的偏导数称为 \\(f(x,y)\\) 对 \\(x\\)、\\(y\\) 的二阶混合偏导数, 记 \\(f_{xy}^{\prime\prime}(x,y)\\) 或 \\(\frac{\partial^2z}{\partial x\partial y}\\)
      若 \\(f_y^\prime(x,y)\\) 对 \\(x\\) 可偏导, 其对 \\(x\\) 的偏导数称为 \\(f(x,y)\\) 对 \\(y\\)、\\(x\\) 的二阶混合偏导数, 记 \\(f_{yx}^{\prime\prime}(x,y)\\) 或 \\(\frac{\partial^2z}{\partial y\partial x}\\)
   
   * 定理:
     若 \\(z=f(x,y)\\) 的二阶混合偏导数 \\(\frac{\partial^2z}{\partial x\partial y}\\)、\\(\frac{\partial^2z}{\partial y\partial x}\\) 皆连续,
     则 \\(\frac{\partial^2z}{\partial x\partial y}=\frac{\partial^2z}{\partial y\partial x}\\) , 即 \\(f_{xy}^{\prime\prime}=f_{yx}^{\prime\prime}\\)

### 全微分

1. 二元函数全微分定义
   设 \\(z=f(x,y)\enspace\\) (\\((x,y)\in D\\)) , \\(M_0(x_0,y_0)\in D\\) ,
   全增量 \\(\Delta z=f(x_0+\Delta x,y_0+\Delta y)-f(x_0,y_0)=f(x,y)-f(x_0,y_0)\\)
   若 \\(\Delta z=A\Delta x+B\Delta y+\circ(\rho)\\) , \\(\rho=\sqrt{(\Delta x)^2+(\Delta y)^2}\\)
   称 \\(f(x,y)\\) 在 \\((x_0,y_0)\\) 处可全微, \\(A\Delta x+B\Delta y\\) 为 \\(f(x,y)\\) 在 \\((x_0,y_0)\\) 处的全微分, 记 \\(\mathrm{d}z|_{(x_0,y_0)}=A\mathrm{d}x+B\mathrm{d}y\\)

   全微分: \\(\mathrm{d}z|_{(x_0,y_0)}=f_x^\prime(x_0,y_0)\mathrm{d}x+f_y^\prime(x_0,y_0)\mathrm{d}y=\frac{\partial z}{\partial x}\mathrm{d}x+\frac{\partial z}{\partial y}\mathrm{d}y\\)
2. 性质
   设 \\(z=f(x,y)\enspace\\) (\\((x, y)\in D\\)) , \\(M_0(x_0,y_0)\in D\\)
   1. 若 \\(f(x,y)\\) 在 \\(M_0\\) 处可微, 则 \\(f(x,y)\\) 在 \\(M_0\\) 连续且可偏导, 反之不对
   2. 可微充分条件: 若 \\(z=f(x,y)\\) 连续可偏导, 则 \\(f(x,y)\\) 可微
   
   例: \\(z=f(x,y)=|x|+|y|\\) 在 \\((0,0)\\) 连续, 证 \\(f(x,y)\\) 在 \\((0,0)\\) 不可微
   证: \\(\lim\limits_{x\to 0}\frac{f(x,0)-f(0,0)}{x}=\lim\limits_{x\to 0}\frac{|x|}{x}\\) 不存在 \\(\rArr f(x,y)\\) 在 \\((0,0)\\) 对 \\(x\\) 不可偏导.
   同理 \\(f(x,y)\\) 在 \\((0,0)\\) 不可偏导
   \\(\therefore f(x,y)\\) 在 \\((0,0)\\) 不可微

### 多元复合函数求导法则

* 情形一: \\(z=f(u,v)\\) , \\(\begin{cases} u=\varphi(t) \\\ v=\psi(t) \end{cases}\rArr z=f[\varphi(t),\psi(t)]\\)
  若 \\(z=f(u,v)\\) 关于 \\(u\\)、\\(v\\) 连续可偏导, \\(\varphi(t)\\) , \\(\psi(t)\\) 可导, 则 \\(z=f[\varphi(t),\psi(t)]\\) 可导,
  且 \\(\frac{\mathrm{d}z}{\mathrm{d}t}=\frac{\partial f}{\partial u}\cdot\frac{\mathrm{d}u}{\mathrm{d}t}+\frac{\partial f}{\partial v}\cdot\frac{\mathrm{d}v}{\mathrm{d}t}=f_{u}^\prime\cdot\varphi(t)^\prime+f_{v}^\prime\cdot\psi^\prime(t)\\)
  * 证明:
    (\\(\Delta u=\varphi(t+\Delta t)-\varphi(t)\\) , \\(\Delta v=\psi(t+\Delta t)-\psi(t)\\))
    \\(\because z=f(u,v)\\) 关于 \\(u\\)、\\(v\\) 连续可偏导
    \\(\therefore z=f(u,v)\\) 可微
    \\(\therefore\Delta z=\frac{\partial f}{\partial u}\Delta u+\frac{\partial f}{\partial v}\Delta v+\circ(\rho)\\) , \\(\rho=\sqrt{(\Delta u)^2+(\Delta v)^2}\\)
    \\(\rArr\frac{\Delta z}{\Delta t}=\frac{\partial f}{\partial u}\frac{\Delta u}{\Delta t}+\frac{\partial f}{\partial v}\frac{\Delta v}{\Delta t}+\frac{\circ(\rho)}{\Delta t}\\)
    \\(\rArr\frac{dz}{dt}=\frac{\partial f}{\partial u}\cdot\frac{du}{dt}+\frac{\partial f}{\partial v}\cdot\frac{dv}{dt}=f_{u}^\prime\cdot\varphi(t)^\prime+f_{v}^\prime\cdot\psi^\prime(t)\\)
* 情形二: \\(z=f(u,v)\\) , \\(\begin{cases} u=\varphi(x,y) \\\ v=\psi(x,y) \end{cases}\rArr z=f[\varphi(x,y),\psi(x,y)]\\)
  \\(z=f(u,v)\\) 关于 \\(u\\)、\\(v\\) 连续可偏导, \\(\begin{cases} u=\varphi(x,y) \\\ v=\psi(x,y) \end{cases}\\) 对 \\((x,y)\\) 可偏导
  则 \\(z=f[\varphi(x,y),\psi(x,y)]\\) 关于 \\(x\\)、\\(y\\) 可偏导,
  且
  \\(\frac{\partial z}{\partial x}=\frac{\partial f}{\partial u}\cdot\frac{\partial u}{\partial x}+\frac{\partial f}{\partial v}\cdot\frac{\partial v}{\partial x}\\)
  \\(\frac{\partial z}{\partial y}=\frac{\partial f}{\partial u}\cdot\frac{\partial u}{\partial y}+\frac{\partial f}{\partial v}\cdot\frac{\partial v}{\partial y}\\)

### 隐函数求导法则

1. 一个约束条件的情形
   隐函数显式化: \\(f(x,y)=0\rArr y=\varphi(x)\\)
   * 定理一:
     设 \\(F(x,y)\\) 在点 \\(M_0(x_0,y_0)\\) 邻域内连续可偏导且 \\(F(x_0,y_0)=0\\) ,
     若 \\(F_y^\prime(x_0,y_0)\neq 0\enspace\\)
     则由 \\(F(x,y)=0\\) 在 \\(M_0\\) 邻域内确定唯一连续可导函数 \\(y=f(x)\\) 使 \\(y_0=f(x_0)\\) (隐函数显式化),
     则 \\(\dfrac{\mathrm{d}y}{\mathrm{d}x}=-\dfrac{F_x^\prime}{F_y^\prime}\\)
     证明:
     \\(F(x,y)=0\\) , 把 \\(y\\) 看成 \\(x\\) 的函数 \\(f(x)\\) , 则 \\(F(x,f(x))=0\\)
     两边对 \\(x\\) 求导, \\(F_x^\prime+F_y^\prime f^\prime(x)=F_x^\prime+F_y^\prime\frac{\mathrm{d}y}{\mathrm{d}x}=0\rArr\frac{\mathrm{d}y}{\mathrm{d}x}=-\frac{F_x^\prime}{F_y^\prime}\\)
   * 定理二:
      设 \\(F(x,y,z)\\) 在 \\(M_0(x_0,y_0,z_0)\\) 邻域内连续可偏导且 \\(F(x_0,y_0,z_0)=0\\)
      若 \\(F_z^\prime(x_0,y_0,z_0)\neq 0\enspace\\)
      则由 \\(F(x,y,z)=0\\) 在 \\(M_0\\) 邻域内确定唯一连续可偏导函数 \\(z=\varphi(x,y)\\) 使 \\(z_0=\varphi(x_0,y_0)\\) ,
      则 \\(\dfrac{\partial z}{\partial x}=-\dfrac{F_x^\prime}{F_z^\prime}\\) , \\(\dfrac{\partial z}{\partial y}=-\dfrac{F_y^\prime}{F_z^\prime}\\)
      证明:
      \\(F(x,y,z)=0\rArr z=\varphi(x,y)\\)
      两边对 \\(x\\) 求偏导, \\(F_x^\prime+F_z^\prime\frac{\partial z}{\partial x}=0\rArr\frac{\partial z}{\partial x}=-\frac{F_x^\prime}{F_z^\prime}\\)
      两边对 \\(y\\) 求偏导, \\(F_y^\prime+F_z^\prime\frac{\partial z}{\partial y}=0\rArr\frac{\partial z}{\partial y}=-\frac{F_y^\prime}{F_z^\prime}\\)

### 多元函数微分学的几何应用

1. 空间曲线(求曲线切线和法平面)
   
   {% asset_img 32.png %}
   设 \\(M_0(x_0,y_0,z_0)\in L\\) , \\(M(x_0+\Delta x,y_0+\Delta y,z_0+\Delta z)\in L\\)
   \\(\overrightarrow{M_0M}=\\{\Delta x,\Delta y,\Delta z\\}\\)
   直线 \\(\overline{M_0M}:\frac{x-x_0}{\Delta x}=\frac{y-y_0}{\Delta y}=\frac{z-z_0}{\Delta z}\\)
   * 情况一 \\(L:\begin{cases} x=\varphi(t) \\\ y=\psi(t) \\\ z=\omega(t) \end{cases}\\) , \\(M_0(x_0,y_0,z_0)\hArr t=t_0\\) , \\(M(x_0+\Delta x,y_0+\Delta y,z_0+\Delta z)\hArr t=t_0+\Delta t\\)
     \\(\overline{M_0M}=\frac{x-x_0}{\Delta x}=\frac{y-y_0}{\Delta y}=\frac{z-z_0}{\Delta z}\hArr\frac{x-x_0}{\frac{\Delta x}{\Delta t}}=\frac{y-y_0}{\frac{\Delta y}{\Delta t}}=\frac{z-z_0}{\frac{\Delta z}{\Delta t}}\\)
     当 \\(\Delta t\to 0\\) 时, \\(\overline{M_0M}\\) 即为切线
     \\(\therefore\\) 切线: \\(\frac{x-x_0}{\varphi^\prime(t_0)}=\frac{y-y_0}{\psi^\prime(t_0)}=\frac{z-z_0}{\omega^\prime(t_0)}\\) ,
     曲线方向向量 \\(\vec{T}=\\{\varphi^\prime,\psi^\prime,\omega^\prime\\}\\) ,
     法平面 \\(\varphi^\prime(x-x_0)+\psi^\prime(y-y_0)+\omega^\prime(z-z_0)=0\\)
   * 情况二 \\(L:\begin{cases} F(x,y,z)=0 \\\ G(x,y,z)=0 \end{cases}\\) , \\(M_0(x_0,y_0,z_0)\in L\\)
     曲线方向向量 \\(\vec{T}=\\{\begin{vmatrix} F_y^\prime & F_z^\prime \\\ G_y^\prime & G_z^\prime \end{vmatrix},\begin{vmatrix} F_z^\prime & F_x^\prime \\\ G_z^\prime & G_x^\prime \end{vmatrix},\begin{vmatrix} F_x^\prime & F_y^\prime \\\ G_x^\prime & G_y^\prime \end{vmatrix}\\}\\)
     将曲线方向向量代入切线和法平面方程即可(方程参考情况一)
2. 空间曲面(求曲面切平面和法线)
   求空间曲面上某一点的法向量:
   设曲面 \\(\Sigma:F(x,y,z)=0\\) , \\(M_0(x_0,y_0,z_0)\in\Sigma\\)
   在 \\(\Sigma\\) 内过 \\(M_0\\) 任取一曲线 \\(L:\begin{cases} x=\varphi(t) \\\ y=\psi(t) \\\ z=\omega(t) \end{cases}\\) , \\(M_0\hArr t=t_0\\)
   \\(\because L\subset\Sigma\\)
   \\(\therefore F[\varphi(t),\psi(t),\omega(t)]=0\\)
   两边对 \\(t\\) 求导:
   \\(F_x^\prime[\varphi(t),\psi(t),\omega(t)]\cdot\varphi^\prime(t)+F_y^\prime[\varphi(t),\psi(t),\omega(t)]\psi^\prime(t)+F_z^\prime[\varphi(t),\psi(t),\omega(t)]\omega^\prime(t)=0\enspace\\) (多元复合函数求导情形一)
   将 \\(t=t_0\\) 代入:
   \\(F_x^\prime(x_0,y_0,z_0)\varphi^\prime(t_0)+F_y^\prime(x_0,y_0,z_0)\psi^\prime(t_0)+F_z^\prime(x_0,y_0,z_0)\omega^\prime(t_0)=0\\)
   可拆为两个向量点乘: \\(\\{F_x^\prime,F_y^\prime,F_z^\prime\\}_{M_0}\cdot\\{\varphi^\prime(t_0),\psi^\prime(t_0),\omega^\prime(t_0)\\}=0\\)
   则法向量 \\(\vec{n}=\\{F\_x^\prime,F\_y^\prime,F\_z^\prime\\}\_{M\_0}\\) (后者是曲线在点 \\(M_0\\) 的方向向量, 那么与之垂直的前者就是法向量了)

### 方向导数与梯度

1. 方向导数
   1. 定义
      * 二元函数
         
        {% asset_img 33.png %}
        {% asset_img 34.png %}
        设 \\(z=f(x,y)\enspace\\) (\\((x,y)\in D\\)) , \\(M_0(x_0,y_0)\in D\\)
        在 \\(xOy\\) 面内过 \\(M_0\\) 作射线 \\(L\\) ,
        取 \\(M(x_0+\Delta x,y_0+\Delta y)\in L\\) , \\(\rho=\sqrt{(\Delta x)^2+(\Delta y)^2}\\)
        \\(\Delta z=f(x_0+\Delta x,y_0+\Delta y)-f(x_0,y_0)\\)
        若 \\(\lim\limits_{\rho\to 0}\frac{\Delta z}{\rho}\\) 存在, 称此极限为函数 \\(z=f(x,y)\\) 在 \\(M_0\\) 处沿射线 \\(L\\) 的方向导数, 记 \\(\frac{\partial z}{\partial L}|_{M_0}\\)
      * 三元函数
        设 \\(u=f(x,y,z)\enspace\\) (\\((x,y,z)\in\Omega\\)) , \\(M_0(x_0,y_0,z_0)\in\Omega\\)
        过 \\(M_0\\) 作射线 \\(L\\),
        取 \\(M(x_0+\Delta x,y_0+\Delta y,z_0+\Delta z)\in L\\) , \\(\rho=\sqrt{(\Delta x)^2+(\Delta y)^2+(\Delta z)^2}\\)
        \\(\Delta u=f(x_0+\Delta x,y_0+\Delta y,z_0+\Delta z)-f(x_0,y_0,z_0)\\)
        若 \\(\lim\limits_{\rho\to 0}\frac{\Delta u}{p}\\) 存在, 称此极限为 \\(u=f(x,y,z)\\) 在 \\(M_0\\) 处沿射线 \\(L\\) 的方向导数, 记 \\(\frac{\partial u}{\partial L}|_{M_0}\\)
   2. 方向导数计算方法
      * 二元函数
        \\(z=f(x,y)\\) 在 \\(M_0(x_0,y_0)\\) 可微,
         
        {% asset_img 35.png %}
        在 \\(xOy\\) 面内过 \\(M_0\\) 作射线 \\(L\\) , 方向角为 \\(\alpha\\)、\\(\beta\\) ,
        则 \\(\frac{\partial z}{\partial L}|_{M_0}=f_x^\prime(x_0,y_0)\cdot\cos\alpha+f_y^\prime(x_0,y_0)\cos\beta\\)
      * 三元函数
        \\(u=f(x, y, z)\\) 在 \\(M_0(x_0, y_0, z_0)\\) 可微,
        过 \\(M_0\\) 作射线 \\(L\\) , 方向角为 \\(\alpha\\)、\\(\beta\\)、\\(\gamma\\) ,
        则 \\(\frac{\partial u}{\partial L}|\_{M\_0}=\frac{\partial u}{\partial x}|\_{M\_0}\cos\alpha+\frac{\partial u}{\partial y}|\_{M\_0}\cos\beta+\frac{\partial u}{\partial z}|\_{M\_0}\cos\gamma\\)
2. 梯度
   \\(u=f(x,y,z)\\) , \\(M_0(x_0,y_0,z_0)\in\Omega\\) , 过 \\(M_0\\) 作射线 \\(L\\) , 方向角为 \\(\alpha\\)、\\(\beta\\)、\\(\gamma\\)
   则有方向导数 \\(\frac{\partial u}{\partial L}|\_{M\_0}=\frac{\partial u}{\partial x}|\_{M\_0}\cos\alpha+\frac{\partial u}{\partial y}|\_{M\_0}\cos\beta+\frac{\partial u}{\partial z}|\_{M\_0}\cos\gamma\\)
   上式可分离为两个向量点乘:
   \\(\frac{\partial u}{\partial L}|\_{M\_0}=\\{\frac{\partial u}{\partial x},\frac{\partial u}{\partial y},\frac{\partial u}{\partial z}\\}|\_{M\_0}\cdot\\{\cos\alpha,\cos\beta,\cos\gamma\\}\\)
   这两个向量中前者称作梯度, 即函数 \\(u\\) 的梯度: \\(\nabla u=\\{\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial u}{\partial z}\\}|\_{M\_0}\\)
   后者是与 \\(L\\) 同向的单位向量, 记 \\(\vec{e}=\\{\cos\alpha,\cos\beta,\cos\gamma\\}\\)
   则 \\(\frac{\partial u}{\partial L}|\_{M\_0}=\nabla u\cdot\vec{e}=\sqrt{(\frac{\partial u}{\partial x})^2+(\frac{\partial u}{\partial y})^2+(\frac{\partial u}{\partial z})^2}\cdot1\cdot\cos\theta\enspace\\) (\\(\theta\\) 为 \\(\nabla u\\) 与 \\(\vec{e}\\) 间的夹角)
   由该式可知当 \\(\cos\theta=1\\) , 即 \\(\theta=0\\) 时, 这个点的方向导数 \\(\frac{\partial u}{\partial L}|\_{M\_0}\\) 取最大值
   因此**梯度的方向即函数增大速度最快的方向, 或方向导数取最大值的方向**

### 代数应用--多元函数的极值

1. 定义:
   设\\(z=f(x,y)\enspace\\) (\\((x, y)\in D\\)) , \\(M_0(x_0,y_0)\in D\\)
   若 \\(\exist\delta>0\\) , \\(\forall (x,y)\in\mathring{\bigcup}(M_0,\delta)\\)
   * \\(f(x,y)>f(x_0,y_0)\\) , 称 \\((x_0,y_0)\\) 为极小点
   * \\(f(x,y)<f(x_0,y_0)\\) , 称 \\((x_0,y_0)\\) 为极大点
2. 无条件极值
   设 \\(z=f(x,y)\enspace\\) (\\((x, y)\in D\\)) , \\(D\\) 为开区域
   求 \\(z=f(x,y)\\) 在 \\(D\\) 内的极值称为无条件极值
   1. 通过令 \\(\begin{cases} \frac{\partial z}{\partial x}=0 \\\ \frac{\partial z}{\partial y}=0 \end{cases}\\) 求对应 \\(x\\)、\\(y\\) 值
   2. 判别法
      设 \\((x_0,y_0)\\) 为驻点, \\(A=f_{xx}^{\prime\prime}(x_0,y_0)\\) , \\(B=f_{xy}^{\prime\prime}(x_0,y_0)\\) , \\(C=f_{yy}^{\prime\prime}(x_0,y_0)\\)
      1. 若 \\(AC-B^2>0\rArr(x_0,y_0)\\) 为极值点
         \\(A<0\rArr(x_0,y_0)\\) 为极大点
         \\(A>0\rArr(x_0,y_0)\\) 为极小点
      2. 若 \\(AC-B^2<0\rArr(x_0,y_0)\\) 不是极值点
3. 条件极值
   * 二元函数: \\(z=f(x,y)\\) , 约束条件 \\(\varphi(x,y)=0\\)
     解法:
     设 \\(F=f(x,y)+\lambda\varphi(x,y)\\)
     令 \\(\begin{cases} F_x^\prime=\frac{\partial F}{\partial x}=f_x^\prime+\lambda\varphi_x^\prime=0 \\\ F_y^\prime=\frac{\partial F}{\partial y}=f_y^\prime+\lambda\varphi_y^\prime=0 \\\ F_\lambda^\prime=\frac{\partial F}{\partial\lambda}=\varphi(x,y)=0 \end{cases}\\)
      解方程组, 求出 \\(x\\)、\\(y\\) 值
      (之后的就不必多说了吧, 懂得都懂)
   * 三元函数(以及更多元): \\(u=f(x,y,z)\\) , 约束条件 \\(\begin{cases} \varphi(x,y,z)=0 \\\ \psi(x,y,z)=0 \end{cases}\\)
     解法:
     设 \\(F=f+\lambda\varphi+\mu\psi\\)
     令 \\(\begin{cases} F_x^\prime=0 \\\ F_y^\prime=0 \\\ F_z^\prime=0 \\\ F_\lambda^\prime=0 \\\ F_\mu^\prime=0 \end{cases}\\)
     解方程组, 求出 \\(x\\)、\\(y\\)、\\(z\\) 值

## 重积分

### 二重积分的概念与性质

1. 二重积分的定义
   设 \\(f(x,y)\\) 在 \\(xOy\\) 面有限闭区域 \\(D\\) 内有界
   1. \\(D\\) 可划分为 \\(\Delta\sigma_1,\Delta\sigma_2,\dots,\Delta\sigma_n\\)
   2. \\(\forall(\xi_i,\eta_i)\in\Delta\sigma_i\\)
      作 \\(\displaystyle\sum_{i=1}^n f(\xi_i,\eta_i)\Delta\sigma_i\enspace\\) (\\(\Delta\sigma_i\\) 可视为底面面积)
   3. \\(\lambda\\) 为 \\(\Delta\sigma_1,\Delta\sigma_2,\dots,\Delta\sigma_n\\) 中的最大值
      若 \\(\lim\limits_{\lambda\to 0}\displaystyle\sum_{i=1}^n f(\xi_i,\eta_i)\Delta\sigma_i\\) 存在, 称此极限为 \\(f(x,y)\\) 在 \\(D\\) 上的二重积分, 记 \\(\iint\limits_D f(x,y)\mathrm{d}\sigma\\)
      
      {% asset_img 36.png %}
2. 二重积分的性质
   1. 设 \\(f(x,y)\\)、\\(g(x,y)\\) 在区域 \\(D\\) 上可积, 则
      \\(\iint\limits_D[af(x,y)+bg(x,y)]\mathrm{d}\sigma=a\iint\limits_D f(x,y)\mathrm{d}\sigma+b\iint\limits_D g(x,y)\mathrm{d}\sigma\\)
   2. 若 \\(D=D_1+D_2\\) 且 \\(D_1\cap D_2=\varnothing\\) , 则
      \\(\iint\limits_D f(x,y)\mathrm{d}\sigma=\iint\limits_{D_1}f(x,y)\mathrm{d}\sigma+\iint\limits_{D_2}f(x,y)\mathrm{d}\sigma\\)
   3. \\(\iint\limits_D 1\mathrm{d}\sigma=A\\)
   4. 若 \\(f(x,y)\geqslant g(x,y)\enspace\\) (\\((x, y)\in D\\)) 则 \\(\iint\limits_D f(x,y)\mathrm{d}\sigma\geqslant\iint\limits_D g(x,y)\mathrm{d}\sigma\\)
   5. 若 \\(f(x,y)\\) 和 \\(|f(x,y)|\\) 在 \\(D\\) 上可积, 则 \\(|\iint\limits_D f(x,y)\mathrm{d}\sigma|\leqslant\iint\limits_D|f(x,y)|\mathrm{d}\sigma\\)
   6. 二重积分中值定理
      \\(D\\) 为有限闭区域, \\(f(x,y)\\) 在 \\(D\\) 上连续
      则 \\(\exist(\xi,\eta)\in D\\) , 使 \\(\iint\limits_D f(x,y)\mathrm{d}\sigma=f(\xi,\eta)A\enspace\\) (\\(A\\) 为区域 \\(D\\) 的面积)
      证明:
      \\(\because f(x,y)\in c(D)\\)
      \\(\therefore f(x,y)\\) 在 \\(D\\) 上有上下界 \\(m\\)、\\(M\\) , 使 \\(m\leqslant f(x,y)\leqslant M\\)
      \\(\therefore \iint\limits_D m\mathrm{d}\rho\leqslant\iint\limits_D f(x,y)\mathrm{d}\sigma\leqslant \iint\limits_D M\mathrm{d}\rho\\)
      \\(\rArr m\iint\limits_D 1\mathrm{d}\rho\leqslant\iint\limits_D f(x,y)\mathrm{d}\sigma\leqslant M\iint\limits_D 1\mathrm{d}\rho\\)
      \\(\rArr mA\leqslant\iint\limits_D f(x,y)\mathrm{d}\sigma\leqslant MA\\)
      \\(\rArr m\leqslant\frac{1}{A}\iint\limits_D f(x,y)\mathrm{d}\sigma\leqslant M\\)
      \\(\exist(\xi,\eta)\in D\\) , 使 \\(f(\xi,\eta)=\frac{1}{A}\iint\limits_D f(x,y)\mathrm{d}\sigma\rArr\iint\limits_D f(x,y)\mathrm{d}\sigma=f(\xi,\eta)A\\)

### 二重积分的计算法

1. 直角坐标法计算二重积分
   * 情况1 (沿着 \\(x\\) 轴扫 \\(y\\) 轴)
     \\(D=\\{(x,y)|a\leqslant x\leqslant b,\varphi_1(x)\leqslant y\leqslant \varphi_2(x)\\}\\)\
     则 \\(\iint\limits_D f(x,y)\mathrm{d}\sigma=\int_a^b[\int_{\varphi_1(x)}^{\varphi_2(x)}f(x,y)\mathrm{d}y]\mathrm{d}x\\)
     
     {% asset_img 37.png %}
   * 情况2 (沿着 \\(y\\) 轴扫 \\(x\\) 轴)
     \\(D=\\{(x,y)|c\leqslant y\leqslant d,\varphi_1(y)\leqslant x\leqslant\varphi_2(y)\\}\\)
     则 \\(\iint\limits_D f(x,y)\mathrm{d}\sigma=\int_c^d[\int_{\varphi_1(y)}^{\varphi_2(y)}f(x,y)\mathrm{d}x]\mathrm{d}y\\)

     {% asset_img 38.png %}
2. 极坐标法计算二重积分
   1. 特征:
      区域 \\(D\\) 的边界含 \\(x^2+y^2\\)
      \\(f(x,y)\\) 含 \\(x^2+y^2\\)
   2. 变换:
      
      {% asset_img 39.png %}
      \\(\begin{cases} x=r\cos\theta \\\ y=r\sin\theta \end{cases}\\) , \\(\alpha\leqslant\theta\leqslant\beta\\) , \\(r_1(\theta)\leqslant r\leqslant r_2(\theta)\\)
   3. \\(\mathrm{d}\sigma\\)
      取 \\([\theta,\theta+d\theta]\\)
      取 \\([r,r+dx]\\)
      则 \\(\mathrm{d}\sigma=\mathrm{d}r\cdot r\mathrm{d}\theta\\)

      {% asset_img 40.png %}
   
   \\(\therefore\iint\limits_D f(x,y)\mathrm{d}\sigma=\int_\alpha^\beta[\int_{r_1(\theta)}^{r_2(\theta)}r\cdot f(r\cos\theta, r\sin\theta)\mathrm{d}r]\mathrm{d}\theta\\)

### 三重积分

1. 三重积分的定义
   设 \\(\Omega\\) 为空间有限几何体, \\(f(x,y,z)\\) 在 \\(\Omega\\) 上有界
   将 \\(\Omega\\) 划分为 \\(\Delta V_1,\Delta V_2,\dots,\Delta V_n\\)
   \\(\forall(\xi_i,\eta_i,\zeta_i)\in\Delta V_i\\) , 作 \\(\displaystyle\sum_{i=1}^n f(\xi_i,\eta_i,\zeta_i)\Delta V_i\\)
   \\(\lambda\\) 为 \\(\Delta V_1,\Delta V_2,\dots,\Delta V_n\\) 直径最大值
   若 \\(\lim\limits_{\lambda\to 0}\displaystyle\sum_{i=1}^n f(\xi_i,n_i,\zeta_i)\Delta V_i\\) 存在, 称此极限为 \\(f(x,y,z)\\) 在 \\(\Omega\\) 上的三重积分, 记 \\(\iiint\limits_\Omega f(x,y,z)\mathrm{d}v\\)
   即 \\(\iiint\limits_\Omega f(x,y,z)\mathrm{d}v=\lim\limits_{\lambda\to 0}\displaystyle\sum_{i=1}^n f(\xi_1,\eta_i,\zeta_i)\Delta V_i\\)
   (三重积分的几何意义是空间几何体的质量)
2. 三重积分的性质
   1. \\(\iiint\limits_\Omega 1\mathrm{d}v=V\\)
   2. 三重积分中值定理: \\(\Omega\\) 为有限闭区域, \\(f(x,y,z)\\) 在 \\(\Omega\\) 上连续, 则 \\(\exist(\xi,\eta,\zeta)\in\Omega\\) 使 \\(\iiint\limits_\Omega f(x,y,z)\mathrm{d}v=f(\xi,\eta,\zeta)V\\)
3. 三重积分的计算方法
   1. 直角坐标法
      1. 铅直投影法
         
         {% asset_img 41.png %}
         (\\(\Sigma_1\\) 为下半球曲面, \\(\Sigma_2\\) 为上半球曲面)
         \\(\Omega=\\{(x,y,z)|(x,y)\in Dxy,\varphi_1(x,y)\leqslant z\leqslant\varphi_2(x,y)\\}\\)
         \\(\iiint\limits_\Omega f(x,y,z)\mathrm{d}v=\iint\limits_{Dxy}[\int_{\varphi_1(x,y)}^{\varphi_2(x,y)}f(x,y,z)\mathrm{d}z]\mathrm{d}x\mathrm{d}y\\)
      2. 切片法
         
         {% asset_img 42.png %}
         (每层切片的 \\(D\\) 都不同, 用 \\(Dz\\) 表示)
         \\(\Omega=\\{(x,y,z)|(x,y)\in Dz, c\leqslant z\leqslant d\\}\\)
         \\(\iiint\limits_\Omega f(x,y,z)\mathrm{d}v=\int_c^d[\iint\limits_{Dz} f(x,y,z)\mathrm{d}x\mathrm{d}y]\mathrm{d}z\\)
   2. 柱面坐标变换法(柱面坐标=极坐标+\\(z\\) 轴)
      1. 特征:
         1. 区域 \\(\Omega\\) 的边界含 \\(x^2+y^2\\)
         2. \\(f(x,y,z)\\) 含 \\(x^2+y^2\\)
      2. 变换:
         \\(\Omega=\\{(x,y,z)|(x,y)\in Dxy,\varphi_1(x,y)\leqslant z\leqslant\varphi_2(x,y)\\}\\)
         令 \\(\begin{cases} x=r\cos\theta \\\ y=r\sin\theta \\\ z=z \end{cases}\\) ,
         其中 \\(\alpha\leqslant\theta\leqslant\beta\\) , \\(r_1(\theta)\leqslant r\leqslant r_2(\theta)\\) , \\(\varphi_1(r\cos\theta,r\sin\theta)\leqslant z\leqslant\varphi_2(r\cos\theta,r\sin\theta)\\)
         
         {% asset_img 43.png %}
      3. \\(\mathrm{d}v\\)
         {% asset_img 44.png %}
         \\(\mathrm{d}v=\mathrm{d}r\cdot r\mathrm{d}\theta\cdot\mathrm{d}z\\) (再乘上 \\(z\\) 轴的微分)
         
      \\(\iiint\limits_{\Omega}f(x,y,z)\mathrm{d}v=\int_\alpha^\beta\mathrm{d}\theta\int_{r_1(\theta)}^{r_2(\theta)}\mathrm{d}r\int_{\varphi_1(r\cos\theta,r\sin\theta)}^{\varphi_2(r\cos\theta,r\sin\theta)}r\cdot f(r\cos\theta, r\sin\theta,z)\mathrm{d}z\\)
   3. 球面坐标变换法
      1. 特征:
         1. \\(\Omega\\) 的表面含 \\(x^2+y^2+z^2\\)
         2. \\(f(x,y,z)\\) 含 \\(x^2+y^2+z^2\\)
      2. 变换
         
         {% asset_img 45.png %}
         (\\(OM\\) 跟 \\(Ox\\) 方向的夹角为 \\(\theta\\) ; 跟 \\(Oz\\) 方向的夹角为 \\(\varphi\\))
         \\(\begin{cases} x=r\cos\theta\sin\varphi \\\ y=r\sin\theta\sin\varphi \\\ z=r\cos\varphi \end{cases}\\)
      3. \\(\mathrm{d}v\\)
         \\([\theta,\theta+\mathrm{d}\theta]\\)
         \\([\varphi,\varphi+\mathrm{d}\varphi]\\)
         \\([r,r+\mathrm{d}r]\\)
         (\\(\mathrm{d}v\\) 是一个立方体)
         
         {% asset_img 46.png %}
         \\(\mathrm{d}v=\mathrm{d}r\cdot r\mathrm{d}\varphi\cdot r\sin\varphi\mathrm{d}\theta=r^2\sin\varphi\mathrm{d}r\mathrm{d}\theta\mathrm{d}\varphi\\)

### 重积分的应用

1. 几何应用
   1. 面积
      1. \\(D\\) 为 \\(xOy\\) 面内有限闭区域, 则 \\(D\\) 的面积为 \\(A=\iint\limits_D 1\mathrm{d}\sigma\\)
      2. 空间曲面的面积
         \\(\Sigma:z=f(x,y)\enspace\\) (\\((x,y)\in Dxy\\))

         {% asset_img 47.png %}
         1. \\(\forall\mathrm{d}\sigma\subset Dxy\\)
         2. 法向量 \\(\vec{n}=\\{-f_x^\prime,-f_y^\prime,1\\}\\)
            推导:
            (来自多元函数微分学的几何应用-空间曲面上某一点的法向量)
            若 \\(\Sigma:F(x,y,z)=0\\), 法向量 \\(\vec{n}=\\{F_x^\prime,F_y^\prime,F_z^\prime\\}_{M_0}\\) 
            这里 \\(\Sigma:z=f(x,y)\rArr F(x,y,z)=z-f(x,y)=0\\)
            因此 \\(\vec{n}=\\{-f_x^\prime,-f_y^\prime,1\\}\\)
         3. \\(\mathrm{d}s=\sqrt{1+f_x^{\prime 2}+f_y^{\prime 2}}\mathrm{d}\sigma\\)
            推导:
            \\(\cos\gamma=\frac{1}{\sqrt{1+f_x^{\prime 2}+f_y^{\prime 2}}}\\) (法向量和 \\(z\\) 轴夹角, 参见向量及其线性运算-向量方向角和方向余弦)
            \\(\because\mathrm{d}s\cos\gamma=\mathrm{d}\sigma\\)
            \\(\therefore\mathrm{d}s=\sqrt{1+f_x^{\prime 2}+f_y^{\prime 2}}\mathrm{d}\sigma\\)
         4. 面积 \\(A=\iint\limits_{Dxy}\mathrm{d}s=\iint\limits_{Dxy}\sqrt{1+f_x^{\prime 2}+f_y^{\prime 2}}\mathrm{d}\sigma\\)
2. 物理应用
   1. 质心
      1. 二维
         
         {% asset_img 48.png %}
         \\(m=\iint\limits_D\rho(x,y)\mathrm{d}\sigma\\)
         \\(\bar{x}=\frac{\iint\limits_D x\rho(x,y)\mathrm{d}\sigma}{\iint\limits_D\rho(x,y)\mathrm{d}\sigma}\\) , \\(\bar{y}=\frac{\iint\limits_D y\rho(x,y)\mathrm{d}\sigma}{\iint\limits_D\rho(x,y)\mathrm{d}\sigma}\\)
      2. 三维
         
         {% asset_img 49.png %}
         \\(m=\iiint\limits_\Omega\rho(x,y,z)\mathrm{d}v\\)
         \\(\bar{x}=\frac{\iiint\limits_\Omega x\rho(x,y,z)\mathrm{d}v}{\iiint\limits_\Omega\rho(x,y,z)\mathrm{d}v}\\) , \\(\bar{y}=\frac{\iiint\limits_\Omega y\rho(x,y,z)\mathrm{d}v}{\iiint\limits_\Omega\rho(x,y,z)\mathrm{d}v}\\) , \\(\bar{z}=\frac{\iiint\limits_\Omega z\rho(x,y,z)\mathrm{d}v}{\iiint\limits_\Omega\rho(x,y,z)\mathrm{d}v}\\)
   2. 转动惯量(刚体绕轴转动时的惯性, 大小为质量乘以距离的平方 \\(I=mr^2\\))
      1. 二维
         
         {% asset_img 50.png %}
         绕直线 \\(L\\) 旋转: \\(I_L=\iint\limits_D d^2\rho(x,y)\mathrm{d}\sigma\\)
         绕 \\(x\\) 轴旋转: \\(I_x=\iint\limits_D y^2\rho(x,y)\mathrm{d}\sigma\\)
         绕 \\(y\\) 轴旋转: \\(I_y=\iint\limits_D x^2\rho(x,y)\mathrm{d}\sigma\\)
         绕原点旋转: \\(I_o=\iint\limits_D(x^2+y^2)\rho(x,y)\mathrm{d}\sigma\\)
      2. 三维
         
         {% asset_img 51.png %}
         \\(I_x=\iiint\limits_\Omega(y^2+z^2)\rho(x,y,z)\mathrm{d}v\\)
         \\(I_y=\iiint\limits_\Omega(x^2+z^2)\rho(x,y,z)\mathrm{d}v\\)
         \\(I_z=\iiint\limits_\Omega(x^2+y^2)\rho(x,y,z)\mathrm{d}v\\)

## 曲线积分与曲面积分

### 对弧长的曲线积分

1. 背景:
   \\(\rho(x,y)\\) 为线密度函数
   经典积分思想:

   {% asset_img 52.png %}
   1. \\(L\\) 划分为 \\(\Delta S_1,\dots,\Delta S_n\\)
   2. \\(\forall(\xi_i,\eta_i)\in\Delta S_i\\)
      \\(\Delta m_i=\rho(\xi_i,\eta_i)\Delta S_i\\)
   3. 取 \\(\lambda\\) 为 \\(\Delta S_1,\dots,\Delta S_n\\) 最大值
      曲线总质量 \\(m=\lim\limits_{\lambda\to 0}\displaystyle\sum_{i=1}^n\rho(\xi_i,\eta_i)\Delta S_i\\)
   
   元素法思想:

   {% asset_img 53.png %}
   1. \\(\forall\mathrm{d}s\subset L\\)
   2. \\(\mathrm{d}m=\rho(x,y)\mathrm{d}s\\)
   3. \\(m=\int_L\mathrm{d}m=\int_L\rho(x,y)\mathrm{d}s\\)
2. 对弧长曲线积分定义: \\(\int_L f(x,y)\mathrm{d}s\\)
3. 性质
   1. \\(\int_L\alpha f+\beta g\mathrm{d}s=\alpha\int_L f\mathrm{d}s+\beta\int_L g\mathrm{d}s\\)
   2. \\(L=L_1+L_2\\) 且 \\(L_1\cap L_2=\varnothing\\) , 则 \\(\int_L f(x,y)\mathrm{d}s=\int_{L_1} f(x,y)\mathrm{d}s+\int_{L_2} f(x,y)\mathrm{d}s\\)
   3. \\(\int_L 1\mathrm{d}s=L\\)
   4. 若在 \\(L\\) 上 \\(f(x,y)\leqslant g(x,y)\\) , 则 \\(\int_L f(x,y)\mathrm{d}s\geqslant\int_L g(x,y)\mathrm{d}s\\)
   5. \\(|\int_L f(x,y)\mathrm{d}s|\leqslant\int_L|f(x,y)|\mathrm{d}s\\)
4. 对弧长曲线积分计算方法
   1. \\(L\\) 为直角坐标形式
      1. \\(L:y=\varphi(x)\enspace\\) (\\(a\leqslant x\leqslant b)\\)
      2. \\(\mathrm{d}s=\sqrt{(\mathrm{d}x)^2+(\mathrm{d}y)^2}=\sqrt{1+(\frac{\mathrm{d}y}{\mathrm{d}x})^2}\mathrm{d}x=\sqrt{1+[f^\prime(x)]^2}\mathrm{d}x\\)
      3. \\(\int_L f(x,y)\mathrm{d}s=\int_a^b f[x,\varphi(x)]\sqrt{1+[f^\prime(x)]^2}\mathrm{d}x\\)
   2. \\(L\\) 为参数形式
      1. \\(L:\begin{cases} x=\varphi(t) \\\ y=\psi(t) \end{cases}\enspace\\) (\\(\alpha\leqslant t\leqslant\beta\\))
      2. \\(\mathrm{d}s=\sqrt{[\varphi^\prime(t)]^2+[\psi^\prime(t)]^2}\mathrm{d}t\\)
      3. \\(\int_L f(x,y)\mathrm{d}s=\int_\alpha^\beta f[\varphi(t),\psi(t)]\cdot\sqrt{[\varphi^\prime(t)]^2+[\psi^\prime(t)]^2}\mathrm{d}t\\)

### 对坐标的曲线积分(第二类曲线积分)

1. 背景: 做功(力的正交分解)
   1. 二维
      
      {% asset_img 54.png %}
      \\(\vec{F}=\\{P(x,y),Q(x,y)\\}\\)
      1. \\(\forall\vec{\mathrm{d}s}\subset L\\)
         \\(\vec{\mathrm{d}s}=\\{\mathrm{d}x,\mathrm{d}y\\}\\)
      2. \\(\mathrm{d}w=\vec{F}\cdot\vec{\mathrm{d}s}=P(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y\\)
      3. \\(w=\int_L\mathrm{d}w=\int_L p(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y\\)
   2. 三维
      
      {% asset_img 55.png %}
      1. \\(\forall\vec{d}s\subset L\\)
         \\(\vec{d}s=\\{\mathrm{d}x,\mathrm{d}y,\mathrm{d}z\\}\\)
      2. \\(\mathrm{d}w=\vec{F}\cdot\vec{\mathrm{d}s}=P\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z\\)
      3. \\(w=\int_L\mathrm{d}w=\int_L P\mathrm{d}x+Q\mathrm{d}y+R\mathrm{d}z\\)
2. 对坐标的曲线积分定义
   1. 二维: \\(\int_L P(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y\\)
      其中 \\(\int_L P(x,y)\mathrm{d}x\\) 称为函数 \\(P(x,y)\\) 在有向曲线段 \\(L\\) 上对坐标 \\(x\\) 的曲线积分.
   2. 三维: \\(\int_L P(x,y,z)\mathrm{d}x+Q(x,y,z)\mathrm{d}y+R(x,y,z)\mathrm{d}z\\)
3. 性质
   1. \\(\int_L [af_1(x,y)+bf_2(x,y)]\mathrm{d}x=a\int_L f_1(x,y)\mathrm{d}x+b\int_L f_2(x,y)\mathrm{d}x\\)
   2. \\(\int_{L^-}P(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y=-\int_L P(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y\\)
4. 对坐标的曲线积分基本计算法(二维)
   1. 直角坐标法
      对 \\(\int_L P(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y\\)
      1. \\(L:y=\varphi(x)\enspace\\) (\\(x\in[a,b]\\))
      2. \\(\int_L P(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y=\int_a^b P[x,\varphi(x)]\mathrm{d}x+Q[x,\varphi(x)]\cdot\varphi^\prime(x)\mathrm{d}x\\)
   2. 参数方程法
      1. \\(L:\begin{cases} x=\varphi(t) \\\ y=\psi(t) \end{cases}\enspace\\) (\\(t\in[\alpha,\beta]\\))
      2. \\(\int_L P(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y=\int_\alpha^\beta P[\varphi(t),\psi(t)]\varphi^\prime(t)\mathrm{d}t+Q[\varphi(t),\psi(t)]\psi^\prime(t)\mathrm{d}t\\)

### 格林公式及应用

1. 二维区域的边界
   
   {% asset_img 56.png %}
   (单连通区域边界逆时针为正向; 多连通区域外边界逆时针为正向, 内边界顺时针为正向)
2. 格林公式:
   设 \\(D\\) 为连通区域, \\(L\\) 为 \\(D\\) 的**正向边界**
   若 \\(P(x,y)\\)、\\(Q(x,y)\\) 在 \\(D\\) 上连续可偏导, 则
   \\(\oint_L P\mathrm{d}x+Q\mathrm{d}y=\iint\limits_D(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})\mathrm{d}\sigma\enspace\\) (\\(\oint\\) 表示封闭边界, 和 \\(\int\\) 基本等价)
   证明:
   * \\(\oint_L P\mathrm{d}x=-\iint\limits_D\frac{\partial P}{\partial y}\mathrm{d}\sigma\\)
     {% asset_img 57.png %}
     \\(\oint_L P\mathrm{d}x=\int_{L_1}P\mathrm{d}x+\int_{L_2}P\mathrm{d}x\\)
     \\(=\int_a^b P[x,\varphi_1(x)]\mathrm{d}x+\int_b^a P[x,\varphi_2(x)]\mathrm{d}x\\)
     \\(=\int_a^b\\{P[x,\varphi_1(x)]-P[x,\varphi_2(x)]\\}\mathrm{d}x\\)
   
     \\(\iint\limits_D\frac{\partial P}{\partial y}d\sigma=\int_a^b\mathrm{d}x\int_{\varphi_1(x)}^{\varphi_2(x)}\frac{\partial P}{\partial y}\mathrm{d}y\\)
     \\(=\int_a^b P(x,y)|_{\varphi_1(x)}^{\varphi_2(x)}\mathrm{d}x=\int_a^b\\{P[x,\varphi_2(x)]-P[x,\varphi_1(x)]\\}\mathrm{d}x\\)
     \\(\therefore\oint_L P\mathrm{d}x=-\iint\limits_D\frac{\partial P}{\partial y}\mathrm{d}\sigma\\)
   * \\(\oint\_L Q\mathrm{d}y=\iint\limits\_{D}\frac{\partial Q}{\partial x}\mathrm{d}\sigma\\)
     {% asset_img 58.png %}
     \\(\oint_L Q\mathrm{d}y=\int_{L_1}Q\mathrm{d}y+\int_{L_2}Q\mathrm{d}y\\)
     \\(=\int_d^c Q[\psi_1(y),y]\mathrm{d}y+\int_c^d Q[\psi_2(y),y]\mathrm{d}y\\)
     \\(=\int_c^d\\{Q[\psi_2(y),y]-Q[\psi_1(y),y]\\}\mathrm{d}y\\)

     \\(\iint\limits_{D}\frac{\partial Q}{\partial x}\mathrm{d}\sigma=\int_c^d\mathrm{d}y\int_{\psi_1(y)}^{\psi_2(y)}\frac{\partial Q}{\partial x}\mathrm{d}x\\)
     \\(=\int_c^d Q(x,y)|_{\psi_1(y)}^{\psi_2(y)}\mathrm{d}y=\int_c^d\\{Q[\psi_2(y),y]-Q[\psi_1(y),y]\\}\mathrm{d}y\\)
     \\(\therefore\oint\_L Q\mathrm{d}y=\iint\limits\_{D}\frac{\partial Q}{\partial x}\mathrm{d}\sigma\\)
   
   \\(\oint_L P\mathrm{d}x+Q\mathrm{d}y=\iint\limits_D(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})\mathrm{d}\sigma\enspace\\)

### 对面积的曲面积分

计算方法: 二重积分法
1. \\(\Sigma:z=\varphi(x,y)\enspace\\) (\\((x,y)\in Dxy\\))
2. \\(\mathrm{d}s=\sqrt{(\mathrm{d}x)^2+(\mathrm{d}y)^2}=\sqrt{1+z_x^{\prime 2}+z_y^{\prime^2}}\mathrm{d}\sigma\\)
3. 面积 \\(\iint\limits_\Sigma f(x,y,z)\mathrm{d}s=\iint\limits_D f[x,y,\varphi(x,y)]\cdot\sqrt{1+\varphi_x^{\prime 2}+\varphi_y^{\prime 2}}\mathrm{d}\sigma\\)

### 对坐标的曲面积分

1. 对坐标的曲面积分的定义
   \\(\Sigma\\) 有侧曲面块, \\(P(x,y,z)\\)、\\(Q(x,y,z)\\)、\\(R(x,y,z)\\) 在有侧曲面上有界
   1. \\(\Sigma\\) 分为 \\(\overrightarrow{\Delta S_1},\overrightarrow{\Delta S_2},\dots,\overrightarrow{\Delta S_n}\\)
   2. \\(\overrightarrow{\Delta S_i}\\) 在 \\(yOz\\) 面、\\(xOz\\) 面、\\(xOy\\) 面投影为 \\((\Delta S_i)yz\\)、\\((\Delta S_i)xz\\)、\\((\Delta S_i)xy\\) , 
      \\(P(\xi_i, \eta_i, \zeta_i)\in\overrightarrow{\Delta S_i}\\) ,
      作
      \\(\displaystyle\sum_{i=1}^n P(\xi_i, \eta_i, \zeta_i)(\Delta S_i)yz\\)
      \\(\displaystyle\sum_{i=1}^n Q(\xi_i, \eta_i, \zeta_i)(\Delta S_i)xz\\)
      \\(\displaystyle\sum_{i=1}^n R(\xi_i, \eta_i, \zeta_i)(\Delta S_i)xy\\)
   3. 令 \\(\lambda\\) 为 \\(\overrightarrow{\Delta S_1} , \overrightarrow{\Delta S_2} , \dots , \overrightarrow{\Delta S_n}\\) 直径最大值
      若 \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n P(\xi_i, \eta_i, \zeta_i)(\Delta S_i)yz\\) 存在, 则
      \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n P(\xi_i, \eta_i, \zeta_i)(\Delta S_i)=\iint_\Sigma P(x, y, z)dydz \enspace\\) (P 在有侧曲面 \\(\Sigma\\) 上对坐标 y, z 的曲面积分)
      \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n Q(\xi_i, \eta_i, \zeta_i)(\Delta S_i)xz=\iint_\Sigma Q(x, y, z)dxdz\\)
      \\(\lim\limits_{\lambda\to0}\displaystyle\sum_{i=1}^n R(\xi_i, \eta_i, \zeta_i)(\Delta S_i)xy=\iint_\Sigma R(x, y, z)dxdy\\)
      \\(\iint_\Sigma Pdydz+\iint_\Sigma Qdxdz+\iint_\Sigma Rdxdy=\iint_\Sigma Pdydz+Qdxdz+Rdxdy\\)
   
   性质:
   1. \\(\iint_\Sigma=\iint_{\Sigma_1}+\iint_{\Sigma_2}\\)
   2. \\(\iint_{\Sigma^-}=-\iint_\Sigma\\)

### 对坐标的曲面积分基本计算法-二重积分法

TODO: 分析例题

### 两类曲面积分关系

TODO: 补充图片
对 \\(\iint_\Sigma Pdyd+Qdzdx+Rdxdy\\)
\\(dydz=ds\cdot\cos\alpha\\)
\\(dxdz=ds\cdot\cos\beta\\)
\\(dxdy=ds\cdot\cos\gamma\\)
\\(\iint_\Sigma Pdydz+Qdxdz+Rdxdy=\iint_\Sigma (P\cos\alpha+Q\cos\beta+R\cos\gamma)ds\\)

## 高斯公式

定义:
1. \\(\Omega\\) 为集合体, \\(\Sigma\\) 为 \\(\Omega\\) 的外表面
2. \\(P, Q, R\\) 在 \\(\Omega\\) 上连续可偏导, 则
   \\(\oiint_\Sigma Pdydz+Qdzdx+Rdxdy=\iiint_\Omega(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z})dV\\)

## 斯托克斯公式

定义:
1. \\(\Sigma\\) 为光滑曲面块, \\(\Gamma\\) 为 \\(\Sigma\\) 的界, \\(\Sigma\\) 的侧与 \\(\Gamma\\) 的方向按右手确定
2. \\(P, Q, R\\) 在 \\(\Sigma\\) 连续可偏导, 则
   \\(\oint_L Pdx+Qdy+Rdz=\iint_\Sigma \begin{vmatrix} dydz & dzdx & dxdy \\\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\\ P & Q & R \end{vmatrix}=\iint_\Sigma \begin{vmatrix} \cos\alpha & \cos\beta & \cos\gamma \\\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\\ P & Q & R \end{vmatrix}ds\\)
   其中 \\(\cos\alpha, \cos\beta, \cos\gamma\\) 为曲面 \\(\Sigma\\) 法向量的方向余弦
