---
title: vector-algebra-and-space-analytic-geometry
category: postgraduate-advanced-mathematics
lang: zh-cn
date: 2020-05-22 17:01:57
tags:
---

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
      \\(\vec{a} , \vec{b}\\) 夹角为 \\(\theta\\) , 记 \\((\widehat{\vec{a} , \vec{b}})=0 \quad (0\leqslant\theta\leqslant\pi)\\)
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

## 向量应用

### 平面及其方程

### 空间直线

## 空间曲面及方程

## 空间曲线及方程

