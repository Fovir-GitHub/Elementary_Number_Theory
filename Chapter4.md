# The Order of An Integer

$$
\begin{array}{c}
    a \in \mathbb{Z}, a \ne 0, n \in \mathbb{Z}^+, \gcd(a,n) = 1 \\
    a^x \equiv 1 \mod n \quad x \space \text{is the smallest integer} \\
    x = \text{ord}_n{a}
\end{array}
$$

## Euler's Theorem

$$
\gcd(a,n) = 1 \Longrightarrow a^{\phi(n)} \equiv 1 \pmod n
$$

## Theorem 1

$$
\begin{array}{c}
    \gcd(a,n) = 1, a \ne 0, n \in \mathbb{Z}^+ \\
    a^x \equiv 1 \mod n \Longleftrightarrow \text{ord}_n{a} \mid x
\end{array}
$$

**Proof:**

$$
\begin{array}{c}
    \text{let} \quad \text{ord}_na = d \\
    \therefore a^d \equiv 1 \mod n \\
    \text{suppose} \quad a^x \equiv 1 \mod n \\
    \text{to prove:} \quad d \mid x \\
    \text{let} \quad x = qd + r \\
    \therefore a^{qd + r} \equiv 1 \mod n \\
    (a^d)^q \cdot a^r \equiv 1 \mod n \\
    \because a^d \equiv 1 \mod n \\
    \therefore a^r \equiv 1 \mod n \\
    \therefore r = 0 \\
    \therefore x = qd \\
    \therefore d \mid x \\
\end{array}
$$

## Corollary

$$
\gcd(a,n) = 1, n \gt 0 \Longrightarrow \text{ord}_n{a} \mid \phi(n)
$$

**Proof:**

$$
\begin{array}{c}
    \because a^{\phi(n)} \equiv 1 \pmod n \\
    \phi(n) \gt 0 \\
    \therefore \text{ord}_n{a} \mid \phi(n)
\end{array}
$$

## Theorem 2

$$
\begin{array}{c}
    \text{If} \quad \gcd(a,n) = 1, n \gt 0 \\
    \text{then} \quad a^i \equiv a^j \pmod n \Longleftrightarrow i \equiv j \pmod {\text{ord}_n{a}}\\
\end{array}
$$

**Proof:**

$$
\begin{array}{c}
    \text{let} \quad \gcd(a,n) = 1, n \gt 0, \text{ord}_n{a} = d \\
    \therefore a^d \equiv 1 \pmod n \\
    \therefore a^i \equiv a^j \pmod n \\
    a^{i-j} \equiv 1 \pmod n \\
    \because \text{ord}_n{a} \leq {i-j} \\
    \therefore (i-j) \mid \text{ord}_n{a} \\
    \therefore i \equiv j \pmod{\text{ord}_n{a}}
\end{array}
$$

# Primitive Roots

If $\gcd(r,n) = 1, n \gt 0$, and $\text{ord}_n{r} = \phi(n)$, then $r$ is called a primitive root modulo $n$, or a primitive root of $n$.

## Theorem 1

If $r$ is a primitive root modulo $n$, then

$$
r^1, r^2, \dots , r^{\phi(n)}
$$

form a reduced residue system modulo $n$

## Theorem 2

$$
\begin{array}{c}
    \text{If} \quad \text{ord}_n{a} = t, u \in \mathbb{Z}^+ \\
    \text{then} \quad \text{ord}_n{a^u} = \frac{t}{\gcd(t,u)} \\
    \text{ord}_n{a^u} = \frac{\text{ord}_n{a}}{\gcd(\text{ord}_n{a},u)} \\
    \text{ord}_n{a^u} = \frac{\phi(n)}{\gcd(\phi(n),u)} \\
\end{array}
$$

## Corollary

$$
\begin{array}{c}
    \text{If} \quad \text{ord}_n{r} = \phi(n) \\
    \text{then} \quad \text{ord}_n{r^t} \Longleftrightarrow \gcd(t, \phi(n)) = 1 \\
