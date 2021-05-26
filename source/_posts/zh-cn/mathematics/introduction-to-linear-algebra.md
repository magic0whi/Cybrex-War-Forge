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

TODO: keep all the vector symbols have a boldface style.

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
     \\[\textbf{Income}=(q_1,q_2,q_3)\cdot(p_1,p_2,p_3)=q_1p_1+q_2p_2+q_3p_3\\]
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
     Multiplication by rows: \\(Ax=\begin{bmatrix} (\textbf{row 1})\cdot x \\\ (\textbf{row 2})\cdot x \\\ (\textbf{row 3})\cdot x \end{bmatrix}\\)
     Multiplication by columns: \\(Ax=x_1(\textbf{column 1})+x_2(\textbf{column 2})+x_3(\textbf{column 3})\\)
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
   1. The Matrix Form of One Elimination Step
      The **identity matrix** has 1's on the diagonal and otherwise 0's. Then \\(Ib=b\\) for all b.
      The **elementary matrix or elimination matrix** \\(E_{ij}\\) has the extra nonzero entry \\(-\ell_{ij}\\) in the \\(i,j\\) position. Then \\(E_{ij}\\) subtracts a multiple \\(\ell_{ij}\\) of row \\(j\\) from row \\(i\\).
      The purpose of \\(E_{31}\\) is to product a zero in the \\((3,1)\\) position of the matrix.
   2. Matrix Multiplication
      Associative law is true: \\(A(BC)=(AB)C\\)
      Commutative law is false: \\(\text{Often}\enspace AB\neq BA\\)
      Matrix multiplication \\(AB=A\begin{bmatrix} b_1 & b_2 & b_3 \end{bmatrix}=\begin{bmatrix} Ab_1 & Ab_2 & Ab_3 \end{bmatrix}\\)
   3. The Matrix \\(P_{ij}\\) for a Row Exchange
      A row exchange is needed when zero is in the pivot position.
      **Row Exchange Matrix**: \\(P_{ij}\\) is the identity matrix with rows \\(i\\) and \\(j\\) reversed.
      When this "**permutation matrix**" \\(P_{ij}\\) multiplies a matrix, it exchanges rows \\(i\\) and \\(j\\)
      for example: to exchange equations 1 and 3 multiply by \\(P_{13}=\begin{bmatrix} 0 & 0 & 1 \\\ 0 & 1 & 0 \\\ 1 & 0 & 0 \end{bmatrix}\\)
   4. The Augmented Matrix
      Elimination does the same row operations to \\(A\\) and to \\(b\\) . We can include \\(b\\) as an extra column and follow it through elimination. The matrix \\(A\\) is enlarged or "augmented" by the extra column \\(b\\) :
      \\(\begin{bmatrix} A & b \end{bmatrix}=\begin{bmatrix} 2 & 4 & -2 & \mathbf{2} \\\ 4 & 9 & -3 & \mathbf{8} \\\ -2 & -3 & 7 & \mathbf{10} \end{bmatrix}\\)
      For the augmented matrix \\(\begin{bmatrix} A & b \end{bmatrix}\\) , that first elimination step gives \\(\begin{bmatrix} E_{21}A & E_{21}b \end{bmatrix}\\)

   Elimination multiplies \\(Ax=b\\) by \\(E_{21},E_{31},\dots,E_{n1}\\) , then \\(E_{32},E_{42},\dots,E_{n2}\\) , and onward.
