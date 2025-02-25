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

If $a \equiv b \pmod m, \; c \equiv d \pmod m$, then:

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

Proof:

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
[a]_m = \{x \in \mathbb{Z} \mid x \equiv a \pmod m\}
$$

# Complete System of Residues Modulo $m$

If $R$ is a complete system of residues modulo $m$, it is:

$$
\begin{array}{c}
    R = \{r_1,r_2,\dots r_m\} \\
    \forall n \in \mathbb{Z} \quad (n \mod m) \in R
\end{array}
$$

**Example:**

A complete system of residues modulo 7 is

$$
R=\{0,1,2,3,4,5,6\}
$$
