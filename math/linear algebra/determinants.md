---
tags:
  - math
  - linear-algebra
  - matrices
  - determinants
---

# Determinants
A determinant is only defined for square [matrices](<math/linear algebra/matrices>), i.e. matrices with an $n \times n$ dimension. This operation is denoted with the absolute value sign: $\lvert A \rvert$.

## Fundamental Determinant
The __fundamental determinant__  is for a $2 \times 2$ matrix defined by 
$$\lvert A \rvert = ad - bc$$

where
$$
A = \begin{bmatrix} 
    a & b\\
    c & d\\
\end{bmatrix}
$$

## Determinants for a $3 \times 3$ Matrix

For a $3 \times 3$ matrix, we can find the determinant using __Cofactor Expansion__. We multiply the elements, the cofactor, in the top row by the determinant of the matrix obtained by deleting the row and column of the cofactor.
$$
\begin{align*}
\begin{vmatrix} 
    a & b & c\\
    d & e & f\\
    g & h & i\\
\end{vmatrix}
&=
a \begin{vmatrix} e & f\\ h & i\\ \end{vmatrix} -
b \begin{vmatrix} d & f\\ g & i\\ \end{vmatrix} +
c \begin{vmatrix} d & e\\ g & h\\ \end{vmatrix} \\
&= a(ei - fh) - b(di - fg) + c(dh - eg) \\
\end{align*}
$$

We are __expanding__ about the first row.

### Generalizing Cofactor Expansion
We can generalize this method by being able to expand about any row or column we want and for any $n \times n$ matrix where $n \ge 2$. Cofactor expansion can be generalized into
$$
\sum{(-1)^{i+j}\lvert M_{ij}\rvert}
$$

where $i$ and $j$ are the $i^\text{th}$ row and $j^\text{th}$ column of the cofactor, respectively, and $M_{ij}$ is the matrix obtained by deleting the $i^\text{th}$ and $j^\text{th}$ row and column of the matrix, respectively.

It can be more helpful by remembering this sign chart of alternating pluses and minuses.
$$
\begin{bmatrix}
+ & - & + & - & \dots\\
- & + & - & + & \dots\\
+ & - & + & - & \dots\\
- & + & - & + & \dots\\
\vdots & \vdots & \vdots & \vdots & \ddots\\ 
\end{bmatrix}
$$

For example, the determinant of a $3 \times 3$ matrix expanded about the second column is
$$
\begin{align*}
\begin{vmatrix} 
    a & b & c\\
    d & e & f\\
    g & h & i\\
\end{vmatrix}
&=
-b \begin{vmatrix} d & f\\ g & i\\ \end{vmatrix} +
e \begin{vmatrix} a & c\\ g & i\\ \end{vmatrix} -
h \begin{vmatrix} a & c\\ d & f\\ \end{vmatrix} \\
&= -b(di - fg) + e(ai - cg) - h(af - cd) \\
\end{align*}
$$

## Triangular Matrices
The determinant for any [triangular](<math/linear algebra/matrices#Triangular Matrices>) and anti-triangular matrix is simply the product of the elements in their respective diagonal. This also applies to [diagonal matrices](<math/linear algebra/matrices#Diagonal Matrices>).
$$
\begin{vmatrix}
    a & 0 & 0\\
    x & b & 0\\
    y & z & c\\
\end{vmatrix}
=
\begin{vmatrix}
    x & y & a\\
    z & b & 0\\
    c & 0 & 0\\
\end{vmatrix}
= abc
$$

The proof can be trivially shown by using cofactor expansion and expanding about the row with only one non-zero element.

## Identity Matrices
The determinant of any [identity matrix](<math/linear algebra/matrices#Identity Matrix>) is $1$. The proof can be trivially shown by using cofactor expansion and expanding about the first row.