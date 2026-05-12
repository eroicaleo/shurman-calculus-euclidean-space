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

### 4.4.1.

Prove part (2) of Proposition 4.4.1.

**Proof**: See ch04 notes.

$\square$

### 4.4.2.

Prove part (2) of Proposition 4.4.2.

**Proof**: See ch04 notes.

$\square$

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

### 4.4.5.

Let $f(x,y,z) = xyz$. Find $Df_{(a,b,c)}$ for arbitrary $(a,b,c) ∈ R^3$.
(Hint: $f$ is the product $XYZ$,
where $X$ is the linear function $X(x,y,z) = x$ and
similarly for $Y$ and $Z$.)

**Solution**:

$$ 
\begin{align*}
f(x,y,z) &= XYZ \\
Df_{(a,b,c)} &=
D(XYZ)_{(a,b,c)} \\
&= X(a,b,c)D(YZ)_{(a,b,c)} + (YZ)(a,b,c) DX_{(a,b,c)} \\
&= a (Y(a,b,c) DZ_{(a,b,c)} + Z(a,b,c) DY_{(a,b,c)}) + bcX \\
&= abZ + acY + bcX \\
\end{align*} 
$$

$\square$

### 4.4.6.

Define $f(x,y) = xy^2/(y − 1)$ on $\{(x,y) \in R^2 : y \neq 1\}$.
Find $Df_{(a,b)}$ where $(a,b)$ is a point in the domain of $f$.

**Solution**:

Define $X(x, y) = x, Y(x,y) = y$, then we have:

$$ 
\begin{align*}
&Df_{a,b}(h,k) \\
&=
\frac{
(Y-1)(a,b) D(XY^2)_{(a,b)} - (XY^2)(a,b)D(Y-1)_{(a,b)}
}{
(Y-1)^2(a,b)
}(h,k) \\
&=
\frac{
(b-1)(X(a,b)D(Y^2)_{(a,b)}+Y^2(a,b)DX_{(a,b)}) - ab^2 Y
}{
(b-1)^2
}(h,k) \\
&=
\frac{
(b-1)(2abY + b^2X) - ab^2 Y
}{
(b-1)^2
}(h,k) \\ 
&=
\left( 
\frac{b^2}{b-1}X +
\frac{ab^2-2ab}{(b-1)^2}Y
\right) (h,k)
\end{align*} 
$$

$\square$

### 4.4.7

(A generalization of the product rule.) Recall that a function

$$ 
f : \mathbb{R}^n \times \mathbb{R}^n \longrightarrow \mathbb{R}
$$

is called bilinear if for all $x,x',y,y' ∈ \mathbb{R}^n$ and all
$\alpha \in \mathbb{R}$,

$$ 
\begin{align*}
f(x+x',y) &= f(x,y)+f(x',y), \\
f(x,y +y') &= f(x,y)+f(x,y'), \\
f(αx,y) &= αf(x,y) = f(x,αy). \\
\end{align*}
$$

(a) Show that if $f$ is bilinear then $f(h,k)$ is $o(h,k)$.

**Proof**:

Let

$$ 
\begin{align*}
h &= h_1 e_1 + \cdots + h_n e_n \\
k &= k_1 e_1 + \cdots + k_n e_n \\
\end{align*} 
$$

Then

$$ 
\begin{align*}
f(h,k) &= \sum_{i = 1}^{n} \sum_{j = 1}^{n} h_i k_j f(e_i, e_j)
\end{align*}
$$

We can find a $M$ such that $|f(e_i, e_j)| \leq M$ for all $i, j$.
We also know $|h_i| \leq |h| \leq |(h,k)|, |k_j| \leq |k| \leq |(h,k)|$ for all $i, j$.

So we have

$$
\begin{align*}
|f(h,k)| &= 
\left| 
\sum_{i = 1}^{n} \sum_{j = 1}^{n} h_i k_j f(e_i, e_j)
\right| \\
& \leq
\sum_{i = 1}^{n} \sum_{j = 1}^{n} |h_i k_j f(e_i, e_j)| \\
& \leq
|h||k| n^2 M \\
& \leq n^2 M |(h,k)|^2 \\
&= o(h, k)
\end{align*} 
$$

$\square$

(b) Show that if $f$ is bilinear then $f$ is diﬀerentiable with
$Df_{(a,b)}(h,k) = f(a,k)+f(h,b)$.

**Proof**:

First of all, we need to show $Df_{(a,b)}(h,k)$ is a linear function
of $(h,k)$.

Given $(h_1,k_1)$ and $(h_2,k_2)$

$$ 
\begin{align*}
& Df_{(a,b)}((h_1,k_1) + (h_2,k_2)) \\
&= Df_{(a,b)}(h_1+h_2,k_1+k_2) \\
&= f(a, k_1+k_2) + f(h_1+h_2, b) \\
&= (f(a,k_1)+f(h_1,b)) + (f(a,k_2)+f(h_2,b)) \\
&= Df_{(a,b)}(h_1,k_1) + Df_{(a,b)}(h_2,k_2) \\
\end{align*} 
$$

