# Set 3
**Brandon Feder**
## Exploration
### Problem 1
	
$P_0=0  \quad\quad\quad Q_0=1$
$P_1=a_1 \quad\quad\quad Q_1=a_1+1$
$P_2=a_2a_1+1 \quad\quad\quad Q_2={a_2}{a_1}+{a_2}$ $P_3={a_3}a_2a_1+a_3+a_1 \quad\quad\quad Q_3={a_3}a_2a_1+a_3a_2$
	
### Problem 2 - I have no clue

---
## Numerical
### Problem 3

Find one such value of $x$, and $y$ can be done using the extended euclidean algorithm. One such solution is $x=1016$, and $y=-3081$. That is, $7469(1016)+2463(-3081)=1$. There are, however, many such values of $x$, and $y$. This solution is similar to finding the multiplicative invere of $2463\;(\;\mathrm{mod}\;7469\;)$:

$\mathrm{define}\;x$ such that $2463\equiv \;x^{-1}\;(\;\mathrm{mod}\;7469\;)$. This implies that $2463x\equiv1\;(\;\mathrm{mod}\;7469\;)$. Therefore, $2463=7469y+1$ where $y\in\mathbb{Z}$. This can be rewritten as $2463+(-7649)y=1$ which can now be solved using the extended euclidean algorithm. This leads to the answer $x\equiv6162\;(\;\mathrm{mod}\;7469\;)$. Therefore, the multiplicative modular inverse is $6162$.


### Problem 4

This can be solved by noting the following:
$$x\equiv10\pmod{102}\implies x=102n+10$$
$$x\equiv5\pmod{7}\implies x=7k+5$$
for some $n, k\in\Z$. By substitution, $102n+10=7k+5$. This can be rewritten as $7k-102n=5$. Using the extended euclidean algorithm, one finds that one such solution to $(n, k)$ is $(-29, -2)$. However, there are many solutions of the general form  $n=7p-3$, and $k=102p-43$ for $p\in\Z^+$. When plugged back into the equations above, one finds that $x=714p-306$ for $p\in\Z$ which means $x\equiv408\pmod{714}$.

### Problem 5

This can be solved by first solving the equation $123x ≡ 1 \pmod{30031}$ Using the extended euclidean algorithm, you get the following:
$$9=16\.1+13$$
$$16=13\.1+3$$
$$13=3\.4+1$$
$$3=1\.3+0$$
After using the magic table, we get that the result is $$x=-3174$$ After multiplying the result by $999$ and putting the result into mod 30031, we get that $$x=12460$$

---
## Podasip
### Problem 6
###### Part A
To begin, $a\equiv b\pmod m$, and $c\equiv d \pmod m$. Then, by the definition of modular congruency, $$a=b+mp_1$$
$$c=d+mp_2$$
where $p_1,p_2\in Z$. 
Then, by the additive property of equality, $$a+c=b+d+mp_1+mp_2$$ 
By distribution, $$a+c=b+d+m(p_1+p_2)$$
Lastly, by the definition of modular congruency, $$a+b\equiv c+d \pmod m$$

###### Part B
To begin, $a\equiv b\pmod m$, and $c\equiv d \pmod m$. Then, by the definition of modular congruency, $$a=b+mp_1$$
$$c=d+mp_2$$
where $p_1,p_2\in Z$. 
Then, by the multiplicative property of equality , $$ac=bd+mbp_2+mdp_1+m^2p_1p_2$$
By distribution, $$ac=bd+m(bp_2+dp_1+mp_1p_2)$$

By the definition of modular congruency, $$ac\equiv bd
\pmod m$$

###### Part C
To begin, $a\equiv b\pmod m$. Then, by the definition of modular congruency, $$a=b+mp$$
where $p\in Z$.  By the multiplicative property of equality, $$a\.a\.a=(b+mp)(b+mp)(b+mp)$$
With distribution as well as the definition of exponents, this can be simplified to 
$$a^3=b^3+m(3b^2p+3bp^2m+p^3m^2)$$
By the definition of modular congruency, $$a^3\equiv b^3 \pmod m$$
	
### Problem 7
>**Lemma 1: If a and b are integers then one and only one of the following is possible: $a<b$, $a=b$, or $a>b$ **
By the definition of an additive inverse, $-b\in \Z$ since $b\in\Z$. Therefore, by additive closure, $a+^-b\in \Z$. By Trichotomy, either $a-b<0,;a-b=0,$ or $a-b>0$. Thus, by the additive property of order, either $a<b,;a=b,$ or $a>b.$

###### Disproof By Contradiction
>Assume that $d<e$. Additionally, it is given that $e|a$ and $e|b$, and that $\gcd(a,b)$ is defined as $$p\in\P\text{ where }p|a, p|b , \text{ and } \forall \; k\in\{\P,k|a, k|b\}, k≤p$$
>
> According to **Lemma 1**, $d$ is not $≥e$. Thus, by the definition of $\gcd(a,b)$, $d$ is not the $\gcd(a,b)$ as $d$ is not $≥e$.
> 
> Since this validates the given, the assumption must be false. Therefore $e$ cannot be greater than $d$. Since, $e < d$, $e=d+p$, by the definition of less than, and $d$ cannot divide $e$ if $e<d$ as proven in problem set 1 $d|e$ also doesn't follow.

