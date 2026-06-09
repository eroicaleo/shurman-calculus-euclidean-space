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

We would like to first prove: given a multilinear function
$f(h_1, h_2, a_3, \cdots, a_k)$ and any $c > 0$, for any $|a_i| \leq M$, we can 
find $h > 0$ such that if $|(h_1, h_2)| < h$,

$$ 
|f(h_1, h_2, a_3, \cdots, a_k)| < c|(h_1, h_2)|
$$

We use induction on $k$. When $k = 3$, assume

$$ 
a_3 = x_1 e_1 + \cdots + x_n e_n
$$

Then

$$
\begin{align*}
& |f(h_1, h_2, a_3)| \\
&=
\left| \sum_{i = 1}^{n} x_i f(h_1, h_2, e_i)  \right| \\
&\leq \sum_{i = 1}^{n} \left| x_i f(h_1, h_2, e_i) \right| \\
&= \sum_{i = 1}^{n} |x_i| |f(h_1, h_2, e_i)| \\
& \leq M \sum_{i = 1}^{n} |f(h_1, h_2, e_i)|
\end{align*} 
$$

For each $i$ we can find $k_i$ such that if $|(h_1, h_2)| < k_i$,
then $|f(h_1, h_2, e_i)| < c/(nM) \cdot |(h_1, h_2)|$. Let $h = \min k_i$, then
if $|(h_1, h_2)| < h$,

$$ 
M \sum_{i = 1}^{n} |f(h_1, h_2, e_i)| <
M \cdot n \cdot c/(nM) \cdot |(h_1, h_2)|
= c|(h_1, h_2)|
$$

Then assume the statement is true for $3 \leq k \leq m$.

We will prove when $k = m+1$, assume

$$ 
a_{m+1} = x_1 e_1 + \cdots + x_n e_n
$$

then

$$
\begin{align*}
&|f(h_1, h_2, a_3, \cdots, a_m, a_{m+1})| \\
& \leq \sum_{i = 1}^{n} \left| x_i f(h_1, h_2, a_3, \cdots, a_m, e_i) \right| \\
& = \sum_{i = 1}^{n} \left| x_i | | f(h_1, h_2, a_3, \cdots, a_m, e_i) \right| \\
& \leq M \sum_{i = 1}^{n} | f(h_1, h_2, a_3, \cdots, a_m, e_i) | \\
\end{align*} 
$$

Let $g_i(h_1, h_2, a_3, \cdots, a_m) = 
f(h_1, h_2, a_3, \cdots, a_m, e_i)$ and $g_i$ is a multilinear function with only $k = m$ parameters.

Now we can apply the induction, for each $g_i$, we can find $k_i$ such that
if $|(h_1, h_2)| < k_i$,
then $|g_i(h_1, h_2, a_3, \cdots, a_m)| < c/(nM) \cdot |(h_1, h_2)|$. Let $h = \min k_i$, then
if $|(h_1, h_2)| < h$,

$$ 
M \sum_{i = 1}^{n} |g_i(h_1, h_2, a_3, \cdots, a_m)| <
M \cdot n \cdot c/(nM) \cdot |(h_1, h_2)|
= c|(h_1, h_2)|
$$

So in summary, we proved given a multilinear function
$f(h_1, h_2, a_3, \cdots, a_k)$ and any $c > 0$, we can 
find $h > 0$, as long as $|a_i| \leq M$, and $|(h_1, h_2)| < h$,

$$ 
|f(h_1, h_2, a_3, \cdots, a_k)| < c|(h_1, h_2)|
$$

The above statement can be generalized to given a multilinear function
$f(a_1, a_2, a_3, \cdots, a_k)$ and any $c > 0$, we can 
find $h > 0$, as long as $|a_i| \leq M$, and $|(h_i, h_j)| < h$, we have

$$ 
|f(a_1,...,h_i,...,h_j,...,a_k)| < c |(h_i, h_j)|
\leq c |(h_1, \cdots, h_k)|
$$

Then note that

