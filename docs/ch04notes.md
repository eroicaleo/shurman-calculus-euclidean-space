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

## 4.3 One-Variable Revisionism: The Derivative Redefined

The one-variable derivative as recalled at the beginning of the chapter,

$$ 
f'(a) = \lim \limits_{h \to 0}
\frac{
f(a+h) - f(a)
}{h}
$$

is a construction. To rethink the derivative,
we should characterize it instead.

Consider

$$ 
g(h) = f(a+h)−f(a)−th.
$$

To reiterate, the idea
that f has a tangent of slope t at $(a,f(a))$ has been normalized to
the tidier idea that $g$ has slope $0$ at the origin:

> To say that the graph of $g$ is horizontal at the origin is to say that for
> every positive real number $c$, however small, the region between the
> lines of slope $±c$ contains the graph of $g$ close enough to the origin.

that is

> The intuitive condition for the graph of $g$ to be horizontal at the origin
> is precisely that $g$ is $o(h)$.
> The horizontal nature of the graph of $g$ at the
> origin connotes that the graph of $f$ has a tangent of slope $t$ at
> $(a,f(a))$.

### Definition 4.3.1 (Interior point).

Let $A$ be a subset of $R^n$, and let a be
a point of $A$. Then $a$ is an interior point of $A$ if some $ε$-ball about
$a$ is a subset of $A$.
That is, $a$ is an interior point of $A$ if $B(a,ε) ⊂ A$ for some $ε > 0$.

### Definition 4.3.2 (Derivative).

Let $A$ be a subset of $R^n$, let $f : A → R^m$
be a mapping, and let $a$ be an interior point of $A$. Then $f$ is 
diﬀerentiable at $a$ if there exists a linear mapping $T_a : R^n → R^m$ 
satisfying the condition

$$ 
\tag{4-1}
f(a+h)−f(a)−Ta(h) \text{ is } o(h).
$$

This $T_a$ is called the derivative of $f$ at $a$,
written $Df_a$ or $(Df)_a$. When $f$
is diﬀerentiable at $a$, the matrix of the linear mapping $Df_a$
is written $f'(a)$
and is called the Jacobian matrix of $f$ at $a$.

### Proposition 4.3.3 (Uniqueness of the derivative).

Let $f : A → R^m$
(where $A ⊂ R^n$) be diﬀerentiable at $a$.
Then there is only one linear mapping satisfying the definition of $Df_a$.

**Proof**:

Assume we have $T, \tilde{T}$,

$$ 
\begin{align*}
f(a+h) - f(a) - T(h) &= o(h) \\
f(a+h) - f(a) - \tilde{T}(h) &= o(h) \\
& \Rightarrow \\
T(h) - \tilde{T}(h) &= o(h) \\
& \Rightarrow \\
(T - \tilde{T})(h) &= o(h)
\end{align*}
$$

Since the only linear $o(h)$ mapping is $0$ mapping, then $T = \tilde{T}$.

$\square$

### Proposition 4.3.4.

If $f$ is diﬀerentiable at $a$ then $f$ is continuous at $a$.

**Proof**:

$$ 
\begin{align*}
f(a+h)−f(a) \\
&= f(a+h)−f(a)−T_a(h)+T_a(h) \\
&= o(h)+O(h) \\
&= O(h) \\
&= o(1).
\end{align*} 
$$

$\square$

## 4.4 Basic Results and the Chain Rule

### Proposition 4.4.1 (Derivatives of constant and linear mappings).

(1) Let $C : A → R^m$ (where $A ⊂ R^n$) be the constant mapping
$C(x) = c$ for
all $x ∈ A$, where $c$ is some fixed value in $R^m$.
Then the derivative of $C$ at
every interior point $a$ of $A$ is the zero mapping.

**Proof**:

$$ 
\begin{align*}
&C(a+h) - C(a) - 0(h) \\
&= c - c - 0 \\
&= 0 \\
&= o(h)
\end{align*} 
$$

$\square$

(2) The derivative of a linear mapping $T : R^n → R^m$ at every point $a ∈ R^n$
is again $T$.