\end{array}
$$

**Proof:**

$$
\begin{array}{c}
    \because \text{ord}_n{r} = \phi(n) \\
    \therefore \text{ord}_n{r} = \frac{\phi(n)}{\gcd(t,\phi(n))} \\
    \text{If} \space r^t \space \text{is a primitive root, then} \space \text{ord}_n{r^t} = \phi(n) \\
    \therefore \text{ord}_n{r^t} \Longleftrightarrow \gcd(t, \phi(n)) = 1 \\
\end{array}
$$

## Theorem 3

If $n \in \mathbb{Z}^+$ has a primitive root, then it has a total $\phi(\phi(n))$ incongruent primitive root.

# Primitive Roots for Primes

## Lagrange's Theorem

Let $f(x) = a_nx^n + a_{n-1}x^{n-1} + \dots + a_1x + a_0$ be a polynomial of degree $n$, where $n \gt 1$.

If the leading term $p \nmid a_n$, then $f(x) \equiv 0 \mod p$ has at most $n$ incongruent roots modulo $p$.

## Theorem 1

If $p$ is a prime number, and $d \mid (p-1)$, then $x^d-1$ has exactly $d$ incongruent root modulo $p$.

$$
\begin{array}{c}
    x^d - 1 \equiv 0 \pmod p \\
    x^d \equiv 1 \pmod p \quad p \space \text{is a prime and} \space d \mid (p-1)
\end{array}
$$

## Theorem 2

$$
\begin{array}{c}
    p \space \text{is a prime} \quad d \mid (p-1) \\
    \text{card}(\\{n \in \mathbb{Z}^+ \mid n \lt \text{ord}_p{d}\\}) = \phi(d) \\
\end{array}
$$

## Corollary

Every prime has a primitive root.

$$
\forall p \space \text{is a prime number}, \exists r, \text{ord}_p{r} = \phi(p)
$$

## Theorem 3

If $p$ is a prime number.

$$
\begin{array}{c}
    \text{If} \quad p \mod 2 = 1, \space \text{ord}_p{r} = \phi(p) \\
    \text{If} \quad r^{p-1} \equiv 1 \pmod{p^2}, \quad \text{then} \space \text{ord}_{p^2}{r} = p - 1 \\
    \text{If} \quad r^{p-1} \not \equiv 1 \pmod{p^2}, \quad \text{then} \space \text{ord}_{p^2}{r} = p^2 - p
\end{array}
$$

## Theorem 4

If $p$ is an odd prime.

$$
\begin{array}{c}
    \text{If} \quad \text{ord}_p{r} = \phi(p) \quad \text{ord}_{p^2}{r} \ne p - 1 \\
    \text{then} \quad \text{ord}_{p^2}{r} = \phi(p^2) = p^2 - p \\
    \text{If} \quad \text{ord}_{p^2}{r} = p - 1 \\
    \text{then} \quad \text{ord}_{p^2}{(r + p)} = \phi(p^2)
\end{array}
$$

**Proof of Case 1**

$$
\begin{array}{c}
    \because \text{ord}_p{r} = \phi(p) = p - 1 \\
    \therefore r^{p - 1} \equiv 1 \pmod p \\
    \because \text{ord}_{p^2}{r} \ne p - 1 \\
    \because \phi(p^2) = p^2 - p = p(p-1) \\
    \therefore \text{ord}_{p^2}{r} = p^2 - p \ne p - 1
\end{array}
$$

## Theorem 5

If $p$ is an odd prime.

$$
\begin{array}{c}
    \forall k \in \mathbb{Z}^+, \exists r \space \text{ord}_{p^k}{r} = \phi(p^k) \\
    \text{If} \quad \text{ord}_{p^2}{r} = \phi(p^2) \quad \text{then} \quad \forall k \in \mathbb{Z} \space \text{ord}_{p^k}{r} = \phi(p^k)
