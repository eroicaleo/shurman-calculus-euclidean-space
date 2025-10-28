# Chapter 3 Linear Mappings and Their Matrices

## 3.1 Linear Mappings

### 3.1.1.

Prove that $T : \mathbb{R}^n \longrightarrow \mathbb{R}^m$  is linear if and only if 
it satisfies (3.1) and (3.2). (It may help to rewrite (3.1) with the symbols
$x_1$ and $x_2$ in place of $x$ and $y$.
Then prove one direction by showing that (3.1) and (3.2) are
implied by the defining condition for linearity, and prove the other direction
by using induction to show that (3.1) and (3.2) imply the defining condition.
Note that as pointed out in the text, one direction of this argument has a bit
more substance than the other.)

**Proof**:

$\Rightarrow$

Use induction, when $k = 1$

$$ 
T(α_1 x_1) = α_1 T(x_1)
$$

This is (3.2).

Then assume $k = n$ holds, we are checking $k = n + 1$.

$$
\begin{align*}
T(\sum_{i = 1}^{n+1} α_i x_i)
&= T((\sum_{i = 1}^{n} α_i x_i) + α_{n+1} x_{n+1}) \\
&= T((\sum_{i = 1}^{n} α_i x_i)) + T(α_{n+1} x_{n+1}) \qquad \text{Use (3.1)}\\
&= T((\sum_{i = 1}^{n} α_i x_i)) + α_{n+1} T(x_{n+1}) \qquad \text{Use (3.2)}\\
&= \sum_{i = 1}^{n}α_kT(x_k) + α_{n+1} T(x_{n+1}) \qquad \text{Use induction}\\
&= \sum_{i = 1}^{n+1}α_kT(x_k)\\
\end{align*}
$$

$\Leftarrow$

To prove (3.1), set $k = 2, α_1 = α_2 = 1$.

To prove (3.2), set $k = 1$.

$\square$


### 3.1.2.

Suppose that $T : \mathbb{R}^n \longrightarrow \mathbb{R}^m$ is linear.
Show that $T(0_n) = 0_m$. (An intrinsic argument is nicer.)

**Proof**:

Note in both $\mathbb{R}^n, \mathbb{R}^m$, $0 v = 0$.
So

$$ 
T(0) = T(0 v_n) = 0 T(v_n) = 0 v_m = 0
$$

$\square$

### 3.1.3

Fix a vector $a ∈ \mathbb{R}$. Show that the mapping
$f : \mathbb{R}^n \longrightarrow \mathbb{R}$  given by
$T(x) = ⟨a,x⟩$ is linear, and that $T(e_j) = a_j$ for $j = 1,...,n$.

**Proof**:

(3.1) $T(x + y) = ⟨a,x+y⟩ = ⟨a,x⟩ + ⟨a,y⟩ = T(x) + T(y)$

(3.2) $T(αx) = ⟨a,αx⟩ = α ⟨a,x⟩ = αT(x)$

$T(e_j) = a_j$ follows the definition of the inner product.

$\square$

### 3.1.4

Find the linear mapping $T : \mathbb{R}^3 \longrightarrow \mathbb{R}$
such that $T(0,1,1) = 1$, $T(1,0,1) = 2$, and $T(1,1,0) = 3$.

**Solution**

We need to solve this equations

$$ 
\begin{cases}
    0x + 1y + 1z = 1 &\text{}\\
    1x + 0y + 1z = 2  &\text{}\\
    1x + 1y + 0z = 3  &\text{}\\
\end{cases} 
$$

So $T(x) = ⟨a,x⟩, a = (2, 1, 0)$.

$\square$

### 3.1.5.

Complete the proof of the componentwise nature of linearity.

**Proof**:

For $α \in \mathbb{R}, x \in \mathbb{R}^n$

If $T_1, \cdots, T_m$ are linear, then

$$ 
T(αx) =
(T_1(\alpha x), \cdots, T_m(\alpha x)) \\
= (αT_1(x), \cdots, αT_m(x)) \\
= α (T_1(x), \cdots, T_m(x)) \\
= α T(x)
$$

On the other hand, if $T$ is linear,

Then

$$ 
\begin{split}
(T_1(\alpha x), \cdots, T_m(\alpha x))
&= T(αx)  \\
&= α T(x)  \\
&= α (T_1(x), \cdots, T_m(x))  \\
&= (αT_1(x), \cdots, αT_m(x)) \\
\end{split}
$$

So $T_i(αx) = α T_i(x)$

$\square$

### 3.1.6.

Carry out the matrix-by-vector multiplications

**Solution**:

(a) $[1,3,6]$

(b) $(ax+by, cx+dy, ex+fy)$

(c) $(x_1 y_1, \cdots, x_n y_n)$ 

(d) $(0,0,0)$

$\square$

### 3.1.7.

Prove that the identity mapping $\text{id} : \mathbb{R}^n \longrightarrow \mathbb{R}^n$ is linear. What is its matrix? Explain.

**Proof**

(3.1) $\text{id}(x+y) = x+y = \text{id}(x) + \text{id}(y)$

(3.2) $\text{id}(αx) = αx = α \text{id}(x)$

Then matrix is

$$ 
\begin{bmatrix}
1 &0 &\cdots &0 \\
0 &1 &\cdots &0 \\
\vdots &\vdots &\ddots &\vdots \\
0 &0 &\cdots &1 \\
\end{bmatrix}
$$

$\square$

### 3.1.8.

Let $θ$ denote a fixed but generic angle. Argue geometrically that the
mapping $R : \mathbb{R}^n \longrightarrow \mathbb{R}^n$ given by counterclockwise
rotation by $θ$ is linear, and then find its matrix.