**Proof**:

$$ 
\begin{align*}
& T(a+h) - T(a) - T(h) \\
&= T(a) + T(h) - T(a) - T(h) \\
&= 0 \\
&= o(h) \\
\end{align*} 
$$

$\square$

### Proposition 4.4.2 (Linearity of the derivative).

Let $f : A → R^m$
(where $A ⊂ R^n$) and $g : B → R^m$ (where $B ⊂ R^n$) be mappings,
and let a be
a point of $A∩B$. Suppose that $f$ and $g$ are diﬀerentiable at a with 
derivatives $Df_a$ and $Dg_a$. Then:

(1) The sum $f + g : A ∩ B → R^m$ is diﬀerentiable at $a$ with derivative
$D(f +g)_a = Df_a +Dg_a$.

**Proof**:

$$
\begin{align*}
&(f+g)(a+h) - (f+g)(a) - (Df_a +Dg_a)(h) \\
&=
(f(a+h) - f(a) - Df_a(h)) +
(g(a+h) - g(a) - Dg_a(h)) \\
&= o(h) + o(h) \\
&= o(h)
\end{align*} 
$$

$\square$

(2) For every $\alpha ∈ R$, the scalar multiple $\alpha f : A → R^m$ is 
diﬀerentiable 
at $a$ with derivative $D(\alpha f)_a = \alpha Df_a$.

**Proof**:

$$ 
\begin{align*}
&(\alpha f)(a+h) - (\alpha f)(a) - (\alpha Df_a)(h) \\
&= \alpha (f)(a+h) - \alpha (f)(a) - \alpha (Df_a)(h) \\
&= \alpha (f(a+h) - f(a) - (Df_a)(h)) \\
&= \alpha o(h) \\
&= o(h)
\end{align*}
$$

$\square$

### Theorem 4.4.3 (Chain rule).

Let $f : A \rightarrow R^m$ (where $A ⊂ R^n$) be a
mapping, let $B ⊂ R^m$ be a set containing $f(A)$, and
let $g : B \rightarrow R^ℓ$ be a mapping.
Thus the composition $g◦f : A \rightarrow R^ℓ$ is defined. If $f$ is 
diﬀerentiable at the point $a ∈ A$, and $g$ is diﬀerentiable
at the point $f(a) ∈ B$, then the
composition $g ◦f$ is diﬀerentiable at the point $a$,
and its derivative there is

$$ 
D(f \circ g)_a =
Dg_{f(a)} \circ Df_a
$$

In terms of Jacobian matrices, since the matrix of a composition is the product
of the matrices, the chain rule is

$$ 
(g ◦f)'(a) = g '(f(a))f'(a).
$$

**Proof**:

For simplicity, we first take $a = 0_n$ and $f(a) = 0_m$.

$$ 
\begin{align*}
f(h) &= S(h) + o(h) \\
g(k) &= T(k) + o(k) \\
\end{align*} 
$$

Then

$$
\begin{align*}
g(f(h)) &= T(f(h)) + o(f(h)) \\
&= T(S(h) + o(h)) + o(S(h) + o(h)) \\
&= T(S(h)) + T(o(h)) + o(O(h) + o(h)) \\
&= T(S(h)) + O(o(h)) + o(O(h)) \\
&= T(S(h)) + o(h) + o(h) \\
&= T(S(h)) + o(h) \\
\end{align*}  
$$

Then for the general

$$ 
\begin{align*}
f(a + h) &= f(a) + S(h) + o(h) \\
g(f(a) + k) &= g(f(a)) + T(k) + o(k) \\
\end{align*} 
$$

Then

$$ 
\begin{align*}
g(f(a+h))
&= g(f(a) + S(h) + o(h)) \\
&= g(f(a)) + T(S(h) + o(h)) + o(S(h) + o(h)) \\
&= g(f(a)) + T(S(h)) + T(o(h)) + o(O(h) + o(h)) \\
&= g(f(a)) + T(S(h)) + O(o(h)) + o(O(h)) \\
&= g(f(a)) + T(S(h)) + o(h) + o(h) \\
&= g(f(a)) + T(S(h)) + o(h) \\
\end{align*} 
$$

