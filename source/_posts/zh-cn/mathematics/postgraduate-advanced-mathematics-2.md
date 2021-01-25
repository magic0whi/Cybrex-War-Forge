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
         则 \\(\vec{a}\times\vec{b}=\\{b_1c_2-b_2c_1,a_2c_1-a_1c_2,a_1b_2-a_2b_1\\}\\)
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
   
   例: 同一个方程 \\(x^2+y^2=4\\) , 在二维坐标系中是一个半径为 2 的圆(称作母线); 在三维坐标系中在 \\(z\\) 轴无限延申, 成为了到 \\(z\\) 轴的距离为 2 的点形成的曲面

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
      将 \\(\overrightarrow{M_0M}=\\{x-x_0,y-y_0,z-z_0\\}\\) 代入
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
