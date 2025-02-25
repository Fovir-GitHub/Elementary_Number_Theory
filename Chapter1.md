# Algebraic numbers

If $a$ is an algebraic number, there is a polynomial:

$$
p(x) = c_nx^n + c_{n-1}x^{n-1} + \dots + c_1x +c_0
$$

with integer coefficients such that $p(a)=0$

**Conditions:**

1. $a$ is a non-zero polynomial.
2. $x$ is a root.
3. The coefficients are rational numbers.

**Example:**

$x^2+5x+6$ is an algebraic number.

# Transcendental numbers

A number that is not algebraic.

**Example:**

$\pi$

# Well Ordering Principle

Every non-empty subset of positive integers has a smallest element.

Sign of empty set: $\emptyset$ or $\{\}$

# Principle of Mathematical Induction

If $P(n)$ is a sequence of statements indexed by $\mathbb{Z}^+$ and

1. $P(1)$ is true.
2. If $P(n)$ is true, then $P(n+1)$ is true.

Then, $P(n)$ is true for all $n\in\mathbb{Z}^+$.

# Principle of Strong Mathematical Induction

1. $P(1)$ is true.
2. If $P(k)$ is true for all $k \leq n$, then $P(n+1)$ is true.

Then $P(n)$ is true for all $n \in \mathbb{Z}^+$

# Divide

If $a = bc$, where $a,b,c \in \mathbb{Z}$ and $b \ge 0$, we say **$b$ divides $a$**, which can be written as $b \mid a$. If not, it can be written as $b \nmid a$.

# Prime Number

## Theorem 1

Every number greater than 1 has a prime divisor.

## Theorem 2

There are infinitely many prime numbers.

## Theorem 3

If $n$ is not a prime number, it has a prime divisor not larger than $\sqrt{n}$.

## Eratosthenes Sieve

**Goal:** Given a number $n$, find out all prime numbers not greater than $n$.

**Steps:**

1. Form a table from $1$ to $n$.
2. Calculate $\sqrt{n}$.
3. Let $i \in \mathbb{Z}^+, i \in [2,\sqrt{n}]$.
4. Multiply $i$ with a positive integer $k$ where $k \gt 1$ until $i \times k \gt n$, and mark all $i \times k$ as composite numbers.
5. Finally, the remaining numbers are prime numbers that not greater than $n$.

## $\pi(x)$

**Definition:** The number of prime numbers that does not exceed $x$.

**Example:**

$\pi(30) = 10$

## Consecutive Composite Numbers

$\forall n \in \mathbb{Z}^+$, we can find $n$ consecutive composite numbers.

The consecutive composite numbers are:

$$
\begin{align*}
    \begin{cases}
        (n+1)! + 2 \\
        (n+1)! + 3 \\
        (n+1)! + 4 \\
        \vdots \\
        (n+1)!+(n+1)
    \end{cases}
\end{align*}
$$

## Conjectures about Primes

### Twin Prime Conjecture

There are infinitely many pairs of primes $p$ and $p+2$.

### Goldbach's Conjecture

Every even positive integer greater than $2$ can be written as the sum of two primes.

# Greatest Common Divisor

The greatest common divisor of $a$ and $b$ can be written as $\gcd(a,b)$ or $(a,b)$.

## Theorem 1

If $\gcd(a,b) = d$, then $\gcd(\frac{a}{d},\frac{b}{d})=1$.

### Proof

$$
\begin{array}{c}
    \text{let}\quad \gcd(a,b)=d \\
    \text{then} \quad a = dx, b=dy \\
    \text{d is the greatest common divisor} \\
    \therefore \gcd(x,y) = 1 \\
    \text{and} \quad x=\frac{a}{d} \quad y=\frac{b}{d} \\
    \therefore \gcd(\frac{a}{d},\frac{b}{d})=1
\end{array}
$$

## Theorem 2

$$
\begin{align*}
    a,b,c \in \mathbb{Z} \\
    \gcd(a+cb,b)=\gcd(a,b)
\end{align*}
$$

### Proof

$$
\begin{align*}
    \text{let} \; \gcd(a,b)=d \\
    \text{then} \; a=d \cdot k \quad b=d \cdot m \\
    a+c\cdot b = d \cdot k + c \cdot (d \cdot m) = d \cdot (k+c \cdot m) \\
    \gcd(a+cb,b) = \gcd(d(k+cm),dm)= d \cdot \gcd(k+cm,m) \\
    \text{suppose} \; \exists \; e \in \mathbb{Z}^+, e \mid m \; \land \; e \mid {k+cm} \\
    m = e \cdot t\;,\; t \in \mathbb{Z} \\
    k + cm = e \cdot s \;,\; s \in \mathbb{Z} \\
    \text{substitute} \; m \; \text{into} \; {k+cm} \\
    k+c(e \cdot t) = e \cdot s \\
    k=e(s-ct) \\
    \because s-ct \in \mathbb{Z} \\
    \therefore e \mid k \\
    \because \gcd(k,m)=1 \\
    \therefore e = 1 \\
    \therefore \gcd(k+cm,m) = 1 \\
    \therefore \gcd(d(k+cm),dm)=d \cdot 1 = d \\
    \because d = \gcd(a,b) \\
    \therefore \gcd(a+cb,b) = gcd(a,b)
