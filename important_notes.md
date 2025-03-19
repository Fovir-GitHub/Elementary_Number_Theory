# $\pi$ Function

$\pi(n)$ is the number of prime numbers less than $n$.

# Divide

If $a=bc$, then $b$ divides $a$ or $a$ is divided by $b$, which is $b \mid a$.

# Consecutive Composite Numbers

$$
\begin{cases}
    (n+1)!+2 \\
    (n+1)! + 3 \\
    \vdots \\
    (n+1)!+(n+1)\\
\end{cases}
$$

# Theorems of GCD and LCM

1. $\gcd(\frac{a}{\gcd(a,b)},\frac{b}{\gcd(a,b)})=1$
2. $\gcd(a+cb,b) = \gcd(a,b)$
3. $\gcd(a,b) = 1 \text{ and } a \mid bc \Rightarrow a \mid c$
4. If $a = \displaystyle\sum_{i=1}^{n}(p_i^{a_i}) \quad b = \displaystyle\sum_{i=1}^{n}(p_i^{b_i})$, then

$$
\gcd(a,b) = \displaystyle\sum_{i=1}^{n}(p_i^{\min{a_i,b_i}}) \quad \text{lcm}(a,b) = \displaystyle\sum_{i=1}^{n}(p_i^{\max(a_i,b_i)})
$$

5. $\gcd(a,b) \cdot \text{lcm}(a,b) = a \cdot b$

# Diophantine Equation

$ax + by = c$

Let $d = \gcd(a,b)$, if $d \nmid c$, then there is no integral solution. If $d \mid c$, then there is infinitely many solutions.

The solution is:

$$
\begin{cases}
    x = x_0 + \frac{b}{d} \cdot n \\
    y = y_0 - \frac{a}{d} \cdot n
\end{cases}
$$

where $x_0$ and $y_0$ are particular solution

# Linear Congruence

1. $a \equiv b \pmod m \Leftrightarrow m \mid (a-b) \Leftrightarrow a = km + b, k \in \mathbb{Z}$
2. If $a \equiv b \pmod m$ and $c \equiv d \pmod m$, then
   1. $a + c \equiv b + d \pmod m$
   2. $a - c \equiv b - d \pmod m$
   3. $ac \equiv bd \pmod m$
3. If $ac \equiv bc \pmod m$, then $a \equiv b \pmod{\frac{m}{\gcd(c,m)}}$
4. $a \equiv b \mod m_1$ and $a \equiv b \mod m_2$, then $a \equiv b \mod \text{lcm}(m_1,m_2)$
5. $a^n \mod m = (a \mod m)^n \mod m$
6. $a \equiv b \pmod m \Rightarrow a^n \equiv b^n \pmod m$

# Congruence Class

If $a$ is a congruence class modulo $m$, $a$ is:

## $[a]_m = \\{x \in \mathbb{Z} \mid x \equiv a \pmod m\\}$

# Fermat's Little Theorem

If $p$ is a prime number,

1. $(p-1)! \equiv -1 \mod p$
2. $p \nmid a \Rightarrow a^{p-1} \equiv 1 \mod p$
3. $a^p \equiv a \mod p$

# Euler's Theorem

## $\gcd(a,m) = 1 \Rightarrow a^{\phi(m)} \equiv 1 \mod m$

# Three Functions

| Function    | Definition                                                                       | Meaning                                                                      | Formula                                                                                        |
| ----------- | -------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| $\phi(n)$   | $\phi(n) = card(\\{x \in \mathbb{Z}^+ \mid \gcd(x,n) = 1, x \in [1,n]\\})$       | The number of integers that is relatively prime to $n$ and not exceeding $n$ | $\phi(p^n)=p^n-p^{n-1}$ or $\phi(n) = n \cdot \displaystyle\prod_{i=1}^{s}{(1-\frac{1}{p_i})}$ |
| $\tau(n)$   | $\tau(n) = \displaystyle\sum_{d \mid n}{f(d)} = \displaystyle\sum_{d \mid n}{1}$ | The number of positive divisors of $n$ that is not exceeding $n$             | $\tau(n) = \displaystyle\prod_{i=1}^{s}{(a_i+1)}$                                              |
| $\sigma(n)$ | $\sigma(n) = \displaystyle\sum_{d \mid n}{d}$                                    | The sum of the positive divisors                                             | $\sigma(p^n) = \frac{p^{n+1} - 1}{p - 1}$                                                      |