\end{array}
$$

**Proof the Second Theorem:**

$$
\begin{array}{c}
    \text{ord}_p{r} = \phi(p) = p - 1 \quad p \space \text{is a prime number} \\
    \text{Assume} \space p^k \space \text{has a primitive root for some} \space k \geq 1 \\
    \text{Show that all} \space p^{k+1} \space \text{also has a primitive root} \\
    \phi(p^k)=p^k-p^{k-1} = p^{k-1}(p-1) \\
    \text{where} \quad \gcd(p, p - 1) = 1 \\
    \because \text{ord}_{p^2}{r} = \phi(p^2) = p^2 - p = p(p-1) \\
    \text{ord}_{p^k}{r} = \phi(p^k) = p^{k-1}(p-1) \\
    \because r^{\phi(p^2)} \equiv 1 \pmod { p^2 }, \text{where} \space \phi(p^2) = \phi(p-1) \\
    \therefore r^{\phi(p^k)} \equiv 1 \pmod{p^k}, \text{where} \space \phi(p^k)=p^{k-1}(p-1) \\
\end{array}
$$

## Theorem 6

$$
\begin{array}{c}
    \text{If} \quad a, k \in \mathbb{Z}, a \mod 2 = 1, k \geq 3 \\
    \text{then} \quad a^{\frac{\phi(2^k)}{2}} = a^{2^{k-2}} \equiv 1 \mod 2^k \\
\end{array}
$$

**Proof:**

$$
\begin{array}{c}
    \phi(2^k) = 2^k - 2^{k-1} = 2^{k-1} \\
    \frac{\phi(2^k)}{2} = \frac{2^{k-1}}{2} = 2^{k-2} \\
    \text{For} \quad k \geq 3 \quad a^{2^{k-2}} \equiv 1 \pmod{2^k} \Rightarrow a^{2^{k-2}} \equiv 1 + m \cdot 2^k, \space m \in \mathbb{Z} \\
    a^{2{k-1}} = (a^{2^{k-2}})^2 = (1 + m \cdot 2^k)^2 = 1 + 2(m \cdot 2^k)^2 + m^2 2^{2k} = 1 + m2^{k+1} + m^2 2^{2k} \\
    a^{2^{k-1}} \equiv 1 \pmod{2^{k+1}} \\
    \therefore a^{2^{k-2}} \equiv 1 \pmod{2^k}
\end{array}
$$

## Theorem 7

$2^k$ has a primitive root if and only if $k = 1$ or $k = 2$

## Theorem 8

$$
k \in \mathbb{Z}^+, k \geq 3 \Rightarrow \text{ord}_{2^k}{5} = 2^{k-2}
$$

## Theorem 9

If $n \in \mathbb{Z}^+$ and $\forall p, n \ne p^k, n \ne 2p^k$, then $n$ does not have a primitive root.

## Theorem 10

Let $p$ be an odd prime and $\text{ord}_{p^k}r = \phi(p^k)$

$$
\begin{array}{c}
    r \mod 2 = 1 \Rightarrow \text{ord}_{2p^k}{r} = \phi(2p^k) \\
    r \mod 2 = 0 \Rightarrow \text{ord}_{2p^k}{r+p^k} = \phi(2p^k) \\
\end{array}
$$

## Theorem 11

If $n \in \mathbb{Z}^+$ has a primitive root, then

$$
\begin{array}{c}
    ( n = 2 ) \lor ( n = 4 ) \lor ( n = p^t ) \lor ( n = 2p^t ) \quad p \space \text{is an odd prime}
\end{array}
$$

# Index Arithmetic

If $\text{ord}_mr = \phi(m)$ and $\gcd(a,m) = 1$, then the unique $x$ with $r^x \equiv a \mod m$ and $1 \leq x \leq \phi(m)$ is called the index of $x$ to the base $r$ modulo $m$ and is denoted by $\text{ind}_ra$.