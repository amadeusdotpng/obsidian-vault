---
tags:
  - math
  - linear-algebra
  - matrices
  - matrix-multiplication
  - triangular-matrix
  - diagonal-matrix
  - identity-matrix
---
# Matrices

A matrix is an $m \times n$ array of numbers denoted as: $A =[a_{jk}]$ where $1 \le j \le m$ and $1 \le k \le n$.
$$
\begin{bmatrix}
    1 & 2 & 3\\
    3 & 1 & 2\\
    2 & 3 & 1\\
\end{bmatrix}
\text{ is a 3$\times$3 matrix}
$$

---

## Matrix Addition
Matrices must have the same dimensions.
$$
\begin{bmatrix}
    a & b\\
    c & d\\
\end{bmatrix}
+
\begin{bmatrix}
    x & y\\
    z & w\\
\end{bmatrix}
=
\begin{bmatrix}
    a + x & b + y\\
    c + z & d + w\\
\end{bmatrix}
$$

## Scalar Multiplication
$$
x
\begin{bmatrix}
    a & b\\
    c & d\\
\end{bmatrix}
=
\begin{bmatrix}
    ax & bx\\
    cx & dx\\
\end{bmatrix}
$$

## Matrix Multiplication
Given matrices $A$ and $B$, they can only be multiplied together, $AB$, if $A$ has the dimension $m \times n$ and $B$ has the dimension $n \times p$ where $AB$ is a $m \times p$ matrix. Matrix multiplication is __not__ commutative.

To multiply two matrices together, an element in the $j^\text{th}$ row and $k^\text{th}$ column is $\langle r_j \rangle \cdot \langle c_k \rangle$ where $\langle r_j \rangle$ is the $j^\text{th}$ row vector of $A$ and $\langle c_k \rangle$ is the $k^\text{th}$ column vector of $B$.

Given 
$$
A = \begin{bmatrix}
    a & b\\
    c & d\\
    e & f\\
\end{bmatrix},\enspace
B = \begin{bmatrix}
    x & y\\
    z & w\\
\end{bmatrix}
$$
then
$$
AB = \begin{bmatrix}
    ax + bz & ay + bw\\
    cx + dz & cy + dw\\
    ex + fz & ey + fw\\
\end{bmatrix}
$$

Given that $A$ is an $m \times n$ matrix, then $AI_m = AI_n = A$.

## Matrix Transpose
Given that $A$ is an $m \times n$ matrix, then $A^T$ is an $n \times m$ matrix s.t. the rows of $A$ is rewritten as columns.
$$
A = \begin{bmatrix}
    a & b\\
    c & d\\
    e & f\\
\end{bmatrix}
\iff A^T = \begin{bmatrix}
    a & c & e\\
    b & d & f\\
\end{bmatrix}
$$

---

## Properties of Matrix Arithmetic
1. Commutative: $A + B = B + A$
2. Associative: $(A + B) + C = A + (B + C)$
3. Distributive:
    - $c(A + B) = cA + cB$
    - $(c + d)A = cA + dA$

## Properties of Matrix Multiplication
1. Associative: $A(BC) = (AB)C$
2. Distributive: $A(B+C) = AB + AC$
3. Scalar Commutative: $c(AB) = (cA)B = A(cB)$

## Properties of Matrix Transpose
1. $(A^T)^T = A$
2. $(A + B)^T = A^T + B^T$
3. $(AB)^T = B^TA^T$

---

## Special Matrices
There are certain matrices with interesting properties.

### Identity Matrix
The __identity matrix__, denoted as $I_n$ is an $n \times n$ matrix where the main diagonal is filled with $1$ and all other elements are $0$. 
$$
I_n = \begin{bmatrix}
    1 & 0 & \dots & 0\\
    0 & 1 & \dots & 0\\
    \vdots & \vdots & \ddots  &\vdots\\
    0 & 0 & \dots & 1\\
\end{bmatrix}
$$

### Triangular Matrices
__Triangular__ matrices are square matrices whose elements above or below the main diagonal are all zero. If all elements _above_ the main diagonal are zero, it is a _lower triangular_ matrix. If all elements _below_ the main diagonal are zero, it is an _upper triangular_ matrix.

This is a lower triangular matrix.
$$
\begin{bmatrix}
    a & 0 & 0\\
    b & c & 0\\
    d & e & f\\
\end{bmatrix}
$$

This is an upper triangular matrix.
$$
\begin{bmatrix}
    a & b & c\\
    0 & d & e\\
    0 & 0 & f\\
\end{bmatrix}\\
$$

__Anti-triangular__ matrices are simply triangular matrices but applied to the antidiagonal. 
$$
\begin{bmatrix}
    0 & 0 & a\\
    0 & b & c\\
    d & e & f\\
\end{bmatrix}\\
$$

### Diagonal Matrices
__Diagonal__ matrices are square matrices whose elements outside of the main diagonal are zero.
$$
\begin{bmatrix}
    a & 0 & 0\\
    0 & b & 0\\
    0 & 0 & c\\
\end{bmatrix}\\
$$

__Anti-diagonal__ matrices, similar to Anti-triangular matrices, are simply diagonal matrices applied to the antidiagonal.
$$
\begin{bmatrix}
    0 & 0 & a\\
    0 & b & 0\\
    c & 0 & 0\\
\end{bmatrix}\\
$$