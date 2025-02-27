# Euler Phi-Function

## Arithmetical Function

$$
f(n) \quad n \in \mathbb{Z}^+
$$

**Example:**

$$
\phi(n)
$$

## Multiplicative Function

$$
\begin{array}{c}
    \text{an arithmetical function} \space f(x) \\
    f(mn) = f(m)f(n), \space \gcd(m,n)=1
\end{array}
$$

## Completely Multiplicative Function

$$
\begin{array}{c}
    \text{an arithmetical function} \space f(x) \\
    f(mn) = f(m)f(n), \space m,n \in \mathbb{Z}^+
\end{array}
$$

### Theorem 1

$$
f(n) \space \text{is completely multiplicative function} \Longrightarrow f(n) \space \text{is multiplicative function}
$$

### Theorem 2

$$
\begin{array}{c}
    f(n) \space \text{is a multiplicative function} \\
    n=\displaystyle\sum_{i=1}^{s}{p_i^{a_i}} \quad \text{is the prmie factorization of} \space n \quad n \in \mathbb{Z}^+ \\
    f(n)=\displaystyle\prod_{i=1}^{s}{f(p_i^{a_i})}
\end{array}
$$

### Theorem 3

$$
\begin{array}{c}
    m,n \in \mathbb{Z}, \space \gcd(m,n) = 1 \\
    \forall d \mid mn \Longrightarrow d=d_1d_2 \\
    d_1 \mid m \quad d_2 \mid n \quad \gcd(d_1,d_2) = 1
\end{array}
$$

### Theorem 4

If $f(n)$ is a multiplicative function, then

$$
F(n) = \displaystyle\sum_{d \mid n}{f(d)}
$$

is also multiplicative

## Theorem 1

$$
\begin{array}{c}
    p \space \text{is a prmie number} \\
    \phi(p) = p - 1
\end{array}
$$

## Theorem 2

$$
\begin{array}{c}
    p \space \text{is a prmie number} \\
    \phi(p^n) = p^n - p^{n-1}
\end{array}
$$

## Theorem 3

Euler Phi-Function is multiplicative.

## Theorem 4

$$
\begin{array}{c}
    n = \displaystyle\prod_{i=1}^{s}{p_i}^{a_i} \quad p_i \space \text{are prime numbers} \\
    \phi(n) = n \cdot \displaystyle\prod_{i=1}^{s}{(1-\frac{1}{p_i})}
\end{array}
$$

# $\tau(n)$ Function

**Definition:**

$$
\tau(n) = \displaystyle\sum_{d \mid n}{f(d)} = \displaystyle\sum_{d \mid n}{1}
$$

$\tau(n)$ counts the number of positive divisors of $n$.

## Theorem 1

$$
\begin{array}{c}
    p \space \text{is a prime number} \\
    \tau(p^a) = a + 1
\end{array}
$$

## Theorem 2

$\tau(n)$ is a multiplicative function.

$$
\begin{array}{c}
    n = \displaystyle\prod_{i=1}^{s}{p_i^{a_i}} \quad p_i \space \text{are prime numbers} \\
    \tau(n) = \displaystyle\prod_{i=1}^{s}{(a_i+1)}
\end{array}
$$

# Sum of $\phi(d)$

$$
F(n) = \displaystyle\sum_{d \mid n}{\phi(d)}
$$

## Theorem

$$
\displaystyle\sum_{d \mid n}{\phi(d)} = n
$$

# Sum of Divisors

**Definition:**

$$
\sigma(n) = \displaystyle\sum_{d \mid n}{d}
$$

## Theorem 1

If $p$ is a prime number.

$$
\sigma(p^n) = \frac{p^{n+1} - 1}{p - 1}
$$

**Proof:**

$$
\begin{array}{c}
    \forall p \in \\{1,p,p^2,\dots,p^n\\}, \space p \mid p^n \\
    \sigma(p^n) = \displaystyle\sum_{i=0}^{n}{p^i} = \frac{p^{n+1} - 1}{p - 1}
\end{array}
$$

## Theorem 2

$\sigma(n)$ is a multiplicative function.

# Conclusion

| Function    | Definition                                                                       | Meaning                                                                      | Formula                                                                                        |
| ----------- | -------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| $\phi(n)$   | $\phi(n) = card(\\{x \in \mathbb{Z}^+ \mid \gcd(x,n) = 1, x \in [1,n]\\})$       | The number of integers that is relatively prime to $n$ and not exceeding $n$ | $\phi(p^n)=p^n-p^{n-1}$ or $\phi(n) = n \cdot \displaystyle\prod_{i=1}^{s}{(1-\frac{1}{p_i})}$ |
| $\tau(n)$   | $\tau(n) = \displaystyle\sum_{d \mid n}{f(d)} = \displaystyle\sum_{d \mid n}{1}$ | The number of positive divisors of $n$ that is not exceeding $n$             | $\tau(n) = \displaystyle\prod_{i=1}^{s}{(a_i+1)}$                                              |
| $\sigma(n)$ | $\sigma(n) = \displaystyle\sum_{d \mid n}{d}$                                    | The sum of the positive divisors                                             | $\sigma(p^n) = \frac{p^{n+1} - 1}{p - 1}$                                                      |

# RSA Cryptography

1. The encryption key is $(n,e)$, where $n=pq$, $p$ and $q$ are prime numbers, $\gcd(e,\phi(n) = (p-1)(q-1)) = 1$. Plus, $e$ is the public key.
2. Calculate the private key $(d,n)$, where $de \equiv 1 \mod \phi(n)$
3. Translate the plaintext into numbers, $m = \\{m_1,m_2,\dots , m_k\\}$
4. The ciphertext are given by:

$$
c_i \equiv m_i^e \mod n
$$

5. To decrypt the message, the plaintext is given by:

$$
m_i \equiv c_i^d \mod n
$$