$\square$

### Lemma 4.4.4 (Derivatives of the product and reciprocal functions).

Define the product function,

$$ 
p : \mathbb{R}^2 \longrightarrow \mathbb{R}, \qquad p(x,y) = xy,
$$

and define the reciprocal function

$$ 
r : \mathbb{R} - \{0\} \longrightarrow \mathbb{R}, \qquad r(x) = 1/x,
$$

Then

(1) The derivative of $p$ at every point $(a,b) ∈ R^2$ exists and is

$$ 
Dp_{(a,b)}(h, k) = ak + bh
$$

**Proof**:

$$ 
\begin{align*}
(x+h)(y+k) - xy - (ak + bh)
&= hk \\
\end{align*}
$$

Since $|h| \leq |(h,k)|, |k| \leq |(h,k)|$, so
$|h||k| \leq |(h,k)|^2 = o(h,k)$.

$\square$

(2) The derivative of $r$ at every nonzero real number a exists and is

$$ 
Dr_a(h) = -h / a^2
$$

**Proof**:

$$ 
\begin{align*}
r(a+h) - r(a) - Dr_a(h)
&= 1/(a+h) - 1/a + h / a^2 \\
&= -h/(a+h)a + h / a^2 \\
&= h ( \frac{1}{a^2} - \frac{1}{a(a+h)}) \\
&= \frac{h}{a} \frac{h}{a(a+h)} \\
&= \frac{h^2}{a^2(a+h)} \\
\end{align*} 
$$

Since when $|h| < |a/2|$, $|a+h| \geq ||a| - |h|| > |a| - |a/2| = |a/2|$.

$$ 
\left| \frac{h^2}{a^2(a+h)} \right| 
\leq
\left| \frac{2h^2}{a^3} \right| 
$$

So it's $o(h)$.

$\square$

### Proposition 4.4.5 (Multivariable product and quotient rules).

Let $f : A → R$ (where $A ⊂ \mathbb{R}^n$) and
$g : B → \mathbb{R}$ (where $B ⊂ \mathbb{R}^n$) be functions,
and let $f$ and $g$ diﬀerentiable at $a$. Then:

(1) $fg$ is diﬀerentiable at $a$ with derivative

$$ 
D(fg)_a = f(a) Dg_a + g(a) Df_a
$$

**Proof**:

Consider

$$ 
\begin{align*}
h : \mathbb{R}^n \longrightarrow \mathbb{R}^2 &\qquad h(a) = (f(a), g(a)) \\
p : \mathbb{R}^2 \longrightarrow \mathbb{R} &\qquad p(x, y) = xy \\
\end{align*} 
$$

Then $fg = p \circ h$.

$$
\begin{align*}
D(fg)_a &= D(p \circ h)_a \\
&= Dp_{h(a)} \circ Dh_a \\
\end{align*} 
$$

Note $Dh_a = (Df_a, Dg_a)$, so we have

$$
\begin{align*}
(Dp_{h(a)} \circ Dh_a)(k)
&= Dp_{h(a)}(Dh_a(k)) \\
&= Dp_{h(a)}(Df_a(k), Dg_a(k)) \\
&= g(a)Df_a(k) + f(a) Dg_a(k) \\
&= (f(a) Dg_a + g(a) Df_a)(k) \\
\end{align*}
$$

(2) If $g(a) \neq 0$ then $f/g$ is diﬀerentiable at a with derivative

$$ 
D(\frac{f}{g})_a =
\frac{
g(a)Df_a−f(a)Dg_a
}{
g(a)^2
}
$$

**Proof**:

Consider

$$
\begin{align*}
D(r \circ g)_a(k)
&= (Dr_{g(a)} \circ Dg_a)(k) \\
&= Dr_{g(a)} (Dg_a(k)) \\
&= -\frac{Dg_a(k)}{g^2(a)} \\
&= (-\frac{Dg_a}{g^2(a)}) (k) \\
\end{align*} 
$$

