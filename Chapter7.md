# Pythagorean Triples

## Definition

A triple of $(x,y,z)$ is called Pythagorean triple if

$$
\begin{array}{c}
    x,y,z \in \mathbb{Z}^+ \\
    x^2+y^2=z^2 \\
\end{array}
$$

## Primitive Pythagorean Triple

If $(x,y,z)$ is a Pythagorean triple and $\gcd(x,y) = \gcd(x,z) = \gcd(y,z) = 1$, then it is a primitive Pythagorean triple

## Lemma

If $(x,y,z)$ is a primitive Pythagorean triple, then $x$ and $y$ must be one odd one even.

## Theorem 1

$$
\begin{array}{c}
    \text{If} \quad r,s \in \mathbb{Z}^+, \gcd(r,s) = 1 \\
    \exists t \in \mathbb{Z}^+, rs = t^2 \Rightarrow \exists m,n \in \mathbb{Z}^+, \gcd(m,n) = 1, r = m^2, s = n^2 \\
\end{array}
$$

## Theorem 2

The triple $(x,y,z)$ of positive integers is a primitive Pythagorean triple, with $y$ even $\Longleftrightarrow \exists m,n \in \mathbb{Z}^+, \gcd(m,n) = 1, m \gt n$, with $m + n$ odd, and

$$
\begin{array}{c}
    x = m^2 - n^2 \\
    y = 2mn \\
    z = m^2 + n^2 \\
\end{array}
$$

# Fermat's Last Theorem

$$
x^n + y^n = z^n \quad x,y,z,n \in \mathbb{Z}
$$

has no solutions in nonzero integers when $n \geq 3$

## Theorem 1

$$
x^4 + y^4 = z^4
$$

has no solutions in nonzero integers

# Sum of Squares

## Theorem 1

$$
n \in \mathbb{Z}^+, \exists a,b \in \mathbb{Z}^+, n = a^2 + b^2 \Rightarrow n \not \equiv 3 \pmod 4
$$

## Theorem 2

If $m$ and $n$ are both sums of two squares, then $mn$ is also a sum of two squares.

## Lemma

$$
\begin{array}{c}
    \text{If $p$ is a prime number} \quad p \equiv 1 \mod 4 \\
    \exists k \in \mathbb{Z}^+, k \in (0,p) \space \exist x,y \in \mathbb{Z} \\
    kp = x^2 + y^2 \\
\end{array}
$$

## Theorem 3

If $p$ is a prime number and $p \equiv 1 \mod 4$, then $p$ can be written as a sum of two squares.

## Corollary

If $p$ is a prime and $p \not \equiv 3 \mod 4$, then $p$ can be written as a sum of two squares.

## Theorem 4

$$
\begin{array}{c}
    n = \displaystyle\sum_{i=1}^{k}{p_i^{e_i}} \quad \text{where $p_i$ are primes} \\
    \exists a,b \in \mathbb{Z}, n = a^2 + b^2 \Leftrightarrow \forall i \in \\{p_i \equiv 3 \mod 4\\}, e_i \space \text{is even}
\end{array}
$$

## Theorem 5

If $m,n \in \mathbb{Z}^+$ and are each the sum of four squares, then $mn$ is also the sum of four squares.

## Theorem 6

$$
\begin{array}{c}
    \text{$p$ is an odd prime}, \exists k,x,y,z,w \in \mathbb{Z}, k \in (0,p) \\
    kp = x^2 + y^2 + z^2 + w^2 \\
\end{array}
$$

## Theorem 7

Let $p$ be a prime, then $x^2 + y^2 + z^2 + w^2 = p$ has a solution, where $x,y,z,w \in \mathbb{Z}$.

## Theorem 8

Every positive integer is the sum of four integers.

## Theorem 9

$$
\begin{array}{c}
    n \in \mathbb{Z}^+ \exists x,y,z \in \mathbb{Z}, n = x^2 + y^2 + z^2 \\
    \Downarrow \\
    n \not \equiv 7 \mod 8
\end{array}
$$

## Theorem 10

If $n \in \mathbb{Z}^+$ can be written as the sum of three squares, if and only if it is not the form $n = 4^km, k \in \mathbb{Z}, k \geq 0, m \equiv 7 \mod 8$.