4. Rules for Matrix Operations
   1. To multiply \\(AB\\) , if \\(A\\) has \\(n\\) columns, \\(B\\) must have \\(n\\) rows.
   2. Matrices \\(A\\) with \\(n\\) columns multiply matrices \\(B\\) with \\(n\\) rows: \\(\boxed{A_{m\times n}B_{n\times p}=C_{m\times p}}\\)
   3. Each entry in \\(AB=C\\) is a dot product: \\(C_{ij}=(\text{row }i\text{ of }A)\cdot(\text{column }j\text{ of }B))\\)
   4. The second, third and fourth way to compute \\(AB\\):
      * Matrix \\(A\\) times every column of \\(B\\) : \\(A\begin{bmatrix} b_1 & \cdots & b_p \end{bmatrix}=\begin{bmatrix} Ab_1 & \cdots & Ab_p \end{bmatrix}\\)
      * Every row of \\(A\\) times matrix \\(B\\) : \\(\begin{bmatrix} \text{row }i\text{ of }A \end{bmatrix}B=\begin{bmatrix} \text{row }i\text{ of }AB \end{bmatrix}\\)
      * Multiply columns 1 to \\(n\\) of \\(A\\) times rows 1 to \\(n\\) of \\(B\\). Add those matrices:
        <div>
        $$
        \begin{bmatrix}
         \text{col 1} & \text{col 2} & \text{col 3} \\
         \cdot & \cdot & \cdot \\
         \cdot & \cdot & \cdot
        \end{bmatrix}
        \begin{bmatrix}
         \text{row 1} & \cdot & \cdot & \cdot \\
         \text{row 2} & \cdot & \cdot & \cdot \\
         \text{row 3} & \cdot & \cdot & \cdot
        \end{bmatrix}
        =(\text{col 1})(\text{row 1})+(\text{col 2})(\text{row 2})+(\text{col 3})(\text{row 3})
        $$
        </div>
   5. Block multiplication: If blocks of \\(A\\) can multiply blocks of \\(B\\) , then block multiplication of \\(AB\\) is allowed. Cuts between columns of \\(A\\) match cuts between rows of \\(B\\):
      \\(\begin{bmatrix} A_{11} & A_{12} \\\ A_{21} & A_{22} \end{bmatrix}\begin{bmatrix} B_{11} \\\ B_{21} \end{bmatrix}=\begin{bmatrix} A_{11}B_{11}+A_{12}B_{21} \\\ A_{21}B_{11}+A_{22}B_{21} \end{bmatrix}\\)
   6. Block elimination: \\(\left[\begin{array}{c|c} I & 0 \\\ \hline -CA^{-1} & I \end{array}\right]\left[\begin{array}{c|c} A & B \\\ \hline C & D \end{array}\right]=\left[\begin{array}{c|c} A & B \\\ \hline 0 & D-CA^{-1}B \end{array}\right]\\)
      The final block \\(D-CA^{-1}B\\) is called ***Schur complement***
5. Inverse Matrices
   1. The inverse matrix gives \\(A^{-1}A=I\\) and \\(AA^{-1}=I\\)
   2. The *algorithm* to test invertibility is elimination: \\(A\\) must have \\(n\\) (nonzero) pivots.
      The *algebra* test for invertibility is the determinant of \\(A\\) : det \\(A\\) must not be zero.
   3. *Important*. If \\(Ax=0\\) for a nonzero vector \\(x\\) , then \\(A\\) has no inverse.
      ***Suppose there is a nonzero vector \\(x\\) such that*** \\(Ax=0\\) . *Then \\(A\\) cannot have an inverse*. No matrix can bring 0 back to \\(x\\)
   4. The Inverse of a Product \\(AB\\)
      If \\(A\\) and \\(B\\) are invertible then so is \\(AB\\) . The inverse of a product \\(AB\\) is \\((AB)^{-1}=B^{-1}A^{-1}\\)
   5. Calculating \\(A^{-1}\\) by Gauss-Jordan Elimination
      \\(AA^{-1}=I\\) is \\(n\\) equations for \\(n\\) columns of \\(A^{-1}\\) . Gauss-Jordan eliminates \\(\begin{bmatrix} A & I \end{bmatrix}\\) to \\(\begin{bmatrix} I & A^{-1}\end{bmatrix}\\) :
   6. Recognizing an Invertible Matrix
      **Diagonally dominant matrices are invertible.** Each \\(a_{ii}\\) on the diagonal is larger than the total sum along the rest of row \\(i\\) . On every row,
      \\[|a_{ii}|>\sum_{j\neq i}|a_{ij}\\]