So $D(r \circ g)_a = -\frac{Dg_a}{g^2(a)}$ 

$$ 
\begin{align*}
h : \mathbb{R}^n \longrightarrow \mathbb{R}^2 &\qquad h(a) = (f(a), 1/g(a)) \\
p : \mathbb{R}^2 \longrightarrow \mathbb{R} &\qquad p(x, y) = xy \\
\end{align*} 
$$

Then $f/g = p \circ h$.

$$
\begin{align*}
D(f/g)_a &= D(p \circ h)_a \\
&= Dp_{h(a)} \circ Dh_a \\
\end{align*} 
$$

Note $Dh_a = (Df_a, -\frac{Dg_a}{g^2(a)})$, so we have

$$ 
\begin{align*}
(Dp_{h(a)} \circ Dh_a)(k)
&= Dp_{h(a)}(Dh_a(k)) \\
&= Dp_{h(a)}(Df_a(k), -\frac{Dg_a}{g^2(a)}(k)) \\
&= \frac{1}{g(a)} Df_a(k) - f(a) \frac{Dg_a}{g^2(a)}(k) \\
&= \left(\frac{g(a) Df_a - f(a) Dg_a}{g^2(a)}\right)(k) \\
\end{align*}
$$

So

$$ 
D\left(\frac{f}{g}\right)_a =
\frac{
g(a)Df_a−f(a)Dg_a
}{
g(a)^2
}
$$

$\square$

### Another example

Consider $f(x,y) = (x^2-y)(y+1)$ for all $(x,y) \in \mathbb{R}^2$

Let

$$ 
\begin{align*}
X(x,y) &= x \\
Y(x,y) &= y \\
\end{align*} 
$$

Then

$$ 
f = \frac{
X^2 - Y
}{
Y + 1
}
$$

Let

$$ 
\begin{align*}
l &= X^2 - Y \\
g &= Y + 1 \\
a &= (x, y) \\
\end{align*} 
$$

Then note

$$
\begin{align*}
g(a) &= y + 1\\
g(a+(h,k)) - g(a) &= (y+k+1) - (y+1) = k\\
Dg_a(h,k) &= k \\
\end{align*} 
$$

Also note

$$
\begin{align*}
l(a) &= x^2 - y \\
l(a+(h, k)) - l(a) &= ((x+h)^2 - (y+k)) - (x^2 - y)\\
&= (2xh + h^2) - k \\
Dl_a(h,k) &= 2xh - k
\end{align*}  
$$

Combine these together, we have

$$ 
\begin{align*}
Df_a(h,k) &=
D\left( \frac{l}{g}\right)_a (h,k)\\
&=
\frac{
g(a) Dl_a - l(a) Dg_a
}{g^2(a)} (h,k) \\
&=
\frac{
(y+1) (2xh-k) - (x^2 - y) k
}{(y+1)^2} \\
&=
\frac{2x}{y+1} h - \frac{x^2+1}{(y+1)^2} k \\
\end{align*} 
$$

This results are confirmed by the textbook.

Now we can follow the approach in the text book.

$$ 
f = \frac{
X^2 - Y
}{
Y + 1
}
$$

