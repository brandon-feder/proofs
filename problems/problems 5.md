# Set 5
**Brandon Feder**

## Problem 1
$\plet
x=p_1^{n_1}p_2^{n_2}p_3^{n_3}...$
$\plet y=p_1^{m_1}p_2^{m_2}p_3^{m_3}...$

In other words, $x$, and $y$ are represented using there prime factorization.

Define $\g(x, y)=p_1^{\min(n_1, k_1)}p_2^{\min(n_2, k_2)}p_3^{\min(n_3, k_3)}...$
Also, define $\l(x, y)=p_1^{\max(n_1, k_1)}p_2^{\max(n_2, k_2)}p_3^{\max(n_3, k_3)}...$.

I conjecture that 
$$\l(x, y)\.\g(x, y)=xy$$.
By the definition of $\g$, and $\l$, 
$$
\begin{align}
&(p_1^{\min(n_1, k_1)}p_2^{\min(n_2, k_2)}p_3^{\min(n_3, k_3)}...)(p_1^{\max(n_1, k_1)}p_2^{\max(n_2, k_2)}p_3^{\max(n_3, k_3)}...)=ab
\end{align}
$$

After substitution,
$$
\begin{align}
&(p_1^{\min(n_1, k_1)}p_2^{\min(n_2, k_2)}p_3^{\min(n_3, k_3)}...)(p_1^{\max(n_1, k_1)}p_2^{\max(n_2, k_2)}p_3^{\max(n_3, k_3)}...)\\
&=(p_1^{n_1}p_2^{n_2}p_3^{n_3}...)(p_1^{m_1}p_2^{m_2}p_3^{m_3}...)
\end{align}
$$

Before simplifying this expression, note that $\min(n_i, m_i)+\max(n_i, m_i)=n_i+m_i$. There are three cases: either $n_i<m_i$, $n_i=m_i$, or $n_i>m_i$.
> **Case 1:** $n_i<m_i$
> In this case, $\min(n_i, m_i)=n_i$, and $\max(n_i, m_i)=m_i$. Therefore, $\min(n_i, m_i)+\max(n_i, m_i)=n_i+m_i$.

> **Case 2:** $n_i=m_i$
> In this case, $\min(n_i, m_i)=\max(n_i, m_i)=m_i=n_i$. Therefore, the choice of the min and max are arbitrary and and substitutable. This implies that $\min(n_i, m_i)+\max(n_i, m_i)=n_i+m_i$.

> **Case 1:** $n_i>m_i$
> In this case, $\min(n_i, m_i)=m_i$, and $\max(n_i, m_i)=n_i$. Therefore, $\min(n_i, m_i)+\max(n_i, m_i)=m_i+n_i$ which, by commutability, implies that $\min(n_i, m_i)+\max(n_i, m_i)=n_i+m_i$.

Back to the main proof. The expression above can be simplified to 

$$
\begin{align}
&p_1^{\min(n_1, k_1)+\max(n_i, m_i)}p_2^{\min(n_2, k_2)+\max(n_2, m_2)}p_3^{\min(n_3, k_3)+\max(n_3, m_3)}\\
&=p_1^{n_1+n_1}p_2^{n_2+n_2}p_3^{n_3+n_3}...)
\end{align}
$$

As shown above, each of the exponents on the left side can be simplified to $n_i+m_i$. Therefore, the expressions are equivalent.

%%Define $k=\gcd(xk, yk)$ where $k\in\Z$ and $x$, and $y$ are coprime.

Define $l=\l(\frac{x}{l},\frac{y}{l})$ where $l\in\Z$ and $\frac{y}{l}$, and $\frac{x}{l}$ are coprime.

I conjecture that

$$\l(a, b)\.\g(a, b)=ab$$

$\plet a=c_ak$, and $b=c_bk$ where $c_a, c_b\in\Z$ and $k\in\Z^+$.
$\plet a=\frac{d_a}{l}$, and $b=\frac{d_b}{l}$ where $d_a, d_b\in\Z$ and $l\in\Z^+$.

This implies, by substitution that%%


%%$\plet k=\gcd(a, b)$. This implies, by the definition of $\g$, that $k|a$, and $k|b$. Therefore, $\frac{a}{k},\frac{b}{k}\in\Z$.

$\plet l=\l(a, b)$. This implies, by the definition of $\l$, that $a|l$, and $b|l$. Therefore, $\frac{l}{a},\frac{l}{b}\in\Z$.

Now, substitute $l$, and $k$ into what was conjectured:
$$l=\frac{ab}{k}$$.%%

## Problem 2
The axioms that apply to both $Z$ and $Z[i]$ are only the ring axioms. The other deals with matters of sign which does not exist in $Z[i]$.

## Problem 3
The primes numbers in the given list include $3$, $7$, $11$, $1+i$, $2+i$.

## Problem 4
Lets first describe a general algorithm for determining the prime factorization of a set of a number.