# Theorems of The Order

If $\gcd(a,n) = 1$

1. $a^x \equiv 1 \mod n \Longleftrightarrow \text{ord}_na \mid x$
2. $\text{ord}_na \mid \phi(n)$
3. $a^i \equiv a^j \mod n \Leftrightarrow i \equiv j \mod \text{ord}_na$

# Theorems of Primitive Root

1. $\text{ord}_n{a^u} = \frac{\text{ord}_na}{\gcd(\text{ord}_na, u)}$
2. There are $\phi(\phi(n))$ incongruent primitive roots.
3. If $n$ has primitive roots, it is one of:
   1. $n=2$
   2. $n=4$
   3. $n=p^t$
   4. $n=2p^t$

# Quadratic Residue and Nonresidues

If $p$ is an odd prime number, then

1. There are $\frac{p-1}{2}$ quadratic residue and non residues.

# Euler's Criterion

## $(\frac{a}{p}) \equiv a^{\frac{p-1}{2}} \mod p$

# Theorems of Legendre Symbol

1. $a \equiv b \mod p \Longrightarrow (\frac{a}{p}) = (\frac{b}{p})$
2. $(\frac{a}{p})(\frac{b}{p}) = (\frac{ab}{p})$
3. $(\frac{a^2}{p}) = 1$
4. $(\frac{-1}{p}) = 1 \Longleftrightarrow p \equiv 1 \mod 4$
5. $(\frac{2}{p}) = 1 \Longleftrightarrow p \equiv \pm 1 \mod 8$

# Theorems of Jacobi Symbol

1. $a \equiv b \mod n \Longrightarrow (\frac{a}{n}) = (\frac{b}{n})$
2. $(\frac{a}{n})(\frac{b}{n}) = (\frac{ab}{n})$
3. $(\frac{-1}{n}) = (-1)^{\frac{n-1}{2}}$
4. $(\frac{2}{n}) = (-1)^{\frac{n^2-1}{8}}$
5. $\gcd(a,n) > 0 \Longleftrightarrow (\frac{a}{n}) = 0$

# Quadratic Irrationals

## $\alpha = \frac{a+\sqrt{b}}{c} \gt 0$ is quadratic irrational.

# Lagrange's Theorem

## The infinite simple continued fraction of an irrational number is periodic if and only if this number is a quadratic irrational number.

# Theorems of Pythagorean Triples

1. If $(x,y,z)$ is a Pythagorean Triple, then $x$ and $y$ must be one odd and one even.
2. If $(x,y,z)$ is a Pythagorean Triple, then
   * $x = m^2 - n^2$
   * $y = 2mn$
   * $z = m^2 + n^2$

# Theorems of Sum of Squares

1. If $n \not \equiv 3 \pmod 4$, then $n$ can be written as the sum of two squares.
2. If $m$ and $n$ are the sum of two squares, then $mn$ is also the sum of two squares.
3. $p$ is a prime number and $p \equiv 1 \mod 4$, then $p$ can be written as the sum of two squares.
4. $n$ can be written as the sum of two squares, the power of the prime factors such that $p \equiv 3 \mod 4$ are all even.
5. Every integer can be written as the sum of four squares.
6. If $n$ can be written as the sum of three squares, then $n \not \equiv 7 \mod 8$
7. If $n$ can be written as the sum of three squares, if and only if $n$ is not the form $n = 4^km$, where $m \equiv 7 \mod 8$ and $k \geq 0$.