$$ 
\begin{align*}
&Df_a(h, k) \\
\\
&\text{Use 4.4.5 (2) quotient rule} \\
&= \frac{
(Y+1)(a)D(X^2-Y)_a - (X^2-Y)(a) D(Y+1)_a
}{(Y+1)^2(a)}(h, k)\\
\\
&\text{Use } (Y+1)(a) = y+1 \\
&= \frac{
(y+1)D(X^2-Y)_a - (X^2-Y)(a) D(Y+1)_a
}{(y+1)^2}(h, k)\\
\\
&\text{Use } (X^2-Y)(a) = x^2-y \\
&= \frac{
(y+1)D(X^2-Y)_a - (x^2-y) D(Y+1)_a
}{(y+1)^2}(h, k)\\
\\
&\text{Use 4.4.2 (Linearity of the derivative)} \\
&= \frac{
(y+1)(D(X^2)_a-DY_a) - (x^2-y) (DY_a+D1_a)
}{(y+1)^2}(h, k)\\
\\
&\text{Use 4.4.1 Derivatives of constant and linear mappings} \\
&= \frac{
(y+1)(D(X^2)_a-Y) - (x^2-y) Y
}{(y+1)^2}(h, k)\\
\\
&\text{Use 4.4.5 (a) product rule} \\
&= \frac{
(y+1)(2X(a)DX_a-Y) - (x^2-y) Y
}{(y+1)^2}(h, k)\\
\\
&\text{Use 4.4.1 Derivatives of constant and linear mappings} \\
&= \frac{
(y+1)(2xX-Y) - (x^2-y) Y
}{(y+1)^2}(h, k)\\
\\
&= \frac{
2x(y+1)X - (x^2+1) Y
}{(y+1)^2}(h, k)\\
\\
&= \frac{
2x
}{(y+1)}h - \frac{x^2+1}{(y+1)^2}k\\
\end{align*}
$$

$\square$

## 4.5 Calculating the Derivative

### Definition 4.5.1 (Partial derivative).

Let $A$ be a subset of $\mathbb{R}^n$, let
$f : A → R$ be a function, and let $a = (a_1,...,a_n)$ be an interior point of $A$. Fix
$j ∈ \{1,...,n\}$. Define

$$ 
\varphi(t) = f(a_1,...,a_{j−1},t,a_{j+1},...,a_n) \quad \text{for } t \text{ near} a_j
$$

Then the $j$th partial derivative of $f$ at $a$ is defined as

$$ 
D_j f(a) = \varphi'(a_j)
$$

if $\varphi'(a_j)$ exists. Here the prime signifies ordinary one-variable diﬀerentiation.

Equivalently,

$$ 
D_j f(a) = \lim \limits_{t \to 0} \frac{
f(a+t e_j) - f(a)
}{t}
$$

if the limit exists and it is not being taken at an endpoint of the domain of
the diﬀerence quotient.

### Theorem 4.5.2 (The derivative in coordinates: necessity).

Let the
mapping $f : A \longrightarrow \mathbb{R}^m$ (where $A ⊂ \mathbb{R}^n$) be 
diﬀerentiable at the point $a ∈ A$.
Then for each $i ∈ \{1,...,m\}$ and $j ∈ \{1,...,n\}$,
the partial derivative $D_{j}f_{i}(a)$ exists.
Furthermore, each $D_{j}f_{i}(a)$ is the $(i,j)$th entry of the Jacobian matrix
of $f$ at $a$. Thus the Jacobian matrix is

$$
f'(a) =
\begin{bmatrix}
D_1f_1(a) & \cdots & D_{n}f_1(a) \newline
D_1f_2(a) & \cdots & D_{n}f_2(a) \newline
\cdots   & \ddots & \cdots   \newline
D_1f_{m}(a) & \cdots & D_{n}f_{m}(a) \newline
\end{bmatrix}
$$

**Proof**:

The derivative of the component function $f_i$ at a is described by the $i$th
row of $f'(a)$.

Call the row entries $d_{i1},d_{i2},...,d_{in}$. Since linear of is matrix
times, it follows that

$$ 
Df_{i}(a)(t e_j) = d_{ij}t \quad \text{ for all } t \in \mathbb{R} 
$$

Let $h= te_j$ with $t$ a variable real number, so that $h → 0_n$ as $t → 0$,

Note that $f_i(a+h)−f_i(a)−Df_i(a)(h) = o(h)$ so we have

$$ 
\begin{align*}
0 &= \lim \limits_{t \to 0}
\frac{
|f_i(a+t e_j)−f_i(a)−Df_i(a)(t e_j)|  
}{| t e_j|} \\
&= \lim \limits_{t \to 0}
\frac{
|f_i(a+t e_j)−f_i(a)− d_{ij}t|  
}{| t |} \\
&= \lim \limits_{t \to 0} \left| 
\frac{
    f_i(a+t e_j)−f_i(a)
}{t} -d_{ij}
 \right| 
