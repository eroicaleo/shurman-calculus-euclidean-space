# Chapter 1 Results from One-Variable Calculus

## 1.1 The Real Number System

### 1.1.1.

Referring only to the field axioms, show that $0x = 0$ for all
$x ∈ R$.

**Proof**:

Use (m2), (d1), (a2), (m2), we have

$$ 
0x + x = 0x + 1x = (0 + 1)x = 1x = x
$$

Let $y$ be the additive inverse of $x$, then

$$ 
(0x + x) + y = 0x + (x + y) = 0x + 0 = 0x \\
x + y = 0
$$

So $0x = 0$

$\square$

### 1.1.2.

Prove that in every ordered field, $1$ is positive. Prove that the 
complex number field $\mathbb{C}$ cannot be made an ordered field.

**Proof**:

If $1 = 0$, then given $x \in \mathbb{F}$, $x = 1x = 0x = 0$.
Then $\mathbb{F} = \{0\}$.

Now we assume $1 \neq 0$. If $1 \not \in \mathbb{F}^+$,
then $-1 \in \mathbb{F}^+$. Then note

$$ 
(-1)(-1) + (-1)1 = (-1)((-1) + 1) = (-1)0 = 0 \\
\Rightarrow \\
(-1)(-1) + (-1) = 0 \\
\Rightarrow \\
(-1)(-1) = 1
$$

So from (o3), $1 \in \mathbb{F}^+$, we have a contradiction.
Then $1 \in \mathbb{F}^+$.

For the second part.

if $i \in \mathbb{C}^+$, then $i \cdot i = -1 \in \mathbb{C}^-$,
we have a contradiction.

if $i \in \mathbb{C}^-$, then $(-i) \cdot (-i) = i^2 = -1 \in \mathbb{C}^-$, we have a contradiction again.

$\square$

### 1.1.3

Use a completeness property of the real number system to show that 2 has a positive square root.

**Proof**:

Let $A = \{x : x \geq 0 \text{ and } x^2 < 2\}$

$A$ is not empty, e.g. $1 \in A$.
$A$ is upper bounded, e.g. $2$ is an upper bound.

Now assume $r$ is the least upper bound.

If $r^2 < 2$, then let $d = 2 - r^2$. We can find
$n$ such that $2r/n + 1/n^2 < d$, then

$$ 
(r + 1/n)^2 = r^2 + 2r/n + 1/n^2 < r^2 + d = 2
$$

That means $r < r+1/n \in A$, so $r$ is not an upper bound,
we have a contradiction.

If $r^2 > 2$, then let $d = r^2 - 2$.
We can find $n$ such that $2r/n - 1/n^2 < d$, then

$$ 
(r - 1/n)^2 = r^2 - 2r/n + 1/n^2 > r^2 - d = 2
$$

That means $r - 1/n$ is an upper bound of $A$.
So $r$ is not the least upper bound.

Then we have to have $r^2 = 2$.

$\square$

### 1.1.4.

(a) Prove by induction that

$$ 
\sum_{i=1}^{n} i^2 = \frac{n(n+1)(2n+1)}{6}
\text{ for all } n \in \mathbb{Z}^+
$$

**Proof**: When $n = 1$,

$$ 
1^2 = \frac{1 \cdot 2 \cdot 3}{6}
$$

Assume when $n = k$ this is correct

$$ 
\begin{split}
\sum_{i=1}^{k+1} i^2
&= \frac{k(k+1)(2k+1)}{6} + (k+1)^2 \\
&= \frac{[k(2k+1) + 6(k+1)](k+1)}{6} \\
&= \frac{(k+1)(k+2)(2(k+1)+1)}{6} \\
\end{split}
$$

So when $n = k + 1$, it's still correct.

$\square$

(b) **(Bernoulli’s inequality)** For every real number $r ≥ −1$, prove that

$$ 
(1+r)^n \geq 1 + rn \text{ for all } n \in \mathbb{N}.
$$

**Proof**: It's correct when $n = 1$.

$$ 
(1+r)^{k+1} \geq (1+rk)(1+r) =
1 + r(k+1) + r^2k \geq 1 + r(k+1)
$$

So it's correct for all $n \in \mathbb{N}$.

$\square$

(c) For what positive integers $n$ is $2^n > n^3$?

**Proof**:

Note when $n = 10$

$$ 
2^{10} = 1024 > 1000 = 10^3 
$$

Assume $2^k > k^3, k \geq 10$

