# Chapter 2 Euclidean Space

## 2.1 Algebra: Vectors

### Theorem 2.1.1 (Vector space axioms).

(A1) Addition is associative

(A2) 0 is an additive identity

(A3) Existence of additive inverses

(A4) Addition is commutative

(M1) Scalar multiplication is associative

(M2) 1 is a multiplicative identity

(D1) Scalar multiplication distributes over scalar addition

(D2) Scalar multiplication distributes over vector addition

*For $n > 1$, $\mathbb{R}^n$ is not endowed with vector-by-vector multiplication.*

If the vector space axioms are satisfied with $V$ and $F$ replacing $\mathbb{R}^n$
and $\mathbb{R}$ then we say that $V$ is a vector space over $F$.

We can use intrinsic vector algebra to prove a result from Euclidean geometry, 
that the three medians of a triangle intersect.

Let

$$
p = \frac{x + y + z}{3}
$$

Rewrite it as

$$ 
p = x + \frac{2}{3}(\frac{y+z}{2} - x)
$$

Note that $\frac{y+z}{2}$ is the middle point of $yz$. Then $\frac{y+z}{2} - x$
is the median from $x$ to $yz$, so $p$ is on the median.

Since $x,y,z$ are symmetric, then $p$ is on all 3 medians.

$\square$

The standard basis of $\mathbb{R}^n$ is the set of vectors

$$ 
e_1 = (1, 0, \cdots 0) \\
e_2 = (0, 1, \cdots 0) \\
\cdots \\
e_n = (0, 0, \cdots 1) \\
$$

So

$$
\tag{2.1}
x = \sum_{i = 1}^{n}x_i e_i
$$

### Definition 2.1.2 (Basis).

A set of vectors $\{f_i\}$ is a basis of $\mathbb{R}^n$ if every
$x ∈ \mathbb{R}^n$ is uniquely expressible as a linear combination of the $f_i$.

$\square$
