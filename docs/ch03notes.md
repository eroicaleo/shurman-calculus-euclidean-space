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

