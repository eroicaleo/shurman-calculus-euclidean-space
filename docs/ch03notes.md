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

## 3.5 The Determinant: Characterizing Properties and Their Consequences

* The goal is to define a function that takes such a matrix, with its
  $n^2$ entries, and returns a single number.

$$ 
\det : M_{n}(\mathbb{R}) \longrightarrow \mathbb{R}
$$

* For every square matrix $A ∈ M_{n}(\mathbb{R})$, the scalar $\det(A)$ 
  should contain as much algebraic and geometric information about the 
  matrix as possible.

> This context nicely demonstrates a pedagogical principle already
> mentioned in Section 3.1: characterizing a mathematical object 
> illuminates its construction and its use. Rather than beginning with a 
> definition of the determinant, we will stipulate a few natural behaviors 
> for it, and then we will eventually see that

* there is a function with these behaviors (existence),
* there is only one such function (uniqueness), and, most importantly,
* these behaviors, rather than the definition, further show how the
  function works (consequences).

If $A$ has rows $r_1,...,r_n$, write $\det(r_1,...,r_n)$ for $\det(A)$.

$$ 
\det : \mathbb{R}^n \times \cdots \times \mathbb{R}^n \longrightarrow \mathbb{R}
$$

The advantage of this viewpoint is that now we can impose conditions on
the determinant, using language already at our disposal in a natural way.
Specifically, we make three requirements:

(1) The determinant is **multilinear**, meaning that it is linear as a function
of each of its vector variables when the rest are held fixed. That is, for all
vectors $r_1,...,r_k,r_k',...,r_n$ and every scalar $α$,

