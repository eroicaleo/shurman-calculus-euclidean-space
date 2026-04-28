# Chapter 4 The Derivative

## 4.2 New Environment: The Bachmann–Landau Notation

### Definition 4.2.1 ($o(1)$-mapping, $\mathcal{O}(h)$-mapping, $o(h)$-mapping).

Consider a mapping from some ball about the origin in one Euclidean space to a
second Euclidean space,

$$ 
\varphi : B(0_n, \epsilon) \rightarrow \mathbb{R}^m
$$

where $n$ and $m$ are positive integers and $ε > 0$ is a positive real number.
The mapping $\varphi$ is smaller than order $1$ if

for every $c > 0$, $|\varphi (h)| ≤ c$ for all small enough $h$.

The mapping $\varphi$ is of order $h$ if

for some $c > 0$, $|\varphi (h)| ≤ c|h|$ for all small enough $h$.

The mapping $\varphi$ is smaller than order $h$ if

for every $c > 0$, $|\varphi (h)| ≤ c|h|$ for all small enough $h$.

A mapping smaller than order $1$ is denoted $o(1)$, a mapping of order $h$ is
denoted $\mathcal{O}(h)$, and a mapping smaller than order $h$ is denoted $o(h)$. Also $o(1)$
can denote the collection of $o(1)$-mappings, and similarly for $\mathcal{O}(h)$ and $o(h)$.

### Proposition 4.2.3 (Dominance principle for the Landau spaces).

Let $\varphi$ be $o(1)$, and suppose that $|\psi (h)| ≤ |\varphi (h)|$ for all small enough $h$.
Then also $ψ$ is $o(1)$. And similarly for $O(h)$ and for $o(h)$.

### Proposition 4.2.4 (Vector space properties of the Landau spaces).

For every fixed domain-ball $B(0_n,ε)$ and codomain-space $\mathbb{R}^m$, the
$o(1)$-mappings form a vector space, and $\mathcal{O}(h)$ forms a subspace, of which $o(h)$ forms a
subspace in turn. Symbolically,

$$ 
o(1) + o(1) = o(1), \mathbb{R}o(1) = o(1) \\
\mathcal{O}(h) + \mathcal{O}(h) = \mathcal{O}(h), \mathbb{R}\mathcal{O}(h) = \mathcal{O}(h) \\
o(h) + o(h) = o(h), \mathbb{R}o(h) = o(h) \\
$$

**Proof**:

$o(1)$:

Assume $\varphi , \psi$ are $o(1)$, for any given $c$, we can find $h_1$ such that when $h < h_1$,
$|\varphi (h)| ≤ c/2$. Similarly, we can find $h_2$ such that when $h < h_2$, $|\psi (h)| ≤ c/2$.

Then let $h_0 = \min \{h_1, h_2\}$, when $h < h_0$,

$$ 
|\varphi(h) + \psi(h)| \leq |\varphi(h)| + |\psi(h)| < c/2 + c/2 = c
$$

For the scalor multiplication, given $\alpha$, we want to show $\alpha \varphi$ is also $o(1)$.
For any given $c$, we can find $\delta > 0$, such that if $|h| \leq \delta$, $|\varphi (h)| \leq  c/|\alpha|$.

So $|\alpha \varphi(h)| = |\alpha | |\varphi (h)| \leq |\alpha| |c/|\alpha| = c$

$\mathcal{O}(h)$:

Assume $\varphi , \psi$ are $\mathcal{O}(h)$.
We can find $c_1, \delta_1$, if $|h| \leq \delta_1, \varphi (h) \leq c_1 |h|$.
We can find $c_2, \delta_2$, if $|h| \leq \delta_2, \psi (h) \leq c_2 |h|$.

Let $c = 2 \cdot \max \{c_1, c_2\}, \delta = \min \{\delta_1, \delta_2\}$, when $|h| \leq \delta$,

$$ 
|\varphi (h) + \psi (h)| \leq |\varphi (h)| + |\psi (h)|
\leq c_1|h| + c_2 |h| \leq c |h|
$$

