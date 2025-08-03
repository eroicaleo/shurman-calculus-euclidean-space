# Chapter 1 Results from One-Variable Calculus

## 1.1 The Real Number System

### Theorem 1.1.1 (Field axioms for ($R,+,·$)).

(a1) Addition is associative

(a2) $0$ is an additive identity

(a3) Existence of additive inverses

(a4) Addition is commutative

(m1) Multiplication is associative

(m2) $1$ is a multiplicative identity

(m3) Existence of multiplicative inverses

(m4) Multiplication is commutative

(d1) Multiplication distributes over addition

### Theorem 1.1.2 (Order axioms).

(o1) Trichotomy axiom: for every real number $x$, exactly one of 
the following conditions holds:

$$ 
x \in \mathbb{R}^+, x \in \mathbb{R}^-, x = 0.
$$

$\square$

(o2) Closure of positive numbers under addition: for all real 
numbers $x$ and $y$, if $x \in \mathbb{R}^+$,
and $y \in \mathbb{R}^+$, then also $x+y \in \mathbb{R}^+$.

$\square$

(o3) Closure of positive numbers under multiplication: for all 
real numbers $x$ and $y$, if $x \in \mathbb{R}^+$,
and $y \in \mathbb{R}^+$, then also $xy \in \mathbb{R}^+$.

$\square$

For all real numbers $x$ and $y$, define

$$ 
x < y
$$

to mean

$$ 
y - x \in \mathbb{R}^+
$$

We want to show this definition is the same as what we learned in
"Understanding Analysis".

$\Rightarrow$ We define this relation, if $x < y$ of $x = y$ then
we say $x \leq y$.

(o1ua) Given any $x, y$, since either

$$ 
x - y \in \mathbb{R}^+, x - y \in \mathbb{R}^-, x - y = 0.
$$

Then either $x \leq y$ or $y \leq x$.

(o2ua) If $x \leq y$, then $x - y \leq 0$. $y \leq x$, then
$y - x \leq 0$. So $x = y$.

(o3ua) If $x \leq y$, then $x - y \leq 0$. $y - z \leq 0$, then
$(x-y) + (y-z) = x - z \leq 0$, i.e. $x \leq z$.

(o4ua) If $y \leq z$, $y - z \leq 0$, then $x + (y-z) \leq x$.
so $x + y \leq x + z$.

(o5ua) It's automatic.

$\Leftarrow$

We define the set to be

$$ 
\mathbb{F}^+ = \{
x : 0 \leq x \text{ and } x \neq 0
\}
$$

We want to showthe following:

(o1) We want to show if $x \not\in \mathbb{F}^+$ and
$x \neq 0$, then $-x \in \mathbb{F}^+$.

Assume $-x \leq 0$, then $-x + x \leq 0 + x$, so $0 \leq x$,
we have a contradiction. So $0 \leq -x$.

Since $x \neq 0$, then if $-x = 0$, we have $0 = x + (-x) = x$,
we have a contradiction again, so $-x \neq 0$.

Then $x \in \mathbb{F}^+$.

(o2) We want to show if $x \in \mathbb{F}^+$,
and $y \in \mathbb{F}^+$, then also $x+y \in \mathbb{F}^+$.

$0 \leq x, 0 \leq y$, then $0 + 0 \leq x + 0 \leq x + y$.

In addition, if $x + y = 0$, then $x = -y$, since
$y \in \mathbb{F}^+$, then $-y \not\in \mathbb{F}^+$, i.e.
$x \not\in \mathbb{F}^+$, we have a contradiction.

(o3) We want to show $x \in \mathbb{F}^+$,
and $y \in \mathbb{F}^+$, then also $xy \in \mathbb{F}^+$.

(o5ua) guarantees $0 \leq x, 0 \leq y$ then $0 \leq xy$.
If $xy = 0$, since $y \neq 0$, we can find $y^{-1}$ such that
$x = xyy^{-1} = 0y^{-1} = 0$, we have a contradiction.

$\square$

Another thing we can show is that no order can be made to a finite
field.

**Proof**: Assume we $\mathbb{F}$ is a finite field. We proved
$1 \in \mathbb{F}^+$. Then consider the sequence

$$ 
1,2,3,\cdots 
$$

Since $\mathbb{F}$ is finite, we must have for some $k,n$
$k = k+n$, then we have $n = 0$. On the other hand,
$n$ is the sum of $n$ $1$s, so $n \in \mathbb{F}^+$.
We have a contradiction.

$\square$

## 1.3 Taylor’s Theorem

Let $I ⊂ \mathbb{R}$ be a nonempty open interval, and let $a ∈ I$ 
be any point. Let $n$ be a nonnegative integer. Suppose that the 
function $f : I \to \mathbb{R}$ has $n$ continuous derivatives

$$ 
f, f', f'', \cdots, f^{(n)} : I \to \mathbb{R}
$$

For every positive integer $k$ and every $x ∈ \mathbb{R}$ define a k-fold nested integral,

$$ 
I_k(x) =
\int_{x_1 = a}^{x}
\int_{x_2 = a}^{x_1}
\cdots
\int_{x_k = a}^{x_{k-1}}
d x_k \cdots d x_2 d x_1
$$

Then we have

$$ 
I_1(x) =
\int_{x_1 = a}^{x} d x_1 = x_1 \Big|_{x_1 = a}^x = x - a
$$

