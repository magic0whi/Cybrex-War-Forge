---
title: introduction-to-linear-algebra
toc: true
category: mathematics
lang: zh-cn
date: 2021-02-24 11:53:14
tags:
---

Introduction to Linear Algebra by Gilbert Strang

The word "**unit**" is always indicating that some measurement equals "one".

<!-- more -->

## Introduction to Vectors

1. Vectors and Linear Combinations
2. Lengths and Dot Products
   1. The "dot product" of \\(v=\begin{bmatrix} 1 \\\ 2 \end{bmatrix}\\) and \\(w=\begin{bmatrix} 4 \\\ 5 \end{bmatrix}\\) is \\(v\cdot w=1\cdot 4+2\cdot 5=4+10=14\\)
   2. The dot product is \\(v\cdot w=0\\) when \\(v\\) is perpendicular to \\(w\\)
      The zero vector is perpendicular to every vector.
      The angle is less \\(90\degree\\) when \\(v\cdot w\\) is positive. The angle is above \\(90\degree\\) when \\(v\cdot w\\) is negative.
      **Proof**: When \\(v\\) and \\(w\\) are perpendicular, they form two sides of a right triangle.
      The third side is \\(v-w\\) (the hypotenuse going across in image below). With Pythagoras Law \\(a^2+b^2+c^2\\) :
      \\[\\|v\\|^2+\\|w\\|^2=\\|v-w\\|^2\\]
      Writing out the formulas for those lengths in two dimensions, this equation is:
      \\[(v_1^2+v_2^2)+(w_1^2+w_2^2)=(v_1-w_1)^2+(v_2-w_2)^2 \\\ \rArr 0=-2v_1w_1-2v_2w_2 \\\ \rArr v_1w_1+v_2w_2=0\\]

      {% asset_img 2.png %}
   3. The length squared of \\(v=\begin{bmatrix} 1 \\\ 3 \\\ 2 \end{bmatrix}\\) is \\(v\cdot v=1+9+4=14\\) . **The length is** \\(|v|=\sqrt{14}\\)
   4. Divide \\(v\\) by its length \\(\\|v\\|\\) to get its unit vector: \\(u=\frac{v}{\\|v\\|}=\frac{v}{\sqrt{14}}=\frac{1}{\sqrt{14}}\begin{bmatrix} 1 \\\ 3 \\\ 2 \end{bmatrix}\\)
      \\(\begin{bmatrix} \cos\theta \\\ \sin\theta \end{bmatrix}\\) were unit vectors. These vectors reach out to the unit circle in images below. Thus \\(\cos\theta\\) and \\(\sin\theta\\) are simply the coordinates of that point at angle \\(\theta\\) on the unit circle.
      
      {% asset_img 1.png %}
   5. The angle \\(\theta\\) between \\(v\\) and \\(w\\) has \\(\cos\theta=\frac{v\cdot w}{\\|v\\|\cdot\\|w\\|}\\)
      All angles have \\(|\cos\theta|\leqslant 1\\) . So all vectors have \\(|v\cdot w|\leqslant\\|v\\|\cdot\\|w\\|\\)
      Unit vector \\(u\\) and \\(U\\) at angle \\(\theta\\) have \\(u\cdot U=\cos\theta\\)
   * Example 2: Put a weight of 4 at the point \\(x=-1\\) (left of zero) and a weight of 2 at the point \\(x=2\\) (right of zero).
     The axis will balance on the center point (like a see-saw).
     The weights balance because the dot product is \\(4\cdot -1+2\times 2=0\\)
     > This example is typical of engineering and science. The vector of weight is \\((w_1,w_2)=(4,2)\\) .
       The vector of distances from the center is \\((v_1,v_2)=(-1,2)\\) . The weights times the distances (\\(w_1v_1\\) and \\(w_2v_2\\)), give the "moments". The equation for the see-saw to balance is \\(w_1v_1+w_2v_2=0\\)
   * Example 3: Dot products enter in economics and business. We have three goods to buy and sell.
     Their prices are \\((p_1,p_2,p_3)\\) for each unit--this is the "price vector" \\(p\\) .
     The quantities we buy or sell are \\((q_1,q_2,q_3)\\) : positive when we sell, negative when we buy.
     Selling \\(q_1\\) units at the price \\(p_1\\) brings in \\(q_1p_1\\) . The total income (quantities \\(q\\) times prices \\(p\\)) is **the dot product \\(q\cdot p\\) in three dimensions**:
     \\[\text{\bf{Income}}=(q_1,q_2,q_3)\cdot(p_1,p_2,p_3)=q_1p_1+q_2p_2+q_3p_3\\]
     > A zero dot product means that "the books balance". Total sales equal total purchases if \\(q\cdot p=0\\) . Then \\(p\\) is perpendicular to \\(q\\) (in three-dimensional space). A supermarket with thousands of goods goes quickly into high dimensions.
       Small note: Spreadsheets have become essential in management. They compute linear combinations and dot products. What you see on the screen is a matrix.
