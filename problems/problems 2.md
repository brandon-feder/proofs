# Set 2
---
## Exploration

1. **Find a property of $\mathbb{Q}$ that is not always a property of $\mathbb{Z}$. Find a property of $\mathbb{Z}$ that is not always a property of $\mathbb{Q}$.  How are these differences reflected in the axiomatic description of integers?**

	As $\mathbb{Q}$ is a field, while $\mathbb{Z}$ is a ring, by definition, $\mathbb{Q}$ must contain a multiplicative inverse of each of its elements while $\mathbb{Z}$ does not.
	
	As $\mathbb{Q}$ does not have a smallest value, it does not have an equivalent of the WOP.
	
	These differences are reflected in the axiomatic description of integers because the axioms define what integers are an how they behave. Similar axioms do the same for the rationals. Because these axioms, though similar, are different, they reflect the differences between these two sets.

2. <b> If $a$ is in $\mathbb{Z}$ or in $\mathbb{Z}_k$, and $n \in  \mathbb{Z}^+$, what is $a^n$. Give a precise definition. Then $a^{m+n}=a^ma^n$, for every $m, n \in \mathbb{Z}^+$. Moreover, $a^{mn}=(a^m)^n$. Can you prove these laws of exponents.</b>
	
	$a^n$ can be defined as $\prod^n_1a$ where $\prod_1^ab$ is the product of $b$, $a$ times. In other words, $a^n=\prod^n_1a$.
	
	$a^{m+n}=a^ma^n$ because $a^{m+n}=\prod^{m+n}_1 a$ This infinite product can be broken down into two sub-products of size $m$, and $n$: $\prod^{m+n}_1 a=(\prod^m_1a)(\prod^n_1a)$. Through substitution, this is equivalent to $a^ma^n$.
	
	$a^{mn}=(a^m)^n$ is easiest to prove by first starting with the $(a^m)^n$ expression. This is equivalent to $\prod^m_1(\prod^n_1a)$. Because the inner product multiplies $a$, $n$ times and the outer product multiplies that $m$ times, this is equivalent to $\prod^{mn}_1a$ which equals $a^{mn}$. By transitivity, this implies that $a^{mn}=(a^m)^n$.

---
## Numerical
3. **For each element of $U_5$ list its powers and find its order. Do the same for $U_7, U_8, U_9, U_{10},\text{ and }U_{11}$. Now that you have worked out as many examples for patterns, make a conjecture!**
	
	I conjecture that if $a\in\U_m$, that $\gcd(a, m)=1$. In other words, $a\in\U_m$ if $a$ and the modulus $m$ are coprime. This is because if $a|m$, then there is a $k\in Z^+$ such that $ak=m$. However, because of this, $ak\equiv\;(\pmod\;m)$. This is a problem, because there is no such $b\in Z_m$ such that $ak\equiv m\equiv0\;(\pmod\;m)$. Therefore, it does not matter what $b$ is because it will be multiplied by a zero element of $Z_m$.
---
## Podasip
4. <b>If $c \neq 0$ and $ac=bc$, then $a=b$. True in $\mathbb{Z}$. True in $\mathbb{Z}_m$.</b>

	This can be proven by first proving the contrapositive of the statement. That is, this can be proven by showing that the statement "<i>If $a\neq b$, then $ac \neq bc$ or $c=0$</i>", or "<i>If $a \not\equiv b\;(mod\;m)$, then $ac \not\equiv bc\;(mod\;m)$ or $c\equiv0\;(mod\;m)$</i>" .
	
	Here are the two proofs:
	- $let\;a \neq b$. Therefore, by multiplication, $ac\neq bc$. This is true only when $c$ is not the $0$ element. However, this is not a concern because $c=0$ is allowed. Because the contrapositive is true, the original statement must also be true.
	
	- $let\;a \not\equiv b\;(mod\;m)$. Therefore, by multiplication, $ac\not\equiv bc\;(mod\;m)$. This is true only when $c$ is not the $0$ element. However, this is not a concern because $c\equiv0\;(mod\;m)$ is allowed. Because the contrapositive is true, the original statement must also be true.
	
5. **($a \leq b$ and $b \leq c$) $\implies a \leq c$**

	$x \leq y \implies x+p=y$ for some $p\in(\mathbb{R}^+\cup\;\{0\})$. With this in mind, $let\;a+p=b$, and $let\;b+k=c$. By substitution, $a+p+k=c$. By additive closure, $p+k\in(\mathbb{R}^+\cup\;\{0\})$. Therefore, $a \leq c$.