$$
\begin{align*}
& f(a_1+h_1, \cdots, a_k+h_k) \\
&= f(a_1, \cdots, a_k) \\
&+
\sum_{j = 1}^{k} f(a_1,...,a_{j−1},h_j,a_{j+1},...,a_k) \\
&+ \text{ items with at least 2 } h_i, h_j 
\end{align*} 
$$

From the previous induction and the generalization, as long as
$|h_i| \leq M, |a_j| \leq M$, then
items with at least 2 $h_i, h_j$ are
$o(h_1,...,h_k)$, so

$$
\begin{align*}
&f(a_1+h_1, \cdots, a_k+h_k) - f(a_1, \cdots, a_k) - Df_{(a_1 ,...,a_k)}(h_1,...,h_k) \\
&= \text{ items with at least 2 } h_i, h_j \\
&= o(h_1,...,h_k)
\end{align*} 
$$

$\square$

Another much cleaner approach suggested by Gemini is to prove this first

$$ 
|f(a_1, \cdots, a_k)| \leq C |a_1| \cdots| a_k|
$$

Assume 

$$ 
a_i = x_{i1} e_1 + \cdots + x_{in} e_n
$$

Then

$$ 
\begin{align*}
&|f(a_1, \cdots, a_k)| \\
& \leq
\sum \limits_{j_1 = 1}^{n} \cdots
\sum \limits_{j_k = 1}^{n} |x_{j_1,1}|\cdots|x_{j_k,k}||f(e_1, \cdots, e_k)| \\
& \leq |a_1| \cdots| a_k|
\sum \limits_{j_1 = 1}^{n} \cdots
\sum \limits_{j_k = 1}^{n} |f(e_1, \cdots, e_k)|
\end{align*} 
$$

$\square$

(c) When $k = n$, what does this exercise say about the determinant?

**Proof**:

It means the determinant is differentiable at any point
$(a_1, \cdots, a_n)$.

$\square$

## 4.5 Calculating the Derivative

### 4.5.1.

Explain why in the discussion beginning this section the tangent
plane $\mathcal{P}$ consists of all points $(a,b,f(a,b)) + (h,k,T(h,k))$
where $T(h,k) = ϕ'(a)h+ψ'(b)k$.

### 4.5.2

This exercise shows that all partial derivatives of a function can exist at
and about a point without being continuous at the point. Define
$f : \mathbb{R}^2 \longrightarrow \mathbb{R}$ by

$$ 
f(x,y) =
\begin{cases}
    \frac{2xy}{x^2+y^2} &\text{if } (x,y) \neq (0,0)\\
    0 &\text{if } (x,y) = (0,0)\\
\end{cases} 
$$

(a) Show that $D_1f(0,0) = D_2f(0,0) = 0$.

**Proof**:

$$ 
\begin{align*}
D_1f(0,0) &=
\lim \limits_{t \to 0} \frac{
f(t,0) - f(0,0)
}{t} \\
&= \lim \limits_{t \to 0}
\frac{\frac{2t \cdot 0}{t^2 + 0^2}-0}{t} \\
&= \lim \limits_{t \to 0}
\frac{0-0}{t} \\
&= 0
\end{align*} 
$$

Similarly $D_{2}f_{}(0,0) = 0$.

$\square$

(b) Show that $D_1f(a,b)$ and $D_2f(a,b)$ exist and are continuous at all other $(a,b) ∈ \mathbb{R}^2$.

**Proof**:

$$ 
\begin{align*}
D_1f(a,b)
&= \frac{2b}{a^2+b^2} -\frac{(2ab)(2a)}{(a^2+b^2)^2} \\
&=
\frac{2a^2b + 2b^3 - 4a^2b}{(a^2+b^2)^2} \\
&=
\frac{2b^3 - 2a^2b}{(a^2+b^2)^2}
\end{align*} 
$$

Similarly,

$$ 
\begin{align*}
D_2f(a,b)
&=
\frac{2a^3 - 2b^2a}{(b^2+a^2)^2}
\end{align*} 
$$

It is a continuous function.

$\square$

(c) Show that $D_1f$ and $D_2f$ are discontinuous at $(0,0)$.

**Proof**:

If we approach $(0,0)$ with $a=b$, then