$$ 
\det (r_1, \cdots, αr_k + r_k', \cdots, r_n) =
α \det (r_1, \cdots, r_k, \cdots, r_n) \\
+ \det (r_1, \cdots, r_k', \cdots, r_n)
$$

Then

(2) The determinant is skew-symmetric as a function of its vector vari-
ables, meaning that exchanging any two inputs changes the sign of the
determinant,

$$ 
\det (r_1, \cdots, r_i, \cdots, r_j, \cdots, r_n) =
- \det (r_1, \cdots, r_j, \cdots, r_i, \cdots, r_n)
$$

(Here $i \neq j$.) Consequently, the determinant is also **alternating**, meaning
that if two inputs $r_i$ and $r_j$ are equal then $\det (r_1, \cdots, r_n) = 0$.

(3) The determinant is **normalized**, meaning that the standard basis has
determinant $1$,

$$ 
\det (e_1, \cdots, e_n) = 1.
$$

### Theorem 3.5.1 (Existence and uniqueness of the determinant).

One, and only one, multilinear skew-symmetric normalized function from the 
n-fold product of $\mathbb{R}^n$ to $R$ exists. This function is the 
determinant,

$$ 
\det : \mathbb{R}^n \times \cdots \times \mathbb{R}^n \longrightarrow \mathbb{R}
$$

Furthermore, all multilinear skew-symmetric functions from the n-fold 
product of $\mathbb{R}^n$ to $R$
are scalar multiples of of the determinant. That is, every multilinear
skew-symmetric function

$$ 
\delta : \mathbb{R}^n \times \cdots \times \mathbb{R}^n \longrightarrow \mathbb{R}
$$

is

$$ 
\delta = c \cdot \det
\quad
\text{where}
\quad
c = \delta (e_1, \cdots, e_n).
$$

$\square$

### The parity of a rearrangement

Independently of the determinant, every rearrangement of n objects
has a well-defined parity, meaning that for every rearrangement of the
objects, either all sequences of pairwise exchanges that put the objects
back in order have even length or all such sequences have odd length.

### Theorem 3.5.2 (The determinant is multiplicative).

For all matrices $A, B \in M_{n}(\mathbb{R})$,

$$ 
\det (AB) = \det (A) \det (B)
$$

In particular, if $A$ is invertible then the determinant of the matrix 
inverse is the scalar inverse of the determinant,

$$ 
\det (A^{-1}) = (\det (A))^{-1}
$$

**Proof**:

Let $B \in M_{n}(\mathbb{R})$ be fixed. Consider the function

$$ 
\delta : M_{n}(\mathbb{R}) \longrightarrow \mathbb{R},
\qquad
\delta (A) = \det (AB)
$$

So we have

$$ 
\delta (r_1, \cdots, r_n) =
\det (r_1B, \cdots, r_nB).
$$

We first show $\delta$ is multilinear.

$$ 
\delta (r_1, \cdots, αr_k + r_k', \cdots, r_n) =
\det (r_1B, \cdots, (αr_k + r_k')B, \cdots, r_nB) \\
= α \delta (r_1B, \cdots, r_kB, \cdots, r_nB) \\
+ \delta (r_1B, \cdots, r_k'B, \cdots, r_nB)
$$

Next we show $\delta$ is skew symmetric.

$$ 
\delta (r_1, \cdots, r_i, \cdots, r_j, \cdots, r_n) = \\
\det (r_1B, \cdots, r_iB, \cdots, r_jB, \cdots, r_nB) = \\
-\det (r_1B, \cdots, r_jB, \cdots, r_iB, \cdots, r_nB) = \\
- \delta (r_1, \cdots, r_j, \cdots, r_i, \cdots, r_n)
$$

So $\delta (A) = c \det (A)$,

$$ 
c = \delta (e_1, \cdots, e_n) \\
= \det (e_1B, \cdots, e_nB) \\
= \det (B)
$$

So $\det (AB) = \det (A) \det (B)$.

Also $1 = \det (I) = \det (A A^{-1}) = \det A \det A^{-1}$,
then $\det (A^{-1}) = (\det (A))^{-1}$.

$\square$

## 3.6 The Determinant: Characterizing Properties and Their Consequences

### Definition 3.6.1 (Permutation).

A permutation of $\{1,2,...,n\}$ is a vector

$$ 
π = (π(1),π(2),...,π(n))
$$

whose entries are $\{1,2,...,n\}$, each appearing once, in any order.
An inversion in the permutation $π$ is a pair of entries with the larger 
one to the left.

The **sign** of the permutation $π$, written $(−1)^π$, is −1 raised to the 
number of inversions in $π$. The set of permutations of $\{1,2,...,n\}$ is 
denoted $S_n$.

Every multilinear function $δ$ (if it exists at all) must satisfy

$$ 
δ (r_1, \cdots, r_n) =
δ \Bigg(
\sum_{i = 1}^{n} a_{1i} e_i,
\sum_{j = 1}^{n} a_{2j} e_j,
\cdots,
\sum_{p = 1}^{n} a_{np} e_p,
  \Bigg) \\
= \sum_{i = 1}^{n}
a_{1i} δ \Bigg(
e_i,
\sum_{j = 1}^{n} a_{2j} e_j,
\cdots,
\sum_{p = 1}^{n} a_{np} e_p,
\Bigg) \\
=
\sum_{i = 1}^{n} a_{1i} 
\Bigg(
\sum_{j = 1}^{n} a_{2j}
δ
\Bigg(
e_i, e_j,
\sum_{k = 1}^{n} a_{3k} e_k,
\cdots,
\sum_{p = 1}^{n} a_{np} e_p
\Bigg)
\Bigg) \\
=
\sum_{i = 1}^{n}
\sum_{j = 1}^{n}
a_{1i} a_{2j}
\Bigg(
e_i, e_j,
\sum_{k = 1}^{n} a_{3k} e_k,
\cdots,
\sum_{p = 1}^{n} a_{np} e_p
\Bigg) \\
\cdots \\
=
\sum_{i = 1}^{n}
\sum_{j = 1}^{n}
\cdots
\sum_{p = 1}^{n}
a_{1i} a_{2j} \cdots a_{np}
δ(e_i, e_j, \cdots, e_p)
$$

If $δ$ is also alternating then for every
$i,j,...,p ∈ \{1,...,n\}$, then

$$ 
δ(e_i, e_j, \cdots, e_p) = 0
$$

If any two subscripts agree.

Thus we may sum only over permutations,

$$ 
δ (r_1, \cdots, r_n) =
\sum_{(i, j, \cdots, p) \in S_n}
a_{1i} a_{2j} \cdots a_{np}
δ(e_i, e_j, \cdots, e_p)
$$

#### Compute $δ(e_i, e_j, \cdots, e_p)$

Consider any permutation $π = (i,j,...,p)$. Suppose that $π$ contains an
inversion, i.e., two elements are out of order. Then necessarily two 
elements in adjacent slots are out of order.

To see this, assume $i > p$, then either $i > j$ (adjacent slots found) or $j > i > p$. In the latter case, $j, p$ is closer than $i, p$ by $1$.
We can continue this process until find adjacent slots.

After finding the adjacent slots, we can swap them and reduce the
\# of inversions by $1$.

Repeating this process until the permutation has no remaining
inversions shows that

$$ 
δ(e_i, e_j, \cdots, e_p) = (-1)^π
δ (e_1, \cdots, e_n)
$$

That is, a possible formula for a multilinear skew-symmetric function $δ$ is

$$ 
δ(r_i, r_j, \cdots, r_p) =
\sum_{π = (i, j, \cdots, p) \in S_n}
(-1)^π
a_{1i} a_{2j} \cdots a_{np}
\cdot c
$$

Where $c = δ (e_1, \cdots, e_n)$.

The previous display gives the unique possible formula for a 
multilinear skew-symmetric normalized
function because every method of rearranging
$(e_i, e_j, \cdots, e_p)$ into order must
produce the same factor $(-1)^π$.

This is because if two rearrangings produce different factor
$-1$ and $1$, then that means we can find a sequence with
odd steps such that

$$ 
(e_1, \cdots, e_n) \longrightarrow
(e_i, e_j, \cdots, e_p) \longrightarrow
(e_1, \cdots, e_n)
$$

Which is not possible as proved in exercise 3.5.2.

### Definition 3.6.2 (Determinant).

The determinant function,

$$ 
\det : M_{n}(\mathbb{R}) \longrightarrow \mathbb{R}
$$

is defined as follows. For every $A \in M_{n}(\mathbb{R})$ with
entries $(a_{ij})$

$$
\det (A) =
\sum_{\pi \in S_n}
(-1)^π
a_{1 \pi(1)} \cdots a_{n \pi(n)}
$$

### Proposition 3.6.3 (Properties of the determinant).

(1) The determinant is linear as a function of each row of $A$.

**Proof**: Let $B$ be a matrix with

$$ 
b_{ij} =
\begin{cases}
  a_{ij} &\text{if } i \neq k\\
  α a_{ij} + a'_{ij} &\text{if } i = k\\
\end{cases} 
$$

Then

$$ 
\det (B) = 
\sum_{\pi \in S_n}
(-1)^π
b_{1 \pi(1)} \cdots b_{k \pi(k)} \cdots b_{n \pi(n)} \\
= 
\sum_{\pi \in S_n}
(-1)^π
a_{1 \pi(1)} \cdots (αa_{k \pi(k)} +a'_{k \pi(k)})\cdots a_{n \pi(n)} \\
=
α \left( 
\sum_{\pi \in S_n}
(-1)^π
a_{1 \pi(1)} \cdots a_{k \pi(k)} \cdots a_{n \pi(n)} \\
 \right)
+
\left( 
\sum_{\pi \in S_n}
(-1)^π
a_{1 \pi(1)} \cdots a'_{k \pi(k)} \cdots a_{n \pi(n)} \\
 \right) \\
=
α \det (r_1, \cdots r_k, \cdots r_n) +
\det (r_1, \cdots r'_k, \cdots r_n)
$$

$\square$

(2) The determinant is skew-symmetric as a function of the rows of 
$A$.

**Proof**:

Let $A = (r_1, \cdots, r_n)$ Suppose that rows
$k$ and $k+1$ are exchanged. The resulting matrix $B$ has

$$ 
b_{ij} =
\begin{cases}
  a_{ij} &\text{if } i \neq k ,\\
  a_{(k+1)j} &\text{if } i = k ,\\
  a_{kj} &\text{if } i = k+1 .\\
\end{cases} 
$$

For each permutation $π ∈ S_n$, define a companion permutation 
$π'$ by exchanging the $k$th and $(k+1)$st entries,

$$
π' = (π(1), \cdots, π(k+1), π(k), \cdots, π(n))
$$

Thus $π'(k) = π(k + 1), π'(k + 1) = π(k)$, and $π'(i) = π(i)$ for all other $i$.
each $π$ we have the relation $(−1)^π =−(−1)^{π'}$ (Exercise 3.6.6). 

Then we have

$$ 
\begin{align*}
\det (B)

&=
\sum_{\pi \in S_n}
(-1)^π
b_{1 \pi(1)} \cdots b_{k \pi(k)} b_{(k+1) \pi(k+1)} \cdots b_{n \pi(n)}
\\

&=
\sum_{\pi \in S_n}
(-1)^π
a_{1 \pi(1)} \cdots a_{(k+1) \pi(k)} a_{k \pi(k+1)} \cdots a_{n \pi(n)}
\\

&=
\sum_{\pi \in S_n}
(-1)^π
a_{1 π'(1)} \cdots a_{(k+1) π'(k+1)} a_{k π'(k)} \cdots a_{n π'(n)}
\\

&=
-\sum_{π \in S_n}
(-1)^{π'}
a_{1 π'(1)} \cdots a_{(k+1) π'(k+1)} a_{k π'(k)} \cdots a_{n π'(n)}
\\

&=
-\sum_{π' \in S_n}
(-1)^{π'}
a_{1 π'(1)} \cdots a_{(k+1) π'(k+1)} a_{k π'(k)} \cdots a_{n π'(n)}
\\

&= - \det (A)

\end{align*} 

$$

To exchange rows $k$ and $k+l$ in $A$ where $l > 0$, we can do
the following exchanges:

$$
\begin{align*}
k &\longleftrightarrow k+1, \\
k+1 &\longleftrightarrow k+2, \\
&\cdots \\
k+l-1 &\longleftrightarrow k+l, \\
k+l-2 &\longleftrightarrow k+l-1, \\
&\cdots \\
k &\longleftrightarrow k+1. \\
\end{align*} 
$$

Note there are $2l+1$ exchanges in total, which is an odd number.

$\square$

(3) The determinant is normalized.

**Proof**:

Consider

$$
\begin{align*}
\det (e_1, \cdots, e_n) \\
&=
\sum_{\pi \in S_n}
(-1)^π
a_{1 \pi(1)} \cdots a_{n \pi(n)} \\
\end{align*}
$$

Note that if $π(i) \neq i$, then $a_{1 \pi(1)} = 0$.
So the only item left from above summation is

$$ 
(-1)^0 a_{11} \cdots a_{nn} = 1
$$

Therefore, the determinant is normalized.

$\square$

> So a unique determinant function with the stipulated behavior exists. And
> we have seen that every multilinear skew-symmetric function must be a
> scalar multiple of the determinant. (This is discussed in the secton)
> before 3.6.2.

> Since the determinant is multilinear and skew-
> symmetric, so are its scalar multiples. This fact was shown in
> Exercise 3.5.3.

### Proposition 3.6.4 (Determinant algorithm).

Given $A ∈ M_{n}(\mathbb{R})$, use row
and column operations—recombines, scales, transpositions—to reduce $A$ to a
triangular matrix $Δ$. Then $\det(A)$ is $\det(Δ)$ times the reciprocal of 
each scale factor and times−1 for each transposition.

$\square$


