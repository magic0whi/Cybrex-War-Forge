---
title: basic-concepts-and-theories-in-chemistry
category: chemistry
lang: zh-cn
date: 2020-05-10 15:17:31
tags:
toc: true
---

## 物质的组成, 分类, 与性质, 分散系

TODO: 补充53P3结构图

1. 物质的组成
   {% plantuml %}
   @startuml
   left to right direction
   skinparam packageStyle rectangle
   rectangle "宏观角度" {
       (元素) --> (单质) : "游离态"
       (元素) --> (化合物) : "化合态"
   }
   
   rectangle "微观角度" {
       (原子) <--> (离子)
       (原子) --> (分子) : "构成"
   }
   
   (单质) --> (物质)
   (元素) --> (物质) : "组成"
   (化合物) --> (物质)
   (离子) --> (物质) : "构成"
   (原子) --> (物质) : "构成"
   (分子) --> (物质) : "构成"
   @enduml
   {% endplantuml %}
2. 物质的性质
   {% plantuml %}
   @startuml
   left to right direction
   rectangle 物质结构
   rectangle 物质性质
   物质结构 --> 物质性质 : "决定"
   物质性质 --> 物质结构 : "推断"
   
   rectangle 物理性质
   rectangle 化学性质
   物质性质 --> 物理性质
   物质性质 --> 化学性质

   rectangle 物理变化
   rectangle 化学变化
   物理性质 --> 物理变化 : "决定"
   物理变化 --> 物理性质 : "表现"
   化学性质 --> 化学变化 : "决定"
   化学变化 --> 化学性质 : "表现"
   @enduml
   {% endplantuml %}
   * 化学性质包括氧化性还原性, 酸碱性
3. 物质的分类方法
   * 单一分类法
   * 交叉分类法
   * 树状分类法
4. 常见无机化合物的分类
   1. 氢化物: \\(\ce{HCl, H2S, H2O, NH3}\\) 等
   2. 氧化物:
      <div>
      $$\begin{cases}
         不成盐氧化物: \ce{CO, NO} 等 \\
         成盐氧化物 \begin{cases}
            酸性氧化物: \ce{CO2, P2O5, Mn2O7} 等 \\
            碱性氧化物: \ce{Na2O, CaO} 等 \\
            两性氧化物: \ce{Al2O3} 等
         \end{cases}\\
         过氧化物: \ce{Na2O2, H2O2} 等
      \end{cases}$$
      </div>
   3. 酸:
      <div>
      $$\begin{cases}
         按电离出的 \ce{H^+} 数 \begin{cases}
            一元酸: \ce{HCl, HNO3} 等 \\
            二元酸: \ce{H2SO4, H2S} 等 \\
            多元酸: \ce{H3PO4} 等
         \end{cases}\\
         按酸根是否含氧 \begin{cases}
            无氧酸: \ce{HCl, H2S} 等 \\
            含氧酸: \ce{HClO4, H2SO4} 等
         \end{cases}\\
         按是否完全电离\begin{cases}
            强酸: \ce{HCl, H2SO4, HNO3} 等 \\
            弱酸: \ce{CH3COOH, HF} 等
         \end{cases}\\
         按有无挥发性 \begin{cases}
            挥发性酸: \ce{HNO3, HCl} 等 \\
            难挥发性酸: \ce{H2SO4, H3PO4} 等
         \end{cases}
      \end{cases}$$
      </div>
   4. 碱:
      <div>
      $$\begin{cases}
         按水溶性: \begin{cases}
            可溶性碱: \ce{NaOH, KOH, Ba(OH)2} 等 \\
            难溶性碱: \ce{Mg(OH)2, Cu(OH)2} 等
         \end{cases}\\
         按是否完全电离: \begin{cases}
            强碱: \ce{NaOH, Ba(OH)2, KOH} 等 \\
            弱碱: \ce{NH3\cdot H2O} 等
         \end{cases}
      \end{cases}$$
      </div>
   5. 盐:
      <div>
      $$\begin{cases}
         正盐: \ce{BaSO4, KNO3, NaCl} 等 \\
         酸式盐: \ce{NaHCO3, KHSO4} 等 \\
         碱式盐 \ce{Cu2(OH)2CO3} 等 \\
         复盐: \ce{KAl(SO4)2\cdot 12H2O} 等
      \end{cases}$$
      </div>
5. 几种分散系的比较
   <table>
   <thead>
     <tr>
       <th rowspan="2">分散系</th>
       <th rowspan="2">溶液</th>
       <th rowspan="2">胶体</th>
       <th colspan="2">浊液</th>
     </tr>
     <tr>
       <td>悬浊液</td>
       <td>乳浊液</td>
     </tr>
   </thead>
   <tbody>
     <tr>
       <td>分散质粒子直径</td>
       <td>&lt; 1nm</td>
       <td>1 ~ 100 nm</td>
       <td colspan="2">&gt; 100 nm</td>
     </tr>
     <tr>
       <td>分散质粒子的构成</td>
       <td>分子, 离子</td>
       <td>许多分子的集合体或大分子</td>
       <td>大两分子聚集成的固体小颗粒</td>
       <td>大量分子聚集成的小液滴</td>
     </tr>
     <tr>
       <td>特点</td>
       <td>均一, 稳定体系</td>
       <td>多数较均一, 较稳定(介稳体系)</td>
       <td>不均一, 不透明, 久置沉淀</td>
       <td>不均一, 不透明, 久置分层</td>
     </tr>
     <tr>
       <td>分散质粒子能否通过滤纸</td>
       <td>能</td>
       <td>能</td>
       <td>不能</td>
       <td></td>
     </tr>
     <tr>
       <td>分散质粒子能否透过半透膜</td>
       <td>能</td>
       <td>不能</td>
       <td>不能</td>
       <td></td>
     </tr>
     <tr>
       <td>实例</td>
       <td>食盐水, 蔗糖溶液</td>
       <td>\(\ce{Fe(OH)3}\) 胶体, 淀粉胶体</td>
       <td>泥水, 石灰乳</td>
       <td>植物油和水混合</td>
     </tr>
   </tbody>
   </table>