Similarly given $\alpha \in \mathbb{R}$,

$$ 
\begin{align*}
& Df_{(a,b)}(\alpha(h,k)) \\
&= Df_{(a,b)}(\alpha h, \alpha k) \\
&= f(a, \alpha k) + f(\alpha h, b) \\
&= \alpha (f(a,k)+f(h,b)) \\
&= \alpha Df_{(a,b)}(h,k)
\end{align*} 
$$

Then finally, we have

$$ 
\begin{align*}
&f(a+h, b+k) - f(a, b) - (f(a,k)+f(h,b)) \\
&=(f(a,b) + f(h, b) + f(a, k) + f(h, k)) - f(a, b) - (f(a,k)+f(h,b)) \\
&= f(h,k) \\
&= o(h, k)
\end{align*} 
$$

So $f$ is diﬀerentiable with $Df_{(a,b)}(h,k) = f(a,k)+f(h,b)$.

$\square$

(c) What does this exercise say about the inner product?

**Solution**:

Since inner product is a bilinear function, then it's diﬀerentiable
at any point of $(a,b)$.

$\square$

A little comments for part (a):

It took me a long way to reach to the solution above. Initially,
I was thinking to use the following way.

Assume $h = |h| r_0, k = |k| r_1$, where $r_0, r_1 \in \mathbb{R}^n$ and
$|r_0| = |r_1| = 1$. Then I want to show $f(h,k) = |h||k|f(r_0, r_1)$,
as long as I can bound $|f(r_0, r_1)|$, then it's done.

So my next thought is to prove $f$ is continuous. 

Given $(x_0, y_0)$ and $(x_1, y_1)$, I want to use triangle inequality.
Ideally, I would like to have the following, but it's not correct.

$$
\begin{align*}
\left| 
f(x_1, y_1) - f(x_0, y_0)
\right|
&=
\left| 
f(x_0, y_1 - y_0) +
f(x_1 - x_0, y_0)
\right| \\
\end{align*} 
$$

So I stuck here. I guess I was kinda inspired by how to prove a linear
map $T$ is continuous which I learned from Gemini.

$\square$

### 4.4.8. (A bigger generalization of the product rule.)

A function

$$ 
f : \mathbb{R}^n \times \cdots \times \mathbb{R}^n \longrightarrow \mathbb{R}
$$

(there are $k$ copies of $\mathbb{R}^n$) is called multilinear if for each
$j ∈ {1,...,k}$, for all $x_1,...,x_j,x_j',...,x_k ∈ \mathbb{R}^n$ and all
$\alpha ∈ \mathbb{R}$,

$$ 
\begin{align*}
f(x_1,...,x_j +x_j',...,x_k) &=
f(x_1,...,x_j,...,x_k)+f(x_1,...,x_j',...,x_k) \\
f(x_1,...,αx_j,...,x_k) &= αf(x_1,...,x_j,...,x_k)
\end{align*} 
$$

(a) Show that if $f$ is multilinear and
$a_1,...,a_k,h_1,...,h_k ∈ \mathbb{R}^n$ then
for $i,j ∈ \{1,...,k\}$ (distinct),
$f(a_1,...,h_i,...,h_j,...,a_k)$ is $o(h_1,...,h_k)$.
(Use the previous problem.)

**Proof**:

Let $g(h_i, h_j) = f(a_1,...,h_i,...,h_j,...,a_k)$ then
$g(h_i, h_j)$ is a bilinear function.

Since $g(h_i, h_j)$ is $o(h_i, h_j)$ from the exercise 4.4.7
and since $|(h_i, h_j)| \leq |(h_1,...,h_k)|$, then we can conclude
$g(h_i, h_j)$ is $o(h_1,...,h_k)$.

$\square$

(b) Show that if $f$ is multilinear then $f$ is diﬀerentiable with

$$ 
Df_{(a_1 ,...,a_k)}(h_1,...,h_k) =
\sum_{j = 1}^{k}
f(a_1,...,a_{j−1},h_j,a_{j+1},...,a_k).
$$

**Proof**:

The linearity of $Df_{(a_1 ,...,a_k)}$ is similarly to exercise 4.4.7 (b).
So we skip here.

Note that

$$
\begin{align*}
& f(a_1+h_1, \cdots, a_k+h_k) \\
&= f(a_1, \cdots, a_k) \\
&+
\sum_{j = 1}^{k} f(a_1,...,a_{j−1},h_j,a_{j+1},...,a_k) \\
&+ \text{ items with at least 2 } h_i, h_j 
\end{align*} 
$$

From part (a), items with at least 2 $h_i, h_j$ are
$o(h_1,...,h_k)$, so

$$
\begin{align*}
&f(a_1+h_1, \cdots, a_k+h_k) - f(a_1, \cdots, a_k) - Df_{(a_1 ,...,a_k)}(h_1,...,h_k) \\
&= \text{ items with at least 2 } h_i, h_j \\
&= o(h_1,...,h_k)
\end{align*} 
$$

$\square$