$$ 
(k+1)^3 = (k^3 + 3k^2 + 3k + 1) < k^3 + 3k^2 + 3k^2 + 3k^2 \\
= k^3 + 9k^2 < k^3 + k^3 = 2 k^3 < 2 \cdot 2^k = 2^{k+1}
$$

$\square$

### 1.1.5.

(a) Use the induction theorem to show that for every natural number $m$, the sum $m+n$ and the product $mn$ are again natural for every natural number $n$. Thus $\mathbb{N}$ is closed under addition and multiplication, and consequently so is $\mathbb{Z}$.

**Proof**: skip

(b) Which of the field axioms continue to hold for the natural numbers?

**Solution**:

The following does not hold:

(a3) Existence of additive inverses

(m3) Existence of multiplicative inverses

(c) Which of the field axioms continue to hold for the integers?

The following does not hold:

(m3) Existence of multiplicative inverses

$\square$

### 1.1.6.

For every positive integer $n$, let $\mathbb{Z}/n\mathbb{Z}$ 
denote the set $\{0,1,...,n−1\}$ with the usual operations of addition 
and multiplication carried out taking remainders on division
by $n$. That is, add and multiply in the usual fashion
but subject to the additional condition that $n = 0$.
For example, in $\mathbb{Z}/5\mathbb{Z}$ we
have $2+4 = 1$ and $2·4 = 3$. For what values of n does
$\mathbb{Z}/n\mathbb{Z}$ form a field?

**Solution**:

If $n$ is a composite number, and assume $n = a \cdot b, a > 1, b > 1$. If $a$ has a multiplication inverse $a'$, then

$$ 
a \cdot a' \equiv 1 \pmod n
$$

So $a \cdot a' - kn = 1$, but $a | n$ and $a | a$, so $a | 1$,
we have a contradiction. So $a$ does not have a multiplication
inverse, then $\mathbb{Z}/n\mathbb{Z}$ is not a field.

If $n$ is prime number, and $1 < a < n$, then $(a, n) = 1$.
We can find $p, q$ such that $ap + nq = 1$. So

$$ 
ap \equiv 1 \pmod n
$$

Then $p$ is the multiplication inverse of $a$.

$\mathbb{Z}/n\mathbb{Z}$ is a field.

$\square$

## 1.2 Foundational and Basic Theorems

### 1.2.1.

Use the intermediate value theorem to show that 2 has a positive 
square root.

## 1.3

### 1.3.1.

(a) Let $n ∈ \mathbb{N}$. What is the $(2n + 1)$st-degree Taylor 
polynomial $T_{2n+1}(x)$ for the function $f(x) = \sin x$ at $0$? 
(The reason for the strange indexing here is that every second 
term of the Taylor polynomial is $0$.) Prove that $\sin x$ is 
equal to the limit of $T_{2n+1}(x)$ as $n → ∞$, similarly to the
argument in the text for $e^x$. Also find $T_{2n}(x)$ for
$f(x) = \cos x$ at $0$, and explain why the argument for $\sin$ 
shows that $\cos x$ is the limit of its even-degree Taylor
polynomials as well.

**Solution**

$$ 
T_{2n+1}(x) = \frac{x}{1!} - \frac{x^3}{3!} + 
+ \frac{x^5}{5!}
- \frac{x^7}{7!}
+
\cdots 
$$

The Taylor remainder is

$$ 
|R_{2n+1}(x)| =
\left| 
\frac{\sin^{(2n+2)}(c)  x^{2n+2}}{(2n+2)!}
\right|
\leq
\frac{x^{2n+2}}{(2n+2)!} \rightarrow 0
$$

For $\cos x$

$$ 
T_{2n}(x) =
1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots
$$

$$ 
|R_{2n}(x)| =
\left| 
\frac{\cos^{(2n+1)}(c)  x^{2n+1}}{(2n+1)!}
\right|
\leq
\frac{x^{2n+1}}{(2n+1)!} \rightarrow 0
$$

$\square$

(b) Many years ago, the author’s high-school physics textbook 
asserted, baﬄingly, that the approximation $\sin x ≈ x$ is good 
for $x$ up to $8^◦$. Deconstruct.

**Solution**:

$8^\circ$ in terms of radius is
$\frac{\pi }{2} \times 8 / 90 \approx 0.14$.

And we have

$$ 
|R_1(x)| \leq \frac{x^2}{2} = \frac{0.14^2}{2} \approx 0.01
$$

So the error with $8^\circ$ is less than $1\%$.

$\square$

### 1.3.2.

What is the $n$th-degree Taylor polynomial $T_n(x)$ for the following functions at $0$?