For the scalor multiplication, given $\alpha$, we want to show $\alpha \varphi$ is also $\mathcal{O}(h)$.

Note $|\alpha \varphi(h)| = |\alpha | |\varphi (h)| \leq (|\alpha |c) |\varphi (h)|$, so
$\alpha \varphi$ is also $\mathcal{O}(h)$.

$o(h)$:

Assume $\varphi , \psi$ are $o(h)$, for any given $c$, we can find $\delta_1$ such that when $h < \delta_1$,
$|\varphi (h)| ≤ c|h|/2$. Similarly, we can find $\delta_2$ such that when $h < \delta_2$, $|\psi (h)| ≤ c|h|/2$.

Then let $\delta = \min \{\delta_1, \delta_2\}$, when $h < \delta$,

$$ 
|\varphi(h) + \psi(h)| \leq |\varphi(h)| + |\psi(h)| < c|h|/2 + c|h|/2 = c|h|
$$

For the scalor multiplication, given $\alpha$, we want to show $\alpha \varphi$ is also $o(h)$.
For any given $c$, we can find $\delta > 0$, such that if $|h| \leq \delta$, $|\varphi (h)| \leq  (c/|\alpha|)|h|$.

So $|\alpha \varphi(h)| = |\alpha | |\varphi (h)| \leq |\alpha| c/|\alpha||h| = c|h|$

$\square$

### Proposition 4.2.5.

Every linear mapping is $\mathcal{O}(h)$. The only $o(h)$
linear mapping is the zero mapping.

**Proof**:

Let $T : \mathbb{R}^n \longrightarrow \mathbb{R}^m$, The unit sphere in
$\mathbb{R}^n$ is compact.

$T$ is linear, then we can find matrix $A$, such that $b = T(a) = Aa$.
Then $b_i = A_{i, .}a$, then $|b_i| = |⟨A_{i, .},a⟩| \leq |A_{i, .}||a|$.
When $|a|$ is small, $|b_i|$ is also small.
So each component is continuous.
So $T$ is continuous.

Then the image of unit sphere is also compact. Since $||$ is also
continuous, then we can find $c$, such that $|T(h_0)| \leq c$ for all $|h_0| = 1$.

Then for any $h$, $h = |h| h_0$, then $|T(|h| h_0)| = ||h|T(h_0)| \leq c|h|$.

Assume $T$ is non-zero, $|T(h_0)| = 2c > 0$. For any $h = |h| h_0$,

$$ 
|T(h)| = |h| |T(h_0)| = 2c|h| > c|h|
$$

$\square$

### Proposition 4.2.6 (Product property for Landau functions).

Consider two scalar-valued functions and their product function,

$$ 
\varphi, \psi , \varphi \psi : B(0_n, \epsilon) \rightarrow \mathbb{R}
$$

If $\varphi$ is $o(1)$ and $ψ$ is $\mathcal{O}(h)$ then $\varphi ψ$ is $o(h)$. Especially, the product of two linear functions is $o(h)$.

**Proof**:

Given $c > 0$. 

Since $ψ$ is $\mathcal{O}(h)$, we can find $d$ such that
$\left| ψ (h) \right| \leq d |h|$ if $|h| \leq \delta_1$.

For $\varphi$, since it's $o(1)$, we can find $\delta_2$, if
$|h| \leq \delta_2$, $\left| \varphi (h) \right| \leq c/d$.

Let $\delta = \min \{\delta_1, \delta_2\}$, if $|h| \leq \delta$, then
$\left| ψ (h)\varphi (h) \right| \leq (c/d)(d|h|) = c|h|$.

$\square$

### Proposition 4.2.7 (Composition properties of the Landau spaces).

The composition of $o(1)$-mappings is again an $o(1)$-mapping. Also, the
composition of $\mathcal{O}(h)$-mappings is again an $\mathcal{O}(h)$-mapping. 
Furthermore, the composition of an $\mathcal{O}(h)$-mapping and an
$o(h)$-mapping, in either order, is again an $o(h)$-mapping. Symbolically,

