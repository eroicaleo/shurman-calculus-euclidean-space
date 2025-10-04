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