3. Matrices
   1. Matrix times vector: \\(Ax=\\) combination of the columns of \\(A\\)
   2. The solution to \\(Ax=b\\) is \\(x=A^{-1}b\\) when \\(A\\) is an invertible matrix.
   3. Matrices which three columns lie in the same plane has no inverses. (e.g. cyclic matrix \\(C\\))
   4. \\(Ax\\) is dot products with columns:
      <div>
      $$
      Ax=\begin{bmatrix}
       1 & 0 & 0 \\
       -1 & 1 & 0 \\
       0 & -1 & 1
      \end{bmatrix}
      \begin{bmatrix}
       x_1 \\
       x_2 \\
       x_3
      \end{bmatrix}
      =x_1\begin{bmatrix}
       1 \\
       -1 \\
       0
      \end{bmatrix}
      +x_2\begin{bmatrix}
       0 \\
       1 \\
       -1
      \end{bmatrix}
      +x_3\begin{bmatrix}
       0 \\
       0 \\
       1
      \end{bmatrix}
      $$
      </div>
      
      \\(Ax\\) is also dot products with rows:
      <div>
      $$
      Ax=\begin{bmatrix}
       1 & 0 & 0 \\
       -1 & 1 & 0 \\
       0 & -1 & 1
      \end{bmatrix}
      \begin{bmatrix}
       x_1 \\
       x_2 \\
       x_3
      \end{bmatrix}
      =\begin{bmatrix}
       (1,0,0)\cdot(x_1,x_2,x_3) \\
       (-1,1,0)\cdot(x_1,x_2,x_3) \\
       (0,-1,1)\cdot(x_1,x_3,x_3)
      \end{bmatrix}
      $$
      </div>

   5. Equation in matrix form \\(Ax=b:\begin{bmatrix} 2 & 5 \\\ 3 & 7 \end{bmatrix}\begin{bmatrix} x_1 \\\ x_2 \end{bmatrix}=\begin{bmatrix} b_1 \\\ b_2 \end{bmatrix}\\) replaces \\(\begin{aligned} 2x_1+5x_2=b_1 \\\ 3x_1+7x_2=b_2 \end{aligned}\\)

## Solving Linear Equations

TODO: integrate the ideas in this chapter

1. Vectors and Linear Equations
   * The Matrix Form of the Equations
     Matrix-vector multiplication \\(Ax\\) can be computed by dot products, a row at a time. But \\(Ax\\) must be understood as a *combination of the columns of \\(A\\)*
     Multiplication by rows: \\(Ax=\begin{bmatrix} (\text{\bf{row 1}})\cdot x \\\ (\text{\bf{row 2}})\cdot x \\\ (\text{\bf{row 3}})\cdot x \end{bmatrix}\\)
     Multiplication by columns: \\(Ax=x_1(\text{\bf{column 1}})+x_2(\text{\bf{column 2}})+x_3(\text{\bf{column 3}})\\)
     The **identity matrix** \\(I=\begin{bmatrix} 1 & 0 & 0 \\\ 0 & 1 & 0 \\\ 0 & 0 & 1 \end{bmatrix}\\) always yields the multiplication \\(Ix=x\\)
2. The Idea of Elimination
   Pivot: first nonzero in the row that does the elimination
   Multiplier \\(\ell\\): entry to eliminate divided by pivot
   1. For matrices with \\(m=n=3\\) , there are three equations \\(Ax=b\\) and three unknowns \\(x_1,x_2,x_3\\)
   2. The equations will like \\(\begin{cases} a_{11}x_1+a_{12}x_2+a_{13}x_3=b_1 \\\ a_{21}x_1+a_{22}x_2+a_{23}x_3=b_2 \\\ a_{31}x_1+a_{32}x_2+a_{33}x_3=b_2 \end{cases}\\)
   3. Column 1. Use the first equation to create zeros below the first pivot.
      Column 2. Use the new eqution 2 to create zeros below the second pivot.
      Columns 3. to \\(n\\). keep going to find all \\(n\\) pivots and the upper triangular \\(U\\).
      
      Eliminate \\(x_1\\) from every remaining equation \\(i\\) by subtracing \\(\frac{a_{i1}}{a_{11}}\\) times the first equation.
      We **subtract** \\(\ell_{ij}\\) times equation \\(j\\) from equation \\(i\\) , to make the \\((i,j)\\) entry zero.
   4. Elimination breaks down if zero appears in the pivot. Exchanging two equations may save it.
      When breakdown is permanent, \\(Ax=b\\) has no solution or infinitely many.
   5. Elimination produces an upper triangular system.
      The upper triangular \\(Ux=c\\) is solved by **back substitution** (starting at the bottom).
3. Elimination Using Matrices
   The word "entry" for a matrix corresponds to "componend" for a vector. General rule: \\(a_{ij}=A(i,j)\\) is in row \\(i\\) , column \\(j\\).
   The **identity matrix** has 1's on the diagonal and otherwise 0's. Then \\(Ib=b\\) for all b.
   The **elementary matrix or elimination matrix** \\(E_{ij}\\) has the extra nonzero entry \\(-\ell\\) in the \\(i,j\\) position. Then \\(E_{ij}\\) subtracts a multiple \\(\ell\\) of row \\(j\\) from row \\(i\\).