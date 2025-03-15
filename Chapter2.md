# Linear Congruence

If $a \pmod m = b \pmod m$, $a$ and $b$ are congruent modulo $m$.

$$
a \equiv b \pmod m \Longleftrightarrow m \mid (a-b) \Longleftrightarrow a=b+km
$$

## Theorem 1

If $a \equiv b \mod m$, then:

1. $\quad a + c \equiv b + c \pmod m$
2. $\quad a - c \equiv b - c \pmod m$
3. $\quad ac \equiv bc \pmod m$

## Theorem 2

If $a \equiv b \pmod m, \space c \equiv d \pmod m$, then:

1. $a + c \equiv b + d \pmod m$
2. $a - c \equiv b - d \pmod m$
3. $ac \equiv bd \pmod m$

## Theorem 3

$$
\begin{array}{c}
    a,b,c,m \in \mathbb{Z}, m \gt 0, d=\gcd(c,m) \\
    \text{if} \quad ac \equiv bc \pmod m \\
    \text{then} \quad a \equiv b \mod \frac{m}{d}
\end{array}
$$

**Proof:**

$$
\begin{array}{c}
    \text{let} \quad ac \equiv bc \pmod m \\
    \therefore m \mid (ac-bc) \\
    \therefore ac-bc=(a-b)c \equiv 0 \pmod m \\
    \because m \mid (a-b)c \\
    \therefore (a-b)c = km \quad k \in \mathbb{Z} \\
    \because d=\gcd(c,m) \\
    \therefore c=dc_1 \quad m=dm_1 \\
    (a-b)(dc_1)=k(dm_1) \\
    \text{Divide it by } d \\
    (a-b)c_1 = km_1 \\
    \because \gcd(c_1,m_1)=1 \\
    \therefore m_1 \mid a-b \\
    \therefore a-b \equiv 0 \pmod m_1 \\
    \because m_1=\frac{m}{d} \\
    \therefore a \equiv b \pmod {\frac{m}{d}}
\end{array}
$$

## Theorem 4

$$
\begin{array}{c}
    a,b,c,m \in \mathbb{Z}, m \gt 0, \gcd(c,m)=1 \\
    \text{if} \quad ac \equiv bc \pmod m \\
    \text{then} \quad a \equiv b \pmod m \\
\end{array}
$$

## Theorem 5

$$
\begin{array}{c}
    \text{if} \quad a \equiv b \mod m_1, \quad a \equiv b \mod m_2 \\
    \text{then} \quad a \equiv b \mod [m_1,m_2]
\end{array}
$$

## Additional Notes

$$
\begin{array}{c}
    (a + b) \mod m = (a \mod m + b \mod m) \mod m \\
    (a - b) \mod m = (a \mod m - b \mod m) \mod m \\
    ab \mod m = [(a \mod m) \cdot (b \mod m)] \mod m \\
    a^n \mod m = (a \mod m)^n \mod m \\
    a \equiv b \pmod m \Rightarrow a^n \equiv b^n \pmod m \quad \forall n \geq 0
\end{array}
$$

# Congruence Classes

If $a$ is a congruence class modulo $m$, $a$ is:

$$
[a]_m = \\{x \in \mathbb{Z} \mid x \equiv a \pmod m\\}
$$

**Example:**

$[0]_4 = \\{\dots,-8,-4,0,4,8,\dots\\}$

Because $-8 \equiv -4 \equiv 0 \equiv 4 \equiv 8 \pmod 4$.

# Complete System of Residues Modulo $m$

If $R$ is a complete system of residues modulo $m$, it is:

$$
\begin{array}{c}
    R = \\{r_1,r_2,\dots r_m\\} \\
    \forall n \in \mathbb{Z} \quad (n \mod m) \in R
\end{array}
$$

**Example:**

A complete system of residues modulo 7 is

$$
R=\\{0,1,2,3,4,5,6\\}
$$

# Linear Congruence in One Variable

## Form

$$
ax \equiv b \mod m
$$

## Solution

Let $\gcd(a,m) = d$, the linear congruence has a solution if and only if $d \mid b$.

When $d \mid b$, $ax \equiv b \mod m$ has exactly $d$ solutions modulo $m$.

# Inverse Modulo

$$
\begin{array}{c}
    \gcd(a,m) = 1 \\
    ax \equiv 1 \mod m \\
    x = a^{-1} \\
\end{array}
$$

The solution of $x$ is called an inverse of $a$ modulo $m$.

## Theorem

$$
a \cdot a^{-1} = 1
$$

## Application

To solve

$$
13x \equiv 7 \mod 31
$$

The steps are:

$$
\begin{array}{c}
    \text{Firstly, solve} \quad 13y \equiv 1 \mod 31 \\
    \because \gcd(13,31) = 1 \\
    \therefore \text{The inverse exists} \\
    y=\frac{31k+1}{13},\quad k \in \mathbb{Z} \\
    \text{When} \space k = 5, y \in \mathbb{Z}\\
    \therefore y = 12 \\
    \therefore 13^{-1} = 12 \\
    13x \cdot 13^{-1} \equiv 7 \cdot 13^{-1} \mod 31 \\
    x \equiv 7 \cdot 12 \mod 31 \\
    x \equiv 84 \mod 31 \\
    x \equiv 22 \mod 31