\end{align*} 
$$

So we have

$$ 
\lim \limits_{t \to 0} 
\frac{
f_i(a+t e_j)−f_i(a)
}{t} = d_{ij}
$$

$\square$

### Example

$$ 
f : \mathbb{R}^2 \longrightarrow \mathbb{R}^2,
\quad
f(x,y) =
\begin{cases}
    \frac{2xy}{x^2+y^2} &\text{if } (x,y) \neq (0,0)\\
    0 &\text{if } (x,y) = (0,0)\\
\end{cases} 
$$

It's easy to see $D_{1}f_{}(0,0) = D_{2}f_{}(0,0) = 0$, but $f$ is
not continuous at $(0,0)$ much less diﬀerentiable there. (If we approach $(0,0)$
from $x = y$.)

### Theorem 4.5.3 (The derivative in coordinates: suﬃciency).

Let $f : A \longrightarrow \mathbb{R}^m$ (where $A ⊂ \mathbb{R}^n$)
be a mapping, and let $a$ be an interior point of $A$.
Suppose that for each $i ∈ \{1,...,m\}$ and $j ∈ \{1,...,n\}$,
the partial derivative
$D_{j}f_{i}$ exists not only at $a$ but at all points in some $ε$-ball about $a$,
and the partial derivative $D_{j}f_{i}$ is continuous at $a$.
Then $f$ is diﬀerentiable at $a$.

The necessary conditions in Theorem 4.5.2 are:

> If a graph has a well-fitting plane at some point, then at that point
we see well-fitting lines in the cross sections parallel to the coordinate
axes.

The suﬃcient conditions in Theorem 4.5.3 are:

> If a graph has well-fitting lines in the cross sections at and near the
point, and if those lines don’t change much as we move among cross
sections at and near the point, then the graph has a well-fitting plane.

**Proof**:

It's enough to prove $m = 1$.

$$ 
\begin{align*}
f(a+h) - f(a) =
&f(a_1 +h_1,a_2 +h_2,a_3 +h_3)−f(a_1,a_2 +h_2,a_3 +h_3) \\
&+ f(a_1,a_2 +h_2,a_3 +h_3)−f(a_1,a_2,a_3 +h_3) \\
&+ f(a_1,a_2,a_3 +h_3)−f(a_1,a_2,a_3) \\
& \text{ apply the mean value theorem
in two directions } \\
& \text{ and the one-variable derivative’s characterizing property in
the third} \\
& \Rightarrow \\
= &D_1f(a_1 +c_1,a_2 +h_2,a_3 +h_3)h_1 \\
&+ D_2f(a_1, a_2 + c_2, a_3+ h_3)h_2 \\
&+ D_3f(a_1, a_2, a_3)h_3 + o(h_3) \\
& \text{ Since partial derivatives are continuous at the point } \\
= &(D_1f(a) + o(1)) h_1 \\
&+ (D_2f(a) + o(1)) h_2 \\
&+ (D_3f(a) + o(1)) h_3 + o(h) \\
= &D_1f(a) h_1 + D_2f(a) h_2 + D_3f(a) h_3 + o(h)
\end{align*} 
$$

$\square$

---
**Thus, to reiterate some earlier discussion and to amplify slightly:**

> The diﬀerentiability of $f$ at a implies the existence of all the partial 
derivatives at $a$, and the partial derivatives are the entries of the 
derivative matrix

> while the existence of all the partial derivatives at and about $a$,
> and their continuity at $a$, combine to imply the
> diﬀerentiability of $f$ at $a$

> but the existence of all partial derivatives at a need not imply the
> diﬀerentiability of $f$ at $a$.

> And in fact, the previous proof shows that we need to check the scope and
continuity only of all but one of the partial derivatives. The proof used
the existence of D3f at a but not its existence near a or its continuity
at a, and a variant argument or a reindexing shows that nothing is special
about the last variable. This observation is a bit of a relief, telling us 
that
in the case of one input variable, our methods do not need to assume that
the derivative exists at and about a point and is continuous at the point
in order to confirm merely that it exists at the point. We codify this bullet
as a variant suﬃciency theorem:

---

### Theorem 4.5.4 (The derivative in coordinates: suﬃciency).

Let $f : A \longrightarrow \mathbb{R}^m$  (where $A ⊂ \mathbb{R}^n$) be a 
mapping, and let $a$ be an interior point of $A$.
Suppose that for each $i \in \{1,\cdots,m\}$,

* for each $j \in \{1,\cdots,n\}$, the partial derivative $D_{j}f_{i}(a)$  
  exists,
* and for each but at most one $j \in \{1,\cdots,n\}$,
  the partial derivative $D_{j}f_{i}$ exists in some $ε$-ball about $a$ and is continuous at $a$.

Then $f$ is diﬀerentiable at $a$.

> Note how all this compares to the discussion of the determinant in the
previous chapter. There we wanted the determinant to satisfy characterizing
properties. We found the only function that could possibly satisfy them, and
then we verified that it did. Here we wanted the derivative to satisfy a char-
acterizing property, and we found the only possibility for the derivative—the
linear mapping whose matrix consists of the partial derivatives, which must
exist if the derivative does.But analysis is more subtle than algebra: this 
linear mapping need not satisfy the characterizing property of the derivative 
unless we add further assumptions.

### Example

$$ 
f(x,y) =
\begin{cases}
    \frac{x^2y}{x^2+y^2} &\text{if } (x,y) \neq (0,0)\\
    0 &\text{if } (x,y) = (0,0)\\
\end{cases} 
$$

Note

$$ 
D_{1}f_{}(0,0) = \lim \limits_{t \to 0} \frac{f(t,0)-f(0,0)}{t}
= \lim \limits_{t \to 0} \frac{0-0}{t} = 0
$$

Similarly $D_{2}f_{}(0,0) = 0$. So the only possibly derivative for $f$
at $(0,0)$ is $0$.

$$ 
\begin{align*}
|f(h,k) - f(0,0)| &=
|f(h,k)| \\
&= \frac{|h|^2|k|}{|(h,k)|^2}
\end{align*} 
$$

If we approach $(0,0)$ with $h = k$, then we have

$$ 
\frac{|h|^2|k|}{|(h,k)|^2} = \frac{|(h,h)|}{2 \sqrt[]{2}}
$$

### Theorem 4.5.5 (Chain rule in coordinates).

Let $f : A \longrightarrow \mathbb{R}^m$ (where
$A ⊂ R^n$) be diﬀerentiable at the point $a$ of $A$,
and let $g : f(A) \longrightarrow \mathbb{R}^l$ be
diﬀerentiable at the point $b= f(a)$. Then the composition
$g ◦f : A \longrightarrow R^ℓ$ is
diﬀerentiable at $a$, and its partial derivatives are

$$ 
D_{j}(g \circ f)_{i}(a) =
\sum_{k = 1}^{n}
D_{k}g_{i}(b) D_{j}f_{k}(a)
\quad \text{for } i = 1,...,ℓ, j = 1,...,n.
$$

$\square$

### example

$z = f(x,t,u), x = g(t,u)$ compute $\frac{\partial z}{\partial t}$.

$$
\begin{align*}
\frac{\partial z}{\partial t} &=
D_{1}(f \circ g)_{1}(a) \\
&= \sum_{k = 1}^{3}
D_{k}f_{1}(b) D_{1}g_{k}(a) \\
&= D_{1}f_{1}(b) D_{1}g_{1}(a) +
D_{2}f_{1}(b) D_{1}g_{2}(a) +
D_{3}f_{1}(b) D_{1}g_{3}(a)
\\
&= D_{1}f_{1}(b) D_{1}g_{1}(a) +
D_{2}f_{1}(b) \cdot 1 +
D_{3}f_{1}(b) \cdot 0 \\
&= \frac{\partial z}{\partial x} \frac{\partial x}{\partial t} +
\frac{\partial z}{\partial t}
\end{align*} 
$$

$\square$
