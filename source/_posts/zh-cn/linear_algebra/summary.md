---
title: summary
lang: zh-cn
category: linear_algebra
date: 2020-10-03 19:18:39
tags:
---

## 行列式

1. 行列式(determinant):
2. 余子式(minor):
3. 代数余子式(cofactor)
4. 行列式按行展开:
5. 行列式按列展开:
6. 克拉默法则(Cramer's rule):

## 矩阵及其运算

* 伴随矩阵(adjugate matrix)
* Aadj(A)=adj(A)A=|A|I
* 奇异矩阵(singular matrix): |A|=0
* 非奇异矩阵(non-singular matrix): |A|≠0

## 线性相关和生成子空间

* 线性组合(linear combination):
* 判断 Ax=b 是否有解相当于确定向量 b 是否在 A 列向量的生成子空间中. 这个特殊的生成子空间被称为 A 的列空间(column space)或者 A 的值域(range)
* 线性无关(linear independent)
* 奇异矩阵(singular matrix)

## 范数

* 范数(norm)用来衡量向量大小, \\(L^p\\) 范数定义为 \\(\Vert x\Vert_p=(\sum_{i} |x_i|^p)^\frac{1}{p}\\)
* 欧几里得范数(Euclidean norm): \\(L^2\\) 范数
* 最大范数(max norm): \\(L^\infty\\) 范数
* Frobenius 范数可以用来衡量矩阵大小:
* 向量点积也可以用范数表示, 即

## 特殊矩阵和向量

* 对焦矩阵(diagonal matrix)
* 对称矩阵(symmetric matrix)
* 单位向量(unit vector)
* 正交(orthogonal)
* 标准正交(orthonormal)
* 正交矩阵(orthogonal matrix)

## 特征分解

* 推荐阅读 [Eigenvectors and Eigenvalues](http://setosa.io/ev/eigenvectors-and-eigenvalues/)
* 特征向量(eigenvector) v 满足 Av=λv . 其中, 标量 λ 为这个特征向量对应的特征值(eigenvalue)
* 如果矩阵 A 有 n 个线性无关的特征向量 \\(\\{v^{(1)}\\}\\)

## 迹