## 物质的量和溶液的配置

### 物质的量
1. 物质的量: 1份物质的量表示 \\(N_A\\) 个粒子的集合体, 符号为 \\(n\\) , 单位为 mol
2. 阿伏伽德罗常数: 规定为 \\(N_A=6.02\cdot10^{23}\\) , 单位为 \\(\ce{mol^{-1}}\\)
   阿伏伽德罗常数与物质的量关系式: \\(n=\dfrac{N}{N_A}\\) , 其中\\(N\\) 为总粒子数
3. 摩尔质量: 表示 1 mol 某种物质重多少, 符号 \\(M\\) , 常用单位 \\(\ce{g\cdot mol^{-1}}\\)
   摩尔质量与物质的量关系式: \\(n=\dfrac{m}{M}\\), 其中 \\(m\\) 为总质量
   **当为纯净物时, 摩尔质量 = 相对原子(分子)质量**
4. 气体摩尔体积: 表示 1 mol 气体占的体积, 符号 \\(V_m\\) , 常用单位 \\(\ce{L\cdot mol^{-1}}\\) . 它的大小与温度, 压强有关.
   标准状况(0 ℃, 101 kPa)下, \\(V_m=22.4\ce{L\cdot mol^{-1}}\\)
   气体摩尔体积与物质的量关系式: \\(n=\dfrac{V}{V_m}\\)

### 物质的量浓度
1. 物质的量浓度: 1L 溶液中所含溶质B的物质的量, 符号为 \\(c_B\\) , 常用单位为 \\(\ce{mol\cdot L^{-1}}\\)
   物质的量浓度计算公式: \\(c_B=\dfrac{n_B}{V}\\)
2. 利用溶质的质量分数和密度来计算
   在已知溶质的质量分数(溶质质量与溶液质量之比) \\(\omega=\dfrac{m_{溶质}}{m_{溶液}}\\) , 溶液密度为\\(\ce{\rho \enspace g\cdot mL^{-1}}\\)
   有浓度换算公式: \\(c_B=\dfrac{1000 \cdot \rho \cdot \omega}{M_B}\\)
3. 一定物质的量浓度溶液的配制
4. 物质的量浓度的相关计算
   1. 溶液稀释或混合的相关计算
      对于任何溶液, 稀释前后\\(m_B\\)和\\(n_B\\)都不变
      根据\\(m_B\\)不变可得公式 \\(\ce{c_稀\cdot V_稀=c_浓\cdot V_浓}\\)
      根据\\(n_B\\)不变可得公式
      <div>
      $$\begin{aligned}
         m_{稀溶液}\cdot \omega_{稀溶液}&=m_{浓溶液}\cdot \omega_{浓溶液} \\
         (体积\cdot密度=质量)\rArr V_{稀溶液}\cdot \rho_{稀溶液}\cdot \omega_{稀溶液}&=V_{浓溶液}\cdot \rho_{浓溶液}\cdot \omega_{浓溶液} \\
         (根据浓度换算公式) \rArr V_{稀溶液}\cdot c_{稀溶液}\cdot M_B&=V_{浓溶液}\cdot c_{浓溶液}\cdot M_B
      \end{aligned}$$
      </div>
   2. 溶解度的计算
      溶解度: 温度的压强一定下, 100ml**水**(水的密度1ml=1g)中溶解的物质的质量
      根据溶解度定义, 溶质溶解度\\(S\\)与溶质质量分数存在换算关系: \\(\omega=\dfrac{S}{100+S}\\)
      将此公式带入物质的量浓度换算公式即得: \\(c=\dfrac{n_B}{V}=\dfrac{1000 \rho \omega}{M_B}=\dfrac{1000\rho S}{M_B(100+S)}\\)
   3. 气体溶于**水**(水的密度1ml=1g)的\\(c_B\\)和\\(\omega\\)计算
      主要的三步:
      1. 先运用气体摩尔体积求出溶质的物质的量: \\(n_B=\dfrac{V_气}{22.4}\\)
      2. 然后运用质量除以密度等于体积公式求出溶液体积: \\(V=\dfrac{m}{\rho}\\)
      3. 最后运用 \\(c=\dfrac{n_B}{V}\\)计算

## 离子反应

### 离子共存

### 离子方程式

## 氧化还原反应

## 原子结构, 物质结构

## 元素周期律和元素周期表

## 化学能与热能

## 化学能与电能

## 化学反应速率 化学反应的方向和限度

## 化学平衡的移动

## 弱电解质的电离和溶液的酸碱性

## 盐类水解和沉淀溶解平衡