$$ 
\begin{align*}
D_1f(a,b)
&=
\frac{2b^3 - 2a^2b}{(a^2+b^2)^2} \\
&=
\frac{2a^3 - 2a^3}{(a^2+a^2)^2} \\
&= 0
\end{align*} 
$$

If we approach $(0,0)$ with $b=2a$, then

$$ 
\begin{align*}
D_1f(a,b)
&=
\frac{2b^3 - 2a^2b}{(a^2+b^2)^2} \\
&=
\frac{16a^3 - 4a^3}{(a^2+4a^2)^2} \\
&=
\frac{12}{25a} \\
& \rightarrow \infty 
\end{align*} 
$$

So $D_1f$ is not continuous at $(0,0)$.
Similarly, $D_2f$ is not continuous at $(0,0)$.

$\square$

### 4.5.3

Define $f : \mathbb{R} \longrightarrow \mathbb{R}$ by

$$ 
f(x) =
\begin{cases}
    x^2 \sin \frac{1}{x} &\text{if } x \neq 0\\
    0 &\text{if } x = 0\\
\end{cases} 
$$

Show that $f'(x)$ exists for all $x$ but that
$f'$ 
is discontinuous at $0$. Explain how
this disproves the converse of Theorem 4.5.3.

**Proof**:

When $x \neq 0$,

$$ 
\begin{align*}
f'(x) &= 2x \sin \frac{1}{x} - x^2 \cos \frac{1}{x} (\frac{1}{x^2}) \\
&= 2x \sin \frac{1}{x} - \cos \frac{1}{x}
\end{align*} 
$$

When $x = 0$,

$$
\begin{align*}
f'(0) &= \lim \limits_{x \to 0}
\frac{x^2 \sin \frac{1}{x} - 0}{x} \\
&= \lim \limits_{x \to 0}
x \sin \frac{1}{x} \\
&= 0
\end{align*} 
$$

Consider $a_n = \frac{1}{2 \pi n}, b_n = \frac{1}{(2n+1) \pi }$,
then $f'(a_n) = -1, f'(b_n) = 1$.

So $f'(x)$ is not continuous at $0$.

$\square$

### 4.5.4.

Discuss the derivatives of the following mappings at the following
points.

(a)
$f(x,y) = \frac{x^2 - y}{y+1}$ 
on
$\{(x,y) \in R^2 : y  \neq −1\}$ at generic $(a,b)$ with $b \neq −1$.

**Proof**:

$$
\begin{align*}
D_{1}f_{}(a,b)
&= \frac{2a}{b+1}
\end{align*}
$$

$$ 
\begin{align*}
D_{2}f_{}(a, b)
&= \frac{-1}{b+1} - \frac{a^2-b}{(b+1)^2} \\
&= -\frac{a^2+1}{(b+1)^2}
\end{align*} 
$$

So

$$ 
Df(a,b) =
\left[ \frac{2a}{b+1}, -\frac{1+a^2}{(b+1)^2} \right] 
$$

$\square$

(b) $f(x,y) = \frac{xy^2}{y-1}$
on $\{(x,y) ∈ \mathbb{R}^2 : y \neq 1\}$ at generic $(a,b)$ with $b \neq 1$.

**Proof**:

$$
\begin{align*}
D_{1}f_{}(a,b)
&= \frac{b^2}{b-1}
\end{align*} 
$$

$$ 
\begin{align*}
D_{2}f_{}(a,b)
&= \frac{2ab}{b-1} - \frac{ab^2}{(b-1)^2} \\
&= \frac{ab^2-2ab}{(b-1)^2}
\end{align*}
$$

So

$$ 
Df(a,b) =
\left[
\frac{b^2}{b-1}, \frac{ab^2-2ab}{(b-1)^2}
\right]
$$

$\square$

(c)

$$ 
f(x,y)=
\begin{cases}
    \frac{xy}{\sqrt[]{x^2+y^2}} &\text{if } (x,y) \neq (0,0)\\
    0 &\text{if } (x,y) = (0,0)\\
\end{cases} 
$$

at generic $(a,b) \neq (0,0)$ and at $(0,0)$.

**Proof**:

First consider $(a,b) \neq (0,0)$.

