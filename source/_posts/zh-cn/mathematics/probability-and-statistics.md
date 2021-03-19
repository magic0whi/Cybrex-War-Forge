---
title: probability-and-statistics
toc: true
category: mathematics
lang: zh-cn
date: 2021-03-02 14:24:35
tags:
---

前五章为概率论基础知识, 第六至第九章是数理统计的基本内容, 第十章至第十一章是随机过程初步

<!-- more -->

## 概率论的基础知识

### 随机试验、样本空间、随机事件

1. 随机试验: 满足下面三个特点的试验, 记为 \\(E\\)
   * 相同条件下可以重复进行
   * 试验可能结果不止一个, 但能明确所有可能结果
   * 结果不可预知
2. 样本空间: 随机试验 \\(E\\) 的所有可能的试验结果所组成的集合, 称为 \\(E\\) 的样本空间, 记为 \\(\Omega\\)
   样本点: 样本空间的每个元素, 即试验的每个结果. 记为 \\(\omega\\)
   * 样本空间的元素可以是有限个, 也可以是可列个, 还可以是不可列个.
3. 随机事件: 在试验过程中有可能发生也有可能不发生的情况. 试验 \\(E\\) 的样本空间 \\(\Omega\\) 的子集称为 \\(E\\) 的随机事件, 简称事件. 通常用 \\(A,B,\dots\\) 表示. 事件发生当且仅当对应的子集中某个样本点出现.
   > 任何事件总是样本空间的子集. 如在掷骰子观察出现点数的试验中, 事件 \\(A\\) :"掷出偶数点", 即 \\(A=\\{2,4,6\\}\\)
   
   必然事件: 若每次试验, 事件 \\(A\\) 对应的样本空间子集 \\(\Omega\\) 中必然有一个样本点出现, 则称事件 \\(A\\) 为必然事件.
   不可能事件: 空集 \\(\varnothing\\) 也是样本空间的子集, 但不包含任何样本点, 因此每次试验必不可能发生. 因此不可能事件记为 \\(\varnothing\\)
   基本事件: 只有单个样本点的事件
4. 事件间的关系及运算
   事件是一个集合, 故事件间的关系、运算可按集合间的关系、运算来处理.
   1. 包含关系
      若 \\(A\subset B\\) , 则称事件 \\(A\\) **包含于**事件 \\(B\\) , 或事件 \\(B\\) **包含**事件 \\(A\\) , 它是指事件 \\(A\\) 发生必然导致事件 \\(B\\) 发生.
      若 \\(A\subset B\\) 且 \\(B\subset A\\) , 则称事件 \\(A\\) 与事件 \\(B\\) **相等**, 记为 \\(A=B\\) .
   2. 事件的和
      称 \\(A\cup B=\\{x|x\in A\text{或}x\in B\\}\\) 为事件 \\(A\\) 与 \\(B\\) 的**和事件**,
      \\(A\cup B\\) 发生当且仅当事件 \\(A\\) 与 事件\\(B\\) 至少有一个发生.
      类似地,
      称 \\(\displaystyle\bigcup_{k=1}^{n}A_k\\) 为 \\(n\\) 个事件 \\(A_1,A_2,\dots,A_n\\) 的和事件;
      称 \\(\displaystyle\bigcup_{k=1}^{+\infty}A_k\\) 为可列个事件 \\(A_1,A_2,\dots\\) 的和事件.
   3. 事件的积
      称 \\(A\cap B=\\{x|x\in A\text{且}x\in B\\}\\) 为事件 \\(A\\) 与事件 \\(B\\) 的**积事件**,
      \\(A\cap B\\) 发生当且仅当事件 \\(A\\) 与事件 \\(B\\) 同时发生. \\(A\cap B\\) 也简记为 \\(AB\\) .
      类似地,
      称 \\(\displaystyle\bigcap_{k=1}^{n}A_k\\) 为 \\(n\\) 个事件 \\(A_1,A_2,\dots,A_n\\) 的积事件;
      称 \\(\displaystyle\bigcap_{k=1}^{+\infty}A_k\\) 为可列个事件 \\(A_1,A_2,\dots\\) 的积事件.
   4. 事件的差
      称 \\(A-B=\\{x|x\in A\text{且}x\notin B\\}\\) 为事件 \\(A\\) 与事件 \\(B\\) 的**差事件**.
      \\(A-B\\) 发生当且仅当事件 \\(A\\) 发生且事件 \\(B\\) 不发生.
   5. 互不相容事件
      若 \\(A\cap B=\varnothing\\) , 则称事件 \\(A\\) 与事件 \\(B\\) **互不相容**, 或称事件 \\(A\\) 与事件 \\(B\\) **互斥**.
      这意味着事件 \\(A\\) 与事件 \\(B\\) 不能同时发生.
   7. 事件的互逆
      若 \\(A\cap B=\varnothing\\) 且 \\(A\cup B=\Omega\\) , 则称事件 \\(A\\) 与事件 \\(B\\) **互逆**或互为**对立事件**.
      这意味着事件 \\(A\\) 与事件 \\(B\\) 不能同时发生, 但必须有一个发生.
      一般地, 事件 \\(A\\) 的对立事件记作 \\(\overline{A}\\) .
      \\(A-B=A\overline{B}\\)
   9. 交换律: \\(A\cup B=B\cup A\\) , \\(A\cap B=B\cap A\\)
      结合律: \\((A\cup B)\cup C=A\cup(B\cup C)\\) , \\((A\cap B)\cap C=A\cap(B\cap C)\\)
      分配律: \\((A\cup B)\cap C=(A\cap C)\cup(B\cap C)\\)
      \\(\mskip{3em}(A\cap B)\cup C=(A\cup B)\cap(B\cup C))\\)
      德摩根(De Morgan)律: \\(\overline{A\cup B}=\overline{A}\cap\overline{B}\\) , \\(\overline{A\cap B}=\overline{A}\cup\overline{B}\\)
      德摩根律可推广到多个事件的情形:
      \\(\displaystyle\overline{\bigcup_{k=1}^{n}A_k}=\bigcap_{k=1}^{n}\overline{A_k}\\) , \\(\displaystyle\overline{\bigcap_{k=1}^{n}A_k}=\bigcup_{k=1}^{n}\overline{A_k}\\)

      \\(\displaystyle\overline{\bigcup_{k=1}^{+\infty}A_k}=\bigcap_{k=1}^{+\infty}\overline{A_k}\\) , \\(\displaystyle\overline{\bigcap_{k=1}^{+\infty}A_k}=\bigcup_{k=1}^{+\infty}\overline{A_k}\\)
      上面关于事件的各种关系可用韦恩(venn)图直观地表示出来 TODO:补充图片

### 频率与概率

1. 事件的频率
