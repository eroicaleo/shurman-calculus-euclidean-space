# Chapter 3 Linear Mappings and Their Matrices

## 3.1 Linear Mappings

## 3.2 Operations on Matrices

The matrices for the linear mapping

$$ 
S+T : \mathbb{R}^n \longrightarrow \mathbb{R}^m
\qquad
\text{and}
\qquad
aS : \mathbb{R}^n \longrightarrow \mathbb{R}^m
$$

Should be denoted

$$ 
A+B \in M_{m, n}(\mathbb{R})
\qquad
\text{and}
\qquad
aA \in M_{m, n}(\mathbb{R})
$$

the jth column of

$$
A + B = (S + T)(e_j) \\
= S(e_j) + T(e_j) \\
= \text{the sum of the jth columns of A and B}.
$$

### Definition 3.2.1 (Matrix addition).

If $A = [a_{ij}]_{m \times n}$ and $B = [b_{ij}]_{m \times n}$
then $A+B = [a_{ij} + b_{ij}]_{m \times n}$.

### Definition 3.2.2 (Scalar-by-matrix multiplication).

If $α ∈ \mathbb{R}$ and $A = [a_{ij}]_{m \times n}$ then
$αA = [αa_{ij}]_{m \times n}$.

### Proposition 3.2.3 ($M_{m, n}(\mathbb{R})$ forms a vector space).

The set $M_{m, n}(\mathbb{R})$ of $m×n$ matrices forms a vector space over $\mathbb{R}$.

### Composition

If

$$ 
S : \mathbb{R}^n \longrightarrow \mathbb{R}^m
\qquad
\text{and}
\qquad
T : \mathbb{R}^p \longrightarrow \mathbb{R}^n
$$

are linear then their composition.

$$ 
S \circ T : \mathbb{R}^p \longrightarrow \mathbb{R}^m
$$

is linear as well. Suppose that $S$ and $T$ respectively
have matrices

$$
A \in M_{m, n}(\mathbb{R})
\qquad
\text{and}
\qquad
B \in M_{n, p}(\mathbb{R})
$$

Then the composition $S◦T$ has a matrix in $M_{m, p}(\mathbb{R})$
that is naturally defined as the matrix-by-matrix product

$$ 
AB \in M_{m, p}(\mathbb{R}),
$$

the order of multiplication being chosen for consistency with the 
composition. Under this specification,

$$ 
\begin{split}
\text{(A times B)’s jth column}
&= (S◦T)(e_j) \\
&= S(T(e_j)) \\
&= \text{A times (B’s jth column).}
\end{split}
$$

### Definition 3.2.4 (Matrix multiplication).

Given two matrices

$$
A \in M_{m, n}(\mathbb{R})
\qquad
\text{and}
\qquad
B \in M_{n, p}(\mathbb{R})
$$

such that $A$ has as many columns as $B$ has rows, their product,

$$ 
AB \in M_{m, p}(\mathbb{R}),
$$

has for its $(i,j)$th entry
(for every $(i,j) ∈ \{1,...,m\}×\{1,...,p\}$) the inner
product of the $i$th row of $A$ and the $j$th column of $B$. In 
symbols,

$$ 
(AB)_{ij} = ⟨\text{$i$th row of $A$}, \text{$j$th column of $B$}⟩,
$$

or, at the level of individual entries, if
$A = [a_{ij}]_{m \times n}$ and $B = [b_{ij}]_{n \times p}$ 
then 

$$ 
AB = \left[ 
\sum_{k = 1}^{n} a_{ik} b_{kj}
 \right]_{m \times p}
$$

$$ 
\text{(A times B)’s jth column $\quad$ equals $\quad$ A times (B’s 
jth column),} \\
\text{ith row of (A times B) $\quad$ equals $\quad$ (ith row of A) 
times B. }
$$

### Proposition 3.2.5 (Properties of matrix multiplication).

Matrix multiplication is associative:

$$ 
(AB)C = A(BC)
$$

Matrix multiplication distributes over matrix addition:

$$ 
A(B +C) = AB +AC  \\
(A+B)C= AC +BC \\
$$

Scalar multiplication passes through matrix multiplication:

$$ 
α(AB) = (αA)B= A(αB) 
$$

The identity matrix is a multiplicative identity,

$$ 
I_mA= A= AI_n 
$$

**Proof**:

The right way to prove these is intrinsic, by recalling that 
addition, scalar multiplication, and multiplication of matrices 
precisely mirror addition,
scalar multiplication, and composition of mappings.

$$ 
\begin{align*}
((S ◦T)◦U)(x)
&= (S ◦T)(U(x))
&\quad \text{by definition of $R◦U$ where $R= S ◦T$} & \\
&= S(T(U(x)))
&\quad \text{by definition of $S ◦T$} & \\
&= S((T ◦U)(x)) 
&\quad \text{by definition of $T ◦U$} & \\
&= (S ◦(T ◦U))(x) 
&\quad \text{by definition of $S ◦V$ where $V= T ◦U$.} & \\
\end{align*} 
$$

Alternatively, one can verify the equalities elementwise by 
manipulating sums.

> The author finds this method
as grim as it is gratuitous: the coordinates work because they must, 
but their presence only clutters the argument.

## 3.3 The Inverse of a Linear Mapping

Given a linear mapping $S : \mathbb{R}^n \longrightarrow \mathbb{R}^m$, 
does it have an inverse? That is, is
there a mapping $T : \mathbb{R}^m \longrightarrow \mathbb{R}^n$ such that

$$ 
S \circ T = id_m
\quad
\text{and}
\quad
T \circ S = id_n
$$