$$
\begin{align*}
D_{1}f_{}(a,b)
&= \frac{b}{\sqrt[]{a^2+b^2}} -
\frac{2a^2b}{2(a^2+b^2)^{3/2}} \\
&=
\frac{2b(a^2+b^2)-2a^2b}{2(a^2+b^2)^{3/2}} \\
&=
\frac{b^3}{(a^2+b^2)^{3/2}}
\end{align*}
$$

Similarly,

$$ 
\begin{align*}
D_{2}f_{}(a,b)
&= \frac{a^3}{(a^2+b^2)^{3/2}}
\end{align*} 
$$

So

$$ 
Df(a,b)=
\left[ 
\frac{b^3}{(a^2+b^2)^{3/2}},
\frac{a^3}{(a^2+b^2)^{3/2}}
\right] 
$$

Then note $D_1f(a,b)$ is not continuous at $(0,0)$.
If we approach $(0,0)$ with $a = b$, then we get

$$ 
\lim \limits_{(a,b) \to (0,0)} D_1f(a,b)
= \frac{1}{2\sqrt[]{2}}
$$

But if we approach $(0,0)$ with $a = 2b$, then we get

$$ 
\lim \limits_{(a,b) \to (0,0)} D_1f(a,b)
= \frac{1}{5\sqrt[]{5}}
$$

Similarly, $D_2f(a,b)$ is not continuous at $(0,0)$.

Now, assume $f$ is differentiable at $(0,0)$ and $Df(0,0) = [c,d]$, and we approach approach $(0,0)$ with $a = b = h$

$$ 
\begin{align*}
f(h,h) - f(0,0) - Df(0,0)(h,h) = \frac{1}{\sqrt[]{2}}|h| - (c+d)h = o(|h|)
\end{align*} 
$$

So if $h > 0$, then $c+d = \frac{1}{\sqrt[]{2}}$ and if $h < 0$, then $c+d = -\frac{1}{\sqrt[]{2}}$.
This is not possible.

So $f$ does not have derivative at $(0,0)$.

$\square$

### 4.5.5.

For what diﬀerentiable mappings $f : A \longrightarrow \mathbb{R}^m$ is
$f'(a)$ a diagonal
matrix for all $a ∈ A$?
(A diagonal matrix is a matrix whose $(i,j)$th entries for
all $i \neq j$ are $0$.)

**Solution**:

It means

$$ 
D_{j}f_{i}(a) =
\begin{cases}
    0 &\text{if } i \neq j \\
    f_i'(a_i) &\text{if } i = j \\
\end{cases} 
$$

So the format is like

$$ 
f(a) = (f_1(a_1), \cdots, f_n(a_n))
$$

Basically, $f_i$ is only one-variable function and is only determined
by $a_i$.

$\square$

### 4.5.6.

Show that if $z = f(xy)$ then $x$, $y$, and z satisfy the diﬀerential equation
$x \cdot z_x−y \cdot z_y = 0$.

**Solution**:

Let

$$ 
g : \mathbb{R}^2 \longrightarrow \mathbb{R},
\qquad
(x,y) \longrightarrow xy
$$

So $z = f (g(x,y)) = (f \circ g)(x,y)$

$$
\begin{align*}
z_x(a,b)
&=
D_1(f \circ g)(a,b) \\
&= D_1 f(g(a,b)) \cdot D_1g(a,b) \\
&= D_1 f(g(a,b)) \cdot b
\end{align*} 
$$

Similarly

$$
\begin{align*}
z_y(a,b)
&=
D_2(f \circ g)(a,b) \\
&= D_1 f(g(a,b)) \cdot D_2g(a,b) \\
&= D_1 f(g(a,b)) \cdot a
\end{align*} 
$$

So we have

$$ 
a \cdot z_x(a,b) = ab D_1 f(g(a,b)) = b \cdot z_y(a,b)
$$

i.e.

$$ 
x \cdot z_x−y \cdot z_y = 0
$$

$\square$

### 4.5.7.

Let $w = F(xz,yz)$. Show that $x \cdot w_x +y \cdot w_y = z \cdot w_z$.

**Proof**:

Let