**Proof**:

Geometrically is quite obvious.

Consider

$$ 
R(e_1) = (\cos θ, \sin θ) \\
R(e_2) = (-\sin θ, \cos θ) \\
$$

Then matrix is

$$ 
\begin{bmatrix}
\cos θ & -\sin θ \\
\sin θ & \cos θ \\
\end{bmatrix}
$$

$\square$

### 3.1.9.

Show that the mapping $Q : \mathbb{R}^2 \longrightarrow \mathbb{R}^2$ given by reflection 
through the x-axis is linear. Find its matrix.

$$ 
R(e_1) = (1, 0) \\
R(e_2) = (0, -1) \\
$$

Then matrix is

$$ 
\begin{bmatrix}
1 & 0 \\
0 & -1 \\
\end{bmatrix}
$$

$\square$

### 3.1.10.

Show that the mapping $P : \mathbb{R}^2 \longrightarrow \mathbb{R}^2$ given by
orthogonal projection onto the diagonal line $x = y$ is 
linear. Find its matrix. (See Exercise 2.2.15.)

**Proof**:

We can use vector $d = (1,1)$ to represent the
diagonal line $x = y$.

Then for $x, y \in \mathbb{R}^2$ 

$$ 
P(x) = \frac{⟨d,x⟩}{|d|^2} d \\
P(y) = \frac{⟨d,y⟩}{|d|^2} d \\
P(x+y) = \frac{⟨d,x+y⟩}{|d|^2} d \\
= \frac{⟨d,x⟩}{|d|^2} d + \frac{⟨d,y⟩}{|d|^2} d = P(x) + P(y)
$$

Also

$$ 
P(αx) = \frac{⟨d,αx⟩}{|d|^2} d = α\frac{⟨d,x⟩}{|d|^2} d = α P(x)
$$

So $P$ is linear.

$$ 
R(e_1) = (\sqrt[]{2}/2, \sqrt[]{2}/2) \\
R(e_2) = (\sqrt[]{2}/2, \sqrt[]{2}/2) \\
$$

Then matrix is

$$ 
\begin{bmatrix}
\sqrt[]{2}/2 & \sqrt[]{2}/2 \\
\sqrt[]{2}/2 & \sqrt[]{2}/2 \\
\end{bmatrix}
$$

$\square$

### 3.1.11.

Draw the graph of a generic linear mapping from $\mathbb{R}^2$ to $\mathbb{R}^3$.

**Solution**: skip.

### 3.1.12.

Continue the proof of Proposition 3.1.8 by proving the other three
statements about $S + T$ and $aS$ satisfying (3.1) and (3.2).

**Proof**:

(3.2) for $S+T$.

$$ 
(S+T)(αx) = S(αx) + T(αx) = αS(x) + αT(x) = α (S(x) + T(x)) = α (S+T)(x)
$$

Next, (3.1) for $aS$.

$$ 
\begin{align*}
(aS)(x+y)
&= a(S(x + y))       & \quad \text{definition of the } aS \\
&= a(S(x) + S(y))    & \quad \text{S is linear} \\
&= aS(x) + aS(y)     & \quad \text{Vector space axioms D2} \\
&= (aS)(x) + (aS)(y) & \quad \text{definition of the } aS \\
\end{align*}
$$

Next, (3.2) for $aS$.

$$ 
\begin{aligned}
(aS)(αx)
&= a(S(αx))   & \quad \text{definition of the } aS \\
&= a(αS(x))   & \quad \text{S is linear} \\
&= α(aS(x))   & \quad \mathbb{R} \text{ is a field} \\
&= α((aS)(x)) & \quad \text{definition of the } aS \\
\end{aligned} 
$$

$\square$

### 3.1.13.

If $S \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$ and $T \in \mathcal{L}(\mathbb{R}^p, \mathbb{R}^n)$,
show that $S \circ T : \mathbb{R}^p \longrightarrow \mathbb{R}^m$
lies in $\mathcal{L}(\mathbb{R}^p, \mathbb{R}^m)$.

**Proof**:

(3.1)

$$
\begin{align*}
(S \circ T)(x+y)
&= S(T(x+y))                       \\
&= S(T(x) + T(y))                  \\
&= (S \circ T)(x) + (S \circ T)(y) \\
\end{align*}
$$

Next (3.2)

$$ 
\begin{align*}
(S \circ T)(αx)
&= S(T(αx))                       \\
&= S(αT(x))                       \\
&= α(S(T(x)))                     \\
&= α((S \circ T)(x))              \\
\end{align*} 
$$

So $S \circ T \in \mathcal{L}(\mathbb{R}^p, \mathbb{R}^m)$.

### 3.1.14

(a) Let $S \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$. Its transpose is the mapping

$$ 
S^T : \mathbb{R}^m \longrightarrow \mathbb{R}^n
$$

defined by the characterizing condition

$$ 
⟨x,S^T(y)⟩ = ⟨S(x),y⟩ \qquad \text{for all } x \in \mathbb{R}^n \text{ and } y \in \mathbb{R}^m.
$$

Granting that indeed a unique such $S^T$ exists, use the characterizing condition to show that

$$ 
S^T(y+y') = S^T(y) + S^T(y') \qquad \text{for all } y, y' \in \mathbb{R}^m
$$

by showing that

$$ 
⟨x,S^T(y+y')⟩ = ⟨x,S^T(y)+S^T(y')⟩
\qquad \text{for all } x \in \mathbb{R}^n \text{ and } y, y' \in \mathbb{R}^m.
$$

**Proof**:

$$ 
\begin{align*}
⟨x,S^T(y+y')⟩
&= ⟨S(x),y+y'⟩              \\
&= ⟨S(x),y⟩ + ⟨S(x),y'⟩     \\
&= ⟨x,S^T(y)⟩ + ⟨x,S^T(y')⟩ \\
&= ⟨x,S^T(y) + S^T(y')⟩     \\
\end{align*}
$$

Because $x$ can be arbitrary, so we have

$$ 
S^T(y+y') = S^T(y) + S^T(y') \qquad \text{for all } y, y' \in \mathbb{R}^m
$$

$\square$

(b) Keeping S from part (a), now further introduce $T \in  \mathcal{L}(\mathbb{R}^p, \mathbb{R}^n)$,
so that also $S \circ T \in \mathcal{L}(\mathbb{R}^p, \mathbb{R}^m)$.
Show that the transpose of the composition is
the composition of the transposes in reverse order,

$$ 
(S ◦T)^T = T^T ◦S^T,
$$

by showing that

$$ 
⟨x,(S ◦T)^T(z)⟩ = ⟨x, (T^T ◦S^T)(z)⟩
$$

**Proof**:

$$
\begin{align*}
⟨x,(S ◦T)^T(z)⟩ 
&= ⟨(S◦T)(x), z⟩       \\
&= ⟨S(T(x)), z⟩        \\
&= ⟨T(x), S^T(z)⟩      \\
&= ⟨x, T^T (S^T(z))⟩   \\
&= ⟨x, (T^T ◦ S^T)(z)⟩ \\
\end{align*} 
$$

$\square$

### 3.1.15

A mapping $f : \mathbb{R}^n \longrightarrow \mathbb{R}^m$ 
is called aﬃne if it has the form
$f(x) = T(x) + b$, where
$T ∈ \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$ and
$b ∈ \mathbb{R}^m$.
State precisely and prove: the composition of aﬃne 
mappings is aﬃne.

**Proof**:

If $f : \mathbb{R}^p \longrightarrow \mathbb{R}^n$ and
$g : \mathbb{R}^n \longrightarrow \mathbb{R}^m$ are affine,
then

$$ 
g \circ f : \mathbb{R}^p \longrightarrow \mathbb{R}^m
\quad \text{ is affine}.
$$

$$ 
\begin{align*}
g(f(x))
&= g(T(x) + b)        \\
&= g(T(x)) + g(b)     \\
&= S(T(x)) + c + g(b) \\
\end{align*} 
$$

$\square$

### 3.1.16

Let $T : \mathbb{R}^n \longrightarrow \mathbb{R}^m$
be a linear mapping. Note that since $T$ is
continuous and since the absolute value function on $\mathbb{R}^m$ is 
continuous, the composite function

$$ 
|T| : \mathbb{R}^n \longrightarrow \mathbb{R}
$$

is continuous.

(a) Let $S= \{x ∈ \mathbb{R}^n : |x| = 1\}$. Explain why $S$ is a compact 
subset of $\mathbb{R}^n$.
Explain why it follows that $|T|$ takes a maximum value $c$ on $S$.

**Proof**: $S$ is bounded. Then we just need to show
$S$ is closed.

Use "Sequential characterization of closed sets", assume $\{x_ν\} \rightarrow p \in \mathbb{R}^n$.

Since $||$ is a continuous function and

$$ 
\lim_{\nu \to \infty} |x_ν| = 1
$$

Then $|p| = 1$.

So $p \in S$, then $S$ is closed. So $S$ is compact.

Then based on Theorem 2.4.15 (Extreme value theorem),
$|T|$ takes a maximum value $c$ on $S$.

$\square$

(b) Show that $|T(x)| ≤ c|x|$ for all $x ∈ \mathbb{R}^n$.
This result is the linear
magnification boundedness lemma. We will use it in Chapter 4.

**Proof**:

$$
x =  |x|\frac{x}{|x|}\\
\begin{align*}
T(x)
&= T(|x|\frac{x}{|x|}) \\
&= |x|T(\frac{x}{|x|}) &\qquad T\text{ is linear} \\
&\leq c|x| &\qquad \left| \frac{x}{|x|} \right| = 1 \\
\end{align*}  
$$

$\square$

### 3.1.17.

Let $T : \mathbb{R}^n \longrightarrow \mathbb{R}^m$ be a linear mapping.

(a) Explain why the set $D = \{x ∈ \mathbb{R}^n : |x| = 1\}$ is compact.

**Proof**: See 3.1.16 (a)

(b) Use part (a) of this exercise and part (b) of the preceding exercise
to explain why therefore the set $\{|T(x)| : x ∈ D\}$ has a maximum. This
maximum is called the norm of $T$ and is denoted $\left\| T \right\|$.

**Proof**:

See 3.1.16 (b).

(c) Explain why $\left\| T \right\|$ is the smallest value 
$K$ that satisfies the condition
from part (b) of the preceding exercise,
$|T(x)| ≤ K|x|$ for all $x ∈ \mathbb{R}^n$.

**Proof**:

First, we know from 3.1.16 (b),
$|T(x)| ≤ \left\| T \right\|  |x|$.

Next, we can find a point $c \in D$ such that

$$ 
|T(c)| = \left\| T \right\| |c| = \left\| T \right\|
$$

$\square$

(d) Show that for every
$S,T ∈ \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$ and
every $a ∈ \mathbb{R}$,


$$
\left\| S + T \right\| \leq
\left\| S \right\| +
\left\| T \right\|
\qquad \text{and} \qquad
\left\| aT \right\| =
|a|\left\| T \right\|
$$

Define a distance function

$$ 
d:
\mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)
\times
\mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)
\longrightarrow
\mathbb{R},
\quad
d(S, T) = \left\| S - T \right\|
$$

Show that this function satisfies the distance properties 
of Theorem 2.2.8.

**Proof**:

$$ 
\left\| S+T \right\| = |(S+T)(c)| \\
= |S(c) + T(c)| \\
\leq |S(c)| + |T(c)| \\
\leq \left\| S \right\| + \left\| T \right\|
$$

$$ 
\left\| aT \right\| = |(aT)(c)| \\
|a(T(c))| = |a| |T(c)| = |a| \left\| T \right\|
$$

$\square$

(D1) $d(S, T) \geq 0$.

Since $|(S - T)(x)| \geq 0$, then
$\left\| S-T \right\| \geq 0$.

$d(S,T) = 0$ if and only if $S = T$.

$\square$

(D2) $d(S,T) = d(T,S)$

Because

$$ 
|(S-T)(x)| = |(T-S)(x)|
$$

$\square$

(D3) $d(R,T) ≤ d(R,S)+d(S,T)$

$$ 
d(R,T) =
\left\| R - T \right\|
= |(R-T)(c)| \\
= |R(c) - T(c)| \\
= |(R(c)-S(c)) + (S(c)-T(c))| \\
\leq |R(c)-S(c)| + |S(c)-T(c)| \\
= |(R-S)(c)| + |(S-T)(c)| \\
\leq \left\| R-S \right\| + \left\| S-T \right\| \\
= d(R,S)+d(S,T)
$$

$\square$

(e) Show that for every
$S \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$
and every $T \in \mathcal{L}(\mathbb{R}^p, \mathbb{R}^n)$

$$ 
\left\| ST \right\| \leq
\left\| S \right\|
\left\| T \right\|
$$

**Proof**:

Assume

$$ 
\left\| ST \right\| = |S(T(c))|
$$

Let $x = T(c) \in \mathbb{R}^n$.

$$ 
|S(x)| \leq \left\| S \right\| |x| \\
|x| = |T(c)| \leq \left\| T \right\| |c| =
\left\| T \right\|
$$

Therefore

$$ 
\begin{align*}
\left\| ST \right\|
&= |S(T(c))| \\
&= |S(x)| \\
&\leq  \left\| S \right\| |x| \\
&\leq  \left\| S \right\| \left\| T \right\| \\
\end{align*} 
$$

$\square$

## 3.2 Operations on Matrices

### 3.2.1.

Justify Definition 3.2.2 of scalar multiplication of matrices.

**Solution**:

The $j$th column of $αA$ is

$$ 
(αS)(e_j) = α (S(e_j)) = α \times \text{($j$th column of A)}
$$

So it's reasonable to define $αA = [αa_{ij}]_{m \times n}$.

$\square$

### 3.2.2.

Carry out the matrix multiplications.

**Solution**: skipped.

### 3.2.3

Prove more of Proposition 3.2.5, that
$A(B+C) = AB+AC$, $(αA)B= A(αB)$, and
$I_mA= A$ for suitable matrices $A,B,C$ and any scalar $α$.

**Proof**:

$$ 
\begin{align*}
(R ◦ (S + T))(x)
&= R((S+T)(x))
&\quad \text{by definition of $R ◦ (S + T)$} \\
&= R(S(x)+T(x))
&\quad \text{by definition of $(S + T)$} \\
&= R(S(x)) + R(S(x))
&\quad \text{$R$ is linear mapping} \\
&= (R ◦ S)(x) + (R ◦ T)(x)
&\quad \text{by definition of $R ◦ S$ and $R ◦ T$}
\end{align*}
$$

$$
\begin{align*}
((αS) ◦ T)(x)
&= (αS)(T(x))
&\quad \text{by definition of $(αS) ◦ T$} \\
&= α (S(T(x)))
&\quad \text{by definition of $(αS)$} \\
&= S(αT(x))
&\quad \text{$S$ is linear} \\
&= S((αT)(x))
&\quad \text{by definition of $(αT)$} \\
&= (S◦(αT))(x)
&\quad \text{by definition of $S◦(αT)$} \\
\end{align*} 
$$

$$
\begin{align*}
(\text{id} ◦ A) (x)
&= \text{id}(A(x))
&\quad \text{by definition of id $ ◦ A$} \\
&= A(x)
&\quad \text{by definition of id} \\
\end{align*} 
$$

### 3.2.4.

(If you have not yet worked Exercise 3.1.14 then do so before working
this exercise.) 

Let $A = [a_{ij}]_{m \times n} \in M_{m, n}(\mathbb{R})$
be the matrix of $S \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$
Its transpose $A^T \in M_{n, m}(\mathbb{R})$
is the matrix of the transpose mapping $S^T$.
Since $S$ and $S^T$ act respectively as multiplication by
$A$ and $A^T$, the characterizing
property of $S$ from Exercise 3.1.14 gives

$$ 
⟨x,A^T y⟩ = ⟨Ax,y⟩ \quad \text{for all } x \in \mathbb{R}^n \text{ and } y \in \mathbb{R}^m.
$$

Make specific choices of x and y to show that the transpose $A^T \in M_{m, n}(\mathbb{R})$
is obtained by flipping $A$ about its northwest–southeast diagonal; that is, show
that the $(i,j)$th entry of $A^T$ is $a_{ji}$. 

It follows that the rows of $A^T$ are the
columns of $A$, and the columns of $A^T$ are the rows of $A$.

**Proof**:

Given any $1 \leq p \leq m, 1 \leq q \leq n$, let $x = e_p \in \mathbb{R}^n, y = e_q \in \mathbb{R}^m$.

Let $A = [a_{ij}]_{m \times n}, A^T = [b_{ij}]_{n \times m}$.

Then $A^T y = A^T e_q = j \text{th column of }A^T$, then $⟨x,A^T y⟩ = b_{ij}$.

On the other hand, $Ax = i \text{th column of }A$, then $⟨Ax,y⟩ = a_{ji}$.

So we proved.

> (Similarly, let $B \in M_{n, p}(\mathbb{R})$ be the matrix of
> $T \in \mathcal{L}(\mathbb{R}^p, \mathbb{R}^n)$ so that $B^T$
> is the matrix of $T^T$. Because matrix multiplication is compatible with linear
> mapping composition, we know immediately from Exercise 3.1.14(b), with no
> reference to the concrete description of the matrix transposes $A^T$ and $B^T$ in
> terms of the original matrices $A$ and $B$, that the transpose of the product is
> the product of the transposes in reverse order,

$$ 
(AB)^T = B^T A^T \quad \text{for all } A \in M_{m, n}(\mathbb{R}) \text{ and }
B \in M_{n, p}(\mathbb{R}).
$$

> That is, by characterizing the transpose mapping in Exercise 3.1.14, we
> easily derived the construction of the transpose matrix here and obtained the
> formula for the product of transpose matrices with no reference to their construction.)

$\square$

### 3.2.5.

The trace of a square matrix $A \in M_{n}(\mathbb{R})$ is the sum of its diagonal
elements,

$$ 
\text{tr}(A) = \sum_{i = 1}^{n} a_{ii}
$$

Show that

$$ 
\text{tr}(AB) = \text{tr}(BA), \quad A,B \in M_{n}(\mathbb{R})
$$

**Proof**:

$$ 
\text{tr}(AB) = \sum_{i = 1}^{n} c_{ii} \\
= \sum_{i = 1}^{n} \left( \sum_{j = 1}^{n} a_{ij} b_{ji} \right) \\
= \sum_{i = 1}^{n} \sum_{j = 1}^{n} a_{ij} b_{ji} \\
= \sum_{j = 1}^{n} \sum_{i = 1}^{n} b_{ji} a_{ij} \\
= \sum_{j = 1}^{n} \left( \sum_{i = 1}^{n} b_{ji} a_{ij}  \right) \\
= \text{tr}(BA)
$$

$\square$

### 3.2.6

For every matrix $A \in M_{m, n}(\mathbb{R})$ and column vector
$a \in \mathbb{R}^m$, define the aﬃne mapping (cf. Exercise 3.1.15)

$$ 
\text{Aff}_{A, a} : \mathbb{R}^n \longrightarrow \mathbb{R}^m
$$

by the rule $\text{Aff}_{A, a} = Ax + a$ for all
$x \in \mathbb{R}^n$, viewing $x$ as a column vector.

(a) Explain why every aﬃne mapping from $\mathbb{R}^n$ to
$\mathbb{R}^m$ takes this form.

**Proof**:

An affine mapping is this form: $f(x) = T(x) + b$,
$T \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$ and
$b \in \mathbb{R}^m$.

Since $T \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$,
then we can find matrix $A \in M_{m, n}(\mathbb{R})$ such that
$T(x) = A(x)$.

So $\text{Aff}_{A, a} = Ax + a$.

$\square$

(b) Given such $A$ and $a$, define the matrix
$A' \in M_{{m+1}, {n+1}}(\mathbb{R})$ to be 

$$
A' =
\begin{bmatrix}
    A          & a \\
    \bold{0}_n & 1 \\
\end{bmatrix}.
$$

Show that for all $x ∈ \mathbb{R}^n$,

$$ 
A'
\begin{bmatrix}
x \\
1 \\
\end{bmatrix}
=
\begin{bmatrix}
\text{Aff}_{A, a}(x) \\
1
\end{bmatrix}.
$$

Thus, aﬃne mappings, like linear mappings, behave as 
matrix-by-vector multiplications but where the vectors are the usual 
input and output vectors augmented with an extra “1” at the bottom.

**Proof**:

For $e_j, j < n+1$,

$$ 
A' e_j =
\begin{bmatrix}
A_j \\
0 \\
\end{bmatrix} \\
A' e_{n+1} =
\begin{bmatrix}
a \\
1 \\
\end{bmatrix}
$$

Let
$$
x' = \begin{bmatrix}
x \\
1 \\
\end{bmatrix}
$$

Then

$$ 
x' = \sum_{j = 1}^{n} x_j e_j + e_{n+1}
$$

Then

$$ 
A'x' = \sum_{j = 1}^{n} x_j A' e_j + A' e_{n+1} \\
= \sum_{j = 1}^{n} x_j A_j +
\begin{bmatrix}
a \\
1 \\
\end{bmatrix} \\
= \sum_{j = 1}^{n}
\begin{bmatrix}
A_j x_j \\
0 \\
\end{bmatrix} +
\begin{bmatrix}
a \\
1 \\
\end{bmatrix}  \\
=
\begin{bmatrix}
\text{Aff}_{A, a}(x) \\
1
\end{bmatrix}
$$

$\square$

(c) The aﬃne mapping
$\text{Aff}_{B, b} : \mathbb{R}^p \longrightarrow \mathbb{R}^n$
determined by $B \in M_{n, p}(\mathbb{R})$ and $b \in \mathbb{R}^n$
has matrix

$$ 
B' =
\begin{bmatrix}
B          & b \\
\bold{0}_p & 1 \\
\end{bmatrix}
$$

Show that

$\text{Aff}_{A, a} \circ \text{Aff}_{B, b} : \mathbb{R}^p \longrightarrow \mathbb{R}^m$ has matrix $A'B'$.
That is, matrix
multiplication is compatible with composition of aﬃne mappings.

**Proof**:

First we know

$$
B'x =
\begin{bmatrix}
\text{Aff}_{B, b}(x) \\
1
\end{bmatrix}
$$

Then

$$
\begin{align*}
(A'B')x
&=
A' (B'x) &\quad \text{Properties of matrix multiplication} \\
&=
A' \begin{bmatrix}
\text{Aff}_{B, b}(x) \\
1
\end{bmatrix} &\quad \text{Compute $B'x$ from (b)} \\ 
&= 
\begin{bmatrix}
\text{Aff}_{A, a} ( \text{Aff}_{B, b}(x) ) \\
1 \\
\end{bmatrix} &\quad \text{Again from (b)} \\
&=
\begin{bmatrix}
(\text{Aff}_{A, a} \circ \text{Aff}_{B, b})(x) \\
1
\end{bmatrix} &\quad \text{Definition of composition of maps.} 
\end{align*} 
$$

$\square$

### 3.2.7.

The exponential of a square matrix $A$ is the infinite matrix sum

$$ 
e^A =
I + A + \frac{1}{2!} A^2 + \frac{1}{3!} A^3 + \cdots 
$$

Compute the exponentials of the following matrices.

**Solution**:

(a) $A = [λ]$

$$ 
e^A = [e^λ]
$$

$\square$

(b)

$$ 
A =
\begin{bmatrix}
    λ & 1 \\
    0 & λ \\
\end{bmatrix}
$$

$$ 
A^2 = 
\begin{bmatrix}
    λ & 1 \\
    0 & λ \\
\end{bmatrix}
\begin{bmatrix}
    λ & 1 \\
    0 & λ \\
\end{bmatrix} \\
=
\begin{bmatrix}
λ^2 & 2λ \\
0   & λ^2 \\
\end{bmatrix}

$$

$$ 
A^3 =
\begin{bmatrix}
λ^2 & 2λ \\
0   & λ^2 \\
\end{bmatrix}
\begin{bmatrix}
    λ & 1 \\
    0 & λ \\
\end{bmatrix} \\
=
\begin{bmatrix}
λ^3 & 3λ^2 \\
0   & λ^3 \\
\end{bmatrix}
$$

Then

$$ 
e^A =
\begin{bmatrix}
e^λ & e^λ \\
0   & e^λ \\
\end{bmatrix}
$$

$\square$

(c)

$$ 
A =
\begin{bmatrix}
λ & 1 & 0 \\
0 & λ & 1 \\
0 & 0 & λ \\
\end{bmatrix}
$$

$$ 
A^2 =
\begin{bmatrix}
λ & 1 & 0 \\
0 & λ & 1 \\
0 & 0 & λ \\
\end{bmatrix}
\begin{bmatrix}
λ & 1 & 0 \\
0 & λ & 1 \\
0 & 0 & λ \\
\end{bmatrix} \\
=
\begin{bmatrix}
λ^2 & 2λ  & 1 \\
0   & λ^2 & 2λ \\
0   & 0   & λ^2 \\
\end{bmatrix}
$$

$$ 
A^3 =
\begin{bmatrix}
λ^2 & 2λ  & 1 \\
0   & λ^2 & 2λ \\
0   & 0   & λ^2 \\
\end{bmatrix}
\begin{bmatrix}
λ & 1 & 0 \\
0 & λ & 1 \\
0 & 0 & λ \\
\end{bmatrix} \\
=
\begin{bmatrix}
λ^3 & 3λ^2  & 3λ \\
0   & λ^3   & 3λ^2 \\
0   & 0     & λ^3 \\
\end{bmatrix}
$$

$$ 
A^4 =
\begin{bmatrix}
λ^3 & 3λ^2  & 3λ \\
0   & λ^3   & 3λ^2 \\
0   & 0     & λ^3 \\
\end{bmatrix}
\begin{bmatrix}
λ & 1 & 0 \\
0 & λ & 1 \\
0 & 0 & λ \\
\end{bmatrix} \\
=
\begin{bmatrix}
λ^4 & 4λ^3  & 6λ^2 \\
0   & λ^4   & 4λ^3 \\
0   & 0     & λ^4 \\
\end{bmatrix}
$$

So

$$ 
e^A =
\begin{bmatrix}
e^λ & e^λ  & e^λ/2 \\
0   & e^λ   & e^λ \\
0   & 0     & e^λ \\
\end{bmatrix}
$$

$\square$

(d)

$$ 
A =
\begin{bmatrix}
λ & 1 & 0 & 0 \\
0 & λ & 1 & 0 \\
0 & 0 & λ & 1 \\
0 & 0 & 0 & λ \\
\end{bmatrix}
$$

$$ 
A^2 =
\begin{bmatrix}
λ & 1 & 0 & 0 \\
0 & λ & 1 & 0 \\
0 & 0 & λ & 1 \\
0 & 0 & 0 & λ \\
\end{bmatrix}
\begin{bmatrix}
λ & 1 & 0 & 0 \\
0 & λ & 1 & 0 \\
0 & 0 & λ & 1 \\
0 & 0 & 0 & λ \\
\end{bmatrix} \\
=
\begin{bmatrix}
λ^2 & 2λ  & 1   & 0   \\
0   & λ^2 & 2λ  & 1   \\
0   & 0   & λ^2 & 2λ  \\
0   & 0   & 0   & λ^2 \\
\end{bmatrix}
$$

So

$$ 
\frac{1}{2!} A^2 =
\begin{bmatrix}
\frac{1}{2!} λ^2 & λ  & \frac{1}{2}   & 0   \\
0   & \frac{1}{2!} λ^2 & λ  & \frac{1}{2}   \\
0   & 0   & \frac{1}{2!} λ^2 & λ  \\
0   & 0   & 0   & \frac{1}{2!} λ^2 \\
\end{bmatrix}
$$

Then

$$ 
A^3 = 
\begin{bmatrix}
λ^2 & 2λ  & 1   & 0   \\
0   & λ^2 & 2λ  & 1   \\
0   & 0   & λ^2 & 2λ  \\
0   & 0   & 0   & λ^2 \\
\end{bmatrix}
\begin{bmatrix}
λ & 1 & 0 & 0 \\
0 & λ & 1 & 0 \\
0 & 0 & λ & 1 \\
0 & 0 & 0 & λ \\
\end{bmatrix} \\
=
\begin{bmatrix}
λ^3 & 3λ^2 & 3λ   & 1   \\
0   & λ^3  & 3λ^2 & 3λ   \\
0   & 0    & λ^3  & 3λ^2  \\
0   & 0    & 0    & λ^3 \\
\end{bmatrix}
$$

So

$$ 
\frac{1}{3!} A^3 =
\begin{bmatrix}
\frac{1}{3!} λ^3 & \frac{1}{2!} λ^2              & \frac{1}{2} λ   & \frac{1}{3!}   \\
0                & \frac{1}{3!} λ^3  & \frac{1}{2!} λ^2 & \frac{1}{2} λ   \\
0                & 0                 & \frac{1}{3!} λ^3  & \frac{1}{2!} λ^2  \\
0                & 0                 & 0    & \frac{1}{3!} λ^3 \\
\end{bmatrix}
$$

Then

$$ 
A^4 =
\begin{bmatrix}
λ^3 & 3λ^2 & 3λ   & 1   \\
0   & λ^3  & 3λ^2 & 3λ   \\
0   & 0    & λ^3  & 3λ^2  \\
0   & 0    & 0    & λ^3 \\
\end{bmatrix}
\begin{bmatrix}
λ & 1 & 0 & 0 \\
0 & λ & 1 & 0 \\
0 & 0 & λ & 1 \\
0 & 0 & 0 & λ \\
\end{bmatrix} \\
=
\begin{bmatrix}
λ^4 & 4 λ^3 & 6 λ^2 & 4 λ \\
0   & λ^4   & 4 λ^3 & 6 λ^2 \\
0   & 0     & λ^4   & 4 λ^3 \\
0   & 0     & 0     & λ^4 \\
\end{bmatrix} \\
$$

So

$$ 
\frac{1}{4!} A^4
=
\begin{bmatrix}
(1/4!)λ^4 & (1/3!) λ^3 & (1/2)(1/2!) λ^2 & (1/3!) λ \\
0   & (1/4!)λ^4   & (1/3!) λ^3 & (1/2)(1/2!) λ^2 \\
0   & 0     & (1/4!)λ^4   & (1/3!) λ^3 \\
0   & 0     & 0     & (1/4!)λ^4 \\
\end{bmatrix} \\
$$

Then finally

$$ 
e^A =
\begin{bmatrix}
e^λ & e^λ & \frac{1}{2!} e^λ & \frac{1}{3!} e^λ \\
0 & e^λ & e^λ & \frac{1}{2!} e^λ \\
0 & 0 & e^λ & e^λ \\
0 & 0 & 0 & e^λ \\
\end{bmatrix} \\
$$

$\square$

### 3.2.8.

Let $a,b,d$ be real numbers with $ad = 1$. show that

$$ 
\begin{bmatrix}
a & b \\
0 & d \\
\end{bmatrix}
=
\begin{bmatrix}
1 & ab \\
0 & 1  \\
\end{bmatrix}
\begin{bmatrix}
a & 0 \\
0 & d  \\
\end{bmatrix}
$$.

**Proof**: Just regular matrix multiplication.

(b)

Let $a,b,c,d$ be real numbers with $c \neq 0$ and $ad−bc = 1$. Show that

$$ 

$$

$\square$

## 3.3 The Inverse of a Linear Mapping

### 3.3.8.

For each matrix $A$ solve the equation $Ax= 0$.

(a)

$$ 
\begin{bmatrix}
-1 & 1 & 4 \\
 1 & 3 & 8 \\
 1 & 2 & 5 \\
\end{bmatrix}
$$

**Solution**:

Multiply by $R_{2;1,1}$ we got 

$$ 
\begin{bmatrix}
-1 & 1 & 4 \\
 0 & 4 & 12 \\
 1 & 2 & 5 \\
\end{bmatrix}
$$

Multiply by $R_{3;1,1}$ we got

$$ 
\begin{bmatrix}
-1 & 1 & 4 \\
 0 & 4 & 12 \\
 0 & 3 & 9 \\
\end{bmatrix}
$$

Multiply by $S_{1,-1}$ we got

$$ 
\begin{bmatrix}
 1 & -1 & -4 \\
 0 & 4 & 12 \\
 0 & 3 & 9 \\
\end{bmatrix}
$$

Multiply by $R_{1;3,1/3}$ we got

$$ 
\begin{bmatrix}
 1 & 0 & -1 \\
 0 & 4 & 12 \\
 0 & 3 & 9 \\
\end{bmatrix}
$$

Multiply by $R_{2;3,-4/3}$ we got

$$ 
\begin{bmatrix}
 1 & 0 & -1 \\
 0 & 0 & 0  \\
 0 & 3 & 9  \\
\end{bmatrix}
$$

Multiply by $T_{2;3}$ we got

$$ 
\begin{bmatrix}
 1 & 0 & -3 \\
 0 & 3 & 9  \\
 0 & 0 & 0  \\
\end{bmatrix}
$$

Multiply by $S_{2,1/3}$ we got

$$ 
\begin{bmatrix}
 1 & 0 & -1 \\
 0 & 1 & 3  \\
 0 & 0 & 0  \\
\end{bmatrix}
$$

Then $x = (1, -3, 1)$ can be one solution.

$\square$

### 3.3.9.

Balance the chemical equation

$$ 
\text{Ca} + \text{H}_3 \text{PO}_4
\rightarrow
\text{Ca}_3 \text{P}_2 \text{O}_8 + \text{H}_2
$$

**Solution**

$$ 
\begin{bmatrix}
    1 & 0 & -3 &  0 \\
    0 & 3 &  0 & -2 \\
    0 & 1 & -2 &  0 \\
    0 & 4 & -8 &  0 \\
\end{bmatrix}
$$

So $(3, 2, 1, 3)$ is a solution.

$$ 
3 \text{Ca} + 2\text{H}_3 \text{PO}_4
\rightarrow
1 \text{Ca}_3 \text{P}_2 \text{O}_8 + 3 \text{H}_2
$$

$\square$

### 3.3.10.

Prove by induction that the only square echelon matrix with all new
columns is the identity matrix.

**Proof**:

Assume this is true for $n \times n$, i.e. $E_n = I_n$.

Consider $(n+1) \times (n+1)$ echelon matrix. Since the last column
is a new column, then

$$ 
E_{n+1} =
\begin{bmatrix}
    A & 0 \\
    0 & 1 \\
\end{bmatrix}
$$

If any column of $A$ is not a new column, then it does not have a leading $1$'s.
Then that column does not have a leading $1$'s in $E_{n+1}$ either.
So it's not a new column in $E_{n+1}$. We have a contradiction.

So every column in $A$ is a new column, and since its size is $n \times n$,
then $A = I_n$. So $E_{n+1} = I_{n+1}$.

$\square$

### 3.3.11.

Are the following matrices invertible? Find the inverse when possible,
and then check your answer.

**Solution**:

We check (b)

$$ 
B = [P | I] = \\
\begin{bmatrix}
2 &  5 & -1 &  1 &  0 &  0 \\
4 & -1 &  2 &  0 &  1 &  0 \\
6 &  4 &  1 &  0 &  0 &  1 \\
\end{bmatrix}
$$

Apply $R_{2;1,-2}$

$$ 
\begin{bmatrix}
2 &  5  & -1 &   1 &  0 &  0 \\
0 & -11 &  4 &  -2 &  1 &  0 \\
6 &  4  &  1 &   0 &  0 &  1 \\
\end{bmatrix}
$$

Apply $R_{3;1,-3}$

$$ 
\begin{bmatrix}
2 &  5   & -1 &   1 &  0 &  0 \\
0 & -11  &  4 &  -2 &  1 &  0 \\
0 & -11  &  4 &  -3 &  0 &  1 \\
\end{bmatrix}
$$

Apply $R_{3;2,-1}$

$$ 
\begin{bmatrix}
2 &  5   & -1 &   1 &  0  &  0 \\
0 & -11  &  4 &  -2 &  1  &  0 \\
0 &   0  &  0 &  -1 &  -1 &  1 \\
\end{bmatrix}
$$

So it's not invertible.

$\square$

### 3.3.12.

The matrix $A$ is called lower triangular if $a_{ij} = 0$ whenever $i < j$.
If $A$ is a lower triangular square matrix with all diagonal entries equal to $1$,
show that $A$ is invertible and $A^{−1}$ takes the same form.

**Proof**:

We can mutiply $A$ with $R_{2;1,-a_{2,1}}, \cdots R_{n;1,-a_{n,1}}$ to get the
first column to become a new column, let the new matrix be $A_1$. And the right
half be $B_1$. Then $B_1$ is still a lower triangular.

Similarly, we can mutiply $A_1$ with
$R_{3;2,-a_{3,2}}, \cdots R_{n;2,-a_{n,2}}$ to get $A_2$ and $B_2$ which are also
lower triangular.

Eventually, we can get $A_n = I_n$ and $B_n$, which are also lower triangular.

$\square$

### 3.3.13.

This exercise refers back to the Gram–Schmidt exercise in Chapter 2.
That exercise expresses the relation between the vectors $\{x'_j\}$  and 
the vectors
$\{x_j\}$ formally as $x' = Ax$, where $x'$ is a column vector whose 
entries are 
the vectors $x'_1, \cdots, x'_n$, $x$ is the corresponding column vector 
of $x_j$’s, and $A$ is an $n×n$ lower triangular matrix.

Show that each $x_j$ has the form

$$ 
x_j = a'_{j1} x'_1 + \cdots + a'_{j,j-1} x'_{j-1} + x'_j
$$

and thus every linear combination of the original $\{x_j\}$ is also a 
linear combination of the new $\{x'_j\}$.

**Proof**:

Since $A$ is lower triangular matrix, from 3.3.12, $A$ is invertible,
and $A^{-1}$ is also a lower triangular matrix, such that

$$ 
x = A^{-1} x'
$$

If we expand it, we have

$$ 
x_j = a'_{j1} x'_1 + \cdots + a'_{j,j-1} x'_{j-1} + x'_j
$$

$\square$