Note the inverse $T$, if it exists, must be unique,

$$ 
T' = T' \circ id_m = T' \circ (S \circ T) = (T' \circ S) \circ T =
id_n \circ T.
$$

If the inverse $T$ exists then it too is linear.

Assume $y_1, y_2 \in \mathbb{R}^m$, then we can find
$x_1, x_2 \in \mathbb{R}^m$, such that
$S(x_1) = y_1, S(x_2) = y_2$.

Then

$$
\begin{align*}
T(y_1 + y_2)
&= T(S(x_1) + S(x_2))
&\quad \text{above discussion} \\
&= T(S(x_1 + x_2))
&\quad \text{$S$ is linear} \\
&= (T \circ  S)(x_1 + x_2)
&\quad \text{Definition of composition} \\
&= x_1 + x_2
&\quad \text{$T$ inverts $S$} \\
&= T(y_1) + T(y_2)
&\quad \text{above discussion} \\
\end{align*} 
$$

If the equation $Ax = 0_m$ has a nonzero solution
$x \in \mathbb{R}^n$ then $A$ has no inverse.

$$ 
x = (A^{-1} A) x = A^{-1} 0 = 0
$$

We have a contradiction.

### Definition 3.3.1 (Elementary matrices).

* Recombine matrix: (Here the a sits in the (i,j)th position, the diagonal 
  entries are $1$ and all other entries are 0. The $a$ is above the 
  diagonal as shown only when $i < j$; otherwise it is below.)
* Scale matrix: Here the a sits in the ith diagonal position, all other 
  diagonal entries are $1$, and all other entries are $0$.
* Transposition matrix: Here the diagonal entries are 1 except the ith and 
  jth, the (i,j)th and (j,i)th entries are 1, and all other entries are 0.

### Proposition 3.3.2 (Eﬀects of the elementary matrices).

Let $M$ be an $m×n$ matrix; call its rows $r_k$. Then:

(1) The $m×n$ matrix $R_{i;j,a}M$ has the same rows as $M$ except that its ith row
is $r_i +ar_j$.

(2) The $m×n$ matrix $S_{i,a}M$ has the same rows as $M$ except that its ith row
is $ar_i$.

(3) The $m×n$ matrix $T_{i;j}M$ has the same rows as $M$ except that its ith row
is $r_j$ and its jth row is $r_i$.

### Lemma 3.3.3 (Invertibility of products of the elementary matrices).

Products of elementary matrices are invertible. More specifically:
(1) The elementary matrices are invertible by other elementary matrices.
Specifically,

$$ 
(R_{i;j,a})^{−1} = R_{i;j,-a},
\quad
(S_{i,a})^{−1} = S_{i,a^{-1}} , 
\quad
(T_{i;j})^{−1} = T_{i;j}.
$$

$\square$

(2) If the m×m matrices $M$ and $N$ are invertible by $M^{−1}$ and $N^{−1}$, then the
product matrix $MN$ is invertible by $N^{−1}M^{−1}$. (Note the order reversal.)

(3) Every product of elementary matrices is invertible by another such product,
specifically the product of the inverses of the original matrices, but taken
in reverse order.

$\square$

### Proposition 3.3.4 (Persistence of solution).

Let $A$ be an $m × n$ matrix and let $P$ be a product of $m×m$ elementary matrices.
Then the equations

$$ 
Ax= 0_m
\quad
\text{and}
\quad
(PA)x = 0_m
$$

are satisfied by the same vectors $x$ in $\mathbb{R}^n$.

$\square$

### Definition 3.3.5 (Echelon matrix).

A matrix $E$ is called echelon if it has the form

$$ 
E =
\begin{bmatrix}
0 & \cdots & 0 & 1 & * & \cdots & * & 0 & * & \cdots & * & 0 & * & \cdots \\
  &        &   &   &   &        &   & 1 & * & \cdots & * & 0 & * & \cdots \\
  &        &   &   &   &        &   &   &   &        &   & 1 & * & \cdots \\
  &        &   &   &   &        &   &   &   &        &   &   &   &        \\
\end{bmatrix}
$$

Here the $∗$'s are arbitrary entries, and all entries below the stairway are $0$.
Thus each row’s first nonzero entry is a $1$, each row’s leading $1$ is farther right
than that of the row above it, each leading $1$ has a column of $0$’s above it, and
any rows of $0$’s are at the bottom.

$\square$

### Theorem 3.3.6 (Matrices reduce to echelon form).

Every matrix $A$ row reduces to a unique echelon matrix $E$.

In an echelon matrix $E$, the columns with leading $1$'s are called
**new columns**, and all others are **old columns**.

### Theorem 3.3.7 (Invertibility and echelon form for matrices).

A nonsquare matrix $A$ is never invertible. A square matrix $A$ is invertible if and
only if its echelon form is the identity matrix.

### Proposition 3.3.8 (Matrix inversion algorithm).

Given $A ∈ M_n(\mathbb{R}^n)$, set up the matrix

$$ 
B = [A | I_n]
$$

in $M_{n,2n}(\mathbb{R}^n)$. Carry out row operations on this matrix to reduce the
left side to echelon form. If the left side reduces to In then $A$ is invertible and
the right side is $A^{−1}$. If the left side doesn’t reduce to In then $A$
is not invertible.

### Theorem 3.3.9 (Echelon criterion for invertibility).

The linear mapping $S : \mathbb{R}^n \longrightarrow \mathbb{R}^m$ is invertible only when
 $m = n$ and its matrix $A$ has
echelon matrix $I_n$, in which case its inverse $S^{−1}$ is the linear mapping with
matrix $A^{−1}$ .

$\square$