6. **Suppose $a, b, x, y\in\mathbb{Z}$. Then $a \leq b$ and $x \leq y$ implies $a+x\leq b+y$ and $ax\leq by$. **
	
	Based on the definition of $a\leq b$, $let\;a+p=b$, and $let\;x+k=y$. By addition and substitution, $a+p+x+k=b+y$. This can be re-written as $(a+x)+(p+k)=b+y$. Once again, by additive closure, $p+k\in(\mathbb{R}^+\cup\;\{0\})$. Therefore, by the definition of $\leq$, $a+x\leq b+y$.
	
	Based on the definition of $a\leq b$ in the previous problem, $let\;a+p=b$, and $let\;x+k=y$. By multiplication and substitution, $(a+p)(x+k)=by$. This can be re-written as $ax+(px+pk+ak)=by$. By additive and multiplicative closure, $p+k\in(\mathbb{R}^+\cup\;\{0\})$. Therefore, by the definition of $\leq$, $ax\leq by$.
	
7. **Suppose $x\in\mathbb{Z}$ and $x>0$. Then $x\geq1$.**

	$x > y \implies x=y+p$ for some $p\in\mathbb{R}^+$
	$x \geq y \implies x=y+p$ for some $p\in(\mathbb{R}^+\cup\;\{0\})$
	
	$let\;0+p=x$ for some $p\in\mathbb{R}^+$ because of the definition of $>$. Therefore, $p=x$. Because $x\in\mathbb{Z}$, $p\in(\mathbb{Z}\cap\mathbb{R}^+)$, or that $p\in P$. Now, assume that $1$ is not the least element of $P$. This would imply that there is an integer $z<1$ where $z\in\mathbb{Z}$. This implies that $z+k=1$ for some $k\in\mathbb{Z}^+$ for the same reasons as above. This indirectly contradicts the WOP principle and therefore is not correct. This implies that $1$ is the least integer in $Z^+$ and that $\therefore x\geq1$.
8. **If $a$ and $b$ are integers, and $a|b$, then $a\leq b$.**

	To begin, $$let\;ap=b$$ where $p\in \mathbb{P}$. Then factor: $$a(p)=b$$ 
	Since $^-1+1=0$ by the definition of an additive inverse, 
	It follows that
	$$a\left(p+(^-1+1)\right)=b$$
	$$a\left((p+^-1)+1\right)=b$$$$a(p+^-1)+a=b$$
	$$a+a(p+^-1)=b$$ 
	As shown in question 7, 1 is the smallest positive integer. Therefore, $$a+a(1+^-1)≤a+a(p+^-1)$$ this implies that $$a+a(1+^-1)≤b$$. Because $-1\cdot a=-a$ 
	$$a+(a+^-a)≤b$$ and reduced though the definition of an additive inverse and the zero ring axiom to $$a≤b$$ Thus, $$a≤b$$
9.
	##### Definition
	
	The product of common factors of $a$ and $b$, for $a, b\in\P$ can be written as $X_{a,b}$, the product of the primes divisible by $a$ and $b$. $X_{a, b}$ can be written as $$X_{a,b}=\prod_{p\in\mathbb{N}_P}p\text{ where }  p|a, p|b$$
	
	The $\gcd(a,b)$ is the greatest number divisible by $a$ and $b$. It can be notated as $$\gcd(a, b)=X_{a,b}\text{ where }a, b\in\P$$ 
	##### Proof
	It is given that $a=bq+r$. By the definition of $>$, $a>bq$. Therefore, $a+^-bq=r$. Next, by the definition of a $\gcd$, the $\gcd(a,b)$, $X_{a,b}$ divides both $a$ and $b$. Rewriting these as equations, we get that $$X_{a,b}|a$$
	$$X_{a,b}|b$$
	Next, by the definition of dividing, $$X_{a,b}p_1=a$$
	$$X_{a,b}p_2=b$$
	With substitution, we can rewrite the original equation, that $a=bq+r$, as $$X_{a,b}p_1=X_{a,b}p_2q+r$$
	By the additive property of order,
	$$X_{a,b}p_1+^-X_{a,b}p_2q=r$$
	Next, we can use distribution to find that
	$$X_{a,b}(p_1+^-p_2q)=r$$
	Since $r=X_{a,b}(p_1+^-p_2q)$ and $b=X_{a,b}p_2$, $r$ and $b$ share a common factor $X_{a,b}$. Thus, $\gcd(a,b)≤\gcd(b,r)$. If $p_1+^-p_2q$ and $p_2$ have a GCD of 1, then $\gcd(b,r)=X_{a,b}$ and, by substitution, $\gcd(a,b)=\gcd(b,r)$
1. <mark>Todo. Nick's does not work very well.</mark>