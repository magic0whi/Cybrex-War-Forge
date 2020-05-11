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
   2. 氧化物: \\(\\)

## 物质的量, 物质的聚集状态和溶液的配置

## 离子反应

## 氧化还原反应

## 原子结构, 物质结构

## 元素周期律和元素周期表

## 化学能与热能

## 化学能与电能

## 化学反应速率 化学反应的方向和限度

## 化学平衡的移动

## 弱电解质的电离和溶液的酸碱性

## 盐类水解和沉淀溶解平衡