6. Elimination = Factorization: \\(A=LU\\)
   1. Gaussian elimination (with no row exchanges) factors \\(A\\) into \\(L\\) times \\(U\\)
   1. Each elimination step \\(E_{ij}\\) in inverted by \\(E_{ij}^{-1}=L_{ij}\\) . Off the main diagonal change \\(-\ell_{ij}\\) to \\(+\ell_{ij}\\)
   2. The whole forward elimination process (with no row exchanges) is inverted by \\(L\\) :
      \\[\bm{L}=(L_{21}L_{31}\dots L_{n1})(L_{32}\dots L_{n2})(L_{43}\dots L_{n3})\dots(L_{nn-1})\\]
   3. That product matrix \\(L\\) is still lower trignaular. **Every multiplier \\(\bm{\ell_{ij}}\\) is in row \\(\bm{i}\\) , column \\(\bm{j}\\)**
   4. The original \\(A\\) is recovered from \\(U\\) by \\(\bm{A=LU}=(\text{lower triangular})(\text{upper triangular})\\)
      * **Better balance from LDU**
        ***Divide \\(\bm{U}\\) by a diagonal matrix \\(\bm{D}\\) that contains the pivots:***
        Split \\(U\\) into \\(\begin{bmatrix} d_1 & & & \\\ & d_2 & & \\\ & & \ddots & \\\ & & & d_n \end{bmatrix}\begin{bmatrix} 1 & \frac{u_{12}}{d_1} & \frac{u_{13}}{d_1} & \cdot \\\ & 1 & \frac{u_{23}}{d_2} & \cdot \\\ & & \ddots & \vdots \\\ & & & 1 \end{bmatrix}\\)

   5. Elimination on \\(Ax=b\\) reaches \\(Ux=c\\) . Then back-substitution solves \\(Ux=c\\)
      (\\(Ax=b\rArr LUx=b\rArr Ux=L^{-1}b=c\\))
   6. Solving a triangular system takes \\(\frac{n^2}{2}\\) multiply-subtracts. Elimination to find \\(U\\) takes \\(\frac{n^3}{3}\\)
7. Transposes and Permutations
   1. Transpose exchange rows and columns: \\((A^T)\_{ij}=A\_{ji}\\)
   2. The transposes of:
      | | |
      |-|-|
      | Sum | The transpose of \\(A+B\\) is \\(A^T+B^T\\) |
      | Product | The transpose of \\(AB\\) is \\((AB)^T=B^TA^T\\) |
      | Inverse | The transpose of \\(A^{-1}\\) is \\((A^{-1})^T=(A^T)^{-1}\\) |
      The reverse order rule extends to three or more factors: \\((ABC)^T\\) equals \\(C^TB^TA^T\\)
      * Product proof:
        To understand \\((AB)^T=B^TA^T\\) , start with \\((Ax)^T=x^TA^T\\) when \\(B\\) is just a vector:
        ***\\(\bm{Ax}\\) combines the columns of \\(\bm{A}\\) while \\(\bm{x^TA^T}\\) combines the rows of \\(\bm{A^T}\\)***\\((x^TA^T=x_1\cdot(\textbf{row 1})+x_2\cdot(\textbf{row 2})+x_3\cdot(\textbf{row 3}))\\)
        Now we can prove the formula \\((AB)^T=B^TA^T\\) , when \\(B\\) has several columns.
        Transposing \\(AB=\begin{bmatrix} Ab_1 & Ab_2 & \cdots \end{bmatrix}\\) gives \\(\begin{bmatrix} b_1^TA^T \\\ b_2^TA^T \\\ \vdots \end{bmatrix}\\) which is \\(B^TA^T\\)
      * Inverse proof:
        Transpose of inverse \\(A^{-1}A=I\\) is transposed to \\(A^T(A^{-1})^T=I\rArr(A^{-1})^T=(A^T)^{-1}\\)
   3. The dot product (inner product) is \\(x\cdot y=x^Ty\\) . This is \\((1\times n)(n\times 1)=(1\times 1)\\) matrix.
      The outer product is \\(xy^T=\\) column times row \\(=(n\times 1)(1\times n)=n\times n\\) matrix.
   4. The idea behind \\(A^T\\) is that \\(Ax\cdot y=x\cdot A^Ty\\) because \\((Ax)^Ty=x^TA^Ty=x^T(A^Ty)\\)
   5. A **symmetric matrix** has \\(S^T=S\\) (and the product \\(A^TA\\) is always symmetric, because the transpose of \\(A^TA\\) is \\(A^T(A^T)^T=A^TA\\))
      ***If \\(S=S^T\\) is factored into \\(LDU\\) with no row exchanges, then \\(U\\) is exactly \\(L^T\\) , which is \\(S=LDL^T\\)***
   6. Permutation Matrices
      There are \\(n!\\) permutation matrices of size \\(n\\). *Half even, half odd.*
      Permutation Matrices are even with Orthogonal Matrix \\(Q\\) (The columns of \\(Q\\) are orthogonal unit vectors.) 
   7. Transpose in Permutation Matrices: **\\(\bm{P^{-1}=P^T}\\)**
   8. The \\(PA=LU\\) Factorization with Row Exchanges
      If \\(A\\) is invertible then a permutation \\(P\\) will reorder its rows for \\(PA=LU\\)
      > Sometimes row exchanges are needed to produce pivots. Then \\(A=(E^{-1}\cdots P^{-1}\cdots E^{-1}\cdots P^{-1})U\\).
      > (Every row exchange is carried out by a \\(P_{ij}\\) and inverted by that \\(P_{ij}\\)).
      > The main question is where to collect the \\(P_{ij}\\)'s. There are two good possibilities:
      > 1. The row exchanges can be done *in advance*. Their product \\(P\\) puts the rows of \\(A\\) in the right order, so that no exchanges are needed for \\(PA\\). ***Then \\(\bm{PA=LU}\\)***.
      > 2. If we hold row exchanges until *after elimination*, the pivot rows are in a strange order. \\(P_1\\) puts them in the correct triangular order in \\(U_1\\). ***Then \\(\bm{A=L_1P_1U}\\)***
      >
      > \\(PA=LU\\) is constantly used in all computing. **We will concentrate on this form**.