$$ 
\begin{align*}
    o(o(1)) &= o(1)\\
    \mathcal{O}(\mathcal{O}(h)) &= \mathcal{O}(h) \\
    o(\mathcal{O}(h)) &= o(h) \\
    \mathcal{O}(o(h)) &= o(h) \\
\end{align*} 
$$

That is, $o(1)$ and $\mathcal{O}(h)$ absorb themselves, and $o(h)$ absorbs 
$\mathcal{O}(h)$ from either side.

**Proof**:

$o(o(1)) = o(1)$

Assume $\psi, \varphi$ are both $o(1)$.

Given $c > 0$.

Since $ψ$ is $o(1)$, we can find $\delta_1$ , such that
if $|h| \leq \delta_1$, $\left| ψ (h) \right| \leq c$.

Since $\varphi$ is $o(1)$, we can find $\delta_2$ , such that
if $|h| \leq \delta_2$, $\left| \varphi (h) \right| \leq \delta_1$.

Let $\delta = \min \{\delta_1, \delta_2\}$, if $|h| \leq \delta$,
$|\varphi (h)|\leq \delta_1$.

Then

$$ 
|\psi (\varphi (h))| \leq c
$$

---
$\mathcal{O}(\mathcal{O}(h)) = \mathcal{O}(h)$

Assume $\psi, \varphi$ are both $\mathcal{O}(h)$.

Since $ψ$ is $\mathcal{O}(h)$, we can find $c_1$ and $\delta_1$ , such that
if $|h| \leq \delta_1$, $\left| ψ (h) \right| \leq c_1 |h|$ 

Since $\varphi$ is $\mathcal{O}(h)$, we can find $c_2$ and $\delta_2$,
such that
if $|h| \leq \delta_2$, $\left| \varphi (h) \right| \leq c_2 |h|$

Let $\delta = \min \{\delta_1 / c_2, \delta_2\}$, if $|h| \leq \delta$,
$|\varphi (h)|\leq c_2 |h| \leq \delta_1$.

Then

$$ 
|\psi (\varphi (h))| \leq
c_1 |\varphi (h)| \leq c_1 c_2|h|
$$

So we find $c_1 \cdot c_2$.

---
$o(\mathcal{O}(h)) = o(h)$

Assume $ψ$ is $\mathcal{O}(h)$ and $\varphi$ is $o(h)$.

Given $c > 0$.

Since $ψ$ is $\mathcal{O}(h)$, we can find $d$ and $\delta_1$ , such that
if $|h| \leq \delta_1$, $\left| ψ (h) \right| \leq d |h|$ 

Since $\varphi$ is $o(h)$, we can find $\delta_2$, if $|h| \leq \delta_2$,
$|\varphi (h)| \leq (c/d) |h|$.

So let $|h| \leq \min \{\delta_1, \delta_2 / d\}$,
so $|\psi (h)| \leq d|h| \leq \delta_2$.
Then

$$
\left| \varphi (\psi (h)) \right| \leq (c/d)|\psi (h)|
\leq (c/d) (d |h|) = c|h|
$$

---
$\mathcal{O}(o(h)) = o(h)$

Assume $ψ$ is $\mathcal{O}(h)$ and $\varphi$ is $o(h)$.

Given $c > 0$.

Since $ψ$ is $\mathcal{O}(h)$, we can find $d$ and $\delta_1$ , such that
if $|h| \leq \delta_1$, $\left| ψ (h) \right| \leq d |h|$ 

Since $\varphi$ is $o(h)$, we can find $\delta_2$, if $|h| \leq \delta_2$,
$|\varphi (h)| \leq (c/d) |h|$.

So let $|h| \leq \min \{(d/c)\delta_1, \delta_2\}$, so
$|\varphi (h)| \leq (c/d)|h| \leq \delta_1$.

$$ 
|\psi (\varphi (h))| \leq d |\varphi (h)| \leq d ((c/d)|h|) = c|h|
$$

$\square$