###### Salvage
> $d$ can be equal to $e$. If $e=d$, then $e|a$ and $e|b$ by substitution (since it is known from the definition of $\gcd$ that $d|a$ and $d|b$). In addition, $d$ is still the $\gcd(a,b)$ as it is still greater than or equal to $\forall \; k\in\{\P,k|a, k|b\}$.

### Problem 8
	
Let $|x|_m$ be defined as the remainder when $x$ is divided by $m$.

The euclidean algorithm can be defined, and is commonly implemented, using a piecewise-recursive function as follows:

$$\gcd(a, b)=\begin{cases}
	\gcd(b, |a|_b) \quad &|a|_b\neq0\\
	b \quad &|a|_b=0
\end{cases}$$

where $a\geq b$ ( $a$ and $b$ can be swapped otherwise).

This piecewise function can be rewritten as a series of two variables as follows:

> Given $a_0, b_0\in\Z$ where $a\geq b$,
$$\mathrm{let}\;a_{n+1}=b_n$$
$$\mathrm{let}\;b_{n+1}=|a_n|_{b_n}$$
until $b_{n+1}=0$ in which case, return $a_{n+1}$

Since the goal is to prove that $b_{n+1}$ will eventually become $0$, the $a_{n+1}$ series can be ignored and substituted into the $b_{n+1}$ equation as follows:

> Given $a_0, b_0\in\Z$ where $a\geq b$, 
> $$\mathrm{let}\;b_{n+1}=|b_{n-1}|_{b_n}$$
> until $b_{n+1}=0$

Before continuing, note that by the definition of modular arithmetic, $|a|_b<b$.  Also note that $b_1$ will always be positive because $x=|y|_z$ restricts $x$ such that $x\in\Z_z$.

With this in mind, it is trivial to show that $b_{n+1} <b_n$. Because $b_{n+1}=|b_{n-1}|_{b_n}$, $b_{n+1}<b_n$ <mark>due to some definition we cant prove</mark>. Therefore, $b_{n+1}$ is monotonically decreasing and will eventually converge to 0.

### Problem 9

### Problem 10
###### Disproof
This can be disproved by evaluating a counter-example.
$$\mathrm{let}\;a=3$$
$$\mathrm{let}\;b=2$$
Therefore, the following statement should be true
$$\gcd(10^3-1, 10^2-1)=10^2-1$$
However, a simple evaluation shows that this is not true:
$$\gcd(10^3-1, 10^2-1)\not=10^2-1$$
$$\gcd(999, 99)\not=99$$
$$9\not =99$$
Therefore, this claim must be invalid.
###### Salvage
Though the original statement is false, the following statement can be proven true:
$$\gcd(10^a, 10^b)=10^{\min(a, b)} \;\;\text{for}\;\; a,b\in\Z^+$$

There are two cases: either $\min(a, b)=a$, or $\min(a, b)=b$. 

** Case 1 ($\min(a, b)=a$) **
Define $\gcd(ak, bk)=k$ for some $k\in Z^+$ such that $a$, and $b$ share no common factors but $1$.

$$\text{let}\;\gcd(10^a, 10^b)=k$$

Note that $\min(a, b)=a\implies a\leq b$. Now, factors $10^a$, and $10^b$ as follows:

$$\gcd(10^a(1), 10^a(10^{b-a}))$$
Now, note that the only factors of $1$ is $1$ which implies, by the definition of $\gcd$, that 

$$\gcd(10^a(1), 10^a(10^{b-a}))=10^a$$

Then, substitute $\min(a, b)=a$ into the equation
$$\gcd(10^a(1), 10^a(10^{b-a}))=10^{\min(a, b)}$$
And finally, substitute the left side
$$\gcd(10^a, 10^b)=10^{\min(a, b)}$$


##### Case 2 ($\min(a, b)=b$) 
Define $\gcd(ak, bk)=k$ for some $k\in Z^+$ such that $a$, and $b$ share no common factors but $1$.

$$\text{let}\;\gcd(10^a, 10^b)=k$$

Note that $\min(a, b)=b\implies b\leq a$. Now, factors $10^a$, and $10^b$ as follows:

$$\gcd(10^b(10^{a-b}), 10^b(1))$$
Now, note that the only factors of $1$ is $1$ which implies, by the definition of $\gcd$, that 

$$\gcd(10^b(10^{a-b}), 10^b(1))=10^b$$

Then, substitute $\min(a, b)=b$ into the equation
$$\gcd(10^b(10^{a-b}), 10^b(1))=10^{\min(a, b)}$$
And finally, substitute the left side
$$\gcd(10^a, 10^b)=10^{\min(a, b)}$$

##### Conclusion
Because in both cases, $\gcd(10^a, 10^b)=10^{\min(a, b)}$, the statement must be true.