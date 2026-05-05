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

### 4.3.4.

Let $f(x,y) = (x^2 −y^2, 2xy)$. 
Show that $Df_{(a,b)}(h,k) = (2ah−2bk, 2bh+2ak)$
for all $(a,b) ∈ R^2$.
(By the previous problem, you may work component-wise.)

**Proof**:

First component:

$$ 
\begin{align*}
&f(a+h, b+k) - f(a, b) - (2ah−2bk) \\
&=((a+h)^2-(b+k)^2) - (a^2 - b^2) - (2ah−2bk) \\
&= (2ah + h^2) - (2bk + k^2) - (2ah−2bk) \\
&= h^2 - k^2 \\
&= o(h)
\end{align*} 
$$

Second component:

$$ 
\begin{align*}
& f(a+h, b+k) - f(a, b) - (2ah+2bk) \\
&= 2(a+h)(b+k) - 2ab - (2ah+2bk) \\
&= hk \\
&= o(h)
\end{align*} 
$$

$\square$

### 4.3.5

Let $g(x,y) = xe^y$. Show that $Dg_{(a,b)}(h,k) = he^b +kae^b$
for all $(a,b) ∈ R^2$.
(Note that because $e^0 = 1$ and because the derivative of the exponential
function at 0 is 1, the one-variable characterizing property says that
$e^k −1 = k +o(k)$.)

**Proof**:

$$ 
\begin{align*}
&g(a+h,b+k) - g(a,b) - (he^b +kae^b) \\
&= (a+h)e^{b+k} - ae^b - (he^b + kae^b) \\
&= (a+h)(e^{b+k}-e^b) - kae^b \\
&= (a+h)e^b(k + o(k)) - kae^b \\
&= h e^b k + ae^b o(k) + h e^b o(k) \\
&= o(h) + o(k) + o(h) \\
&= o(h)
\end{align*} 
$$

$\square$

### 4.3.6.

Show that if $f : R^n → R^m$ satisfies $|f(x)| ≤ |x|^2$ for all $x ∈ R^n$ then
$f$ is diﬀerentiable at $0^n$.

**Proof**:

Note $|f(0)| \leq |0|^2 = 0$. We will show $Df_a(0) = 0$ 

$$
\begin{align*}
& |f(h) - f(0) - 0 \cdot h| \\
&= |f(h)| \\
& \leq |h|^2 \\
&= o(h)
\end{align*} 
$$

So $Df_a(0) = 0$.

$\square$

### 4.3.7

Show that the function $f(x,y) = |xy|$ for all $(x,y) ∈ R^2$ is not
diﬀerentiable at $(0,0)$.
(First see what $Df_{(0,0)}(h,0)$ and $Df_{(0,0)}(0,k)$ need to be.)

**Proof**:

First assume $Df_{(0,0)}$ exists and it's $(\alpha, \beta)$.

We first check $Df_{(0,0)}(h,0)$

$$
\begin{align*}
& f(h,0) - f(0,0) - (\alpha, \beta)(h,0)^T \\
&= 0 - 0 - \alpha h \\
&= -\alpha h
\end{align*}
$$

For $Df_{(0,0)}(h,0)h$ to be $o(h)$, we must have $\alpha = 0$.
Similarly, we must have $\beta = 0$.

So if $Df_{(0,0)}$ exists, it can only be $0$. 

Then we check

$$
\begin{align*}
& f(h,h) - f(0,0) - Df_{(0,0)} h \\
&= |h| - 0 - 0 \\
&= |h| \\
& = \mathcal{O}(h) \\
& \neq o(h)
\end{align*} 
$$

This shows $Df_{(0,0)}$ cannot be $0$, then we have a contradiction.

So $f$ is not diﬀerentiable at $(0,0)$

$\square$

## 4.4 Basic Results and the Chain Rule

### 4.4.3.

Prove part (2) of Lemma 4.4.4.

Define the reciprocal function

$$ 
r : \mathbb{R} - \{0\} \longrightarrow \mathbb{R}, \qquad
r(x) = 1/x
$$

Then the derivative of $r$ at every nonzero real number a exists and is

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

### 4.4.4

Prove the quotient rule.

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