$$ 
I_2(x) =
\int_{x_1 = a}^{x}
\int_{x_2 = a}^{x_1}
d x_2 d x_1 =
\int_{x_1 = a}^{x}
I_1(x_1) d x_1
=
\frac{1}{2} (x_1 - a)^2 \Big|_{x_1 = a}^x
=
\frac{1}{2} (x - a)^2
$$

So in general

$$ 
I_k(x) = \frac{1}{k!} (x - a)^k, k \in \mathbb{Z}^+.
$$

According to the fundamental theorem,

$$ 
f(x) = f(a) + \int_{a}^{x} f'(x_1) d x_1 \\
f'(x_1) = f'(a) + \int_{a}^{x_1} f''(x_2) d x_2 \\
$$

So we have

$$
\begin{split}
f(x)
&= T_0(x) + \int_{a}^{x} f'(x_1) d x_1 \\
&= T_0(x) + f'(a) I_1(x) +
\int_{a}^{x} 
\int_{a}^{x_1}
f''(x_2) d x_2 d x_1 
 \\
&= T_1(x) +
\int_{a}^{x} 
\int_{a}^{x_1}
f''(x_2) d x_2 d x_1 \\
&\cdots \\
&= T_n(x) +
\int_{x_1 = a}^{x}
\int_{x_2 = a}^{x_1}
\cdots
\int_{x_{n+1} = a}^{x_{n}}
f^{(n+1)}(x_{n+1}) d x_{n+1} \cdots d x_2 d x_1 \\
&= T_n(x) + R_n(x)
\end{split}
$$

Assume $m \leq f^{(n+1)}(x_{n+1}) \leq M$, then

$$ 
m I_1(x_n) \leq 
\int_{x_{n+1} = a}^{x_{n}}
f^{(n+1)}(x_{n+1}) d x_{n+1}
\leq
M I_1(x_n)
$$

and

$$ 
m I_2(x_{n-1}) \leq 
\int_{x_{n} = a}^{x_{n-1}}
\int_{x_{n+1} = a}^{x_{n}}
f^{(n+1)}(x_{n+1}) d x_{n+1} d x_n
\leq
M I_2(x_{n-1})
$$

and so on. Eventually, we have

$$ 
m I_{n+1}(x)
\leq
R_n(x)
\leq
M I_{n+1}(x)
$$

i.e.

$$ 
m \frac{(x-a)^{n+1}}{(n+1)!}
\leq
R_n(x)
\leq
M \frac{(x-a)^{n+1}}{(n+1)!}
$$

If we let

$$ 
g(t) = f^{(n+1)}(t) \frac{(x-a)^{n+1}}{(n+1)!},
t \in [a, x]
$$

Then we have
$$
g(t_m) = m \frac{(x-a)^{n+1}}{(n+1)!},
g(t_M) = M \frac{(x-a)^{n+1}}{(n+1)!}
$$ and since $g(t)$ is
continuous, we can find $c \in [a, x]$, such that $g(c) = R_n(x)$.

$\square$

Next, we discuss the case for $x < a$.

Consider $\tilde{f} : -I \to \mathbb{R}$, $\tilde{f}(-x) = f(x)$

With chain rule, we can see

$$ 
\tilde{f}^{(n)}(-x) = (-1)^n f^{(n)}(x)
$$

If $x < a$ in $I$ then $−x >−a$ in $−I$, and so we know by the 
version of Taylor’s theorem that we have already proved that

$$ 
\tilde{f}(-x) = \tilde{T}_n(-x) + \tilde{R}_n(-x)
$$

To get the $\tilde{T}_n(-x)$,

$$ 
\tilde{T}_n(-x) =
\sum_{k = 0}^{n}
\frac{\tilde{f}^{(k)}(-a)}{k!} (-x - (-a))^k \\
= \sum_{k = 0}^{n}
(-1)^k \frac{f^{(k)}(a)}{k!} (a-x)^k \\
= \sum_{k = 0}^{n}
\frac{f^{(k)}(a)}{k!} (x-a)^k \\
$$

and also

$$ 
\tilde{R}_n(-x) =
\frac{\tilde{f}^{(n+1)}(-c)}{(n+1)!} (-x - (-a))^{n+1}
=
(-1)^{n+1}
\frac{f^{(n+1)}(c)}{(n+1)!} (a-x)^{n+1}
\\
= \frac{f^{(n+1)}(c)}{(n+1)!} (x-a)^{n+1}
$$

So we proved when $x < a$.

$\square$

* Whereas our proof of Taylor’s theorem relies primarily on the fundamental theorem of integral calculus
    * a similar proof relies on repeated integration byparts(Exercise1.3.6) (Also see Jay Cumming's Real Analysis)
    * many proofs rely instead on the mean value theorem.
      Also see Understanding Analysis.

* Our proof neatly uses three diﬀerent mathematical techniques for 
  the three diﬀerent parts of the argument:
    * To find the Taylor polynomial $T_n(x)$, we diﬀerentiated 
      repeatedly, using a substitution at each step to determine a 
      coeﬃcient.
    * To get a precise (if unwieldy) expression for the remainder 
      $R_n(x) = f(x)− T_n(x)$, we integrated repeatedly, 
      usingthefundamental theorem of integral calculus at each 
      step to produce a term of the Taylor polynomial.
    * To express the remainder in a more convenient form, we used 
      the extreme value theorem and then the intermediate value 
      theorem once each. These foundational theorems are not 
      results from calculus but (as we will discuss in
      Section 2.4) from an area of mathematics called topology.