$$ 
g : \mathbb{R}^3 \longrightarrow \mathbb{R}^2,
\qquad
(x,y,z) \longrightarrow (xz, yz)
$$

Then $w = F(g(x,y,z)) = (F \circ g)(x,y,z)$

$$
\begin{align*}
w_x(a,b,c) &= D_{1}(F \circ g)_{1}(a,b,c) \\
&= D_{1}F_{1}(g(a,b,c))D_{1}g_{1}(a,b,c)+
D_{2}F_{1}(g(a,b,c))D_{1}g_{2}(a,b,c) \\
&= D_{1}F_{1}(g(a,b,c)) \cdot c + D_{2}F_{1}(g(a,b,c)) \cdot 0 \\
&= D_{1}F_{1}(g(a,b,c)) \cdot c
\end{align*}
$$

$$ 
\begin{align*}
w_y(a,b,c) &= D_{2}(F \circ g)_{1}(a,b,c) \\
&= D_{1}F_{1}(g(a,b,c))D_{2}g_{1}(a,b,c)+
D_{2}F_{1}(g(a,b,c))D_{2}g_{2}(a,b,c) \\
&= D_{1}F_{1}(g(a,b,c)) \cdot 0 + D_{2}F_{1}(g(a,b,c)) \cdot c \\
&= D_{2}F_{1}(g(a,b,c)) \cdot c
\end{align*} 
$$

$$ 
\begin{align*}
w_z(a,b,c) &= D_{3}(F \circ g)_{1}(a,b,c) \\
&= D_{1}F_{1}(g(a,b,c))D_{3}g_{1}(a,b,c)+
D_{2}F_{1}(g(a,b,c))D_{3}g_{2}(a,b,c) \\
&= D_{1}F_{1}(g(a,b,c)) \cdot a + D_{2}F_{1}(g(a,b,c)) \cdot b \\
\end{align*}
$$

So

$$ 
(x \cdot w_x)(a,b,c) = ac D_{1}F_{1}(g(a,b,c)) \\
(y \cdot w_y)(a,b,c) = bc D_{2}F_{1}(g(a,b,c)) \\
(z \cdot w_z)(a,b,c) = ac D_{1}F_{1}(g(a,b,c)) + bc D_{2}F_{1}(g(a,b,c))
$$

Therefore

$$ 
x \cdot w_x +y \cdot w_y = z \cdot w_z
$$

$\square$

### 4.5.8.

If $z = f(ax+by)$, show that $bz_x = az_y$.

**Proof**:

Let

$$ 
g : \mathbb{R}^2 \longrightarrow \mathbb{R}^1,
\qquad
(x,y) \longrightarrow ax+by
$$

So $z = f(g(x,y)) = (f \circ g)(x,y)$.

$$
\begin{align*}
z_x(c,d)
&= D_{1}(f \circ g)_{1}(c,d) \\
&= D_{1}f_{1}(g(c,d))D_{1}g_{1}(c,d) \\
&= D_{1}f_{1}(g(c,d)) \cdot a
\end{align*} 
$$

$$
\begin{align*}
z_y(c,d)
&= D_{2}(f \circ g)_{1}(c,d) \\
&= D_{1}f_{1}(g(c,d))D_{2}g_{1}(c,d) \\
&= D_{1}f_{1}(g(c,d)) \cdot b
\end{align*} 
$$

So we have

$$ 
b z_x(c,d) = abD_{1}f_{1}(g(c,d)) = a z_y(c,d)
$$

So we have $bz_x = az_y$.

$\square$

### 4.5.9.

The function $f : \mathbb{R}^2 \longrightarrow \mathbb{R}$ is called 
homogeneous of degree $k$ if
$f(tx,ty) = t^kf(x,y)$ for all scalars $t$ and vectors $(x,y)$.
Letting $f_1$ and $f_2$
denote the first and second partial derivatives of $f$, show that such $f$ 
satisfies the diﬀerential equation

$$ 
xf_1(x,y)+yf_2(x,y) = kf(x,y).
$$

(Hint: First diﬀerentiate the homogeneity condition with respect to $t$, 
viewing $x$ and $y$ as fixed but generic; the derivative of one side will 
require the chain rule. Second, since the resulting condition holds for all 
scalars $t$, it holds for any particular $t$ of your choosing.)