## Vector Spaces and Subspaces

1. Spaces of Vectors
   1. The standard \\(n\\)-dimensional space \\(\textbf{R}^n\\) contains all real column vectors with \\(n\\) components.
     (The components of \\(v\\) are real numbers, which is the reason for the letter \\(\textbf{R}\\). A vector whose \\(n\\) components are complex numbers lies in the space \\(\textbf{C}^n\\))
   2. If \\(v\\) and \\(w\\) are in a **vector space** \\(\bm{S}\\) , every combination \\(c\\bm{v}+d\bm{v}\\) must be in \\(\bm{S}\\) .
   3. \\(\textbf{M}\\) : The vector space of ***all real 2 by 2 matrices***.
      \\(\textbf{F}\\) : The vector space of ***all real functions*** \\(f(x)\\) .
      \\(\textbf{Z}\\) : The vector space that consists only of a ***zero vector***.
   4. A **subspace** of \\(\textbf{R}^n\\) is a vector space inside \\(\textbf{R}^n\\).
      Here is a list of all the possible subspaces of \\(\textbf{R}^3\\) :
      <div>
      $$
      \boxed{\begin{array}{ll}
      (\textbf{L}) \text{ Any line through } (0,0,0) & (\textbf{R}^3) \text{ The whole space} \\
      (\textbf{P}) \text{ Any plane through } (0,0,0) & (\textbf{Z}) \text{ The single vector } (0,0,0)
      \end{array}}
      $$
      </div>

      ***A subspace containing \\(\bm{v}\\) and \\(\bm{w}\\) must contain all linear combinations \\(c\bm{v}+d\bm{w}\\)***
   5. The **column space** of \\(A\\) (called \\(\bm{C}(A)\\)) contains all combinations of the columns of \\(A\\) (A subspace of \\(\textbf{R}^m\\)) .
      Reverse, the column space is "spanned" by the columns of \\(A\\) .
   6. The column space contains all the vectors \\(Ax\\) . So \\(A\bm{x}=b\\) is solvable when \\(b\\) is in \\(\bm{C}(A)\\)
2. **The Nullspace of A: Solving \\(\bm{Ax=0}\\) and \\(\bm{Rx=0}\\)**
   1. The **nullspace** \\(\bm{N}(A)\\) in \\(\bm{R}^n\\) contains all solutions \\(x\\) to \\(A\bm{x}=0\\) . This includes \\(\bm{x}=0\\)
   2. Elimination (from \\(A\\) to \\(R\\)) does not change the nullspace: \\(\bm{N}(A)=\bm{N}(U)=\bm{N}\(R\)\\)
   3. When \\(A\\) is rectangular, elimination will not stop at the uppertriangular \\(U\\) .
      We can continue to make this matrix somplex, in two ways. These steps bring us to the best matrix -- reduced row echelon matrix \\(R\\) :
      1. ***Produce zeros above the pivots*.** Use pivot rows to eliminate upward in \\(\bm{R}\\) .
      2. ***Produce ones in the pivots.*** Divice the whole pivot row by its pivot
      
      The **reduced row echelon from \\(\bm{R=\textbf{rref}(A)}\\)** has all pivots \\(=1\\) , with zeros above and below.
   4. Every free column leads to a special solution.
      If column \\(j\\) of \\(R\\) is free (no pivot), there is a ***"special solution"*** to \\(Ax=0\\) with \\(x_j=1\\) , and the other free variables are 0.
   5. Number of pivots \\(=\\) number of nonzero rows in \\(R=\textbf{rank r}\\) . There are \\(n-r\\) free columns.
      The complete solution to \\(Ax=0\\) is a combination of the \\(n-r\\) special solutions.
   6. Every matrix with \\(m<n\\) has nonzero solutions to \\(Ax=0\\) in nullspace.