\end{array}
$$

# Chinese Remainder Theorem

$$
\begin{array}{c}
    \mathbb{M}=\\{m_1,m_2,\dots,m_r\\} \\
    \forall m_i,m_j \in \mathbb{M}, \gcd(m_i,m_j) = 1, i \ne j \\
    \text{if} \quad
    \begin{cases}
        x \equiv a_1 \mod m_1 \\
        x \equiv a_2 \mod m_2 \\
        \vdots
        x \equiv a_r \mod m_r
    \end{cases} \\
    \text{then} \quad M = \displaystyle\prod_{i=1}^{r}{m_i} \quad \text{is a unique solution modulo}
\end{array}
$$

# System of Linear Congruence

$$
\begin{array}{c}
    \text{To solve} \quad
    \begin{cases}
        ax+by \equiv e \mod m \\
        cx+dy \equiv f \mod m
    \end{cases} \\
    \text{That is} \quad
    \begin{bmatrix}
        a & b \\
        c & d \\
    \end{bmatrix}
    \begin{bmatrix}
        x \\
        y \\
    \end{bmatrix}
    \equiv
    \begin{bmatrix}
        e \\
        f \\
    \end{bmatrix} \pmod m \\
    \text{For} \quad A =
    \begin{bmatrix}
        a & b \\
        c & d
    \end{bmatrix} \\
    \Delta = \det(A) = ad - bc  \\
    \text{If} \quad \gcd(\Delta,m) = 1 \\
    \text{then the system has a unique solution modulo } m \\
    \text{let} \quad X =
    \begin{bmatrix}
        e & b \\
        f & d \\
    \end{bmatrix}
    \quad
    Y =
    \begin{bmatrix}
        a & e \\
        c & f \\
    \end{bmatrix} \\
    \text{The solution is:} \\
    \begin{cases}
        x \equiv \bar{\Delta} \det(X) \pmod m \\
        y \equiv \bar{\Delta} \det(Y) \pmod m \\
    \end{cases}
    \quad \text{where} \space \Delta \cdot \bar{\Delta} \equiv 1 \pmod m \\
\end{array}
$$

If $\gcd(\Delta,m) \ne 1$, if $\Delta \mid m$, then it has a unique solution, else, $\Delta \nmid m$, it is inconsistency (no solution) or infinity many solutions.

# Divide by 9

If the sum of the digits of an integer is divisible by 9, the integer is divisible by 9.

# Divide by 11

If $n \in \mathbb{Z}^+, 11 \mid n$, then the integer formed by alternatingly adding and subtracting the digits is divisible by 11.

**Example:**

$$
\begin{array}{c}
    1234567895 \\
    1-2+3-4+5-6+7-8+9-5=0 \\
    \because 11 \mid 0 \\
    \therefore 11 \mid 1234567895
\end{array}
$$

# Fermat's Little Theorem

## Wilson's Theorem

If $p$ is a prime number, then $(p-1)! \equiv -1 \mod p$

## Fermat's Little Theorem

$$
\begin{array}{c}
    p \space \text{is a prime number} \quad a \in \mathbb{Z}^+ \\
    \text{If} \quad p \nmid a \\
    \text{then} \quad a^{p-1} \equiv 1 \mod p
\end{array}
$$

### Corollary

$$
\begin{array}{c}
    p \space \text{is a prime number} \quad a \in \mathbb{Z}^+ \\
    a^p \equiv a \mod p
\end{array}
$$

# Euler's Theorem

## Euler phi-function

$$
\phi(n) = card(\\{x \in \mathbb{Z}^+ \mid \gcd(x,n) = 1, x \in [1,n]\\})
$$

## Reduced Residue System

$$
\begin{array}{c}
    rrs = \\{r_1,r_2,\dots,r_{\phi(n)}\\} \\
    \forall r \in rrs, \gcd(r,n) = 1 \\
    \forall r_i, r_j \in rrs, i \ne j, r_i \not \equiv r_j \pmod m
\end{array}
$$

### Theorem 1

$$
\begin{array}{c}
    rrs = \\{r_1,r_2,\dots,r_{\phi(n)}\\} \\
    a \in \mathbb{Z}^+, \gcd(a,n) = 1 \\
    \\{ar_1,ar_2,\dots,ar_{\phi(n)}\\} \space \text{is also a reduced residue system modulo n}
\end{array}
$$

### Theorem 2

$$
\forall r \in rrs, r^{-1} \space \text{exists}
$$

### Euler's Theorem

$$
\begin{array}{c}
    m \in \mathbb{Z}^+, a \in \mathbb{Z} \quad \gcd(a,m) = 1 \\
    a^{\phi(m)} \equiv 1 \mod m
\end{array}
$$