**Proof**:

Let

$$ 
g : \mathbb{R}^3 \longrightarrow \mathbb{R}^2,
\qquad
g(x,y,t) \longrightarrow (tx, ty)
$$

Then $f(tx,ty) = f(g(x,y,t)) = (f \circ g)(x,y,t)$,

$$
\begin{align*}
D_{3}(f \circ g)(a,b,c)
&= D_{1}f(g(a,b,c)) D_{3}g_{1}(a,b,c) +
D_{2}f(g(a,b,c)) D_{3}g_{2}(a,b,c) \\
&= D_{1}f(g(a,b,c)) \cdot a +
D_{2}f(g(a,b,c)) \cdot b
\end{align*} 
$$

On the other hand since $f(tx,ty) = t^kf(x,y)$, then

$$ 
D_{3}(f \circ g)(a,b,c) = kc^{k-1}f(a,b)
$$

If we plug $c = 1$ in both equation, then for any $a,b$ we get

$$
a D_{1}f(a, b) + b D_{2}f(a,b) = k f(a,b)
$$

Then that's exactly

$$ 
xf_1(x,y)+yf_2(x,y) = kf(x,y)
$$

$\square$

### 4.5.10

Let

$$ 
f : \mathbb{R}^2 \longrightarrow \mathbb{R}
$$

be a function such that for all $(x,y) ∈ \mathbb{R}^2$, the integral

$$ 
F : \mathbb{R}^2 \longrightarrow \mathbb{R},
\qquad
F(x,y) = \int_{v=0}^{y} f(x,v) dv
$$

exists and is diﬀerentiable with respect to $x$,
its partial derivative with respect
to $x$ being obtained by passing the $x$-derivative through the $v$-integral,

$$ 
\begin{align*}
\frac{\partial F(x,y)}{\partial x}
&= \frac{\partial }{\partial x}
\int_{v=0}^{y} f(x,v) dv \\
&= \lim \limits_{h \to 0}
\frac{
\int_{v=0}^{y}f(x+h,v)dv - \int_{v=0}^{y}f(x,v)dv
}{h} \\
&= \lim \limits_{h \to 0}
\int_{v=0}^{y}
\frac{
f(x+h,v) - f(x,v)
}{h} dv \\
& \overset{!}{=}
\int_{v=0}^{y}
\lim \limits_{h \to 0}
\frac{
f(x+h,v) - f(x,v)
}{h} dv \\
&=
\int_{v=0}^{y}
\frac{ \partial f
}{\partial x} (x,v) dv
\end{align*} 
$$

(The "!" step requires justification, but under reasonable circumstances it can
be carried out.)
Define a function

$$ 
G : \mathbb{R} \longrightarrow \mathbb{R},
\qquad
G(x) = \int_{v=0}^{x}f(x,v)dv
$$

Thus $x$ aﬀects $G$ in two ways: as a parameter for the integrand,
and as the
upper limit of integration. What is $dG(x)/dx$?

**Solution**:

Note $G(x) = F(x, x)$, now we can consider

$$ 
g : \mathbb{R} \longrightarrow \mathbb{R}^2,
\qquad
g(x) = (x, x)
$$

Now we have $G(x) = (F \circ g)(x)$, so

$$
\begin{align*}
\frac{dG}{dx}(a)
&= D_{1}(F \circ g)_{1}(a) \\
&= D_{1}F_{1}(g(a)) D_{1}g_{1}(a) +
D_{2}F_{1}(g(a)) D_{1}g_{2}(a) \\
&= D_{1}F_{1}(a, a) \cdot 1 + D_{2}F_{1}(a, a) \cdot 1 \\
&=
\left( \int_{v=0}^{a}
\frac{ \partial f
}{\partial x} (a,v) dv \right)  + f(a,a)
\end{align*} 
$$

$\square$

## 4.6 Higher-Order Derivatives

### 4.6.2