(a) $f(x) = \arctan x$. (This exercise is not just a matter of 
routine mechanics. One way to proceed involves the geometric 
series, and another makes use of the factorization
$1 + x^2 = (1-ix)(1+ix).)$

**Solution**:

Here are steps in Understanding Analysis

First, we know

$$ 
\arctan ' x = \frac{1}{1 + x^2}
$$

Note the following geometric series converges in $(-1, 1)$.

$$ 
\frac{1}{1 - x} = 1 + x + x^2 + \cdots 
$$

We replace $x$ with $-x^2$ and get

$$ 
\frac{1}{1 + x^2} = 1 - x^2 + x^4 - x^6 + \cdots 
$$

Now take anti-differentiation on both side:

$$ 
\arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} +
\cdots
$$

This is the $n$th-degree Taylor polynomial $T_n(x)$ for
$\arctan x$.

$\square$

(b) $f(x) = (1 + x)^α$ where $α ∈ \mathbb{R}$.
(Although the answer can be written in a uniform way for all $α$, 
it behaves diﬀerently when $α ∈ \mathbb{N}$. Introduce the
generalized binomial coeﬃcient symbol

$$ 
\binom{α}{k} = \frac{α(α-1)(α-2)\cdots (α-k+1)}{k!}, k \in \mathbb{N}
$$

to help produce a tidy answer.)

**Solution**:

$$ 
f'(x) = α(1+x)^{α-1} = \binom{α}{1} \\
f''(x) = α(α-1)(1+x)^{α-2} = 2! \binom{α}{2} \\
\cdots \\
f^{n}(x) = α(α-1)\cdots(α-n+1) (1+x)^{α-n} = n! \binom{α}{n} \\
$$

So

$$ 
T_n(x) = 1 + \binom{α}{1} x + \binom{α}{2} x^2 + \cdots +
\binom{α}{n} x^n  
$$

$\square$

### 1.3.3.

(a) Further tighten the numerical estimate of $\ln(1.1)$ from this 
section by reasoning as follows. As n increases, the Taylor 
polynomials $T_n(0.1)$ add terms of decreasing magnitude and 
alternating sign. Therefore $T_4(0.1)$ underestimates $\ln(1.1)$. Now that we know this, it is useful to find the smallest
possible value of the remainder (by setting $c = 0.1$ rather than 
$c = 0$ in the formula). Then $\ln(1.1)$ lies between $T_4(0.1)$ 
plus this smallest possible remainder value and $T_4(0.1)$ plus 
the largest possible remainder value, obtained in the
section. Supply the numbers, and verify by machine that the 
tighter estimate of $\ln(1.1)$ is correct.

**Solution**:

$$ 
T_n(x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots
= \sum_{k=1}^{n} (-1)^{k-1} \frac{x^k}{k},
$$

And we also have

$$ 
R_n(x) = \frac{(-1)^n x^{n+1}}{(1+c)^{n+1}(n+1)}
$$

And we can plug $c = 0, 0.1, x = 0.1$ into the above equation.
So we have

$$ 
\frac{0.1^5}{(1.1^5 \cdot 5)} \leq R_4(x) \leq
\frac{0.1^5}{(1.0^5 \cdot 5)}
$$

We calculate $\ln (1.1) = 0.09531018$, $T_4(1.1) = 0.09530833$

$$ 
T_4(1.1) + \frac{0.1^5}{(1.1^5 \cdot 5)} = 0.09530957
$$

Which is indeed than the lower bound obtained in the book,
which is $0.09530633$.

$\square$

(b) In Figure 1.1, identify the graphs of $T_1$ through $T_5$ and the graph of $\ln$ near $x = 0$ and near $x = 2$.

**Solution**: It's easy to see $T_1$ is a straight line.

Now focus on $x \geq 0$. From part (a), we know
$T_1(x) > T_3(x) > T_5(x) > \ln (x)$ and
$T_2(x) < T_4(x) < \ln (x)$.

Then focus on $x < 0$, notice

$$ 
T_{n}(x) - T_{n+1}(x) = (-1)^{n+1} \frac{x^{n+1}}{n+1}
$$

No matter of $n$, it is always positive, so

$T_1(x) > T_2(x) > \cdots > T_5(x) > \ln (x)$.

$\square$

### 1.3.4.

Working by hand, use the third-degree Taylor polynomial for 
$\sin(x)$ at $0$ to approximate a decimal representation of
$\sin(0.1)$. Also compute the decimal representation of an upper 
bound for the error of the approximation.
Bound $\sin(0.1)$ between two decimal representations.

**Solution**:

$$ 
T_3(x) = \frac{x}{1} - \frac{x^3}{3!}
$$

And also

$$ 
|R_3(x)| \leq \frac{x^4}{4!}
$$

$$ 
T_3(0.1) = 0.09983333 \\
|R_3(0.1)| \leq \frac{0.1^4}{4!} = 0.00000417 \\
0.09982916 \leq \sin (0.1) \leq 0.0998375
$$

With calculator, $\sin (0.1) \approx 0.09983342$.

### 1.3.5.

Use a second-degree Taylor polynomial to approximate
$\sqrt[]{4.2}$. Use Taylor’s theorem to find a guaranteed
accuracy of the approximation and thus to find upper and lower 
bounds for $\sqrt[]{4.2}$.

**Solution**:

Consider $f(x) = \sqrt[]{4+x}$

$$
\begin{split}
f'(x) &= \frac{1}{2} (4+x)^{-\frac{1}{2}} \\
f''(x) &= -\frac{1}{2^2} (4+x) ^{-\frac{3}{2}} \\
f^{(3)}(x) &= \frac{1 \cdot 3}{2^3} (4+x) ^{-\frac{5}{2}} \\
\end{split}
$$

So we have

$$ 
T_2(x) = f(0) + f'(0) x + \frac{f''(0)}{2!}x^2 \\
= 2 + \frac{x}{4} - \frac{x^2}{64}
$$

The remainder is:

$$ 
|R_2(x)| =
\left| 
\frac{f^{(3)}(c)}{3!}x^3
\right| \leq
\frac{f^{(3)}(0)}{3!}x^3 =
\frac{3x^3}{3!2^8} = \frac{x^3}{512}
$$

Then we have

$$ 
T_2(0.2) = 2.049375 \\
|R_2(0.2)| = \frac{0.2^3}{512} = 0.00001562 \\
\sqrt[]{4.2} = 2.04939015 \\
$$

Finally, we have

$$ 
2.04935938 = T_2(0.2) - |R_2(0.2)| < \sqrt[]{4.2} < T_2(0.2) + |R_2(0.2)|
= 2.04939062
$$

$\square$

### 1.3.6.

(a) Another proof of Taylor’s Theorem uses the fundamental theorem
of integral calculus once and then integrates by parts repeatedly. 
Begin with the hypotheses of Theorem 1.3.3, and let $x ∈ I$.
By the fundamental theorem,

$$ 
f(x) = f(a) + \int_{a}^{x} f'(t) dt
$$

Let $u = f'(t)$ and $v = t - x$, so that the integral is
$\int_{a}^{x} u v'$, and integrating by parts gives

$$ 
\int_{a}^{x} u v' = uv \bigg|_{a}^{x} - \int_{a}^{x} u'v
= f'(x)(x - x) - f'(a) (a - x) - \int_{a}^{x} f''(t)(t-x) \\
= f'(a) (x - a) - \int_{a}^{x} f''(t)(t-x) dt
$$

So

$$ 
f(x) = f(a) + f'(a) (x - a) - \int_{a}^{x} f''(t)(t-x) dt
$$

Now let $u = f''(t)$ and $v = \frac{1}{2} (t - x)^2$,

$$ 
\begin{split}
\int_{a}^{x} u v'
&= uv \bigg|_{a}^{x} - \int_{a}^{x} u'v \\
&= f''(x) \frac{1}{2} (x-x)^2 - f''(a) \frac{1}{2}(a - x)^2
- \int_{a}^{x} f'''(t) \frac{1}{2} (t-x)^2 dt
\end{split}
$$

So

$$ 
f(x) = f(a) + f'(a) (x - a) + f''(a) \frac{(x-a)^2}{2}
+ \int_{a}^{x} f'''(t) \frac{1}{2} (t-x)^2 dt
$$

Then we can use induction and assume

$$ 
f(x) = T_n(x) + (-1)^n \int_{a}^{x} f^{(n+1)}(t)
\frac{(t-x)^n}{n!} dt
$$

Let $u = f^{(n+1)}(t), v = \frac{(t-x)^{(n+1)}}{(n+1)!}$

$$ 
\begin{split}
\int_{a}^{x} u v'
&= uv \bigg|_{a}^{x} - \int_{a}^{x} u'v \\
&= f^{(n+1)}(x) \frac{(x-x)^{n+1}}{{(n+1)}!} -
f^{(n+1)}(a) \frac{(a-x)^{n+1}}{{(n+1)}!} -
\int_{a}^{x} f^{(n+2)}(t) \frac{(t-x)^{(n+1)}}{(n+1)!}
\\
&= (-1) \cdot
\left( 
f^{(n+1)}(a) \frac{(a-x)^{n+1}}{{(n+1)}!}
+
\int_{a}^{x} f^{(n+2)}(t) \frac{(t-x)^{(n+1)}}{(n+1)!}
\right) 
\end{split}
$$

No mattern $n$ is even or odd, $(-1)^{n} (a-x)^n = (x-a)^n$
So

$$ 
f(x) = T_{n+1} +
(-1)^{n+1} \int_{a}^{x} f^{(n+2)}(t) \frac{(t-x)^{(n+1)}}{(n+1)!} 
dt
$$

Whereas the expression for $f(x)−T_n(x)$ in Theorem 1.3.3 is 
called the Lagrange form of the remainder, this exercise has 
derived the integral form of the remainder. Use the extreme value 
theorem and the intermediate value theorem to derive the Lagrange 
form of the remainder from the integral form.

**Proof**:

We want to estimate

$$ 
A = (-1)^n \int_{a}^{x} f^{(n+1)}(t)
\frac{(t-x)^n}{n!}
$$

Assume $m \leq f^{(n+1)}(t) \leq M$, and let

$$ 
B = (-1)^n \int_{a}^{x} \frac{(t-x)^n}{n!} dt =
(-1)^n \frac{(t-x)^{(n+1)}}{{(n+1)}!}\Bigg|_{a}^{x} =
(-1)^{n+1} \frac{(a-x)^{(n+1)}}{{(n+1)}!} =
\frac{(x-a)^{(n+1)}}{{(n+1)}!}
$$

Note $(-1)^n \frac{(t-x)^n}{n!} \geq 0, t \in [a, x]$, so

$$ 
m \frac{(x-a)^{(n+1)}}{{(n+1)}!} \leq
(-1)^n \int_{a}^{x} f^{(n+1)}(t)
\frac{(t-x)^n}{n!} \leq
M \frac{(x-a)^{(n+1)}}{{(n+1)}!}
$$

i.e.

$$ 
mB \leq A \leq MB
$$

Since $f^{(n+1)}$ is continuous, with extreme value theorem,
we can find $f^{(n+1)}(t_m) = m, f^{(n+1)}(t_M) = M$.

Then with intermediate value theorem, we can find $c$, such that
$f^{(n+1)}(c) = A/B$, i.e.

$$ 
(-1)^n \int_{a}^{x} f^{(n+1)}(t) \frac{(t-x)^n}{n!} dt =
\frac{f^{(n+1)}(c)}{(n+1)!}(x-a)^{n+1}
$$

$\square$

(b) Use the integral form of the remainder to show that

$$ 
\ln (1+x) = T(x) \text{ for } x \in (-1, 1]
$$

**Proof**:

$$ 
f^{(n+1)}(t) = \frac{(-1)^n n!}{(1+t)^{n+1}}
$$

So

$$
\begin{split}
(-1)^n \int_{0}^{x} f^{(n+1)}(t) \frac{(t-x)^n}{n!} dt
&= (-1)^{2n} \int_{0}^{x}
\frac{(-1)^n n!}{(1+t)^{n+1}} \frac{(t-x)^n}{n!} dt \\
&= \int_{0}^{x}
\frac{(t-x)^n}{(1+t)^{n+1}} dt
\end{split}
$$

Consider, $x \in (-1, -1/2]$, and $t \geq x$.

$$ 
t \geq x > (2+t)x \\
\Rightarrow \\
t > (2+t)x \\
\Rightarrow \\
t - x > x + tx \\
\Rightarrow \\
\frac{t-x}{1+t} > x \\
$$

So $\left| \frac{t-x}{1+t} \right| < |x|$

Then

$$
\begin{split}
\left| 
\int_{x}^{0}
\frac{(t-x)^n}{(1+t)^{n+1}} dt
\right|
& \leq
\int_{x}^{0}
\left| 
\frac{(t-x)^n}{(1+t)^{n+1}}
\right|  dt\\
& \leq
\frac{1}{1+x}
\int_{x}^{0}
\left| 
\frac{(t-x)}{(1+t)}
\right|^n  dt\\
& \leq
\frac{1}{1+x}
\int_{x}^{0}
|x|^n  dt\\
&= \frac{|x|^{n+1}}{1+x} \to 0
\end{split}
$$

The book has proved the case for $(-1/2, 1]$.
Then we can conclude

$$ 
\ln (1+x) = T(x) \text{ for } x \in (-1, 1]
$$

$\square$
