# Set 4
**Brandon Feder**

## Numerical
#### Problem 1
To solve the equation $7469x+2463y= 1$ for $x$, and $y$, first note that $7469$ and $2463$ are coprime. That is, $\gcd(7469,2463)=1$.

Also, as stated in set 3, problem 3, one such solution to the equation above is 
$$x=1016 \quad \text{and}$$
$$y=-3081$$

Therefore, the general form of $x$, and $y$ is $$x=\lcm(7469,2463)\ n\ +\ 1016$$
$$y=\frac{(1-7469x)}{2463}$$

where $n\in\Z$. Now, substitute $7469\.2463=18396147$ for $\lcm(7469,2463)$:
$$x=18396147n\ +\ 1016$$
$$y=\frac{(1-7469x)}{2463}$$

In modular form, this is equivalent to
$$x\equiv1016\;(\pmod\;18396147)$$
$$y=\frac{(1-7469x)}{2463}$$

#### Problem 2
###### Part A
The first expressions can be evaluated by first determining the period of the periodic series that corresponds to the consecutive multiplications of $2$ to itself $(\pmod\;9)$. The series goes as follows:
$$2, 4, 8, 7, 5, 1, 2, 4, 8, ...$$
Therefore, the period is $6$. Next, find the remainder of dividing the exponent, $3250$, by $6$. The remainder is $4$. Therefore, the answer is the $4th$ element of the series above, $7$.

###### Part B
The second expression can be solved almost identically. However, to simplify the process, start by replacing $3142$ with $7$ because $3142\equiv 7\;(\pmod\;11)$:
$$7^{2718}\;(\pmod\;11)$$

Note that because $7$ and $11$ are coprime, period of the series corresponding to the consecutive multiplications of $7$ to itself will be $11$. Therefore, because $2718\equiv1\;(\pmod\;11)$, 
$$7^1 \equiv7^{2718}\;(\pmod\;11)$$
Which can be simplified to 
$$7 \equiv7^{2718}\;(\pmod\;11)$$
Therefore, the answer is $7$.

---
## Exploration 1
#### Problem 3
$7\.5$ is the unique factorization of $35$. To say a number, $n\in\Z^+$, factors uniquely as a product of primes means that it can be represented as the product of a finite number of prime numbers and that there is only one set of prime numbers such that the product of that set equals $n$. Note that $n$ must be a positive integer because otherwise one or more of the products would have to be negative and therefore non-prime.

---
## Podasip
#### Problem 4
**Claim**: If $a\in\Z$, then $a$ represents a unit $(\pmod\;m) \iff \gcd(a, m)=1$

**Proof of first part**
$\plet a$ be a unit $(\pmod\;m)$

Now, assume that $\gcd(a, m)=k$ where $k\in Z^+$ and $k\not=1$. Therefore, $k|a$, and $k|m$. This implies, by the definition of divisibility, that there are a $x, y\in Z^+$ such that $kx=a$, and $ky=m$.

By the definition of a unit  $(\pmod\;m)$, $a$ has a multiplicative inverse, $b\in\Z^+$ such that $ab\equiv 1\;(\pmod\;m)$

If you substitute the values of $a$ and $k$,  you get $kxb\equiv 1\;(\pmod\;ky)$. However, because modulus contains a common factor with the left-hand expression, besides 1, $0\equiv 1\;(\pmod\;ky)$. However, this is invalid and shows that $\gcd(a, m)=1$.

**Proof of second part**
...

#### Problem 5
First, simplify 
$$r_k=(-1)^k
\begin{vmatrix}\begin{bmatrix}  
	P_k & a\\  
	Q_k & b  
\end{bmatrix}\end{vmatrix}$$
by solving for the determinant
$$r_k=(-1)^k(P_kb-Q_ka)$$
As stated in set 3, problem 1, $$P_{k+1}=a_{k+1}P_k+P_{k-1}$$
$$P_{-1}=0\text{ and }P_0=1$$
and, similarly, 
$$Q_{k+1}=a_{k+1}Q_k+Q_{k-1}$$
$$Q_{-1}=1\text{ and }Q_0=0$$
Therefore, 
$$P_k=a_kP_{k-1}+P_{k-2}$$
$$Q_k=a_kQ_{k-1}+Q_{k-2}$$
This leads, by substitution and commutativity, to the recursive definition of $r_k$:
$$r_k=(-1)^k(a_kP_{k-1}-a_kQ_{k-1}+P_{k-2}-Q_{k-2})$$
Now, replace