3. The Complete Solution to \\(Ax=b\\)
   1. **Complete solution** to \\(A\bm{x}=\bm{b}\\) : \\(\bm{x}=(\text{one particular solution }\bm{x_p})+(\text{any }\bm{x_n}\text{ in the nullspace})\\) .
   2. \\(A\bm{x}=\bm{b}\\) and \\(R\bm{x}=\bm{d}\\) are solvable only when all zero rows of \\(R\\) have zeros in \\(\bm{d}\\) .
   3. When \\(R\bm{x}=\bm{d}\\) is solvable, ony very particular solution \\(\bm{x_p}\\) has all free variables qeual to zero.
   4. ***The four possibilities for linear equations depend on the rank \\(\bm{r}\\)***
      <div>
      $$
      \begin{array}{llll}
       r=m\text{ and }r=m & \textit{Square and invertible} & R=\begin{bmatrix} I \end{bmatrix} & Ax=b\text{ has 1 solution} \\
       r=m\text{ and }r\lt m & \textit{Short and wide} & R=\begin{bmatrix} I & F \end{bmatrix} & Ax=b\text{ has }\infty\text{ solutions} \\
       r\lt m\text{ and }r=n & \textit{Tall and thin} & R=\begin{bmatrix} I \\ 0 \end{bmatrix} & Ax=b\text{ has 0 or 1 solution} \\
       r\lt m\text{ and }r\lt n & \textit{Not full rank} & R=\begin{bmatrix} I & F \\ 0 & 0 \end{bmatrix} & Ax=b\text{ has 0 or }\infty\text{ solutions}
      \end{array}
      $$
      </div>

      \\(F\\) means free matrix.
      Full column rank \\(r=n\\) means no free variables, its nullspace \\(\bm{N}(A)=\\) zero vector
      Full row rank \\(r=m\\) means one solution if \\(m=n\\) or infinitely many if \\(m<n\\) , its column space \\(\bm{C}(A)\\) is \\(\textbf{R}^m\\) , \\(A\bm{x}=\bm{b}\\) is always solvable.
4. Independence, Basis and Dimension
   1. **Independent columns** of \\(A\\) : The only solution to \\(Ax=0\\) is \\(x=0\\) . The nullspace is \\(Z\\) .
   2. Independent vectors: The only zero combination \\(c_1v_1+\dots+c_kv_k=0\\) has all \\(c\\)'s \\(=0\\)
   3. A matrix with \\(m<n\\) has **dependnt columns**: At least \\(n-m\\) free variables/special solutions.
   4. The vectors \\(v_1,\dots,v_k\\) **span the space S** if \\(S=\\) all combinations of the \\(v\\)'s.
   5. The vectors \\(v_1,\dots,v_k\\) are a **basis for S** if they are independent and they span \\(S\\) .
   6. The **dimension of a space S** is the number of vectors in every basis for **S**.
   7. If \\(A\\) is 4 by 4 and invertible, its columns are a basis for \\(\textbf{R}^4\\) . The dimension of \\(\textbf{R}^4\\) is 4.
5. Dimensions of the Four Subspaces
   1. Four Fundamental Subspaces
      1. The ***row space*** is \\(\bm{C}(A^T)\\) , a subspace of \\(\textbf{R}^n\\) .
      2. The ***column space*** is \\(\bm{C}(A)\\) , a subspace of \\(\textbf{R}^m\\) .
      3. The ***nullspace*** is \\(\bm{N}(A)\\) , a subspace of \\(\textbf{R}^n\\) .
      4. The ***left nullspace*** is \\(\bm{N}(A^T)\\) , a subspace of \\(\textbf{R}^m\\) . This is our new space.
   2. The column space \\(C(A)\\) and the row space \\(C(A^T)\\) both have *dimension* \\(r\\) (the rank of \\(A\\))
   3. The nullspace \\(\bm{N}(A)\\) has *dimension* \\(n-r\\) . The left nullspace \\(\bm{N}(A^T)\\) has *dimension* \\(m-r\\) .
   4. Elimination produces bases for the row space and nullspace of \\(A\\) :
      They are the same as for \\(R\\) .
      Notice \\(\bm{C}(A)\neq\bm{C}\(R\)\\) , elimination often changes the column space and left nullspace (but dimensions don't change).
   5. **Rank one matrices** : 
      \\(\bm{C}(A)\\) has basis \\(\bm{u}\\) , \\(\bm{C}(A^T)\\) has basis \\(v\\) , then \\(A=\bm{uv}^T=\\) column times row.