Suppose $u$, as a function of $x$ and $y$, satisfies
the diﬀerential equation
$u_{xx} − u_{yy} = 0$.
Make the change of variables $x = s + t, y= s− t$. What
corresponding diﬀerential equation does $u$ satisfy when viewed as a function
of $s$ and $t$? (That is, find a nontrivial relation involving
at least one of $u, u_s, u_t, u_{ss}, u_{tt},$ and $u_{st}$.)

**Solution**:

$$ 
\begin{align*}
u_s &= u_x x_s + u_y y_s \\
&=u_x + u_y \\
u_t &= u_x x_t + u_y y_t \\
&= u_x - u_y
\end{align*} 
$$

$$
\begin{align*}
u_{ss} &= u_{xx}x_s + u_{xy} y_s + u_{yx} x_s + u_{yy} y_s \\
&= u_{xx} + u_{xy} + u_{yx} + u_{yy} \\
&= u_{xx} + 2 u_{xy} + u_{yy}
\end{align*} 
$$ 

$$
\begin{align*}
u_{st} &= u_{xx}x_t + u_{xy} y_t + u_{yx} x_t + u_{yy} y_t \\
&= u_{xx} - u_{xy} + u_{yx} - u_{yy} \\
&= u_{xx} - u_{yy} \\
&= 0
\end{align*} 
$$ 

$$ 
\begin{align*}
u_{tt} &= u_{xx}x_t + u_{xy} y_t - u_{yx} x_t - u_{yy} y_t \\
&= u_{xx} - u_{xy} - u_{yx} + u_{yy} \\
&= u_{xx} - 2 u_{xy} + u_{yy}
\end{align*} 
$$

So the function is $u_{st}$

$\square$

### 4.6.3. (The wave equation)

(a) Let $c$ be a constant, tacitly understood to
denote the speed of light. Let $x$ and $t$ denote a space variable and a time
variable, and introduce variables

$$ 
p =x+ct, \qquad q = x-ct.
$$

Show that a quantity $w$, viewed as a function of $x$ and $t$,
satisfies the wave equation,

$$ 
c^2 w_{xx} = w_{tt}
$$

if and only if it satisfies the equation

$$ 
w_{pq} = 0
$$

**Proof**:

$\Rightarrow$

$$
\begin{align*}
x &= \frac{p+q}{2} \\
t &= \frac{p-q}{2c} \\
x_p = 1/2 &, x_q = 1/2 \\
t_p = 1/(2c) &, t_q = -1/(2c) 
\end{align*} 
$$

$$
\begin{align*}
w_p &= w_x x_p + w_t t_p \\
&= \frac{1}{2} w_x + \frac{1}{2c} w_t \\
\end{align*} 
$$

$$
\begin{align*}
w_{pq} &=
\frac{1}{2} w_{xx}x_q + \frac{1}{2} w_{xt} t_q +
\frac{1}{2c} w_{tx}x_q + \frac{1}{2c} w_{tt}t_q \\
&= \frac{1}{4} w_{xx} - \frac{1}{4c} w_{xt}
+ \frac{1}{4c} w_{tx} - \frac{1}{4c^2} w_{tt} \\
&= 0
\end{align*} 
$$

$\Leftarrow$

$$
\begin{align*}
p_x = 1, &\qquad p_t = c \\
q_x = 1, &\qquad q_t = -c \\
\end{align*} 
$$

$$
\begin{align*}
w_x &= w_p p_x + w_q q_x \\
&= w_p + w_q \\
w_t &= w_p p_t + w_q q_t \\
&= w_p c - w_q c \\
w_{xx} &= w_{pp} p_x + w_{pq} q_x + w_{qp} p_x + w_{qq} q_x \\
&= w_{pp} + w_{pq} + w_{qp} + w_{qq} \\
&= w_{pp} + w_{qq} \\
w_{tt} &= c (w_{pp} p_t + w_{pq} q_t - w_{qp} p_t - w_{qq} q_t) \\
&= c (w_{pp} c - w_{pq} c - w_{qp} c + w_{qq} c) \\
&= c^2 (w_{pp} - w_{pq} - w_{qp} + w_{qq}) \\
&= c^2 (w_{pp} + w_{qq}) \\
\end{align*} 
$$

So $w_{tt} = c^2 w_{xx}$ as required.

$\square$