\end{align*}
$$

## The Euclidean Algorithm

Given integers $a$ and $b$ with $a \geq b \gt 0$, let $r_0=a$ and $r_1=b$

$$
\begin{align*}
    a=bq_1+r_2 \\
    b=r_2q_2+r_3 \\
    r_2=r_3q_3+r_4 \\
    \vdots \\
    r_{n-1}=r_nq_n
\end{align*}
$$

Then,

$$
r_n = (r_n,0)=(r_{n-1},r_n)=(r_{n-2},r_{n-1})=\dots=(b,a)
$$

# Bezout's Identity

$\forall a,b \in \mathbb{Z}^+$, let $\gcd(a,b)=d$, $\exist m,n \in \mathbb{Z}$

$$
d=ma+nb
$$

## Theorem 1

Let $a,b \in \mathbb{Z}, S=\{ma+nb \mid m,n \in \mathbb{Z}\}$. Then $d=\gcd(a,b)$ is the smallest positive integer in $S$, and

$$
S = \{kd \mid k \in \mathbb{Z}\}
$$

## Theorem 2

$$
\gcd(a_1,a_2,\dots,a_{n-1},a_n) = \gcd(\gcd(a_1,a_2,\dots,a_{n-1}),a_n)
$$

# Fundamental Theorem of Arithmetic

## Lemma 1

$$
\begin{align*}
    \text{if} \; a,b,c \in \mathbb{Z}^+ \\
    (\gcd(a,b)=1)  \land (a \mid bc) \\
    \text{then} \; a \mid c
\end{align*}
$$

## Lemma 2

If $p$ is a prime number, then

$$
\begin{align*}
    \forall a \in \mathbb{Z} \\
    \gcd(p,a)=p \\
    \text{or} \\
    \gcd(p,a)=1 \\
\end{align*}
$$

## Lemma 3

If $p$ is a prime number.

$$
\begin{align*}
    \text{if} \quad p \mid a_1a_2 \dots a_n \\
    \text{then} \quad \exists i \in [1,n], p \mid a_i
\end{align*}
$$

## Fundamental Theorem of Arithmetic

$$
\begin{align*}
    \forall m \in \mathbb{Z}^+, m \gt 1 \\
    m=\sum_{i=1}^{k}(p_i^{a_i}) \quad p_i \; \text{is prime number and} \; a_i \in \mathbb{Z}^+
\end{align*}
$$

# Least Common Multiple

The smallest positive integer that is a multiple of both $a$ and $b$ can be written as $lcm(a,b)$ or $[a,b]$ where $a,b \in \mathbb{Z}$

## Theorem 1

$$
\begin{align*}
    \text{if} \quad a=\sum_{i=1}^{n}(p_i^{a_i}) \quad b=\sum_{i=1}^{n}(p_i^{b_i}) \\
    \text{then} \quad \gcd(a,b)=\sum_{i=1}^{n}(p_i^{\min\{a_i,b_i\}}) \quad lcm(a,b) = \sum_{i=1}^{n}{p_i^{\max\{a_i,b_i\}}}
\end{align*}
$$

## Theorem 2

$$
gcd(a,b) \cdot lcm(a,b) = a \cdot b
$$

# Diophantine Equations

The form of the equation:

$$
ax+by=c \quad a,b,c,x,y \in \mathbb{Z}
$$

## Method of solving

let $d=\gcd(a,b)$

1. $d \nmid c \Rightarrow \text{No integral solutions}$
2. $d \nmid c \Rightarrow \text{Infinitely many solutions}$

If $x=x_0, y=y_0$ is a particular solution, all solutions are given by:

$$
\begin{cases}
    x=x_0+\frac{b}{d} \cdot n \\
    y=y_0 - \frac{a}{d} \cdot n \\
\end{cases}
$$

## Example

1. Find the $\gcd(a,b) = d$
2. Find the particular solution by solving:

$$
ax+by=d 
$$

3. Simplify the equation $ax+by=d$ (Optional)

$$
\frac{a}{d}x+\frac{b}{d}y=k
$$

4. Get the particular solution $(x_0,y_0)$
5. If did the step 3, multiply the particular solution with $d$
6. Substitute the particular solution into the formula.