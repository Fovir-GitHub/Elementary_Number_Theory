# Quadratic Residue and Nonresidues

## Definition

If $\gcd(a,m) = 1$, $m \in \mathbb{Z}^+$ and $x^2 \equiv a \mod m$ has a solution, then $a$ is a quadratic residue of $m$. If it has no solution, then $a$ is a quadratic nonresidues of $m$.

## Theorem 1

Let $p$ be an odd prime number, and $a \in \mathbb{Z}, a \nmid p$. The congruence

$$
x^2 \equiv a \mod p
$$

has either no solution or exactly two solutions mod p

## Theorem 2

If $p$ is an odd prime, then there are exactly $\frac{p-1}{2}$ quadratic residues of $p$ and $\frac{p-1}{2}$ quadratic nonresidues of $p$ among $1,2,\dots,p-1$.

## Theorem 3

Let $p$ be a prime.

$$
\begin{array}{c}
    \text{ord}_{p}{r} = \phi(p) \\
    a \in \mathbb{Z}, a \nmid p \\
    \text{ind}_{r}{a} \equiv 0 \mod 2 \Longrightarrow a \space \text{is a quadratic residue of} \space p \\
    \text{ind}_{r}{a} \equiv 1 \mod 2 \Longrightarrow a \space \text{is a quadratic nonresidue of} \space p \\
\end{array}
$$

# Legendre Symbol

Let $p$ be an odd prime and $a \in \mathbb{Z}, a \nmid p$. The Legendre Symbol is:

$$
\begin{array}{c}
    (\frac{a}{p}) =
    \begin{cases}
        1, \quad \text{if} \space a \space \text{is a quadratic residue of} \space p; \\
        -1, \quad \text{if} \space a \space \text{is a quadratic nonresidue of} \space p; \\
    \end{cases}
\end{array}
$$

## Euler's Criterion

$$
(\frac{a}{p}) \equiv a^{\frac{p-1}{2}} \mod p
$$

## Theorem 1

Let $p$ be an odd prime, and $a, b \in \mathbb{Z}, a \nmid p, b \nmid p$, then

$$
\begin{array}{c}
    a \equiv b \mod p \Longrightarrow (\frac{a}{p}) = (\frac{b}{p}) \\
    (\frac{a}{p})(\frac{b}{p}) = (\frac{ab}{p}) \\
    (\frac{a^2}{p}) = 1
\end{array}
$$

## Theorem 2

If $p$ is an odd prime, then $-1$ is a quadratic residue of $p$ if and only if $p \equiv 1 \mod 4$

## Gauss's Lemma

Let $p$ be an odd prime number, and $a \in \mathbb{Z}, \gcd(a,p) = 1$. If $s$ is the number of least positive residue of $ka$, where $k \in \mathbb{Z}, k \in [1,p-1]$ that are greater than $\frac{p-1}{2}$, then $(\frac{a}{p}) = (-1)^s$.

### Example

$p = 7, a = 3$

$$
\begin{array}{c}
    3 \mod 7 = 3 \\
    6 \mod 7 = 6 \\
    9 \mod 7 = 2 \\
    12 \mod 7 = 5 \\
    15 \mod 7 = 1 \\
    18 \mod 7 = 4 \\
    \therefore \text{The residues are} \quad \\{3,6,2,5,1,4\\} \\
    \because \frac{p - 1}{2} = \frac{7-1}{2} = 3 \\
    \therefore s = 3 \\
    \therefore (\frac{3}{7}) = (-1) ^ s = -1
\end{array}
$$

## Theorem 3

Let $p$ be an odd prime.

$$
\exists x, \space x^2 \equiv 2 \mod p \Longleftrightarrow p \equiv \pm 1 \mod 8
$$

# The Law of Quadratic Reciprocity

Let $p$ and $q$ be distinct odd primes. Then

$$
(\frac{p}{q})(\frac{q}{p}) = (-1)^{\frac{p-1}{2} \cdot \frac{q-1}{2}}
$$

# The Jacobi Symbol

If $n$ is an odd positive integer with prime factorization

$$
n = \displaystyle\sum_{i = 1}^{m}{p_i^{t_i}}
$$

And $a \in \mathbb{Z}, \gcd(a,n) = 1$. Then the Jacobi symbol $(\frac{a}{n})$ is defined by:

$$
(\frac{a}{n}) = \displaystyle\sum_{i=1}^{m}{(\frac{a}{p_i})^{t_i}}
$$

If $\gcd(a,n) > 1$, then $(\frac{a}{n}) = 0$

## Properties

Let $n$ be an odd positive integer and $a,b \in \mathbb{Z}, \gcd(a,n) = \gcd(b,n) = 1$, then

1. $a \equiv b \mod n \Longrightarrow (\frac{a}{n})=(\frac{b}{n})$
2. $(\frac{ab}{n})$ = $(\frac{a}{n})(\frac{b}{n})$
3. $(\frac{-1}{n}) = (-1)^{\frac{n-1}{2}}$
4. $(\frac{2}{n}) = (-1)^{\frac{n^2-1}{8}}$

## The Reciprocity Law of Jacobi Symbol

If $m,n \in \mathbb{Z}^+, m \equiv n \equiv 1 \pmod 2, m > 1, n > 1$, then

$$
(\frac{m}{n})(\frac{n}{m})=(-1)^{\frac{m-1}{2} \cdot \frac{n-1}{2}}
$$