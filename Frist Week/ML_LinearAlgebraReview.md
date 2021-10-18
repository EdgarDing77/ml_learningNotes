# ML Linear Algebra Review

# Matrix and Vectors

参考学习：https://zhuanlan.zhihu.com/p/25197792，该部分主要是一些基本数学的复习。

- **Matrix:** Rectangular array of numbers
- **Diemnsion of matrix(数组的维度):** number of rows x number of cloumns

- **Vector:** An n x 1 matrix

**Notation and terms**:

- $A_{ij}$ refers to the element in the $i^th$ row and $j^th$ column of matrix A.
- A vector with 'n' rows is referred to as an 'n'-dimensional vector.
- $v_i$refers to the element in the ith row of the vector.
- In general, all our vectors and matrices will be 1-indexed. Note that for some programming languages, the arrays are 0-indexed.
- Matrices are usually denoted by uppercase names while vectors are lowercase.
- "Scalar" means that an object is a single value, not a vector or matrix.
- $\mathbb{R}$ refers to the set of scalar real numbers.
- $\mathbb{R^n}$ refers to the set of n-dimensional vectors of real numbers.

```python
% The ; denotes we are going back to a new row.
A = [1, 2, 3; 4, 5, 6; 7, 8, 9; 10, 11, 12]

% Initialize a vector 
v = [1;2;3] 

% Get the dimension of the matrix A where m = rows and n = columns
[m,n] = size(A)

% You could also store it this way
dim_A = size(A)

% Get the dimension of the vector v 
dim_v = size(v)

% Now let's index into the 2nd row 3rd column of matrix A
A_23 = A(2,3)

```

## Addition and Scalar Multiplication

Addition（增量）Scalar（标量）

Matrix and Vector addtion and scalar

## Matrix Vector/Matrix Multiplication

### Matrix Vector Multiplication

The result is a **vector**. The number of **columns** of the matrix must equal the number of **rows** of the vector.

An **m x n matrix** multiplied by an **n x 1 vector** results in an **m x 1 vector**.

### Matrix Matrix Multiplication

Commutative 交换律

A x B != B x A(not commutative)

Associative 结合律

(A x B) x C == A x (B x C)

**Identity Matrix 单位矩阵: Denoted I**

For any matrix A, A \* I == I, A == A

## Inverse and Transpose

Inverse（反转 逆矩阵）Transpose（倒置）

**Matrix inverse: $AA^{-1} = A^{-1}A = I$**

![img](https://cdn.jsdelivr.net/gh/edgarding77/images@latest/ML_learningNotes/matrix_inverse.png)

参考：https://www.q-math.com/?p=2056

**Matrix Transpose: $A^T$**

矩阵的转置：设$A$为$m×n$阶矩阵（即$m$行$n$列），第$i $行$j $列的元素是$a(i,j)$，即：$A=a(i,j)$

定义$A$的转置为这样一个$n×m$阶矩阵$B$，满足$B=a(j,i)$，即 $b (i,j)=a(j,i)$（$B$的第$i$行第$j$列元素是$A$的第$j$行第$i$列元素），记${{A}^{T}}=B$。(有些书记为A'=B）

直观来看，将$A$的所有元素绕着一条从第1行第1列元素出发的右下方45度的射线作镜面反转，即得到$A$的转置。

$ {{\left( A\pm B \right)}^{T}}={{A}^{T}}\pm {{B}^{T}} $ ${{\left( A\times B \right)}^{T}}={{B}^{T}}\times {{A}^{T}}$ ${{\left( {{A}^{T}} \right)}^{T}}=A $ ${{\left( KA \right)}^{T}}=K{{A}^{T}} $

