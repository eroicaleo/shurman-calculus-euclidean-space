# Chapter 4 The Derivative

## 4.2 New Environment: The Bachmann–Landau Notation

## 4.3 One-Variable Revisionism: The Derivative Redefined

### 4.3.1.

Let $T : R^n → R^m$ be a linear mapping. Show that for every $ε$ > 0,
the behavior of $T$ on $B(0_n,ε)$ determines the behavior of $T$ everywhere.

**Proof**:

Given any $x$, let $\lambda = 2|x|/\epsilon$ and $x = \lambda x_0$.
Then $|x_0| = \epsilon / 2$, so $x_0 \in B(0_n,ε)$.

$$ 
T(x) = T( \lambda x_0) = \lambda T(x_0)
$$

So $x$ is determined by $x_0$.

$\square$

### 4.3.2.

Give a geometric interpretation of the derivative when $n = m = 2$.
Give a geometric interpretation of the derivative when $n = 1$ and $m = 2$.

**Solution**:

When $n = m = 2$, we can think that there are 2 graphs of Figure 4.4.
So the derivative is 2 planes.

When $n = 1$ and $m = 2$, the derivative is a line.

$\square$

### 4.3.3.

Let $f : A → R^m$ (where $A ⊂ R^n$) have component functions
$f_1,...,f_m$, and let a be an interior point of $A$.
Let $T : R^n → R^m$ be a linear
mapping with component functions $T_1,...,T_m$.
Using the componentwise nature of the $o(h)$ condition,
established in Section 4.2, prove the component-wise nature of 
diﬀerentiability: $f$ is diﬀerentiable at a with derivative $T$
if and only if each component $f_i$ is diﬀerentiable at a with
derivative $T_i$.

**Proof**:

$$
\begin{align*}
f(a+h) - f(a) - T(h) \text{ is } o(h) \\
& \Longleftrightarrow \\
(f_1(a+h) - f_1(a) - T_1(h), \cdots, f_n(a+h) - f_n(a) - T_n(h))
\text{ is } o(h) \\
& \Longleftrightarrow \\
f_i(a+h) - f_i(a) - T_i(h) \text{ is } o(h) \\
& \text{componentwise nature of the } o(h)
\end{align*}  
$$
